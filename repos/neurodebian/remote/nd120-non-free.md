## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:f7aa6820042a4ae50573fa279e16e13bc46733d6563d33ae27245d5996b8c451
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
$ docker pull neurodebian@sha256:00de210443b08e8b2c8fbf850ead46293cad33de7723fb14a0f99c863e096972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72f722934e4956abf8dd454ae7b13bde84b27e8ef8c591805aae139965a2a6a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:33:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d88ed0613cd9f6ce127a874771f0a5544ef2422cd150512bf794376a148581`  
		Last Modified: Tue, 04 Nov 2025 00:33:49 GMT  
		Size: 11.3 MB (11269737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7de111a66b2c9284c76057de96ab17f30a82d8ad810bc3b4f3b84d89c5bd3dc`  
		Last Modified: Tue, 04 Nov 2025 00:33:48 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee5d6e85ebd7f3581af7dca82ba6a8568b5147705f4503667f482f752d8a044`  
		Last Modified: Tue, 04 Nov 2025 00:33:48 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cc6eeb1f11ec6abdd7400f138796119619bb0415aa0e4180aabd5f57fff522`  
		Last Modified: Tue, 04 Nov 2025 00:33:48 GMT  
		Size: 93.4 KB (93381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47630c2cf82d565152418932fc379329fd9b69a55d1d661fad42d7275e56318`  
		Last Modified: Tue, 04 Nov 2025 00:33:48 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6f4fde68622797da6a3786b8f28dc4bd44457d2fc101206246320723eaa4c67a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f86f60783c82b5b329a01422b14d15b3fcd339845eaf02da3ba4c76964dd0c`

```dockerfile
```

-	Layers:
	-	`sha256:2cab0730bf1388e4ac5c5f4de45a53b94c31d95ec0e95de4cc5f4a39fd785ebb`  
		Last Modified: Tue, 04 Nov 2025 11:07:35 GMT  
		Size: 4.1 MB (4075272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afa5bd588286b3f9f7d7162b8c0c8ce54927c35bba01740500a339db5dc18996`  
		Last Modified: Tue, 04 Nov 2025 11:07:36 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ea702a845962eabcccddf7c01f2cbd8836042b5968d7e043c8d80756c63a9c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59709026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd9858ce498b5ec88f7dbf1663f9aa5c6f6742fa8ee3770030c7811681f2df7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:35:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:35:05 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:35:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:35:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002c6b9b6756e1cd8095b0582bd37683c464ec4ab55bac49ec167ca067bde7fb`  
		Last Modified: Tue, 04 Nov 2025 00:35:29 GMT  
		Size: 11.3 MB (11253406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c336a6f4d5727655dc138a98731034ae0e2140e3ffb54b908185b13b9eb4a936`  
		Last Modified: Tue, 04 Nov 2025 00:35:27 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7251c2cbc061371c58cae8b0379696852ae7d1d73ff1b6555b5534118cd208`  
		Last Modified: Tue, 04 Nov 2025 00:35:28 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6135f81ed89c8c4989f4fc3a5fad65bf173a8bcceeae4e41ea3fa1c711f36`  
		Last Modified: Tue, 04 Nov 2025 00:35:28 GMT  
		Size: 93.5 KB (93519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c4972982f632d1d7169aee07767aafb08c185c4c08209a34c4c5e20f5d6c2e`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:16c63757aac4a6c60ff8deaff67aed40b49090b5bfd62b3637d980d504710947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007d0a83f0a35ad1403ea447acde716771606055a9f75513f9b2e3550a01ed99`

```dockerfile
```

-	Layers:
	-	`sha256:a4e4fdb5a783b8192877194764d3941aee0a0f0fd0f4cc0a7cba1d217fc72e61`  
		Last Modified: Tue, 04 Nov 2025 11:07:41 GMT  
		Size: 4.1 MB (4075514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a6535310e81f95a9947a39b6f4ab7dd97131c362c08513b887b186ad02d9dbb`  
		Last Modified: Tue, 04 Nov 2025 11:07:41 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:825404acc68c967e7485b609cbea5d3337d11cdb2d73381d1fd09fe55e5b7bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61253239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7340a74314888926e6b86e06ef8b6994486a23312368806c8d6dc8116a590d25`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:27:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:27:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:27:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:28:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3a9907ae02a89d2535bb875a11c05038e0be4fa333c35747cd42f6f7b49e018d`  
		Last Modified: Tue, 04 Nov 2025 00:12:58 GMT  
		Size: 49.5 MB (49467114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f533d2fca7b3ba5eb10a96c4bc300c35df5344af9d94b133311ba535bde1be7`  
		Last Modified: Tue, 04 Nov 2025 00:28:03 GMT  
		Size: 11.7 MB (11690117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b8e2460139c1d8b721f3aaa55562183415fa40d728ebf397973d0b552742ef`  
		Last Modified: Tue, 04 Nov 2025 00:28:02 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da94aa9d44a01d38241f6a206526b15dd27385151cf99dbf2352c5be5e0e4698`  
		Last Modified: Tue, 04 Nov 2025 00:28:02 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478356a0682b919a8511c7940954eb2b69432f859df6ea178198f69af1b62b56`  
		Last Modified: Tue, 04 Nov 2025 00:28:02 GMT  
		Size: 93.4 KB (93387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412d92d5804d3caad70c12f827b3660462db7a4e38892eab47dd66d91be00bdd`  
		Last Modified: Tue, 04 Nov 2025 00:28:26 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bafa90c68b61ba641ac0f99c3a4a0eb9b54ef53e51d2004ac66192abc07b57b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2164ec6201f5ba21879454d900502211f2c23995819400439f7822f13e8d13a0`

```dockerfile
```

-	Layers:
	-	`sha256:032592e48cf80c53f8ffd21e8bd7745396683b429c1dcb156aab950e47695e37`  
		Last Modified: Tue, 04 Nov 2025 11:07:45 GMT  
		Size: 4.1 MB (4073240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c826d1d86eafd0f44439159f90c8a2515fb823f8f9fb8688b08b1ca590b4885`  
		Last Modified: Tue, 04 Nov 2025 11:07:46 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json
