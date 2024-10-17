<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:focal`](#neurodebianfocal)
-	[`neurodebian:focal-non-free`](#neurodebianfocal-non-free)
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
-	[`neurodebian:nd20.04`](#neurodebiannd2004)
-	[`neurodebian:nd20.04-non-free`](#neurodebiannd2004-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:nd24.04`](#neurodebiannd2404)
-	[`neurodebian:nd24.04-non-free`](#neurodebiannd2404-non-free)
-	[`neurodebian:noble`](#neurodebiannoble)
-	[`neurodebian:noble-non-free`](#neurodebiannoble-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:trixie`](#neurodebiantrixie)
-	[`neurodebian:trixie-non-free`](#neurodebiantrixie-non-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:6fd67d55fd53ff6df3b247a63873f9690c1b471533ec11f775eb30c8eb54725b
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
$ docker pull neurodebian@sha256:3697dda71c97c3f2331d51e833f6004024b1b1ff9c6f985ac48a7f206f372d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66b226bfd77945145ba8dbdb314a327f8d3e57c00b7ff60b8c612e99ec189e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b762b97ea764326ee7c78d3be70939e4158333f93d124f91739a6a96a661fa86`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 11.3 MB (11266584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402ca42a66cb385c6c94651438c30b60632bbdcc199de7afa4b036ed8247d7df`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a35ac53ffb5eb6a25a8b3a501e4ff0a421f6b7e0440548aabbc7c1aad826b53`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a6e032b96453782d4fdb1fff50b61a365a71a9bff219fa43b8faecf4d5d645`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 93.1 KB (93133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46f40f5380579c474973147a5d1d5c436d1e8f8fa806d11cbd13b10e1511b852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a8a55f1f8b9a5e99a76a84ccda60e5a260fe1aeb5043321b56d4d4ee9951eb`

```dockerfile
```

-	Layers:
	-	`sha256:6f4a965387af32daf99856e8ddb053fbdb29217654f0e62264c2dd0649125620`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 3.9 MB (3924252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4881891bbb1e76cc32e634bf22607dbf8586ce82543820147144f8f75940c3de`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 13.8 KB (13823 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:050e6d336e606fbb0e300affdba33b0e7112897488c1080d655e6a8a2bc44425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12cf34310545c647cd06d3fceb8303925590de81448268c048a09001291f1154`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b222ea27d3a13a628f27fb485c2c8953c435cf879ad43c99108ae24a1a8538`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aa7c14ee96487976b1787f395d3da08538e6eb4bc1212666ffac800202f10b`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103fbbaf04667aeef928e69b2b8457085af18a4894f429dfb4cd0ec52dfca876`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370293ac9e0cd3f1e79e181dd7401ddcfc4d9579c4bcc066993cb19373d455b1`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 93.4 KB (93360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6c2dab71f6c0b4093d81cca7238cb6dcd0e421277b6ef15f14c33ffb2d5ae297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d735f4ccf82806b86c0895be8e82f45c0e36446a82405ebc53b10a90017eb2`

```dockerfile
```

-	Layers:
	-	`sha256:e8160276deeea36db3deb56f2bf3cae66d45878144632f200674b7bf3c89c2b2`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 3.9 MB (3924505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dab3dee07749ea50941c86b101d4a545ee827240618545e172488aa205971f7`  
		Last Modified: Thu, 17 Oct 2024 13:30:03 GMT  
		Size: 14.0 KB (13954 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:896545d95a4d05752deb3b2b3f8eb2e710b4f52da6553cee0676abb5a7d4280a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0ad284f6be59a7c68b584bb5c1cc330f70b3690a10445c92e63e73e3d56535`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac817a808ff957a7e831213b07291fc20229bc43affbf623c78a261ec0325c5`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 11.7 MB (11688945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bf606e708bc7cf8f28d6e78f0274840cd2b7301440a2bf866d5204ef18fa14`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ce82a925a96d328fdcab86c0dbae82212e7cc285b177465deebb2d3fbe9067`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3afcf85c6057a5d9d8eb7c146fd97cfe8fd83354d50596c26cbc3d28cd852a3`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 93.2 KB (93249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8607ae6ffd66c4c0da8b82f00cd85627faeea84b5e54044d05b67f735d74af54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ada56f849e4a4098758070e52baa926b4864474eee5fa5d4dc22d1058259af`

```dockerfile
```

-	Layers:
	-	`sha256:5bd90987926d222eb5f929a5da7c7efe871eeb25f75f8c2cb76d7a280d621262`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 3.9 MB (3922169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a0ce6a103d838e660923ca4f89ff0c6248d4d1d71fcc5779c4b15c1bc50d9e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 13.8 KB (13793 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:7e4840f6db5f0eafb9109b71b600b030c1d496111b609440225037c358b9144f
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
$ docker pull neurodebian@sha256:2d73a121aa2a836fdd61c2caaa45f39a60d7135e9fea08a33bc74595a2c2f63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60917132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc4c075aa36307cec499d38e0967a31bb1177449a066237940379b201fe03dc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e3861fe7b114a17685588363e051556e829fd3ee46e28f62d884d28e74e55`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 11.3 MB (11266561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a00ac0906fe55639580577bbd3dd60b722d4c59033a0c14446e5224830a05c8`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d085eb9d9ff2ee88dfca96061cefa20cf9c3d0a7bf1d9ab12247a6977664db72`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1ff7e0b7fca23cd7c1b39fa04005382442d07e9ce890af5fc59dcdf4f81278`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 93.1 KB (93128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44601798f4d155482adaf66f6cac064352d48cb3d7a9772da5500a7a213dcd`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d16d14974557a6a52b575d322f4fb464948fa19fe7409852ac281d2549fbe28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853cf6b4a7404cb7dc08679bfe53a305752c9c1daf86c8db41da8b4019394c64`

```dockerfile
```

-	Layers:
	-	`sha256:3d1b519a35f33eaf08b368bda12cd36f3b6d20193425c489c53d1b4fb859221b`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 3.9 MB (3924292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26665f8ede534d5ee35159984cea4fb23139470098f78b030b8e872244fd4f73`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 15.9 KB (15858 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2cadf68a2031eb58f9fc6f1ffe6aef4ed02a17e61fb6e899e162e11be19e5924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23adc07773d4924502532239ca86fe971d4c52473ddaf831a0ad2f4c5e2875d3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b222ea27d3a13a628f27fb485c2c8953c435cf879ad43c99108ae24a1a8538`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aa7c14ee96487976b1787f395d3da08538e6eb4bc1212666ffac800202f10b`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103fbbaf04667aeef928e69b2b8457085af18a4894f429dfb4cd0ec52dfca876`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370293ac9e0cd3f1e79e181dd7401ddcfc4d9579c4bcc066993cb19373d455b1`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 93.4 KB (93360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d034187a5238f4ac144d3f26372ba2a244669cc6d057318d3f60129559b396`  
		Last Modified: Thu, 17 Oct 2024 13:30:24 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cff90856eaa4cfe55cef01efb7e4a7d6ad9fc13743ac77d3ec2d1b4411602090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6784a5fa44f5349ac857cc8fa34504dc72bdc0c73d227e8c76e86459bd2d1df5`

```dockerfile
```

-	Layers:
	-	`sha256:04944ff3646cbb8d2c015a187bb9f8c4707d4a241a5c5ded62e171f60402f190`  
		Last Modified: Thu, 17 Oct 2024 13:30:24 GMT  
		Size: 3.9 MB (3924545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76cfff78c55d81b9986af70e9de4c9acb0d6a646de7805f6f542277ce9e81bf6`  
		Last Modified: Thu, 17 Oct 2024 13:30:24 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1360a324a787b80218de1b31e8a4bf1585aa0f4d8ca0632db9d4b1f1543510cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1324be94e3ec7d03a9cf2e35cb45480ac0a5381718eb771487a1f35f8dece4e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8e15811c104c2540eadcbc91d0ad8c420b9e7ed2ac33fc059533f236d22a34`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 11.7 MB (11688958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c913a60b2aea27736559d68f57b0c6af1fa233fec72e8e8d5c7c4c43199ae4ee`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72ec95c15f2bc5a6e5f16cc99197ac8aa491212630d4ba05e6289cff9722cef`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b72d6dd64c0de2b1a61e23af324c34b46bb76638afa8602a284cb0ae786c7c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 93.2 KB (93204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b092aabde6d4449b6ed80131da9e46d4b895bc88470d189cdccfa0ce75576069`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:007b4de94d8801338e3e7fbe3ec20314afdc0eb481e48bd4513d73b699b9acb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1461c367a715b910d400bca53db41530c86f17ef50c8272d365faef32c555115`

```dockerfile
```

-	Layers:
	-	`sha256:80806ecded92443b46c358114ef373cdefab1c787613403548a873b003328f3c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 3.9 MB (3922209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4b56190dbb02bcafb5596cfd93692a4b34dff5ee6b38ed1ef4f3c69444d232`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 15.8 KB (15827 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:db35cd2f9748f6b233c53b0fc84bf3a5699604ac5b06898e48f7c15c7d672d82
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
$ docker pull neurodebian@sha256:96625ffae5306bbefb90c138d60615fbbc3b0048004bdddab6c9880c2a1dd3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66288904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7249c84eb570d86afedf4eb3c16a5afe113846e5b771daae85a32dfa8f976ba`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1b510b0107687e655df5468a134f88f9ace83c7baf75178bbad0baefd8454c`  
		Last Modified: Thu, 17 Oct 2024 01:14:13 GMT  
		Size: 11.1 MB (11105105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9910055e69f675b61256717f5fface946970d9e3a19eb1c3ded13d2c80baa278`  
		Last Modified: Thu, 17 Oct 2024 01:14:13 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d1e63ec04e9a741afb3ff13cd8719bec3db300455606c0c6ca0cc2bad81f4e`  
		Last Modified: Thu, 17 Oct 2024 01:14:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba7a3b45b6316252e7fbef945abbe5998041ee3a89d36e3f6894a7b17e26131`  
		Last Modified: Thu, 17 Oct 2024 01:14:13 GMT  
		Size: 101.2 KB (101198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3a024b469dc833f1b117191f4dae4fd036f6729de34fe4c3f5fbe5408f9024c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101928b8d891e205132d409763214714fe01b38136b34a627a4ae94c442116ba`

```dockerfile
```

-	Layers:
	-	`sha256:2aed5a3502308b3aaf448669b2329c76c6b7433ce767399599ae487e5410d6a6`  
		Last Modified: Thu, 17 Oct 2024 01:14:13 GMT  
		Size: 4.2 MB (4223843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60c2ab445d2d8182dbe8fc17588902ed8acf6960844c855371abb68170201531`  
		Last Modified: Thu, 17 Oct 2024 01:14:13 GMT  
		Size: 13.5 KB (13516 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8816f2a11a9a24a5ceb557b7510ac1f52e4380a0d1315fc114bccd78573753de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64943846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a779fc63603b730c637b15731a1e50df693e12e5b5dd77efe660f19eccbbff54`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa186315adacfb2b622451de8307f55c83bf74e5926cf7a13b2237e95e062145`  
		Last Modified: Thu, 17 Oct 2024 13:29:04 GMT  
		Size: 11.1 MB (11105848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3aef7bb5d567bc9ddb61f3ff5d2dea7cc2918d39c69a5122c9002662c4b91f`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb3afca1c9a390e8851a572c7497b59366792c63250de9dece52aaad7385c8e`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74a69755a92c3826c34c23ebbacc2bafd74218d37c26d56b22f2f565ea404a5`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:60968a51d2dbbe8ddfd18d2179d21308e651bde252f4a4bcfb6b65b6876e1f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0e8d67435179a92167b9d4b586b64fab1c482c2a0e3cb6cf19b7a270df14d5`

```dockerfile
```

-	Layers:
	-	`sha256:1d5c77c580ab63b8233a862bf49c9e9fb9dbd695cce715b655519a0ae019c34e`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 4.2 MB (4223448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dc7d369f1baadc307fa80e7fcd2482b6a6da3375ebbbbd347d5ca5692879ce8`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 13.6 KB (13635 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:7ca0e456e3a0a81c71572f9d1c3e40d331a38deb2d2f28e57ce899d529a86757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67681303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfef12c4cc1aa4ac79ab75c71ae969b6bfcad329897065b332346f702886402`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad6f406d084c95bf1a05be3a1e7c6946e064ab06274e6be80133ae9a37d8d61`  
		Last Modified: Thu, 17 Oct 2024 01:14:18 GMT  
		Size: 11.5 MB (11500400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785fb89b81e22ed1038fb070ba1e6f792d7dcb1064180a6a72d0337a0ea69ada`  
		Last Modified: Thu, 17 Oct 2024 01:14:17 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490843939739e2d5334f2691e73b505dab3d7cdc6ec7edad23746bcf6c509fab`  
		Last Modified: Thu, 17 Oct 2024 01:14:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d067cd68047afb861604ab9041e2d7b7d900a995d89023cbd0390c49fd0a99`  
		Last Modified: Thu, 17 Oct 2024 01:14:18 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3fcd7c199628ea6a94e7272ce6eb4a6e50ad342bb83e14b07d576627f482980b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4233793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446483d2c98e9f42219d84b4f774c6b6f710e6a16e89e5453b2d7ced44d01846`

```dockerfile
```

-	Layers:
	-	`sha256:798e972e1b30ec46232b6a35b7a04ba9380151e3819245060f7d7a7308bf97b1`  
		Last Modified: Thu, 17 Oct 2024 01:14:18 GMT  
		Size: 4.2 MB (4220303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3730ceb7b012ee1771baacd2b30efc3350468ac280a0910f296856eb19b60f08`  
		Last Modified: Thu, 17 Oct 2024 01:14:18 GMT  
		Size: 13.5 KB (13490 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:8d27ee78f2e00c10238e7f713ca08ef2dea31e8c18a2cd330d516bdef4323656
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
$ docker pull neurodebian@sha256:d1a43d2f25278216c1a9659bfb7c6ec44c80ccd5066649eaf2b0433519242cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ed153cb8527c84eaed449a92f0a656eee5b7d536a5a321c3461a15b862b1ec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f0102900c339db81394076194f5cabc70fd1bd5249b9e279c4c3dff279fa9a`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 11.1 MB (11105025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27e37472add233bbd47e458c8da9afa77fa6eb3b050d84b6a2344733ed9194c`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef3beccf4e525ee8ecb4d8fadaa6b201ac1d55f2e74262d65ae213b3e54144`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64a8c95417d848f4815e9a7b48787a5276ccc3ec7ba73faa304a009fb1d875`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 101.2 KB (101189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fe45998b41628fa647072b6cd3f22a62e5b9e2905f597f1b0a6932f4c4ee7c`  
		Last Modified: Thu, 17 Oct 2024 01:14:15 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f2422cad8533344783d8b8e9380271e3e9e2d273ad283d1e9c0e4d3a70559869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8ba2c3e63c2a0c16de87d27e28cc4d76d86339bba0163ab49426816a18fcff`

```dockerfile
```

-	Layers:
	-	`sha256:889e8208d5f5df28cee3850569bed5963b2617fc3fafa41ac08273dede19fdf4`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 4.2 MB (4223879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd2f394dbcd432364bb73783b3681f40544b3f30d1673fed9ffcea8ff18b60a`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 15.6 KB (15550 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:53e5c26be17fcd310af32bab934f727db59bf5b3131fe78781f3be135109ba74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64944206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bac3ee2359939f8df6987de2ed95c70bc7bc1d87ec943680aa265ea423bbfec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa186315adacfb2b622451de8307f55c83bf74e5926cf7a13b2237e95e062145`  
		Last Modified: Thu, 17 Oct 2024 13:29:04 GMT  
		Size: 11.1 MB (11105848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3aef7bb5d567bc9ddb61f3ff5d2dea7cc2918d39c69a5122c9002662c4b91f`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb3afca1c9a390e8851a572c7497b59366792c63250de9dece52aaad7385c8e`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74a69755a92c3826c34c23ebbacc2bafd74218d37c26d56b22f2f565ea404a5`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934ef0ee7079660d2db15b0ffa13238f756f54d444d1dabe4f9db4f30d5d54ba`  
		Last Modified: Thu, 17 Oct 2024 13:29:24 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0ab1d82d946c58360e2a6630d5c49be18c5a6981f9a5108baf8fe490452c452a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52106933ff117a899e05fe9719b2e92d354c61337b5a5f6ea69b3541cf7f5d2`

```dockerfile
```

-	Layers:
	-	`sha256:0543bbddbed63383d3185028800ff399d5985db6b29fd7101ded92416736ff7d`  
		Last Modified: Thu, 17 Oct 2024 13:29:24 GMT  
		Size: 4.2 MB (4223484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a2932345dfaa0b574d9ec1414274647c8018eb268c34963c5f709c7ab15a939`  
		Last Modified: Thu, 17 Oct 2024 13:29:24 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e3be5a5c53975c91cbd979fd670794915bea99bd476d526a357ac2ed86967741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67681619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351ec6e66e29aef5a228977c44b8f85e3f12952fe4d8517681a201038797de6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79423534cf5965fe2f04fc5e975a694b4f8638b3320caa4c643e9ed24444bbb8`  
		Last Modified: Thu, 17 Oct 2024 01:14:28 GMT  
		Size: 11.5 MB (11500373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480013482db658c37a6c2ffea386ec2af1f1f4c4f5c2f5e2fff0dfbd003657cb`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce407a6bb2bfdc3323339b75bed14f72ccd45b312cc74e36d338dd1ec0ba424f`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8aa075707f8ed6aa84772b58aa32934020c09898ac7f66af7d51ffcd498d5c`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 101.1 KB (101074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4ec9646e3b4d8c55e9ecdf6614030b3ed43d718ee92062ed8c317666411935`  
		Last Modified: Thu, 17 Oct 2024 01:14:28 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:447a2ef6cca5559abee275287989f394b1340cd5c1401eee08c935ca552bd6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccb8928053c0e11dca31752e4b544026893738954a0e0b3275e7e5f55121f0b`

```dockerfile
```

-	Layers:
	-	`sha256:ca8421cbbb10d45e2d2886e9f17bb470ba726da45075619590b1c0ce67f4a3b3`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 4.2 MB (4220339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c81157c4a2f79bca7249db43b05996ea04ea5426501cf870045d0eece9cbddf`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 15.5 KB (15523 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:8bcdb02c955c552289fb14468e3d0eccac712d0a170f1fff5601f3f3af9d8a49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:a0c6cb45ac1cfbe06c47f14d684929ff5f5907ef7f083c360195214c3ac6aca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1335fc867ea7b822d1b6882dc96ad365e5cc4643152d61c5fc8a7bc5f85a988`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49fa7316f784f5cf307546c8c97bd1b9f3a1fd2943c27fceb71ec2dd6409f48`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 5.4 MB (5360278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb7c65bbf482527df64ccec5d79c08cb11cf2d1f4054f4977e47dad48ff8435`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e678bedd7e50e1ba3e947302d4a3badb36d988b369aab4b47c1fa78259c23552`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9792897da4dcee6732822377f46272804fb1e9b7f31dd60d17894a127edb839`  
		Last Modified: Wed, 16 Oct 2024 16:13:43 GMT  
		Size: 105.3 KB (105327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:848d25161f517586e1457fc807e778d3305bad2daae744ec21fc37849f68173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820220dbbd11c6d8f3103b1a3ed83da871c77d7b02f18798badcf3237303dcae`

```dockerfile
```

-	Layers:
	-	`sha256:27970857ec501c025d084e20e5352a5d5ddc17824cc89a85f49e7025cdcb4a02`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 2.0 MB (2002651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:849d52e89f42eba3812416ede3dd4d1badb9a69a5a982f874e39c325041eb9a2`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 13.4 KB (13444 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1a3f2e41cb72abdd7dcab281d6513ce2dc547865fa3b4ba0776bd58ea8a5de97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2c98411bfbdccf11946d245a8061c56c6ce058ada6075d911256dd80fadff8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6101036d9458690903008f9743d7d9982835f206b38bec0aee1147faccc7c0`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 5.3 MB (5340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a29390bcc04ab62cd8664a0c5eb9c2c8529bc1cf5a8fc1e442f9740f53d73`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a06a5898141ddee96056f1057c0595e290735b4831567d9e98c36af5687cba6`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead23b60010d07ced4212e4cf8a6c4f69eae17b7d32e4a35b7bf00c6df7eacd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 105.4 KB (105412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1f3f34f75e1a4bc32b849a9ffc880a30708443a7fdc0da8a50c2e90180094f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5772b0ce1260ce48effc24ad2f6bdefdb4674ee0d585774b4464dfdaa8df07f`

```dockerfile
```

-	Layers:
	-	`sha256:71ee94546588c20b92a492d129395aac336c0ae8677f9f8048b6890a1e640901`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 2.0 MB (2002879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa10decb4cbaa5f56d95540086539ce9a7bfee79f97ecf26a18eb6160c482bbd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 13.6 KB (13563 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:e1b1eebaa7be7a7ae8986f10c005fbaacce6a33e73c7193cef12dee6f49b40b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2ddc9018acf97b1f5814caa6cde3c3d36dc386f558589639e00bd07b61c4ceed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02507bb93b25ace19e3dbcf9e5a746ee64169a6e6641918f946da8db0e4d17b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f4005701787afe01df59207e8d67264732bba189629db1779b4ffa79571550`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 5.4 MB (5360288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6862ce93e83033ea4be1d4f8bd4ea70b498c761c3664782d446af47aa9926b`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce53e76a062f11aaecdb2eaab737adaf3dfe235440d4e34cfa7bd8bc8634e70`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f662144d756ef598c43631f18e5a5aa12b2a8e2c719e17635359530cbf9a9b`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 105.3 KB (105328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c113f4052eb4bc0e89d69bbfef200be8e9cc348104fc8ae5bc167ebdf6ac683`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fdd9dd95911aad8010d1bd7b668cfc9886a64e712c66aeab16529edd5642e84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419484197e2594f495dc65df02606517cfd33b3e8fb27db49620e293bfb8facc`

```dockerfile
```

-	Layers:
	-	`sha256:96b650f1cbef5c5dbf1b7069ca052e04734ab3f40d4e9ed771e9496d60fd999e`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 2.0 MB (2002687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdacbdc41b77b356c35fb81b7e0fcf121e4d6c1b38d2d913103141df6f522c9a`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b3f6acebf8e01d4ccb64904ddb4e553df094a7fb6223b50f683882a0756a284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9be140461e203793948a95c87503859fadcb667866ac155c79cf9aea88c1edf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6101036d9458690903008f9743d7d9982835f206b38bec0aee1147faccc7c0`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 5.3 MB (5340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a29390bcc04ab62cd8664a0c5eb9c2c8529bc1cf5a8fc1e442f9740f53d73`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a06a5898141ddee96056f1057c0595e290735b4831567d9e98c36af5687cba6`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead23b60010d07ced4212e4cf8a6c4f69eae17b7d32e4a35b7bf00c6df7eacd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 105.4 KB (105412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4975400a8d7cbc9b67c0e50618fd95fa63506aa713da18a3da28accdeb57768`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b26186688e44f87210438ddae17d14c31f634b630c497d04013b36ec09d92089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b3564811c260795602aab1de18bc1a0e9abcc4a1a00d4aa08bf2c13102fd50`

```dockerfile
```

-	Layers:
	-	`sha256:5f09b22f2f9e9d8a1f0ccc85ccd622a779576a09f4ec13d286e85c8831be03eb`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 2.0 MB (2002915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc6326745662ee2e02b1d747a2d2ba13494721e28def82decf35cf47a1614ff`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 15.8 KB (15808 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:8cd25968c7a8dda57e86f5f31179a392780c365d049c245f1563df254a345b6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:b5e2ad2679d21dfb98319132904ff13815643d741d29c2cbd61f795d2cfce2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03035b5fafec30a11ccaf9e676191d30bf2a93a2c961ae50bcdeae21ecee68c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e5fc20939f49ca46aaa63fda94b740a46522034dd33a99dc846c2ab47da385`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 3.6 MB (3622683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d7c12d3dff8024cc7a65a06760eefef7523e92d4ab01561da2876474be6e25`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257f9b0966cd5484318ba1e2300bcf4102ad856d15cf79307d6575cb919be75d`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25429882efb06104ffa477fe41e22a29ad87a1b8b5a97eddc221fb3cfb85bc29`  
		Last Modified: Tue, 17 Sep 2024 00:58:50 GMT  
		Size: 110.0 KB (110041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d732e29d091ef7f0e630eef553f727bdf00995f77c7dcc07b0561d4792f4341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb4b42740c8b876bb56d509444cd2d22fd632ea9c6254cf4af8ef60cb72b5aa`

```dockerfile
```

-	Layers:
	-	`sha256:46449a2a17035de35151d0f04752a18008bd77cdb9bd76b7f1465ab848857267`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 2.0 MB (2041055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229f62c1b512cec8166de552b1e0085eb7526f3474781a15c9cfadf62c2436da`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2e8ddba19dffa270b72c0c17efca5bea22c862945352f06ad9391ca69ae180ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e64399ffc86a2a302a5f8b07efe84fa560a195e25878c4a52e8f5d97367769e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ce4fcc7ac84933f63a18dcc1f51edb6a54d593241a9ad9eda2da49c4a0a93`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 3.6 MB (3594202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420d28ea54fd4f14398ac3479d15abc9d09b6fdfd86904d39445315fa9ccd4a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89798e75750754cd749a20391aabd4a2982ab8ea03464d1069af684488290b27`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a706a92656db8d1c42d48439ae56eb9ef232cfcd87be0f53362d7da0045c9f6`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 110.2 KB (110158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:769792b0a9ae99abbe1b81296f09e1e53c2e662643848544f1a641d54f8b29bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ab15b050723ad8ecd0ff560efdd18d3d1451cbd92375f54cf16c418e647366`

```dockerfile
```

-	Layers:
	-	`sha256:2a92568efc9bccb357a48dc2f8cc5ef4f0d34112762744fc1408de6d45f8e34a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 2.0 MB (2041314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783fe908caebc3d7a05968a298b4c97dd56aff0cc5841272d2f31f8d0eac4efd`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:c35390a21d7dcdaa5248caedb0c2d1d3f2b9a31a1ccc6a5fd082bc8262ef35a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e45ad58f9dc146f7c58fee7c828c3c6831e76bdb9cf7020f9f7c9448d53671ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4ea79fb23e81c99deef7e3da0330d8995389a5ed5528314613545bbc38a650`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e444df7ecce18d9b6a39b30f8f893e46de9a6c8393753ceb73f80be5147d5e`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 3.6 MB (3622684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eb688a315dc9dc281db41ae45a5e1651f96d5b6b93100b8f6b3604a1b7be90`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18efaf2abf8b145da9341e025a8599685148d724adf71187513efcefdc1eb92b`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c03e7463fe28779caf76a60210e080067f4e00e4a28d1ef22b5f71aab3511f`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 110.0 KB (110044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a748ff3cbe6a5eed1e2b979d6648c667fb7a29be6b3e2bc14ea06d88519a0592`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:49d3a7c89f96056348bc2f29c7aaab1b27bde7d7755e5cea5fe7102dbc63a96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0141b248fd4a83635efee725ebffc6599bb6e48aedbb01287016be2df2e9e29d`

```dockerfile
```

-	Layers:
	-	`sha256:2aa3ae2b7c2d8c84a96d9dfae22e8bdbef344f1dea22754309dafd7d8ba3fa7f`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 2.0 MB (2041091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48b6d14af7ecf44b9066d810db720df1078da0e69b612cc31771ef41b2957b4a`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4a2bedc35b23fd303d37b492a4dcd265b749cc561bed81266ef4fd4f072ca3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cc596bfd27c527f722fd0f60344b7c29c0ede0e0215ca28663dd6f7b11334d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ce4fcc7ac84933f63a18dcc1f51edb6a54d593241a9ad9eda2da49c4a0a93`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 3.6 MB (3594202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420d28ea54fd4f14398ac3479d15abc9d09b6fdfd86904d39445315fa9ccd4a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89798e75750754cd749a20391aabd4a2982ab8ea03464d1069af684488290b27`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a706a92656db8d1c42d48439ae56eb9ef232cfcd87be0f53362d7da0045c9f6`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 110.2 KB (110158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0571d1820815c6ffe6445310d6d56c0904985a7a40ce55ea60111c7ab14c14af`  
		Last Modified: Tue, 17 Sep 2024 02:37:09 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15e423dc66f68b2fd18342bafd40c16c24df1ff2d5a105e3d23fe7a7b66e4859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae14030ec66c96db8f89c291fc02780ff4e9dd29fbe18b7deeb19f1a70811d83`

```dockerfile
```

-	Layers:
	-	`sha256:b8a537c7762547e63f17b420cb0912f491db0829af8089494798ac00e311b1a7`  
		Last Modified: Tue, 17 Sep 2024 02:37:09 GMT  
		Size: 2.0 MB (2041350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab7d3d2aaba018f1a288d03ac3c709c72564deb83d89ee6d4197767b31a448c9`  
		Last Modified: Tue, 17 Sep 2024 02:37:08 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:6fd67d55fd53ff6df3b247a63873f9690c1b471533ec11f775eb30c8eb54725b
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
$ docker pull neurodebian@sha256:3697dda71c97c3f2331d51e833f6004024b1b1ff9c6f985ac48a7f206f372d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66b226bfd77945145ba8dbdb314a327f8d3e57c00b7ff60b8c612e99ec189e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b762b97ea764326ee7c78d3be70939e4158333f93d124f91739a6a96a661fa86`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 11.3 MB (11266584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402ca42a66cb385c6c94651438c30b60632bbdcc199de7afa4b036ed8247d7df`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a35ac53ffb5eb6a25a8b3a501e4ff0a421f6b7e0440548aabbc7c1aad826b53`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a6e032b96453782d4fdb1fff50b61a365a71a9bff219fa43b8faecf4d5d645`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 93.1 KB (93133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46f40f5380579c474973147a5d1d5c436d1e8f8fa806d11cbd13b10e1511b852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a8a55f1f8b9a5e99a76a84ccda60e5a260fe1aeb5043321b56d4d4ee9951eb`

```dockerfile
```

-	Layers:
	-	`sha256:6f4a965387af32daf99856e8ddb053fbdb29217654f0e62264c2dd0649125620`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 3.9 MB (3924252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4881891bbb1e76cc32e634bf22607dbf8586ce82543820147144f8f75940c3de`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 13.8 KB (13823 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:050e6d336e606fbb0e300affdba33b0e7112897488c1080d655e6a8a2bc44425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12cf34310545c647cd06d3fceb8303925590de81448268c048a09001291f1154`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b222ea27d3a13a628f27fb485c2c8953c435cf879ad43c99108ae24a1a8538`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aa7c14ee96487976b1787f395d3da08538e6eb4bc1212666ffac800202f10b`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103fbbaf04667aeef928e69b2b8457085af18a4894f429dfb4cd0ec52dfca876`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370293ac9e0cd3f1e79e181dd7401ddcfc4d9579c4bcc066993cb19373d455b1`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 93.4 KB (93360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6c2dab71f6c0b4093d81cca7238cb6dcd0e421277b6ef15f14c33ffb2d5ae297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d735f4ccf82806b86c0895be8e82f45c0e36446a82405ebc53b10a90017eb2`

```dockerfile
```

-	Layers:
	-	`sha256:e8160276deeea36db3deb56f2bf3cae66d45878144632f200674b7bf3c89c2b2`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 3.9 MB (3924505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dab3dee07749ea50941c86b101d4a545ee827240618545e172488aa205971f7`  
		Last Modified: Thu, 17 Oct 2024 13:30:03 GMT  
		Size: 14.0 KB (13954 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:896545d95a4d05752deb3b2b3f8eb2e710b4f52da6553cee0676abb5a7d4280a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0ad284f6be59a7c68b584bb5c1cc330f70b3690a10445c92e63e73e3d56535`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac817a808ff957a7e831213b07291fc20229bc43affbf623c78a261ec0325c5`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 11.7 MB (11688945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bf606e708bc7cf8f28d6e78f0274840cd2b7301440a2bf866d5204ef18fa14`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ce82a925a96d328fdcab86c0dbae82212e7cc285b177465deebb2d3fbe9067`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3afcf85c6057a5d9d8eb7c146fd97cfe8fd83354d50596c26cbc3d28cd852a3`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 93.2 KB (93249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8607ae6ffd66c4c0da8b82f00cd85627faeea84b5e54044d05b67f735d74af54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ada56f849e4a4098758070e52baa926b4864474eee5fa5d4dc22d1058259af`

```dockerfile
```

-	Layers:
	-	`sha256:5bd90987926d222eb5f929a5da7c7efe871eeb25f75f8c2cb76d7a280d621262`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 3.9 MB (3922169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a0ce6a103d838e660923ca4f89ff0c6248d4d1d71fcc5779c4b15c1bc50d9e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 13.8 KB (13793 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:f1861e0571166fbfae31b98ff9b3282e233f809fa114ae25b0463aab1a19ceb5
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
$ docker pull neurodebian@sha256:af988d6adb2891ec552ee9990d0ed9def1f72d4be51fe2d300fdcafc016069a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59654381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394cd951cd1004584c418da9435be7a462e40a81740e3cf4f9bc52d014181909`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43fe9fa1ea5e364ff54cf0d2e96455c6f8402592c32777e452028e59e4f07db`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 6.3 MB (6289386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461430c5027f3982ecc44a03e50c617a66caff8d40bb1cf5ef7414dc7a44a51b`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d7d04684bd6207fd3fcdaa7adb93c457ebb7ede1f494ad1050bee39838aad3`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3c4d8af236dc0db54a33b8a382e921a52f482ebdedddff3af00da511fcb5ca`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 91.1 KB (91135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bce5156dc1fb09c732081a1fc7a9e5ea6ae57c5800e3909700a8f313fa0f99b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813c1b3abd826f7630168733dd6ca5f043765ae343d96d62556dfd0539ad11ee`

```dockerfile
```

-	Layers:
	-	`sha256:736401022b618a8c56d8b7cf8c577987243a98a5a24c0c31342af864ab7fb80d`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 3.5 MB (3529844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9e41aadddcdd8e9c307112d89d858cb3da930d97f8730ae366272fa4cb0e08a`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 13.4 KB (13435 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fceb7880ecff05e3fad1bd34562c0fee903764280c693fc06edbbb6b5093843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59996796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0c1c96bf04b236a96d091b001f637f30fc4267568e19ad379ebe0583a99ec6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207c4d641255ff6bd7b8ce630c8cf947966d1ff05bdf86f951c687f989e2f5e9`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 6.3 MB (6273546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c25f32db1b1126487143c75b9ce0d496e410c5bae14e76068c7767c3979041`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1aa1fca4ed404a2dafbd083628f990869ee0dd7b253df1199afbf67da6e338`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab4cc25b7109f5af55ff37456e9f7fe94f979dff175b36667bc066bff22439`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 91.8 KB (91781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1f7c49f91f70d5fd7fdfb393e1255d65bf3963462449605a6b498c5dd601a397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3544438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c771ab1f610171f7a17f00660c97e22c04d5fa10ecb778aeed2a621ae3e94e5b`

```dockerfile
```

-	Layers:
	-	`sha256:5e03f04196d30611ce1df27f1d3cc5278240cd13a3eab0cd469eb97f145011bd`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 3.5 MB (3530885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec9935b092fb7d33339c675b1c15bbf6ecc7bdb04d95950c01ed5fca038b5e8b`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 13.6 KB (13553 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:b90f2c17e980947a7b20b3fde97e69b919f586f73c3878813c90846e895b4228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60828971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28344bd679e7fa6b7c4fbb3378f9939e9325bab60060c34ac0858e971c02d2ab`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bf9a8e67481cd7b5126ca983ff2eb6360719268ef0d901ef9c0ab1397ebdaf`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 6.6 MB (6617928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93a3157ecf2b3e90f14bb799e97539e5da9b8e54c2fa24fb906ee69c4f58f3b`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7faf9478aaf287f3c93ce350f01a65b610825764a68728311533510f3bc121c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c402fe866ebbf8d95ad0581375c4226649ef229de419a9074877580e2287f4a`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 91.1 KB (91086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5508b170e6de67c39a46f664e38e6a6e388809ca959d663ca63d5647a8995f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3540353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c76c89ee979c78363abaee47580b7730e828bd4277b1eaab481c54ca64e02e5`

```dockerfile
```

-	Layers:
	-	`sha256:a08867bfaef8835491bd411c4b001522f5e609221f242241f719262e6ccda1e5`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 3.5 MB (3526943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d525a98f9cd254f377fa72ecbf05fda0d300d7e311a88722b4e21fcb727eb46`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 13.4 KB (13410 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:f23847bbf2fb1f2064a746206684077fb8f9eeafc6b6e739bcbe6b759c9554a3
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
$ docker pull neurodebian@sha256:b2551aed7873b42c6948e4b859e19766d92fdfa9124e197eb17d7e01396a956f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59654703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdde34f32b6bf6419324db05b4b8b5fb9b6351610e3fb059cee7f5bd4e5195f4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc7e4c0fdb6fdb4dbba108ecd5d312d29ef194ff9fcbe5d6b45de7caada7a15`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 6.3 MB (6289352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93a3157ecf2b3e90f14bb799e97539e5da9b8e54c2fa24fb906ee69c4f58f3b`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7faf9478aaf287f3c93ce350f01a65b610825764a68728311533510f3bc121c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dad48c7fe85a9fcbbcfc1c1083d15785484d25efd58f98a59df48aecc124e08`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 91.1 KB (91103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb07a3a2622e66aa964a597aa305a0c72a9f55414a983c902e52931a87bb172`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f0dc4fccbda04d9082a17dfdcf47af681064b79911dd81b78c74058479c14f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abd151be0aa00d64da82c73b693e2c7729a6a8a65244bf3815c4aa2a56aade9`

```dockerfile
```

-	Layers:
	-	`sha256:646ad1bddf77b612de799f8d4f963ed5e11b83eafd6cf611481dbda0d44dfe7a`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 3.5 MB (3529880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92efed635b4a0876acf283e7170082bb89d0f2d6f397ab3e4a8cf9fe8faa62bf`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 15.5 KB (15467 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e9b1dc92def9b23d4147b701479a4c0cb4287a99fded2945d0f6141c918d1718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59997190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e1d085caeb9723f2e7d1685e044ddfd1251b756793da9068dc8ef89912c923`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207c4d641255ff6bd7b8ce630c8cf947966d1ff05bdf86f951c687f989e2f5e9`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 6.3 MB (6273546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c25f32db1b1126487143c75b9ce0d496e410c5bae14e76068c7767c3979041`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1aa1fca4ed404a2dafbd083628f990869ee0dd7b253df1199afbf67da6e338`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab4cc25b7109f5af55ff37456e9f7fe94f979dff175b36667bc066bff22439`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 91.8 KB (91781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376ca4ce57be9758785676dd94566197e97b56e273d0d68b507106d5fb088f89`  
		Last Modified: Thu, 17 Oct 2024 13:32:59 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dbb9f5c6a73482e60b6f663408c48da9384405cc218fc0247429a4db9e0a0c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3546522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f10c7d37e9b03e2031feb3ef71d8d1bf5349441266305f933b01c78e258c35c`

```dockerfile
```

-	Layers:
	-	`sha256:ae362c8599903d2c6f23db6caf041eec1d93bdbc004c5115130317bed59a413e`  
		Last Modified: Thu, 17 Oct 2024 13:33:00 GMT  
		Size: 3.5 MB (3530921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857190c4726e7bbad6a89b69d081e58436891e0510c537d4d585edd56bfece2d`  
		Last Modified: Thu, 17 Oct 2024 13:32:59 GMT  
		Size: 15.6 KB (15601 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1a746becea805a95a3b1d8e2136c588c82f6640fabbf5b5d22b913ad88128d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60829482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fbed28d59a1fde84fdbeb100a9ebdf604b856235061876e877aad0b4be73e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035359a3193290ee93a025ca5d676f11bf3efa25b6fddf81d67bf8d3589b5028`  
		Last Modified: Thu, 17 Oct 2024 01:14:38 GMT  
		Size: 6.6 MB (6617986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6952f46bac813925be650db4453b8ca209127d3493fe97170e8fdd998bebdc5a`  
		Last Modified: Thu, 17 Oct 2024 01:14:37 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f6a0313c5de2ce998d42e460162c0b4dbe7db82dd1a2ade4329507eaa884aa`  
		Last Modified: Thu, 17 Oct 2024 01:14:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627145859a1fd6976564bc212d417d5a9a021b48d6c5cd0a9c27f2f0c0be85c8`  
		Last Modified: Thu, 17 Oct 2024 01:14:37 GMT  
		Size: 91.1 KB (91141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd40c06f31194f8a4e83082b6d1fcb10e09061c6020cf18bf235dbf216f4e048`  
		Last Modified: Thu, 17 Oct 2024 01:14:38 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5c4d6d229eff64c513e035a637fdf70b11dbed69d4744893382bb2d655526e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8763464ded6610a3ee8e5d2b2c86e7b273c0e22ea00d4f5dd76840ba5564328`

```dockerfile
```

-	Layers:
	-	`sha256:75b677fef86179ceeb75d8f6689cc441eac33fd1413684cda9bbe9c0e9a32c81`  
		Last Modified: Thu, 17 Oct 2024 01:14:38 GMT  
		Size: 3.5 MB (3526979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8a9cdb86f97778094b27f0215ad427744de8426832800947d789f3e3cb0c8d`  
		Last Modified: Thu, 17 Oct 2024 01:14:37 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:db35cd2f9748f6b233c53b0fc84bf3a5699604ac5b06898e48f7c15c7d672d82
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
$ docker pull neurodebian@sha256:96625ffae5306bbefb90c138d60615fbbc3b0048004bdddab6c9880c2a1dd3c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66288904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7249c84eb570d86afedf4eb3c16a5afe113846e5b771daae85a32dfa8f976ba`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1b510b0107687e655df5468a134f88f9ace83c7baf75178bbad0baefd8454c`  
		Last Modified: Thu, 17 Oct 2024 01:14:13 GMT  
		Size: 11.1 MB (11105105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9910055e69f675b61256717f5fface946970d9e3a19eb1c3ded13d2c80baa278`  
		Last Modified: Thu, 17 Oct 2024 01:14:13 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d1e63ec04e9a741afb3ff13cd8719bec3db300455606c0c6ca0cc2bad81f4e`  
		Last Modified: Thu, 17 Oct 2024 01:14:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba7a3b45b6316252e7fbef945abbe5998041ee3a89d36e3f6894a7b17e26131`  
		Last Modified: Thu, 17 Oct 2024 01:14:13 GMT  
		Size: 101.2 KB (101198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3a024b469dc833f1b117191f4dae4fd036f6729de34fe4c3f5fbe5408f9024c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101928b8d891e205132d409763214714fe01b38136b34a627a4ae94c442116ba`

```dockerfile
```

-	Layers:
	-	`sha256:2aed5a3502308b3aaf448669b2329c76c6b7433ce767399599ae487e5410d6a6`  
		Last Modified: Thu, 17 Oct 2024 01:14:13 GMT  
		Size: 4.2 MB (4223843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60c2ab445d2d8182dbe8fc17588902ed8acf6960844c855371abb68170201531`  
		Last Modified: Thu, 17 Oct 2024 01:14:13 GMT  
		Size: 13.5 KB (13516 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8816f2a11a9a24a5ceb557b7510ac1f52e4380a0d1315fc114bccd78573753de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64943846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a779fc63603b730c637b15731a1e50df693e12e5b5dd77efe660f19eccbbff54`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa186315adacfb2b622451de8307f55c83bf74e5926cf7a13b2237e95e062145`  
		Last Modified: Thu, 17 Oct 2024 13:29:04 GMT  
		Size: 11.1 MB (11105848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3aef7bb5d567bc9ddb61f3ff5d2dea7cc2918d39c69a5122c9002662c4b91f`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb3afca1c9a390e8851a572c7497b59366792c63250de9dece52aaad7385c8e`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74a69755a92c3826c34c23ebbacc2bafd74218d37c26d56b22f2f565ea404a5`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:60968a51d2dbbe8ddfd18d2179d21308e651bde252f4a4bcfb6b65b6876e1f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0e8d67435179a92167b9d4b586b64fab1c482c2a0e3cb6cf19b7a270df14d5`

```dockerfile
```

-	Layers:
	-	`sha256:1d5c77c580ab63b8233a862bf49c9e9fb9dbd695cce715b655519a0ae019c34e`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 4.2 MB (4223448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dc7d369f1baadc307fa80e7fcd2482b6a6da3375ebbbbd347d5ca5692879ce8`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 13.6 KB (13635 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:7ca0e456e3a0a81c71572f9d1c3e40d331a38deb2d2f28e57ce899d529a86757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67681303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfef12c4cc1aa4ac79ab75c71ae969b6bfcad329897065b332346f702886402`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad6f406d084c95bf1a05be3a1e7c6946e064ab06274e6be80133ae9a37d8d61`  
		Last Modified: Thu, 17 Oct 2024 01:14:18 GMT  
		Size: 11.5 MB (11500400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785fb89b81e22ed1038fb070ba1e6f792d7dcb1064180a6a72d0337a0ea69ada`  
		Last Modified: Thu, 17 Oct 2024 01:14:17 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490843939739e2d5334f2691e73b505dab3d7cdc6ec7edad23746bcf6c509fab`  
		Last Modified: Thu, 17 Oct 2024 01:14:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d067cd68047afb861604ab9041e2d7b7d900a995d89023cbd0390c49fd0a99`  
		Last Modified: Thu, 17 Oct 2024 01:14:18 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3fcd7c199628ea6a94e7272ce6eb4a6e50ad342bb83e14b07d576627f482980b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4233793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446483d2c98e9f42219d84b4f774c6b6f710e6a16e89e5453b2d7ced44d01846`

```dockerfile
```

-	Layers:
	-	`sha256:798e972e1b30ec46232b6a35b7a04ba9380151e3819245060f7d7a7308bf97b1`  
		Last Modified: Thu, 17 Oct 2024 01:14:18 GMT  
		Size: 4.2 MB (4220303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3730ceb7b012ee1771baacd2b30efc3350468ac280a0910f296856eb19b60f08`  
		Last Modified: Thu, 17 Oct 2024 01:14:18 GMT  
		Size: 13.5 KB (13490 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:8d27ee78f2e00c10238e7f713ca08ef2dea31e8c18a2cd330d516bdef4323656
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
$ docker pull neurodebian@sha256:d1a43d2f25278216c1a9659bfb7c6ec44c80ccd5066649eaf2b0433519242cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ed153cb8527c84eaed449a92f0a656eee5b7d536a5a321c3461a15b862b1ec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f0102900c339db81394076194f5cabc70fd1bd5249b9e279c4c3dff279fa9a`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 11.1 MB (11105025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27e37472add233bbd47e458c8da9afa77fa6eb3b050d84b6a2344733ed9194c`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef3beccf4e525ee8ecb4d8fadaa6b201ac1d55f2e74262d65ae213b3e54144`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c64a8c95417d848f4815e9a7b48787a5276ccc3ec7ba73faa304a009fb1d875`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 101.2 KB (101189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fe45998b41628fa647072b6cd3f22a62e5b9e2905f597f1b0a6932f4c4ee7c`  
		Last Modified: Thu, 17 Oct 2024 01:14:15 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f2422cad8533344783d8b8e9380271e3e9e2d273ad283d1e9c0e4d3a70559869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8ba2c3e63c2a0c16de87d27e28cc4d76d86339bba0163ab49426816a18fcff`

```dockerfile
```

-	Layers:
	-	`sha256:889e8208d5f5df28cee3850569bed5963b2617fc3fafa41ac08273dede19fdf4`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 4.2 MB (4223879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd2f394dbcd432364bb73783b3681f40544b3f30d1673fed9ffcea8ff18b60a`  
		Last Modified: Thu, 17 Oct 2024 01:14:14 GMT  
		Size: 15.6 KB (15550 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:53e5c26be17fcd310af32bab934f727db59bf5b3131fe78781f3be135109ba74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64944206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bac3ee2359939f8df6987de2ed95c70bc7bc1d87ec943680aa265ea423bbfec`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa186315adacfb2b622451de8307f55c83bf74e5926cf7a13b2237e95e062145`  
		Last Modified: Thu, 17 Oct 2024 13:29:04 GMT  
		Size: 11.1 MB (11105848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3aef7bb5d567bc9ddb61f3ff5d2dea7cc2918d39c69a5122c9002662c4b91f`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb3afca1c9a390e8851a572c7497b59366792c63250de9dece52aaad7385c8e`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74a69755a92c3826c34c23ebbacc2bafd74218d37c26d56b22f2f565ea404a5`  
		Last Modified: Thu, 17 Oct 2024 13:29:03 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934ef0ee7079660d2db15b0ffa13238f756f54d444d1dabe4f9db4f30d5d54ba`  
		Last Modified: Thu, 17 Oct 2024 13:29:24 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0ab1d82d946c58360e2a6630d5c49be18c5a6981f9a5108baf8fe490452c452a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52106933ff117a899e05fe9719b2e92d354c61337b5a5f6ea69b3541cf7f5d2`

```dockerfile
```

-	Layers:
	-	`sha256:0543bbddbed63383d3185028800ff399d5985db6b29fd7101ded92416736ff7d`  
		Last Modified: Thu, 17 Oct 2024 13:29:24 GMT  
		Size: 4.2 MB (4223484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a2932345dfaa0b574d9ec1414274647c8018eb268c34963c5f709c7ab15a939`  
		Last Modified: Thu, 17 Oct 2024 13:29:24 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e3be5a5c53975c91cbd979fd670794915bea99bd476d526a357ac2ed86967741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67681619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351ec6e66e29aef5a228977c44b8f85e3f12952fe4d8517681a201038797de6b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:31542b73f2ef95a398c04a3361c14f990df163d3e44e6722e9514136e87e3e77 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cd6bd96dbaa583d06df851786128ccc2ec26b49565e22942268380380fa3588a`  
		Last Modified: Thu, 17 Oct 2024 00:42:53 GMT  
		Size: 56.1 MB (56077823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79423534cf5965fe2f04fc5e975a694b4f8638b3320caa4c643e9ed24444bbb8`  
		Last Modified: Thu, 17 Oct 2024 01:14:28 GMT  
		Size: 11.5 MB (11500373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480013482db658c37a6c2ffea386ec2af1f1f4c4f5c2f5e2fff0dfbd003657cb`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce407a6bb2bfdc3323339b75bed14f72ccd45b312cc74e36d338dd1ec0ba424f`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8aa075707f8ed6aa84772b58aa32934020c09898ac7f66af7d51ffcd498d5c`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 101.1 KB (101074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4ec9646e3b4d8c55e9ecdf6614030b3ed43d718ee92062ed8c317666411935`  
		Last Modified: Thu, 17 Oct 2024 01:14:28 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:447a2ef6cca5559abee275287989f394b1340cd5c1401eee08c935ca552bd6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dccb8928053c0e11dca31752e4b544026893738954a0e0b3275e7e5f55121f0b`

```dockerfile
```

-	Layers:
	-	`sha256:ca8421cbbb10d45e2d2886e9f17bb470ba726da45075619590b1c0ce67f4a3b3`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 4.2 MB (4220339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c81157c4a2f79bca7249db43b05996ea04ea5426501cf870045d0eece9cbddf`  
		Last Modified: Thu, 17 Oct 2024 01:14:27 GMT  
		Size: 15.5 KB (15523 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:6fd67d55fd53ff6df3b247a63873f9690c1b471533ec11f775eb30c8eb54725b
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
$ docker pull neurodebian@sha256:3697dda71c97c3f2331d51e833f6004024b1b1ff9c6f985ac48a7f206f372d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66b226bfd77945145ba8dbdb314a327f8d3e57c00b7ff60b8c612e99ec189e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b762b97ea764326ee7c78d3be70939e4158333f93d124f91739a6a96a661fa86`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 11.3 MB (11266584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402ca42a66cb385c6c94651438c30b60632bbdcc199de7afa4b036ed8247d7df`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a35ac53ffb5eb6a25a8b3a501e4ff0a421f6b7e0440548aabbc7c1aad826b53`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a6e032b96453782d4fdb1fff50b61a365a71a9bff219fa43b8faecf4d5d645`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 93.1 KB (93133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46f40f5380579c474973147a5d1d5c436d1e8f8fa806d11cbd13b10e1511b852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a8a55f1f8b9a5e99a76a84ccda60e5a260fe1aeb5043321b56d4d4ee9951eb`

```dockerfile
```

-	Layers:
	-	`sha256:6f4a965387af32daf99856e8ddb053fbdb29217654f0e62264c2dd0649125620`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 3.9 MB (3924252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4881891bbb1e76cc32e634bf22607dbf8586ce82543820147144f8f75940c3de`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 13.8 KB (13823 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:050e6d336e606fbb0e300affdba33b0e7112897488c1080d655e6a8a2bc44425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12cf34310545c647cd06d3fceb8303925590de81448268c048a09001291f1154`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b222ea27d3a13a628f27fb485c2c8953c435cf879ad43c99108ae24a1a8538`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aa7c14ee96487976b1787f395d3da08538e6eb4bc1212666ffac800202f10b`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103fbbaf04667aeef928e69b2b8457085af18a4894f429dfb4cd0ec52dfca876`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370293ac9e0cd3f1e79e181dd7401ddcfc4d9579c4bcc066993cb19373d455b1`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 93.4 KB (93360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6c2dab71f6c0b4093d81cca7238cb6dcd0e421277b6ef15f14c33ffb2d5ae297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d735f4ccf82806b86c0895be8e82f45c0e36446a82405ebc53b10a90017eb2`

```dockerfile
```

-	Layers:
	-	`sha256:e8160276deeea36db3deb56f2bf3cae66d45878144632f200674b7bf3c89c2b2`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 3.9 MB (3924505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dab3dee07749ea50941c86b101d4a545ee827240618545e172488aa205971f7`  
		Last Modified: Thu, 17 Oct 2024 13:30:03 GMT  
		Size: 14.0 KB (13954 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:896545d95a4d05752deb3b2b3f8eb2e710b4f52da6553cee0676abb5a7d4280a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f0ad284f6be59a7c68b584bb5c1cc330f70b3690a10445c92e63e73e3d56535`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac817a808ff957a7e831213b07291fc20229bc43affbf623c78a261ec0325c5`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 11.7 MB (11688945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bf606e708bc7cf8f28d6e78f0274840cd2b7301440a2bf866d5204ef18fa14`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ce82a925a96d328fdcab86c0dbae82212e7cc285b177465deebb2d3fbe9067`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3afcf85c6057a5d9d8eb7c146fd97cfe8fd83354d50596c26cbc3d28cd852a3`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 93.2 KB (93249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8607ae6ffd66c4c0da8b82f00cd85627faeea84b5e54044d05b67f735d74af54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5ada56f849e4a4098758070e52baa926b4864474eee5fa5d4dc22d1058259af`

```dockerfile
```

-	Layers:
	-	`sha256:5bd90987926d222eb5f929a5da7c7efe871eeb25f75f8c2cb76d7a280d621262`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 3.9 MB (3922169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a0ce6a103d838e660923ca4f89ff0c6248d4d1d71fcc5779c4b15c1bc50d9e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 13.8 KB (13793 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:7e4840f6db5f0eafb9109b71b600b030c1d496111b609440225037c358b9144f
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
$ docker pull neurodebian@sha256:2d73a121aa2a836fdd61c2caaa45f39a60d7135e9fea08a33bc74595a2c2f63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60917132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc4c075aa36307cec499d38e0967a31bb1177449a066237940379b201fe03dc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e3861fe7b114a17685588363e051556e829fd3ee46e28f62d884d28e74e55`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 11.3 MB (11266561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a00ac0906fe55639580577bbd3dd60b722d4c59033a0c14446e5224830a05c8`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d085eb9d9ff2ee88dfca96061cefa20cf9c3d0a7bf1d9ab12247a6977664db72`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1ff7e0b7fca23cd7c1b39fa04005382442d07e9ce890af5fc59dcdf4f81278`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 93.1 KB (93128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44601798f4d155482adaf66f6cac064352d48cb3d7a9772da5500a7a213dcd`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d16d14974557a6a52b575d322f4fb464948fa19fe7409852ac281d2549fbe28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853cf6b4a7404cb7dc08679bfe53a305752c9c1daf86c8db41da8b4019394c64`

```dockerfile
```

-	Layers:
	-	`sha256:3d1b519a35f33eaf08b368bda12cd36f3b6d20193425c489c53d1b4fb859221b`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 3.9 MB (3924292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26665f8ede534d5ee35159984cea4fb23139470098f78b030b8e872244fd4f73`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 15.9 KB (15858 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2cadf68a2031eb58f9fc6f1ffe6aef4ed02a17e61fb6e899e162e11be19e5924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23adc07773d4924502532239ca86fe971d4c52473ddaf831a0ad2f4c5e2875d3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b222ea27d3a13a628f27fb485c2c8953c435cf879ad43c99108ae24a1a8538`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aa7c14ee96487976b1787f395d3da08538e6eb4bc1212666ffac800202f10b`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103fbbaf04667aeef928e69b2b8457085af18a4894f429dfb4cd0ec52dfca876`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370293ac9e0cd3f1e79e181dd7401ddcfc4d9579c4bcc066993cb19373d455b1`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 93.4 KB (93360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d034187a5238f4ac144d3f26372ba2a244669cc6d057318d3f60129559b396`  
		Last Modified: Thu, 17 Oct 2024 13:30:24 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cff90856eaa4cfe55cef01efb7e4a7d6ad9fc13743ac77d3ec2d1b4411602090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6784a5fa44f5349ac857cc8fa34504dc72bdc0c73d227e8c76e86459bd2d1df5`

```dockerfile
```

-	Layers:
	-	`sha256:04944ff3646cbb8d2c015a187bb9f8c4707d4a241a5c5ded62e171f60402f190`  
		Last Modified: Thu, 17 Oct 2024 13:30:24 GMT  
		Size: 3.9 MB (3924545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76cfff78c55d81b9986af70e9de4c9acb0d6a646de7805f6f542277ce9e81bf6`  
		Last Modified: Thu, 17 Oct 2024 13:30:24 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1360a324a787b80218de1b31e8a4bf1585aa0f4d8ca0632db9d4b1f1543510cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1324be94e3ec7d03a9cf2e35cb45480ac0a5381718eb771487a1f35f8dece4e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8e15811c104c2540eadcbc91d0ad8c420b9e7ed2ac33fc059533f236d22a34`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 11.7 MB (11688958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c913a60b2aea27736559d68f57b0c6af1fa233fec72e8e8d5c7c4c43199ae4ee`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72ec95c15f2bc5a6e5f16cc99197ac8aa491212630d4ba05e6289cff9722cef`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b72d6dd64c0de2b1a61e23af324c34b46bb76638afa8602a284cb0ae786c7c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 93.2 KB (93204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b092aabde6d4449b6ed80131da9e46d4b895bc88470d189cdccfa0ce75576069`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:007b4de94d8801338e3e7fbe3ec20314afdc0eb481e48bd4513d73b699b9acb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1461c367a715b910d400bca53db41530c86f17ef50c8272d365faef32c555115`

```dockerfile
```

-	Layers:
	-	`sha256:80806ecded92443b46c358114ef373cdefab1c787613403548a873b003328f3c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 3.9 MB (3922209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4b56190dbb02bcafb5596cfd93692a4b34dff5ee6b38ed1ef4f3c69444d232`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 15.8 KB (15827 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:3c9a5188bfe341e06ae943bbcfca2b56307715b705b7facf6c115e8ca93d826d
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
$ docker pull neurodebian@sha256:a7dec9889aa07f211ad822ba89bad5b6ce8709fb2662aab7acaeb9422f9cf4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118921d922eab791c13d7d4f706358625613c0466bb3ea1f9342a63c16c6df94`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f55ef76d9b4b35f21ab8fec574f6f36f7bd50def9bddc39211c4be1ecf5dcc`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 6.5 MB (6527854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e21780aeb7064d26fa740f8a4b9a09dfe743321ed8ccead5081f20808968b7`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3c1c54dc72253d17aa3a0747904e2f2cbeebe5381d98a4869ebfca8aad329c`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a759645cedce06316e780c1a68071850fdfad6eb284b6a5f289626fc23f9625`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 91.3 KB (91267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:924bb02286a421040b58de5bf703e0deac8f6386582a411747821f339ea70ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6625a391e9fbe8e0454e97d817ba5eac680a9cfe1a9d273a8f79ea499c655425`

```dockerfile
```

-	Layers:
	-	`sha256:ae98b6ac0554424512ec6baa4c19e7137ad6d019c0247b15234f27ba24fa55f3`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 3.5 MB (3538004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d175b07b1e4afad7f0cf9b37637c3cba14123dd767f1b33295271b7ef9010a6`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 13.5 KB (13483 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:53f8645f8bbf3bcdce3887a06d2aa2869341c28b2397f31a7471bf82786d0b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60207064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe24ebd4529e94cbf8859d1c21480465d735c0f9fad6e339b6709aca6ecff62`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507ba0d1af87c79eb5ed21e470daeb6651cd6fd35ac71c7f4316437bcf9838b`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 6.5 MB (6513412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea37e5d08e4432023f6c69cebd438dd20a209a3cd3b94eb789a8c4f80f5fb74`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7766e08b26d04d33fce1a14d04e2233cb4eb74cda5d72aaa29f51748001414e`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41352cbfcbfbb365bc31271939a7c8835966e68a87266f29c649ba4302e4f95`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 91.9 KB (91941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:91e12dc77cd69062c3a5fc7d25bca613c58b29f11cb31adef1fd79a935dfdc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c885ac5fdcd2a78cdb9066851152200accf3e10a11697fab5019a0fe07de241f`

```dockerfile
```

-	Layers:
	-	`sha256:147a5aa5deb953d5f8b7f4c13b3365171a7306962923d3fe3ee5a0bdbddd0129`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 3.5 MB (3539046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdbbd0c40a05bcb4a92f56dbda7232d95e7d4d3bd20dafc56a52e38ff5581810`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 13.6 KB (13601 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:d2802c35bb0627592501ffc30f3df2daefbca9977542caff088c4f35229cab73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61045656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca83b56f3706b8d2edec74ddd0f12387138a0707a310844b3eb8da6b7fce1be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0104c3b9cfda50cdf3421866fc7eb610b28473908b8759e1240cb0d8ad183bc8`  
		Last Modified: Thu, 17 Oct 2024 01:14:33 GMT  
		Size: 6.9 MB (6875022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedd9262fa2e041d173fd0c1c2e00f777d7a35128a6cfb880ba548f143f446f5`  
		Last Modified: Thu, 17 Oct 2024 01:14:32 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d133c2bece8359e935db3b2875d562f307c53ceecbb48708378a24ef45b04c5`  
		Last Modified: Thu, 17 Oct 2024 01:14:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46ff097c43ae4bf706c02448e2466bd9b8c5b37f55b1685a84e9ce94419bd80`  
		Last Modified: Thu, 17 Oct 2024 01:14:32 GMT  
		Size: 91.2 KB (91193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9f1a937c597b21d6d3dcc90d05769817755c541905d0d7cd7abc73c2a3826d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3548558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b107b9695539bdcefef4858e73a9d9eaa93d90271cc4df926ae48ebaaa418605`

```dockerfile
```

-	Layers:
	-	`sha256:6af125565215ecef3d415be15edd88929016e26097df809146fee17a2974dce8`  
		Last Modified: Thu, 17 Oct 2024 01:14:33 GMT  
		Size: 3.5 MB (3535101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87d62435b91d7d078a1c9c759e6cc4625563ddd2f8d8070cdfd20a5465afaa05`  
		Last Modified: Thu, 17 Oct 2024 01:14:32 GMT  
		Size: 13.5 KB (13457 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:8aa073c3cd5fbed8f89f21e0cfc35a9d4a6fb7c1c1b16c96c1185a11b156b74f
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
$ docker pull neurodebian@sha256:a30d0910eee54e78cff1ebacfbf94d0f5d1bcfb233729937a5383b3b8754aebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59860224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58b7b67a10ad31319482f49ce07ffaed1409f4bdc42bdb57591f94a9f55f870`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463f8d68a16e9ac92c12f43868402c6f3f57d26fdad10a18f8469cbe505b5557`  
		Last Modified: Thu, 17 Oct 2024 01:14:31 GMT  
		Size: 6.5 MB (6527838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb52b6a48245f5a8831658b3aabe3cf7c7ff05fac76e80b3f6301fae8148095c`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9838d374d800c72b49ed8fe36ec4a126f57a5db7d2354dd3a32c800f1143d1a7`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0266e43d73ad49f9d716b54f8d979e37b5114c365d04ef4a24186995d7ec2739`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 91.2 KB (91229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf7b9db2b69c3f521edd6792979833642d688b878bb51d6390bb1461a1fa26d`  
		Last Modified: Thu, 17 Oct 2024 01:14:31 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bcdc6c21779357df565f1ad14a6f8c8508b2a8dc04d4b1dbbc25d4b2cd773cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a575d2ce06e3134c6340d5878b4d0403f24d2d7ebc47116f54490e5c6a19ec8f`

```dockerfile
```

-	Layers:
	-	`sha256:26e7003cef78c34f6c8b2ab579f8ffd7624e7c5566f72feec2ab5465909c0ad7`  
		Last Modified: Thu, 17 Oct 2024 01:14:31 GMT  
		Size: 3.5 MB (3538040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51fb57aa93986c771ed7fb9e961105a680c9f6cd0999e682188320cdf94ee724`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9800c97a370a781ffb9871de33494c3a06907666e74ec5dfd30006c9acd5d149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60207488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49241192e3ffb655678dd748976796c720d47028f0001ebb417840254c4d9524`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507ba0d1af87c79eb5ed21e470daeb6651cd6fd35ac71c7f4316437bcf9838b`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 6.5 MB (6513412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea37e5d08e4432023f6c69cebd438dd20a209a3cd3b94eb789a8c4f80f5fb74`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7766e08b26d04d33fce1a14d04e2233cb4eb74cda5d72aaa29f51748001414e`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41352cbfcbfbb365bc31271939a7c8835966e68a87266f29c649ba4302e4f95`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 91.9 KB (91941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d45f485faecfdb395798bd27324e61884a7fa42eb02cb31494f7362503104`  
		Last Modified: Thu, 17 Oct 2024 13:32:06 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b4bf8e13d9e5fde0aa2ec003ed93ba575b296b6a1fa393a343426333a5f3bc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67a8e580c3f4979cbb59915aab3ad2437957ad387641a293eb5a716dab2d9b`

```dockerfile
```

-	Layers:
	-	`sha256:2a1b5b9e67e1dc1eb6abb7fe584c62fd8dc2ddf3e9842df732676c693cc1a80d`  
		Last Modified: Thu, 17 Oct 2024 13:32:06 GMT  
		Size: 3.5 MB (3539082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94b9375ffc08954ec2b358f015f7142cdbd3b31bc5835e0cbea70ffa77c06bad`  
		Last Modified: Thu, 17 Oct 2024 13:32:06 GMT  
		Size: 15.6 KB (15649 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:9c7f1e28a81eaa0320511416c4df234ad4f7600f45586e56abaf446d54c8c688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61046012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441a3e6af0dfa8112ae47502d4c44271690c8d39f51606037000ff9ad08129cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1ffc8190a07ef94376d2867dd7a73d310a6dd7481cc9c26c1a309cefcc3be5`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 6.9 MB (6874953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a00ac0906fe55639580577bbd3dd60b722d4c59033a0c14446e5224830a05c8`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dbbc38a72670aac92fe8264b45b65f1639ceab86ba73989947c33f06386fc4`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cabfbcdfe93633e99167f3116691d7916d684a7d81ea43d9a4b36b13fa770b`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 91.2 KB (91188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3116d94f84b7b8a0808de899de4b7a8d7c6b78353d6d93203f567f84b724d03c`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a6b2876e6dad21b09173111ef3753a8715147a7e56ae7770dc4060809e034a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3550625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617bea8eecaa56f0a9d3b22db9198bfe101fe2ac785cb3c5575ee8ea44214b3f`

```dockerfile
```

-	Layers:
	-	`sha256:b89f9486666bcd9109be18c9320b58d7dfcc763af91aa24e924946324820d2b2`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 3.5 MB (3535137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed201cf8df404b1835b3c3e3e5206232c9e3cb0be2bdf87e8ee937c6c6b19e04`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 15.5 KB (15488 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:8bcdb02c955c552289fb14468e3d0eccac712d0a170f1fff5601f3f3af9d8a49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:a0c6cb45ac1cfbe06c47f14d684929ff5f5907ef7f083c360195214c3ac6aca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1335fc867ea7b822d1b6882dc96ad365e5cc4643152d61c5fc8a7bc5f85a988`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49fa7316f784f5cf307546c8c97bd1b9f3a1fd2943c27fceb71ec2dd6409f48`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 5.4 MB (5360278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb7c65bbf482527df64ccec5d79c08cb11cf2d1f4054f4977e47dad48ff8435`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e678bedd7e50e1ba3e947302d4a3badb36d988b369aab4b47c1fa78259c23552`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9792897da4dcee6732822377f46272804fb1e9b7f31dd60d17894a127edb839`  
		Last Modified: Wed, 16 Oct 2024 16:13:43 GMT  
		Size: 105.3 KB (105327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:848d25161f517586e1457fc807e778d3305bad2daae744ec21fc37849f68173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820220dbbd11c6d8f3103b1a3ed83da871c77d7b02f18798badcf3237303dcae`

```dockerfile
```

-	Layers:
	-	`sha256:27970857ec501c025d084e20e5352a5d5ddc17824cc89a85f49e7025cdcb4a02`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 2.0 MB (2002651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:849d52e89f42eba3812416ede3dd4d1badb9a69a5a982f874e39c325041eb9a2`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 13.4 KB (13444 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1a3f2e41cb72abdd7dcab281d6513ce2dc547865fa3b4ba0776bd58ea8a5de97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2c98411bfbdccf11946d245a8061c56c6ce058ada6075d911256dd80fadff8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6101036d9458690903008f9743d7d9982835f206b38bec0aee1147faccc7c0`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 5.3 MB (5340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a29390bcc04ab62cd8664a0c5eb9c2c8529bc1cf5a8fc1e442f9740f53d73`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a06a5898141ddee96056f1057c0595e290735b4831567d9e98c36af5687cba6`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead23b60010d07ced4212e4cf8a6c4f69eae17b7d32e4a35b7bf00c6df7eacd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 105.4 KB (105412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1f3f34f75e1a4bc32b849a9ffc880a30708443a7fdc0da8a50c2e90180094f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5772b0ce1260ce48effc24ad2f6bdefdb4674ee0d585774b4464dfdaa8df07f`

```dockerfile
```

-	Layers:
	-	`sha256:71ee94546588c20b92a492d129395aac336c0ae8677f9f8048b6890a1e640901`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 2.0 MB (2002879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa10decb4cbaa5f56d95540086539ce9a7bfee79f97ecf26a18eb6160c482bbd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 13.6 KB (13563 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:e1b1eebaa7be7a7ae8986f10c005fbaacce6a33e73c7193cef12dee6f49b40b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2ddc9018acf97b1f5814caa6cde3c3d36dc386f558589639e00bd07b61c4ceed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02507bb93b25ace19e3dbcf9e5a746ee64169a6e6641918f946da8db0e4d17b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f4005701787afe01df59207e8d67264732bba189629db1779b4ffa79571550`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 5.4 MB (5360288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6862ce93e83033ea4be1d4f8bd4ea70b498c761c3664782d446af47aa9926b`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce53e76a062f11aaecdb2eaab737adaf3dfe235440d4e34cfa7bd8bc8634e70`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f662144d756ef598c43631f18e5a5aa12b2a8e2c719e17635359530cbf9a9b`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 105.3 KB (105328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c113f4052eb4bc0e89d69bbfef200be8e9cc348104fc8ae5bc167ebdf6ac683`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fdd9dd95911aad8010d1bd7b668cfc9886a64e712c66aeab16529edd5642e84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419484197e2594f495dc65df02606517cfd33b3e8fb27db49620e293bfb8facc`

```dockerfile
```

-	Layers:
	-	`sha256:96b650f1cbef5c5dbf1b7069ca052e04734ab3f40d4e9ed771e9496d60fd999e`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 2.0 MB (2002687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdacbdc41b77b356c35fb81b7e0fcf121e4d6c1b38d2d913103141df6f522c9a`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b3f6acebf8e01d4ccb64904ddb4e553df094a7fb6223b50f683882a0756a284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9be140461e203793948a95c87503859fadcb667866ac155c79cf9aea88c1edf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6101036d9458690903008f9743d7d9982835f206b38bec0aee1147faccc7c0`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 5.3 MB (5340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a29390bcc04ab62cd8664a0c5eb9c2c8529bc1cf5a8fc1e442f9740f53d73`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a06a5898141ddee96056f1057c0595e290735b4831567d9e98c36af5687cba6`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead23b60010d07ced4212e4cf8a6c4f69eae17b7d32e4a35b7bf00c6df7eacd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 105.4 KB (105412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4975400a8d7cbc9b67c0e50618fd95fa63506aa713da18a3da28accdeb57768`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b26186688e44f87210438ddae17d14c31f634b630c497d04013b36ec09d92089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b3564811c260795602aab1de18bc1a0e9abcc4a1a00d4aa08bf2c13102fd50`

```dockerfile
```

-	Layers:
	-	`sha256:5f09b22f2f9e9d8a1f0ccc85ccd622a779576a09f4ec13d286e85c8831be03eb`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 2.0 MB (2002915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc6326745662ee2e02b1d747a2d2ba13494721e28def82decf35cf47a1614ff`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 15.8 KB (15808 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:8cd25968c7a8dda57e86f5f31179a392780c365d049c245f1563df254a345b6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:b5e2ad2679d21dfb98319132904ff13815643d741d29c2cbd61f795d2cfce2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03035b5fafec30a11ccaf9e676191d30bf2a93a2c961ae50bcdeae21ecee68c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e5fc20939f49ca46aaa63fda94b740a46522034dd33a99dc846c2ab47da385`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 3.6 MB (3622683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d7c12d3dff8024cc7a65a06760eefef7523e92d4ab01561da2876474be6e25`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257f9b0966cd5484318ba1e2300bcf4102ad856d15cf79307d6575cb919be75d`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25429882efb06104ffa477fe41e22a29ad87a1b8b5a97eddc221fb3cfb85bc29`  
		Last Modified: Tue, 17 Sep 2024 00:58:50 GMT  
		Size: 110.0 KB (110041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d732e29d091ef7f0e630eef553f727bdf00995f77c7dcc07b0561d4792f4341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb4b42740c8b876bb56d509444cd2d22fd632ea9c6254cf4af8ef60cb72b5aa`

```dockerfile
```

-	Layers:
	-	`sha256:46449a2a17035de35151d0f04752a18008bd77cdb9bd76b7f1465ab848857267`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 2.0 MB (2041055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229f62c1b512cec8166de552b1e0085eb7526f3474781a15c9cfadf62c2436da`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2e8ddba19dffa270b72c0c17efca5bea22c862945352f06ad9391ca69ae180ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e64399ffc86a2a302a5f8b07efe84fa560a195e25878c4a52e8f5d97367769e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ce4fcc7ac84933f63a18dcc1f51edb6a54d593241a9ad9eda2da49c4a0a93`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 3.6 MB (3594202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420d28ea54fd4f14398ac3479d15abc9d09b6fdfd86904d39445315fa9ccd4a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89798e75750754cd749a20391aabd4a2982ab8ea03464d1069af684488290b27`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a706a92656db8d1c42d48439ae56eb9ef232cfcd87be0f53362d7da0045c9f6`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 110.2 KB (110158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:769792b0a9ae99abbe1b81296f09e1e53c2e662643848544f1a641d54f8b29bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ab15b050723ad8ecd0ff560efdd18d3d1451cbd92375f54cf16c418e647366`

```dockerfile
```

-	Layers:
	-	`sha256:2a92568efc9bccb357a48dc2f8cc5ef4f0d34112762744fc1408de6d45f8e34a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 2.0 MB (2041314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783fe908caebc3d7a05968a298b4c97dd56aff0cc5841272d2f31f8d0eac4efd`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:c35390a21d7dcdaa5248caedb0c2d1d3f2b9a31a1ccc6a5fd082bc8262ef35a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e45ad58f9dc146f7c58fee7c828c3c6831e76bdb9cf7020f9f7c9448d53671ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4ea79fb23e81c99deef7e3da0330d8995389a5ed5528314613545bbc38a650`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e444df7ecce18d9b6a39b30f8f893e46de9a6c8393753ceb73f80be5147d5e`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 3.6 MB (3622684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eb688a315dc9dc281db41ae45a5e1651f96d5b6b93100b8f6b3604a1b7be90`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18efaf2abf8b145da9341e025a8599685148d724adf71187513efcefdc1eb92b`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c03e7463fe28779caf76a60210e080067f4e00e4a28d1ef22b5f71aab3511f`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 110.0 KB (110044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a748ff3cbe6a5eed1e2b979d6648c667fb7a29be6b3e2bc14ea06d88519a0592`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:49d3a7c89f96056348bc2f29c7aaab1b27bde7d7755e5cea5fe7102dbc63a96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0141b248fd4a83635efee725ebffc6599bb6e48aedbb01287016be2df2e9e29d`

```dockerfile
```

-	Layers:
	-	`sha256:2aa3ae2b7c2d8c84a96d9dfae22e8bdbef344f1dea22754309dafd7d8ba3fa7f`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 2.0 MB (2041091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48b6d14af7ecf44b9066d810db720df1078da0e69b612cc31771ef41b2957b4a`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4a2bedc35b23fd303d37b492a4dcd265b749cc561bed81266ef4fd4f072ca3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cc596bfd27c527f722fd0f60344b7c29c0ede0e0215ca28663dd6f7b11334d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ce4fcc7ac84933f63a18dcc1f51edb6a54d593241a9ad9eda2da49c4a0a93`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 3.6 MB (3594202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420d28ea54fd4f14398ac3479d15abc9d09b6fdfd86904d39445315fa9ccd4a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89798e75750754cd749a20391aabd4a2982ab8ea03464d1069af684488290b27`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a706a92656db8d1c42d48439ae56eb9ef232cfcd87be0f53362d7da0045c9f6`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 110.2 KB (110158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0571d1820815c6ffe6445310d6d56c0904985a7a40ce55ea60111c7ab14c14af`  
		Last Modified: Tue, 17 Sep 2024 02:37:09 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15e423dc66f68b2fd18342bafd40c16c24df1ff2d5a105e3d23fe7a7b66e4859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae14030ec66c96db8f89c291fc02780ff4e9dd29fbe18b7deeb19f1a70811d83`

```dockerfile
```

-	Layers:
	-	`sha256:b8a537c7762547e63f17b420cb0912f491db0829af8089494798ac00e311b1a7`  
		Last Modified: Tue, 17 Sep 2024 02:37:09 GMT  
		Size: 2.0 MB (2041350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab7d3d2aaba018f1a288d03ac3c709c72564deb83d89ee6d4197767b31a448c9`  
		Last Modified: Tue, 17 Sep 2024 02:37:08 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:b10148221bce2c9570e277d931e6ba76630f90a7d2dc84f92d7c27dcbbf8388e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:4f4e75ab9e8bf01e3fd097872b816b6dad96363df63039d70ed65b6824957e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33411920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4a4b5acfcc51c28111eb6d5cd5b2cb69fd8fef07fc4fbb33fb840072c5d5b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70ee3f6612bc98b5f6a9dbd0e145996185b900394df37a5b4438f9c178ea1ff`  
		Last Modified: Wed, 16 Oct 2024 16:13:49 GMT  
		Size: 3.6 MB (3558359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9927d073cd3764bebee1b3a7274024f08ebae10170edf4d8a4a7983ba994d39`  
		Last Modified: Wed, 16 Oct 2024 16:13:49 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0909d09c16e9d271e238d74681bd26e108ad03268835a21bf8beb37069fdecaf`  
		Last Modified: Wed, 16 Oct 2024 16:13:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c326b02b52c5b14fd45f178e34514f0ed8be6b9b32f7c2d625ca0fd8a475af`  
		Last Modified: Wed, 16 Oct 2024 16:13:49 GMT  
		Size: 101.2 KB (101205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dda31745ad017dd5a3b9eb6b5d08a128bece425839d9897f2a958478d0f669b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1986520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70226f52b6f3ca4b26ff396fb8f7c8f5e36ec46c3ef55c65751f8c0f217e011`

```dockerfile
```

-	Layers:
	-	`sha256:3c18a76ea0401aeea14be6510a274a27c53fb8873744a023d353ba702cb86f9a`  
		Last Modified: Wed, 16 Oct 2024 16:13:49 GMT  
		Size: 2.0 MB (1973076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77402c34a514ba908efc5f69db6985a559b01f5d4989d9c0179e5504393f355c`  
		Last Modified: Wed, 16 Oct 2024 16:13:49 GMT  
		Size: 13.4 KB (13444 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1a935b6c4bc11684f09930d0b9391f0db414645a05ca2795760d5194620e291e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32547139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee26915a3722f1f7401b6f1ce035233a1a654c8bb05c81b62417d418099d3b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea789099bd6ebe3942b142207baca153ba915bdc75730edccd488aed6d041b`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 3.6 MB (3557475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4a09b01ed47f9b471c2c8ae48b7053ab1d51c00307579e122f2e75623a215e`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942a820a9345a6a033d2fd85db18607d4fd8370d06efc055972c5e44aecac5d9`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eeed11615938af4f334098e62ba967cd10313041ccf1762ab55e8c506f8a93f`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 101.8 KB (101826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:01a91a3b061811a551707c6df5c26cae458b00315f8ca31651bc11a321d48fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73776da87cd8801b4dc0c2ccf5dd9f2ad91d46bf0bd60c1a5a15e27e86a265fa`

```dockerfile
```

-	Layers:
	-	`sha256:49317efb7958f179c63ef030afe475a8d88eb05a4f179d243b89a30a0ceeb447`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 2.0 MB (1974121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7871391a76e34455997ee18c3efa74d7a4da063e5b0f6d1be022c8ba189c6f4`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 13.6 KB (13563 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:0af23b8efe4b5d6a53c257d9f35f692045ed1f7fb51019ff247fac152ae44e8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1a460f508ea63a604eb6e566b9e31bce88b7449210fed79de454bf34c0af6175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33412264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f38e95950ce79563d040ee09442e0ae4c0be4532a0f40042b4037de6d9c6e39`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bf4fd98272901a80c95a9492d3fa0362b758fd8bfadd9cfeb711c923c0e089`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 3.6 MB (3558315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e523e7036a932e22b290ac9772aafa3b80f0612260428eb5aab15dd9bef114`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4197dd867d3f8b793da103f5dfe1c737c4bfaee73a8672a945090fa574f0acdb`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1628a0bcf70ed588686e77536d73ba54c6d706901aa26543480332b16a3dbc42`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 101.2 KB (101192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5c029479c2a21eed03c7570244830dff6586f5247f7d67b41aaf8362f00b9d`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1b1d14591a0c0570c12b6793e6ef272ce176d7687516b271bf7b5320746aba65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e94dc2dc2a41ca2d0b1476fa8ff9e0587f5d50ea47c45bccdd32b06f4893d56`

```dockerfile
```

-	Layers:
	-	`sha256:4e0276974fe9e75d6545fe8a3fdcd16a04037500b5b70b7b2bad9cdca16598b4`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 2.0 MB (1973112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d220a0f4e44151ecbd029dbe933e594a9eaea23bad268002d8014b499549326`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:22fbd0d6d07a45042210655eb29841152243bf6a9b0647ff180c4e15efa192d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32547544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2846820e80dcd608ecee4f40ddb974b576e02b4e51fcdc26418090c550da1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea789099bd6ebe3942b142207baca153ba915bdc75730edccd488aed6d041b`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 3.6 MB (3557475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4a09b01ed47f9b471c2c8ae48b7053ab1d51c00307579e122f2e75623a215e`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942a820a9345a6a033d2fd85db18607d4fd8370d06efc055972c5e44aecac5d9`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eeed11615938af4f334098e62ba967cd10313041ccf1762ab55e8c506f8a93f`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 101.8 KB (101826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f91b520aaca18d0d1598c30a61a7d75fcaf19f70a644b136a3c8f93d09643a0`  
		Last Modified: Wed, 16 Oct 2024 03:54:09 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:82e80e1c2892a68d88eae2c5913badcac80a27fc4af38a23583c2f4443093b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1afcb693b18a051ec65e8070c20a38d7d2b3ac864b80d0aacbc8191d4a5ac2`

```dockerfile
```

-	Layers:
	-	`sha256:b07e02d3c73827e6af99190702f368ab085c108d4f2835a8246f8562a803be75`  
		Last Modified: Wed, 16 Oct 2024 03:54:09 GMT  
		Size: 2.0 MB (1974157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c1d36705970b04a363846cc01d3a69ffbedd62aa2338241b5c62df9675fc2b`  
		Last Modified: Wed, 16 Oct 2024 03:54:09 GMT  
		Size: 15.8 KB (15808 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:b10148221bce2c9570e277d931e6ba76630f90a7d2dc84f92d7c27dcbbf8388e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:4f4e75ab9e8bf01e3fd097872b816b6dad96363df63039d70ed65b6824957e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33411920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4a4b5acfcc51c28111eb6d5cd5b2cb69fd8fef07fc4fbb33fb840072c5d5b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70ee3f6612bc98b5f6a9dbd0e145996185b900394df37a5b4438f9c178ea1ff`  
		Last Modified: Wed, 16 Oct 2024 16:13:49 GMT  
		Size: 3.6 MB (3558359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9927d073cd3764bebee1b3a7274024f08ebae10170edf4d8a4a7983ba994d39`  
		Last Modified: Wed, 16 Oct 2024 16:13:49 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0909d09c16e9d271e238d74681bd26e108ad03268835a21bf8beb37069fdecaf`  
		Last Modified: Wed, 16 Oct 2024 16:13:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c326b02b52c5b14fd45f178e34514f0ed8be6b9b32f7c2d625ca0fd8a475af`  
		Last Modified: Wed, 16 Oct 2024 16:13:49 GMT  
		Size: 101.2 KB (101205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dda31745ad017dd5a3b9eb6b5d08a128bece425839d9897f2a958478d0f669b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1986520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70226f52b6f3ca4b26ff396fb8f7c8f5e36ec46c3ef55c65751f8c0f217e011`

```dockerfile
```

-	Layers:
	-	`sha256:3c18a76ea0401aeea14be6510a274a27c53fb8873744a023d353ba702cb86f9a`  
		Last Modified: Wed, 16 Oct 2024 16:13:49 GMT  
		Size: 2.0 MB (1973076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77402c34a514ba908efc5f69db6985a559b01f5d4989d9c0179e5504393f355c`  
		Last Modified: Wed, 16 Oct 2024 16:13:49 GMT  
		Size: 13.4 KB (13444 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1a935b6c4bc11684f09930d0b9391f0db414645a05ca2795760d5194620e291e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32547139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee26915a3722f1f7401b6f1ce035233a1a654c8bb05c81b62417d418099d3b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea789099bd6ebe3942b142207baca153ba915bdc75730edccd488aed6d041b`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 3.6 MB (3557475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4a09b01ed47f9b471c2c8ae48b7053ab1d51c00307579e122f2e75623a215e`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942a820a9345a6a033d2fd85db18607d4fd8370d06efc055972c5e44aecac5d9`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eeed11615938af4f334098e62ba967cd10313041ccf1762ab55e8c506f8a93f`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 101.8 KB (101826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:01a91a3b061811a551707c6df5c26cae458b00315f8ca31651bc11a321d48fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73776da87cd8801b4dc0c2ccf5dd9f2ad91d46bf0bd60c1a5a15e27e86a265fa`

```dockerfile
```

-	Layers:
	-	`sha256:49317efb7958f179c63ef030afe475a8d88eb05a4f179d243b89a30a0ceeb447`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 2.0 MB (1974121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7871391a76e34455997ee18c3efa74d7a4da063e5b0f6d1be022c8ba189c6f4`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 13.6 KB (13563 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:0af23b8efe4b5d6a53c257d9f35f692045ed1f7fb51019ff247fac152ae44e8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1a460f508ea63a604eb6e566b9e31bce88b7449210fed79de454bf34c0af6175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33412264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f38e95950ce79563d040ee09442e0ae4c0be4532a0f40042b4037de6d9c6e39`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bf4fd98272901a80c95a9492d3fa0362b758fd8bfadd9cfeb711c923c0e089`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 3.6 MB (3558315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e523e7036a932e22b290ac9772aafa3b80f0612260428eb5aab15dd9bef114`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4197dd867d3f8b793da103f5dfe1c737c4bfaee73a8672a945090fa574f0acdb`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1628a0bcf70ed588686e77536d73ba54c6d706901aa26543480332b16a3dbc42`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 101.2 KB (101192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5c029479c2a21eed03c7570244830dff6586f5247f7d67b41aaf8362f00b9d`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1b1d14591a0c0570c12b6793e6ef272ce176d7687516b271bf7b5320746aba65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e94dc2dc2a41ca2d0b1476fa8ff9e0587f5d50ea47c45bccdd32b06f4893d56`

```dockerfile
```

-	Layers:
	-	`sha256:4e0276974fe9e75d6545fe8a3fdcd16a04037500b5b70b7b2bad9cdca16598b4`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 2.0 MB (1973112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d220a0f4e44151ecbd029dbe933e594a9eaea23bad268002d8014b499549326`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:22fbd0d6d07a45042210655eb29841152243bf6a9b0647ff180c4e15efa192d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32547544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2846820e80dcd608ecee4f40ddb974b576e02b4e51fcdc26418090c550da1c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea789099bd6ebe3942b142207baca153ba915bdc75730edccd488aed6d041b`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 3.6 MB (3557475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4a09b01ed47f9b471c2c8ae48b7053ab1d51c00307579e122f2e75623a215e`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942a820a9345a6a033d2fd85db18607d4fd8370d06efc055972c5e44aecac5d9`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eeed11615938af4f334098e62ba967cd10313041ccf1762ab55e8c506f8a93f`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 101.8 KB (101826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f91b520aaca18d0d1598c30a61a7d75fcaf19f70a644b136a3c8f93d09643a0`  
		Last Modified: Wed, 16 Oct 2024 03:54:09 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:82e80e1c2892a68d88eae2c5913badcac80a27fc4af38a23583c2f4443093b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1afcb693b18a051ec65e8070c20a38d7d2b3ac864b80d0aacbc8191d4a5ac2`

```dockerfile
```

-	Layers:
	-	`sha256:b07e02d3c73827e6af99190702f368ab085c108d4f2835a8246f8562a803be75`  
		Last Modified: Wed, 16 Oct 2024 03:54:09 GMT  
		Size: 2.0 MB (1974157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c1d36705970b04a363846cc01d3a69ffbedd62aa2338241b5c62df9675fc2b`  
		Last Modified: Wed, 16 Oct 2024 03:54:09 GMT  
		Size: 15.8 KB (15808 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:7e4840f6db5f0eafb9109b71b600b030c1d496111b609440225037c358b9144f
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
$ docker pull neurodebian@sha256:2d73a121aa2a836fdd61c2caaa45f39a60d7135e9fea08a33bc74595a2c2f63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60917132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc4c075aa36307cec499d38e0967a31bb1177449a066237940379b201fe03dc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2e3861fe7b114a17685588363e051556e829fd3ee46e28f62d884d28e74e55`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 11.3 MB (11266561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a00ac0906fe55639580577bbd3dd60b722d4c59033a0c14446e5224830a05c8`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d085eb9d9ff2ee88dfca96061cefa20cf9c3d0a7bf1d9ab12247a6977664db72`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1ff7e0b7fca23cd7c1b39fa04005382442d07e9ce890af5fc59dcdf4f81278`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 93.1 KB (93128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44601798f4d155482adaf66f6cac064352d48cb3d7a9772da5500a7a213dcd`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d16d14974557a6a52b575d322f4fb464948fa19fe7409852ac281d2549fbe28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853cf6b4a7404cb7dc08679bfe53a305752c9c1daf86c8db41da8b4019394c64`

```dockerfile
```

-	Layers:
	-	`sha256:3d1b519a35f33eaf08b368bda12cd36f3b6d20193425c489c53d1b4fb859221b`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 3.9 MB (3924292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26665f8ede534d5ee35159984cea4fb23139470098f78b030b8e872244fd4f73`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 15.9 KB (15858 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2cadf68a2031eb58f9fc6f1ffe6aef4ed02a17e61fb6e899e162e11be19e5924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23adc07773d4924502532239ca86fe971d4c52473ddaf831a0ad2f4c5e2875d3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b222ea27d3a13a628f27fb485c2c8953c435cf879ad43c99108ae24a1a8538`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 11.2 MB (11232038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aa7c14ee96487976b1787f395d3da08538e6eb4bc1212666ffac800202f10b`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103fbbaf04667aeef928e69b2b8457085af18a4894f429dfb4cd0ec52dfca876`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370293ac9e0cd3f1e79e181dd7401ddcfc4d9579c4bcc066993cb19373d455b1`  
		Last Modified: Thu, 17 Oct 2024 13:30:04 GMT  
		Size: 93.4 KB (93360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d034187a5238f4ac144d3f26372ba2a244669cc6d057318d3f60129559b396`  
		Last Modified: Thu, 17 Oct 2024 13:30:24 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cff90856eaa4cfe55cef01efb7e4a7d6ad9fc13743ac77d3ec2d1b4411602090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6784a5fa44f5349ac857cc8fa34504dc72bdc0c73d227e8c76e86459bd2d1df5`

```dockerfile
```

-	Layers:
	-	`sha256:04944ff3646cbb8d2c015a187bb9f8c4707d4a241a5c5ded62e171f60402f190`  
		Last Modified: Thu, 17 Oct 2024 13:30:24 GMT  
		Size: 3.9 MB (3924545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76cfff78c55d81b9986af70e9de4c9acb0d6a646de7805f6f542277ce9e81bf6`  
		Last Modified: Thu, 17 Oct 2024 13:30:24 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1360a324a787b80218de1b31e8a4bf1585aa0f4d8ca0632db9d4b1f1543510cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1324be94e3ec7d03a9cf2e35cb45480ac0a5381718eb771487a1f35f8dece4e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e37fc0b0dd2624a94de68cdbe58eebaee18abda02198698500c71668b8266ddd in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5ee14e62c4f0d03b8028e0020d16d7a49ad577754f60410febfbc7c58ae5defb`  
		Last Modified: Thu, 17 Oct 2024 00:42:10 GMT  
		Size: 50.6 MB (50576834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8e15811c104c2540eadcbc91d0ad8c420b9e7ed2ac33fc059533f236d22a34`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 11.7 MB (11688958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c913a60b2aea27736559d68f57b0c6af1fa233fec72e8e8d5c7c4c43199ae4ee`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72ec95c15f2bc5a6e5f16cc99197ac8aa491212630d4ba05e6289cff9722cef`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b72d6dd64c0de2b1a61e23af324c34b46bb76638afa8602a284cb0ae786c7c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 93.2 KB (93204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b092aabde6d4449b6ed80131da9e46d4b895bc88470d189cdccfa0ce75576069`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:007b4de94d8801338e3e7fbe3ec20314afdc0eb481e48bd4513d73b699b9acb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1461c367a715b910d400bca53db41530c86f17ef50c8272d365faef32c555115`

```dockerfile
```

-	Layers:
	-	`sha256:80806ecded92443b46c358114ef373cdefab1c787613403548a873b003328f3c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 3.9 MB (3922209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4b56190dbb02bcafb5596cfd93692a4b34dff5ee6b38ed1ef4f3c69444d232`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 15.8 KB (15827 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:f1861e0571166fbfae31b98ff9b3282e233f809fa114ae25b0463aab1a19ceb5
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
$ docker pull neurodebian@sha256:af988d6adb2891ec552ee9990d0ed9def1f72d4be51fe2d300fdcafc016069a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59654381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394cd951cd1004584c418da9435be7a462e40a81740e3cf4f9bc52d014181909`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43fe9fa1ea5e364ff54cf0d2e96455c6f8402592c32777e452028e59e4f07db`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 6.3 MB (6289386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461430c5027f3982ecc44a03e50c617a66caff8d40bb1cf5ef7414dc7a44a51b`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d7d04684bd6207fd3fcdaa7adb93c457ebb7ede1f494ad1050bee39838aad3`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3c4d8af236dc0db54a33b8a382e921a52f482ebdedddff3af00da511fcb5ca`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 91.1 KB (91135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bce5156dc1fb09c732081a1fc7a9e5ea6ae57c5800e3909700a8f313fa0f99b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813c1b3abd826f7630168733dd6ca5f043765ae343d96d62556dfd0539ad11ee`

```dockerfile
```

-	Layers:
	-	`sha256:736401022b618a8c56d8b7cf8c577987243a98a5a24c0c31342af864ab7fb80d`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 3.5 MB (3529844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9e41aadddcdd8e9c307112d89d858cb3da930d97f8730ae366272fa4cb0e08a`  
		Last Modified: Thu, 17 Oct 2024 01:14:29 GMT  
		Size: 13.4 KB (13435 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fceb7880ecff05e3fad1bd34562c0fee903764280c693fc06edbbb6b5093843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59996796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0c1c96bf04b236a96d091b001f637f30fc4267568e19ad379ebe0583a99ec6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207c4d641255ff6bd7b8ce630c8cf947966d1ff05bdf86f951c687f989e2f5e9`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 6.3 MB (6273546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c25f32db1b1126487143c75b9ce0d496e410c5bae14e76068c7767c3979041`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1aa1fca4ed404a2dafbd083628f990869ee0dd7b253df1199afbf67da6e338`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab4cc25b7109f5af55ff37456e9f7fe94f979dff175b36667bc066bff22439`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 91.8 KB (91781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1f7c49f91f70d5fd7fdfb393e1255d65bf3963462449605a6b498c5dd601a397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3544438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c771ab1f610171f7a17f00660c97e22c04d5fa10ecb778aeed2a621ae3e94e5b`

```dockerfile
```

-	Layers:
	-	`sha256:5e03f04196d30611ce1df27f1d3cc5278240cd13a3eab0cd469eb97f145011bd`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 3.5 MB (3530885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec9935b092fb7d33339c675b1c15bbf6ecc7bdb04d95950c01ed5fca038b5e8b`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 13.6 KB (13553 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:b90f2c17e980947a7b20b3fde97e69b919f586f73c3878813c90846e895b4228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60828971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28344bd679e7fa6b7c4fbb3378f9939e9325bab60060c34ac0858e971c02d2ab`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bf9a8e67481cd7b5126ca983ff2eb6360719268ef0d901ef9c0ab1397ebdaf`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 6.6 MB (6617928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93a3157ecf2b3e90f14bb799e97539e5da9b8e54c2fa24fb906ee69c4f58f3b`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7faf9478aaf287f3c93ce350f01a65b610825764a68728311533510f3bc121c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c402fe866ebbf8d95ad0581375c4226649ef229de419a9074877580e2287f4a`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 91.1 KB (91086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5508b170e6de67c39a46f664e38e6a6e388809ca959d663ca63d5647a8995f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3540353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c76c89ee979c78363abaee47580b7730e828bd4277b1eaab481c54ca64e02e5`

```dockerfile
```

-	Layers:
	-	`sha256:a08867bfaef8835491bd411c4b001522f5e609221f242241f719262e6ccda1e5`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 3.5 MB (3526943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d525a98f9cd254f377fa72ecbf05fda0d300d7e311a88722b4e21fcb727eb46`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 13.4 KB (13410 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:f23847bbf2fb1f2064a746206684077fb8f9eeafc6b6e739bcbe6b759c9554a3
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
$ docker pull neurodebian@sha256:b2551aed7873b42c6948e4b859e19766d92fdfa9124e197eb17d7e01396a956f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59654703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdde34f32b6bf6419324db05b4b8b5fb9b6351610e3fb059cee7f5bd4e5195f4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc7e4c0fdb6fdb4dbba108ecd5d312d29ef194ff9fcbe5d6b45de7caada7a15`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 6.3 MB (6289352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93a3157ecf2b3e90f14bb799e97539e5da9b8e54c2fa24fb906ee69c4f58f3b`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7faf9478aaf287f3c93ce350f01a65b610825764a68728311533510f3bc121c`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dad48c7fe85a9fcbbcfc1c1083d15785484d25efd58f98a59df48aecc124e08`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 91.1 KB (91103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb07a3a2622e66aa964a597aa305a0c72a9f55414a983c902e52931a87bb172`  
		Last Modified: Thu, 17 Oct 2024 01:14:26 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f0dc4fccbda04d9082a17dfdcf47af681064b79911dd81b78c74058479c14f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abd151be0aa00d64da82c73b693e2c7729a6a8a65244bf3815c4aa2a56aade9`

```dockerfile
```

-	Layers:
	-	`sha256:646ad1bddf77b612de799f8d4f963ed5e11b83eafd6cf611481dbda0d44dfe7a`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 3.5 MB (3529880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92efed635b4a0876acf283e7170082bb89d0f2d6f397ab3e4a8cf9fe8faa62bf`  
		Last Modified: Thu, 17 Oct 2024 01:14:25 GMT  
		Size: 15.5 KB (15467 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e9b1dc92def9b23d4147b701479a4c0cb4287a99fded2945d0f6141c918d1718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59997190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e1d085caeb9723f2e7d1685e044ddfd1251b756793da9068dc8ef89912c923`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207c4d641255ff6bd7b8ce630c8cf947966d1ff05bdf86f951c687f989e2f5e9`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 6.3 MB (6273546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c25f32db1b1126487143c75b9ce0d496e410c5bae14e76068c7767c3979041`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1aa1fca4ed404a2dafbd083628f990869ee0dd7b253df1199afbf67da6e338`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab4cc25b7109f5af55ff37456e9f7fe94f979dff175b36667bc066bff22439`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 91.8 KB (91781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376ca4ce57be9758785676dd94566197e97b56e273d0d68b507106d5fb088f89`  
		Last Modified: Thu, 17 Oct 2024 13:32:59 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dbb9f5c6a73482e60b6f663408c48da9384405cc218fc0247429a4db9e0a0c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3546522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f10c7d37e9b03e2031feb3ef71d8d1bf5349441266305f933b01c78e258c35c`

```dockerfile
```

-	Layers:
	-	`sha256:ae362c8599903d2c6f23db6caf041eec1d93bdbc004c5115130317bed59a413e`  
		Last Modified: Thu, 17 Oct 2024 13:33:00 GMT  
		Size: 3.5 MB (3530921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857190c4726e7bbad6a89b69d081e58436891e0510c537d4d585edd56bfece2d`  
		Last Modified: Thu, 17 Oct 2024 13:32:59 GMT  
		Size: 15.6 KB (15601 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1a746becea805a95a3b1d8e2136c588c82f6640fabbf5b5d22b913ad88128d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60829482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fbed28d59a1fde84fdbeb100a9ebdf604b856235061876e877aad0b4be73e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035359a3193290ee93a025ca5d676f11bf3efa25b6fddf81d67bf8d3589b5028`  
		Last Modified: Thu, 17 Oct 2024 01:14:38 GMT  
		Size: 6.6 MB (6617986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6952f46bac813925be650db4453b8ca209127d3493fe97170e8fdd998bebdc5a`  
		Last Modified: Thu, 17 Oct 2024 01:14:37 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f6a0313c5de2ce998d42e460162c0b4dbe7db82dd1a2ade4329507eaa884aa`  
		Last Modified: Thu, 17 Oct 2024 01:14:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627145859a1fd6976564bc212d417d5a9a021b48d6c5cd0a9c27f2f0c0be85c8`  
		Last Modified: Thu, 17 Oct 2024 01:14:37 GMT  
		Size: 91.1 KB (91141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd40c06f31194f8a4e83082b6d1fcb10e09061c6020cf18bf235dbf216f4e048`  
		Last Modified: Thu, 17 Oct 2024 01:14:38 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5c4d6d229eff64c513e035a637fdf70b11dbed69d4744893382bb2d655526e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8763464ded6610a3ee8e5d2b2c86e7b273c0e22ea00d4f5dd76840ba5564328`

```dockerfile
```

-	Layers:
	-	`sha256:75b677fef86179ceeb75d8f6689cc441eac33fd1413684cda9bbe9c0e9a32c81`  
		Last Modified: Thu, 17 Oct 2024 01:14:38 GMT  
		Size: 3.5 MB (3526979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8a9cdb86f97778094b27f0215ad427744de8426832800947d789f3e3cb0c8d`  
		Last Modified: Thu, 17 Oct 2024 01:14:37 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:3c9a5188bfe341e06ae943bbcfca2b56307715b705b7facf6c115e8ca93d826d
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
$ docker pull neurodebian@sha256:a7dec9889aa07f211ad822ba89bad5b6ce8709fb2662aab7acaeb9422f9cf4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118921d922eab791c13d7d4f706358625613c0466bb3ea1f9342a63c16c6df94`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f55ef76d9b4b35f21ab8fec574f6f36f7bd50def9bddc39211c4be1ecf5dcc`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 6.5 MB (6527854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e21780aeb7064d26fa740f8a4b9a09dfe743321ed8ccead5081f20808968b7`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3c1c54dc72253d17aa3a0747904e2f2cbeebe5381d98a4869ebfca8aad329c`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a759645cedce06316e780c1a68071850fdfad6eb284b6a5f289626fc23f9625`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 91.3 KB (91267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:924bb02286a421040b58de5bf703e0deac8f6386582a411747821f339ea70ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3551487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6625a391e9fbe8e0454e97d817ba5eac680a9cfe1a9d273a8f79ea499c655425`

```dockerfile
```

-	Layers:
	-	`sha256:ae98b6ac0554424512ec6baa4c19e7137ad6d019c0247b15234f27ba24fa55f3`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 3.5 MB (3538004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d175b07b1e4afad7f0cf9b37637c3cba14123dd767f1b33295271b7ef9010a6`  
		Last Modified: Thu, 17 Oct 2024 01:14:21 GMT  
		Size: 13.5 KB (13483 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:53f8645f8bbf3bcdce3887a06d2aa2869341c28b2397f31a7471bf82786d0b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60207064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe24ebd4529e94cbf8859d1c21480465d735c0f9fad6e339b6709aca6ecff62`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507ba0d1af87c79eb5ed21e470daeb6651cd6fd35ac71c7f4316437bcf9838b`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 6.5 MB (6513412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea37e5d08e4432023f6c69cebd438dd20a209a3cd3b94eb789a8c4f80f5fb74`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7766e08b26d04d33fce1a14d04e2233cb4eb74cda5d72aaa29f51748001414e`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41352cbfcbfbb365bc31271939a7c8835966e68a87266f29c649ba4302e4f95`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 91.9 KB (91941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:91e12dc77cd69062c3a5fc7d25bca613c58b29f11cb31adef1fd79a935dfdc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c885ac5fdcd2a78cdb9066851152200accf3e10a11697fab5019a0fe07de241f`

```dockerfile
```

-	Layers:
	-	`sha256:147a5aa5deb953d5f8b7f4c13b3365171a7306962923d3fe3ee5a0bdbddd0129`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 3.5 MB (3539046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdbbd0c40a05bcb4a92f56dbda7232d95e7d4d3bd20dafc56a52e38ff5581810`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 13.6 KB (13601 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:d2802c35bb0627592501ffc30f3df2daefbca9977542caff088c4f35229cab73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61045656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca83b56f3706b8d2edec74ddd0f12387138a0707a310844b3eb8da6b7fce1be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0104c3b9cfda50cdf3421866fc7eb610b28473908b8759e1240cb0d8ad183bc8`  
		Last Modified: Thu, 17 Oct 2024 01:14:33 GMT  
		Size: 6.9 MB (6875022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedd9262fa2e041d173fd0c1c2e00f777d7a35128a6cfb880ba548f143f446f5`  
		Last Modified: Thu, 17 Oct 2024 01:14:32 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d133c2bece8359e935db3b2875d562f307c53ceecbb48708378a24ef45b04c5`  
		Last Modified: Thu, 17 Oct 2024 01:14:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46ff097c43ae4bf706c02448e2466bd9b8c5b37f55b1685a84e9ce94419bd80`  
		Last Modified: Thu, 17 Oct 2024 01:14:32 GMT  
		Size: 91.2 KB (91193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9f1a937c597b21d6d3dcc90d05769817755c541905d0d7cd7abc73c2a3826d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3548558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b107b9695539bdcefef4858e73a9d9eaa93d90271cc4df926ae48ebaaa418605`

```dockerfile
```

-	Layers:
	-	`sha256:6af125565215ecef3d415be15edd88929016e26097df809146fee17a2974dce8`  
		Last Modified: Thu, 17 Oct 2024 01:14:33 GMT  
		Size: 3.5 MB (3535101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87d62435b91d7d078a1c9c759e6cc4625563ddd2f8d8070cdfd20a5465afaa05`  
		Last Modified: Thu, 17 Oct 2024 01:14:32 GMT  
		Size: 13.5 KB (13457 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:8aa073c3cd5fbed8f89f21e0cfc35a9d4a6fb7c1c1b16c96c1185a11b156b74f
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
$ docker pull neurodebian@sha256:a30d0910eee54e78cff1ebacfbf94d0f5d1bcfb233729937a5383b3b8754aebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59860224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58b7b67a10ad31319482f49ce07ffaed1409f4bdc42bdb57591f94a9f55f870`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463f8d68a16e9ac92c12f43868402c6f3f57d26fdad10a18f8469cbe505b5557`  
		Last Modified: Thu, 17 Oct 2024 01:14:31 GMT  
		Size: 6.5 MB (6527838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb52b6a48245f5a8831658b3aabe3cf7c7ff05fac76e80b3f6301fae8148095c`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9838d374d800c72b49ed8fe36ec4a126f57a5db7d2354dd3a32c800f1143d1a7`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0266e43d73ad49f9d716b54f8d979e37b5114c365d04ef4a24186995d7ec2739`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 91.2 KB (91229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf7b9db2b69c3f521edd6792979833642d688b878bb51d6390bb1461a1fa26d`  
		Last Modified: Thu, 17 Oct 2024 01:14:31 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bcdc6c21779357df565f1ad14a6f8c8508b2a8dc04d4b1dbbc25d4b2cd773cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a575d2ce06e3134c6340d5878b4d0403f24d2d7ebc47116f54490e5c6a19ec8f`

```dockerfile
```

-	Layers:
	-	`sha256:26e7003cef78c34f6c8b2ab579f8ffd7624e7c5566f72feec2ab5465909c0ad7`  
		Last Modified: Thu, 17 Oct 2024 01:14:31 GMT  
		Size: 3.5 MB (3538040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51fb57aa93986c771ed7fb9e961105a680c9f6cd0999e682188320cdf94ee724`  
		Last Modified: Thu, 17 Oct 2024 01:14:30 GMT  
		Size: 15.5 KB (15515 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9800c97a370a781ffb9871de33494c3a06907666e74ec5dfd30006c9acd5d149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60207488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49241192e3ffb655678dd748976796c720d47028f0001ebb417840254c4d9524`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507ba0d1af87c79eb5ed21e470daeb6651cd6fd35ac71c7f4316437bcf9838b`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 6.5 MB (6513412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea37e5d08e4432023f6c69cebd438dd20a209a3cd3b94eb789a8c4f80f5fb74`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7766e08b26d04d33fce1a14d04e2233cb4eb74cda5d72aaa29f51748001414e`  
		Last Modified: Thu, 17 Oct 2024 13:31:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41352cbfcbfbb365bc31271939a7c8835966e68a87266f29c649ba4302e4f95`  
		Last Modified: Thu, 17 Oct 2024 13:31:07 GMT  
		Size: 91.9 KB (91941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d45f485faecfdb395798bd27324e61884a7fa42eb02cb31494f7362503104`  
		Last Modified: Thu, 17 Oct 2024 13:32:06 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b4bf8e13d9e5fde0aa2ec003ed93ba575b296b6a1fa393a343426333a5f3bc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67a8e580c3f4979cbb59915aab3ad2437957ad387641a293eb5a716dab2d9b`

```dockerfile
```

-	Layers:
	-	`sha256:2a1b5b9e67e1dc1eb6abb7fe584c62fd8dc2ddf3e9842df732676c693cc1a80d`  
		Last Modified: Thu, 17 Oct 2024 13:32:06 GMT  
		Size: 3.5 MB (3539082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94b9375ffc08954ec2b358f015f7142cdbd3b31bc5835e0cbea70ffa77c06bad`  
		Last Modified: Thu, 17 Oct 2024 13:32:06 GMT  
		Size: 15.6 KB (15649 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:9c7f1e28a81eaa0320511416c4df234ad4f7600f45586e56abaf446d54c8c688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61046012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441a3e6af0dfa8112ae47502d4c44271690c8d39f51606037000ff9ad08129cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian trixie main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1ffc8190a07ef94376d2867dd7a73d310a6dd7481cc9c26c1a309cefcc3be5`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 6.9 MB (6874953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a00ac0906fe55639580577bbd3dd60b722d4c59033a0c14446e5224830a05c8`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39dbbc38a72670aac92fe8264b45b65f1639ceab86ba73989947c33f06386fc4`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cabfbcdfe93633e99167f3116691d7916d684a7d81ea43d9a4b36b13fa770b`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 91.2 KB (91188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3116d94f84b7b8a0808de899de4b7a8d7c6b78353d6d93203f567f84b724d03c`  
		Last Modified: Thu, 17 Oct 2024 01:14:20 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a6b2876e6dad21b09173111ef3753a8715147a7e56ae7770dc4060809e034a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3550625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617bea8eecaa56f0a9d3b22db9198bfe101fe2ac785cb3c5575ee8ea44214b3f`

```dockerfile
```

-	Layers:
	-	`sha256:b89f9486666bcd9109be18c9320b58d7dfcc763af91aa24e924946324820d2b2`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 3.5 MB (3535137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed201cf8df404b1835b3c3e3e5206232c9e3cb0be2bdf87e8ee937c6c6b19e04`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 15.5 KB (15488 bytes)  
		MIME: application/vnd.in-toto+json
