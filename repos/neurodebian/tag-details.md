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
$ docker pull neurodebian@sha256:ec94bf7c865f976be23788ed104ddcba722d2b21b22964883302f3db52f334ee
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
$ docker pull neurodebian@sha256:2b8b12cb107a339fae3a8c5c4f8406b159a03f22fa0ad6d623bd16b49be537df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45016e4b694e24cbc231ee1f05accbb9afb5360d114865d01f0244908c102a2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:33:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d27a9437dd9fc4b0efd290a2bcb6346624c2dd6c60cdc5371306924ff363e6`  
		Last Modified: Tue, 04 Nov 2025 00:33:42 GMT  
		Size: 11.3 MB (11269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663c2d2d90bc6bcc23bd09c4c13c62c2b13f33aa7990a8367683297aca575fa0`  
		Last Modified: Tue, 04 Nov 2025 00:33:41 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae69ff1ea04b61ba0f99224ac7eecbfc020816dc408515a1c4f2687556492e3`  
		Last Modified: Tue, 04 Nov 2025 00:33:41 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a4eb19871be6279fea378987e872d76dfd7c954a44f4eeaccbf2731d02be1`  
		Last Modified: Tue, 04 Nov 2025 00:33:41 GMT  
		Size: 93.4 KB (93379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4958673bc05f2ecf24b3c3560203043ca1923fec6fbb7b3db2c053d9dd09dbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ddc6fe171c2cafc24b32616ca557363933035f42ff5885d8bafd1af458162f`

```dockerfile
```

-	Layers:
	-	`sha256:62ec6d7f7cd447db60df7966ba8b3ab7b7bcfb5d1bfb634ef231de15d7c9c7fa`  
		Last Modified: Tue, 04 Nov 2025 11:07:24 GMT  
		Size: 4.1 MB (4075236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:067da4b2ed0e3bdb23696defb111cddb528d18310e11a0fce4d129f8305c44c8`  
		Last Modified: Tue, 04 Nov 2025 11:07:25 GMT  
		Size: 14.0 KB (13964 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2ebd3557ce31a6045fd165930762376e37228a68ddbb0cd51d352bf839927a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feed7c361f6454d2ebdca20d62eaa0208f7d77fdfbd2113e9ef339afd892a74a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:35:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:35:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:35:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a362910b4ff4e83d0dc3b8613b0eb94658f52d229b4411d4f0253056bb192017`  
		Last Modified: Tue, 04 Nov 2025 00:35:27 GMT  
		Size: 11.3 MB (11253369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d168b3317492e8db43d805d74c95ede9223b4334101713d7afe9e3c3cc93f27`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2ef3a583754a79f1f722a9b9976c108f72ba8983ec4bb24bb99010aafd6041`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edecae1bdd0f4220f6dcd6a59736227d042b109c1ecb4f47723783982a721431`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 93.5 KB (93501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:75feec74e5eac034fa9504f907235aece10e78c0f0ae41090a321ae023ec50fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82ee58d1c3a9e528dee7608a6c72d3042a584b594500f97872e8eec7b2b19ab`

```dockerfile
```

-	Layers:
	-	`sha256:619ddbb9c8584f00313f967f0c11265fe7dcd92403c29673bae6cc5672555029`  
		Last Modified: Tue, 04 Nov 2025 11:07:29 GMT  
		Size: 4.1 MB (4075478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a3294616fef78ed15fd035f53d08d63dc5079f3496cea9faad865804a8324b`  
		Last Modified: Tue, 04 Nov 2025 11:07:30 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:84ec72fe297f615978027618d7a29b7d4fdc7bdf614f6385c71871a006f781df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50834346a5bc41c0b659202fcd7fb0032352323cc91b14829b1accb034ef8750`
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

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5f053bcc51d8e520d03d28889ec38e3fa1eb698e639b24714846c4efd00d88bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aeb4189f2d1c01f722245843d4d06eb85d1f24ba7af1237d67e43be1890b6ea`

```dockerfile
```

-	Layers:
	-	`sha256:64c060ddfa2a6c4b6b512af8c7896620d501066922edecfb857aef9154314d31`  
		Last Modified: Tue, 04 Nov 2025 11:07:34 GMT  
		Size: 4.1 MB (4073204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:def7727632c070776a3a72db4cf217f26b8e0eefb659bbe3bc34da0dbbc5ef53`  
		Last Modified: Tue, 04 Nov 2025 11:07:42 GMT  
		Size: 13.9 KB (13935 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

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

### `neurodebian:bookworm-non-free` - linux; amd64

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

### `neurodebian:bookworm-non-free` - unknown; unknown

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

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

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

### `neurodebian:bookworm-non-free` - unknown; unknown

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

### `neurodebian:bookworm-non-free` - linux; 386

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

### `neurodebian:bookworm-non-free` - unknown; unknown

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

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:58df9431de6dac5cace8bca542030e9e935a3dbdd32255741b4a4aaac8903cf9
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
$ docker pull neurodebian@sha256:e8a290457fdcb25fd97add176a89aaf05448fa1604f033e5576c669df662fc09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed0150829bee747c74417bc49a1a7ae7b385f0b3d92929c5e18981faa5aa3e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:33:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10fd61e59bab2fc94cf6c8ece723b5b01be52abf9287e8ad4a9e0325bbda9f7`  
		Last Modified: Tue, 04 Nov 2025 00:33:36 GMT  
		Size: 11.1 MB (11105086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53069f91061c1664412e1de03713f16511af4421fb26b3cf5c0834cc5e0f5956`  
		Last Modified: Tue, 04 Nov 2025 00:33:35 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0348217f8861b15dbc928cb9ec299642abee403d4f1c9cdcb54a77fb280929c`  
		Last Modified: Tue, 04 Nov 2025 00:33:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d3db1b8d2466e54a0c98cba6586dee43d21bf61cc29a2d1c31fd2eaf958935`  
		Last Modified: Tue, 04 Nov 2025 00:33:35 GMT  
		Size: 101.4 KB (101387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f2ed622434305153bd8f685c0c5c146c9084bb854c75f81b6c8c0cd8f6616eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a0c559cc49adbfeaa5e73e9f4d74b43be50b2306a5313e2cc008d4ebcc919a`

```dockerfile
```

-	Layers:
	-	`sha256:973ef639fc1a7924a61cc483a9a3391689161787e52c26c8a30c0058f8d90b7a`  
		Last Modified: Tue, 04 Nov 2025 11:09:09 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939958c021b8d787652bb54951123245124f215e3944b7525f94d08aef60a918`  
		Last Modified: Tue, 04 Nov 2025 11:09:10 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ad60d79b65d4ee219870c13df5e5115485fdf0e3a15df30a17b5baf80718b5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b05d297144c8eca61ed67371e8a89c5b7f8231da7ce81b6293eceadf964fd3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:34:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:34:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:34:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:34:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a094538342569d02b91d24b808d205b77d9c9fbf852b9fcd0ca7903bad0bf75c`  
		Last Modified: Tue, 04 Nov 2025 00:35:02 GMT  
		Size: 11.1 MB (11105999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dab4fb4d007e63ce04d999f679515216a96e37397441dbfd194691445fdc850`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab95f778dc7d395951c5fc9a7171fbcb2da9219797d0f275f3893baa6d5567`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e461a23e42babff2e43e305785bb9d0dee54499c7cf927103041a5d495519244`  
		Last Modified: Tue, 04 Nov 2025 00:35:05 GMT  
		Size: 101.1 KB (101121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:60f3bec73acc99c31f72c306ebce80ea10d53f94d0a820dcfab64f5172af7f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49be1e79f5f06e2b68c2e08d12bda1fac934f3f4cf4597c22d1a2e2f54cc3dd8`

```dockerfile
```

-	Layers:
	-	`sha256:2c77cdcd1f4462f411c49db74b7815b153f938cbf01a2225e1b8254e06291e1e`  
		Last Modified: Tue, 04 Nov 2025 11:09:15 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8a2c5b00b6acfddf7a7463416c74a5f72f5a43c484a9ba8a9b444cdea70f44`  
		Last Modified: Tue, 04 Nov 2025 11:09:16 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:bffad495fc2e10c9ffdace390212b97040d9dd6fd7a3f3bb36b7a41ccf054306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64afb566d8d555a881c704ad285707871cbed6226050af4b05f957085be2ebc2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 01:37:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:37:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:37:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:37:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e60c3e4fbf8c19df439b90c2a7f7bbd43579378a671c1afe66083570c61159f0`  
		Last Modified: Tue, 04 Nov 2025 00:13:43 GMT  
		Size: 54.7 MB (54699883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11efeb646c81ee09e63cbbd314b45549a0e2d58975c0a2a4d5cf3b176d3a053`  
		Last Modified: Tue, 04 Nov 2025 01:38:00 GMT  
		Size: 11.5 MB (11500313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f18adc21b713d03131791638b3e0e3d1df3afcc168f3a53a98d4642f066adf`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de3fdc0a50f5c4807dccba9afe1e063eee114d6f77728b1ecb923ce3a56a8cf`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349d451c4654669ab44b9d291f3e6be7912fcf85eb2300008ac567b1bf186277`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 101.3 KB (101269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1c23e7716c1929c22ce60b5a211c7486a20034efa59e7f82f8172d21695917a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da420932dd33557839e97964af02cd54f6c3ad003782ab0ffa74bc0e4a5426ca`

```dockerfile
```

-	Layers:
	-	`sha256:b6e13c2e37e1a78a39ee3d6fe22eaf77db826b0afa8e4741f6f1d2c1a68b2547`  
		Last Modified: Tue, 04 Nov 2025 11:09:20 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e5502ab97137ddc1c1d3d9452d22a75de66d48c5b42f805ec6607488ec4efb1`  
		Last Modified: Tue, 04 Nov 2025 11:09:20 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:45c9f19db7fefcd0d7b140ef5c56f23244818d935d631503cbf616bc47053c6d
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
$ docker pull neurodebian@sha256:a45dd0e3386ce95f44f5c4926dd265d443d3d630f4edcc26b882ad3d51dd4e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce557f76a8782cb27f6a937c46475ed73e4bd342c90ee38a0abf344621bcadb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:33:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627c13d45db1bc3627114590a9a572072f259a283e073fabec89b6927460b0e6`  
		Last Modified: Tue, 04 Nov 2025 00:33:47 GMT  
		Size: 11.1 MB (11105106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08637bae51a885f58cd136663fc6922c49e2424cfcea177ea75f7040bdcdef0`  
		Last Modified: Tue, 04 Nov 2025 00:33:46 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace19d11403316e09784bdc28075bf7d7cbfa95b8f520261d963cffa2a418c38`  
		Last Modified: Tue, 04 Nov 2025 00:33:46 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421f1ebf0d0bf7053cbb682ae089001c7bfade44aa1367c2d04be6247af8dd1a`  
		Last Modified: Tue, 04 Nov 2025 00:33:46 GMT  
		Size: 101.4 KB (101402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfaaf8e2a3d6417a25962517c3ecc4093fcc632c6e230edf8be22f23c41dd13`  
		Last Modified: Tue, 04 Nov 2025 00:33:46 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c4fb7ac3fce0ab555c787455ff2a0ec32e5bb0033e6d9980618ff77152743553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc6a968806e1b986e719546bbcdfc39b1421bcf3527b752fba92ad026ecce8c`

```dockerfile
```

-	Layers:
	-	`sha256:18a19dfe3cfac69d2b3ca907adcf30844b15bdfb17df6270677fad851c8d9d61`  
		Last Modified: Tue, 04 Nov 2025 11:08:07 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6273ed50baba0b581f8e5e9c051fb9c6b3c8961818273cdf5f946541d0cc0c27`  
		Last Modified: Tue, 04 Nov 2025 11:08:08 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:57ae5b2253217ac9ae33b55ab55c5360788cc8f216ffd923363708f83617ef95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb427c73de74a9e991f127a33eb1394dba97a3ee16f787a74ada4d217fc0569`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:34:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:34:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:34:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:34:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:34:50 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb8dca10b60e4cad77c222af29c649ff3a5126ea283485ad6c537bae4008456`  
		Last Modified: Tue, 04 Nov 2025 00:35:06 GMT  
		Size: 11.1 MB (11106030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de57a9ad3fe875764e4fbd92ca4e298f4eefbf492ee92887c4fbde5fca730a23`  
		Last Modified: Tue, 04 Nov 2025 00:35:05 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3b09e452de82ebe7de58f5c3ee447695ea6164a28676cfaa3c2725f63a00f6`  
		Last Modified: Tue, 04 Nov 2025 00:35:05 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a00e295f476d7e6317fe37274cd8cc9211229b98fbcc9a872927fb46dec83be`  
		Last Modified: Tue, 04 Nov 2025 00:35:05 GMT  
		Size: 101.1 KB (101115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c366338618a32829891f215d4a2762da10ce1b2d40b4b4582ccabce53735ff6`  
		Last Modified: Tue, 04 Nov 2025 00:35:05 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:271ebb53e8cdad38f8530e5ba91b09e5f4e8f445217eca3b20a8d6201ae9991c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e8040aadbb5156ea4fe0706203af6f6335ef3922ebfd647454ae60508eefb9`

```dockerfile
```

-	Layers:
	-	`sha256:52a9f7d2fc29ae8cacd332b69f866c721505869a24f567102f48b360f67f9284`  
		Last Modified: Tue, 04 Nov 2025 11:08:15 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfd52c9caf33c39a8a4d52888271a2da0f800be52d634639efcd0ecf36ebbd0`  
		Last Modified: Tue, 04 Nov 2025 11:08:15 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b70e05340f908361cfcb14504eb38d348b67f1385addcb3b71180869cb279b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66304014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b966eb9bcd46c8924e332ce6d8bb2600aef8489ff46439c0b5a74a67130506b5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 01:37:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:37:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:37:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:37:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:37:59 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e60c3e4fbf8c19df439b90c2a7f7bbd43579378a671c1afe66083570c61159f0`  
		Last Modified: Tue, 04 Nov 2025 00:13:43 GMT  
		Size: 54.7 MB (54699883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11efeb646c81ee09e63cbbd314b45549a0e2d58975c0a2a4d5cf3b176d3a053`  
		Last Modified: Tue, 04 Nov 2025 01:38:00 GMT  
		Size: 11.5 MB (11500313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f18adc21b713d03131791638b3e0e3d1df3afcc168f3a53a98d4642f066adf`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de3fdc0a50f5c4807dccba9afe1e063eee114d6f77728b1ecb923ce3a56a8cf`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349d451c4654669ab44b9d291f3e6be7912fcf85eb2300008ac567b1bf186277`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 101.3 KB (101269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b45ea2828a62da8544d87d0ae49408612b86bc5667196c23cd3008df0aeee5`  
		Last Modified: Tue, 04 Nov 2025 01:38:10 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:995258b08a64bb138022f1c4946d369956d5212553fee8721e22bbce4ec305a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07469cbbf480035470d48b72db1f398d6c102c390ce197dc9fdbd0410fd4d5fa`

```dockerfile
```

-	Layers:
	-	`sha256:75b921e38de9846f770e87307dd1af17529c86aa476baa487b8a92f591c72907`  
		Last Modified: Tue, 04 Nov 2025 11:08:19 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c29747f78e39dd80695f1395d1577f9ca3c0cd4fbb0913f7985cda101a09499`  
		Last Modified: Tue, 04 Nov 2025 11:08:20 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:b0fa219b2f2b0e1ef0ebc2ff181ea60aae3e67618dec06fd14784d22c9a9e076
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
$ docker pull neurodebian@sha256:a95a11b0f551d6c581069697c60e42099b556195747382af9b33a2a1e8ce93f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60157262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f25047aef6c2ed146b0d840b041672aafe2ed858eac68e294f3fc82a423e757`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 00:33:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:186ca733686ffcaca03fdc512b51c9498f39b93235775cf08154b1ff0b143901`  
		Last Modified: Tue, 04 Nov 2025 00:12:56 GMT  
		Size: 48.5 MB (48481364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49a1e0dc0b376f0cc4e1d2e12f628424d11aef8cc2b87d1861a241e7b56be80`  
		Last Modified: Tue, 04 Nov 2025 00:34:08 GMT  
		Size: 11.6 MB (11583245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e442443001bb507838d0ace541f13041b1411d5710f72f823ddc28e99d3f80`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631c24460ba15377fa27b5a824758985f589cc6a8e3d9ceb6081711d0313984c`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511bd2e44a8ef113bd55092f7a48daf15c7c5e2d7bddd9c74aff0b231be4e6f5`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 89.8 KB (89752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8159857513732c8d6ec476797d1e7a3eef95188b2f790e79a3bfd35e97222999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93865f95e0647d34d373da23c19eb0a62c166b34d1df3251cd841853a38b981f`

```dockerfile
```

-	Layers:
	-	`sha256:5af3592e7343b7b1c38b837a1377c054ee4e28a40b2baf57476265e9d958e93b`  
		Last Modified: Tue, 04 Nov 2025 11:08:17 GMT  
		Size: 3.6 MB (3577405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ac2d7114b70f666f54881e4a50c6b5c386f5e319cf9276fa4e75dafc807c90`  
		Last Modified: Tue, 04 Nov 2025 11:08:18 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4a1ab300e12ac91c2e44ad39a108a5bb56a3e906ecf1787492a800e49671056a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59936207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c3dba418be4e19359f1b1f1eb385c8c079ccd6229a6cbf94f21c326c33ff0f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:32:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:52d2706ca00f3431b3c37b306b3eb6cc4989781e31180bfdf93c4dd4108e1e3c`  
		Last Modified: Tue, 04 Nov 2025 00:13:40 GMT  
		Size: 48.6 MB (48583638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de1bec0d095ae1671e8e93b5fd0c690333dc3cec029fee404c8ff0ffd5d47fc`  
		Last Modified: Tue, 04 Nov 2025 01:32:59 GMT  
		Size: 11.3 MB (11259161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9e5a0ec4a83df31c8df66ded76dd9f5aaea5fcc1317ed2a8b9dd1503fbf203`  
		Last Modified: Tue, 04 Nov 2025 01:32:58 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ded840b50c25703b8cedff47124e880b4c80660332cde3bd23f80cfbc0cbd6`  
		Last Modified: Tue, 04 Nov 2025 01:32:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d602e5443e53d9509a8ef31c9c5f0b5a2a09fdd1fde958bb31acffa342d92c29`  
		Last Modified: Tue, 04 Nov 2025 01:32:59 GMT  
		Size: 90.5 KB (90502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:682a6d16a7ae5f71baffd961e48cf81d51aba52c6b06868e211e1088afa97f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba6e63f0527eb6106a462f2be1815978786ac89575942a8b59bf6211fa5d013`

```dockerfile
```

-	Layers:
	-	`sha256:650e9ae2490715384b193964e2a59ed8052365d101979d7893dda65ced07355c`  
		Last Modified: Tue, 04 Nov 2025 11:08:22 GMT  
		Size: 3.6 MB (3578281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5bbc6dac0e2c65a14b10e33477ca40edf0246b43d3b141e56450f889368557`  
		Last Modified: Tue, 04 Nov 2025 11:08:23 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:7462d5da772e47bc5cfc2c6b321eff341fee7f8d8ed083e68bb4e6258a89b660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61637327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5ebe96ca47d62929b0f9496e4a90f8ce2a9a78c613cae09a60d476ca7eca4b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:38:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bd86ecb6d3ac97cad4df6e0aeedefdf1790afb18f99112bd09ea68844e318978`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 49.8 MB (49809500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9d5279884080b3a9cc53b22c9970ff61131076fa40ed02a21823c040bc3f88`  
		Last Modified: Tue, 04 Nov 2025 01:38:53 GMT  
		Size: 11.7 MB (11734742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea45ef2b067c6f619d817ae565ce3ae8487840b2727b980c0ac37f18cb60a7d6`  
		Last Modified: Tue, 04 Nov 2025 01:38:52 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354665d7d7917d747ec260c4a0e42a1cdf7ced8f50f34d8515da774536057834`  
		Last Modified: Tue, 04 Nov 2025 01:38:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5fdc3252598c0dc204c07be13ef748ce0649e55a32aa7459d22b41f1a045e9`  
		Last Modified: Tue, 04 Nov 2025 01:38:52 GMT  
		Size: 90.2 KB (90180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d6c19633e7dccb24a6f423af4036e5c7dc575df68786e1782a2eaaa76b2fa17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da159b3b8e0dcdad52660ec976ef25d34304e4e14a84e443061cb6d6a9c35926`

```dockerfile
```

-	Layers:
	-	`sha256:d508ed6522322ff57ccb321b54a299fe8ca0df639f7366551a61a05657dc3119`  
		Last Modified: Tue, 04 Nov 2025 11:08:26 GMT  
		Size: 3.6 MB (3575368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb005d7845f49e8616299d2fcf67924720febfa2686753c18f7ac4e8677f8ca`  
		Last Modified: Tue, 04 Nov 2025 11:08:27 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:384828113ce018b109587fdbd0eed3455ed127d24c20f4cd7b567279f645e467
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
$ docker pull neurodebian@sha256:70189282e254301c784925ce371e2d46b8803e68c3bf317555ba516f7f30faf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60157762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc773844b4e251440616e054ab18d55d4fe865140e940d5f110fc8e0a61fd01d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 00:33:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:50 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:186ca733686ffcaca03fdc512b51c9498f39b93235775cf08154b1ff0b143901`  
		Last Modified: Tue, 04 Nov 2025 00:12:56 GMT  
		Size: 48.5 MB (48481364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2ed7e1eb66e73be7a81904f625e8af8e27bdbcb556d412220b4dd47da85a13`  
		Last Modified: Tue, 04 Nov 2025 00:34:04 GMT  
		Size: 11.6 MB (11583251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a2103db929aa61129b750d42223222a7b4692b76c2285cf0445cdad7ce42d2`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af62a6155153d6cdb65922ed9f2501a9399acd5dc27bd108f4abbeaf8a7ce14`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deca5aeb491ce74b8f40489e25bd1cb7d95e88698917d60cd807d9a6c68db73d`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 89.8 KB (89793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d896b07b7e37a7203598f231523daf17e786b9ab694595a4aff3f90eacaab6a7`  
		Last Modified: Tue, 04 Nov 2025 00:34:04 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bf76392847b143d89f63d547ccd03be8ce62c9af5bb9f0820a2cb949ff456788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfb5753a33312ff7862b3b9d32e1577419c78d795b37b5b5e3ab360f8743e80`

```dockerfile
```

-	Layers:
	-	`sha256:fb10025220538f30c02045c8f5d88fded55d77d4fdd339040983116e4d90af1d`  
		Last Modified: Tue, 04 Nov 2025 11:08:30 GMT  
		Size: 3.6 MB (3577441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b43e03910d7abc9bade8c2dd90b348ebcaa7ff7efcbb066f238608850dbf151`  
		Last Modified: Tue, 04 Nov 2025 11:08:31 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bc8ce6ed3e3c776152f99cb1104daea078494d0b923198a6c142487c62eace11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59936579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c69131f270dca8fcbfd32858708e9d91d5ac087ac5e89454675950b29f061c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:32:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:52d2706ca00f3431b3c37b306b3eb6cc4989781e31180bfdf93c4dd4108e1e3c`  
		Last Modified: Tue, 04 Nov 2025 00:13:40 GMT  
		Size: 48.6 MB (48583638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cd34f0ce98712d55741951246c28dc8f4fb5749fe6f009be810a15bc39e7c7`  
		Last Modified: Tue, 04 Nov 2025 01:32:56 GMT  
		Size: 11.3 MB (11259085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37370e1cb03e1aec0bca31b7c63d049563f347f1cbafba5f70d06d99e86b5dbe`  
		Last Modified: Tue, 04 Nov 2025 01:32:56 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17eba42e5d505fc3a5d3fd9987372e50964fc3542c2cdf1d4a193649b6d79dc7`  
		Last Modified: Tue, 04 Nov 2025 01:32:55 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b804357151b1a683a4a79a6e6c1980ecfd72123c62be18c932e14d3bd0684a`  
		Last Modified: Tue, 04 Nov 2025 01:32:55 GMT  
		Size: 90.5 KB (90502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897b8e80528e0ef186efb3269fdf4ee30234c872372be7fa36d91d07b30d7ca`  
		Last Modified: Tue, 04 Nov 2025 01:32:55 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:47773bc2f2c9cf5068f8d72bdcd2fdb869f026c1927d9f695c39218b8917e292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767d0a3d4a306c0a128156ad9700a3ad79383bdacbd5764b54d4bfa729dd9191`

```dockerfile
```

-	Layers:
	-	`sha256:b40777566d143b66e58a9a658fe6e101d5e37c7b56860fb660b7f69556471886`  
		Last Modified: Tue, 04 Nov 2025 11:08:35 GMT  
		Size: 3.6 MB (3578317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30961153f32eea93b5027e2061824753dd9f37ace2199e650c0e21c4c49e8c64`  
		Last Modified: Tue, 04 Nov 2025 11:08:37 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:63d7073757f8af8afe32eadcc816f9af8a1235863947854f3cec2f8cf7759d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61637813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f76ec57eee1b56c541332f031778cdd216e88f6085d0c30b6e631b2600449bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:38:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bd86ecb6d3ac97cad4df6e0aeedefdf1790afb18f99112bd09ea68844e318978`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 49.8 MB (49809500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3fb4596c99fe5762ade8fb8b49b83646c2974bd279b25a5242783b6be97fa4`  
		Last Modified: Tue, 04 Nov 2025 01:38:58 GMT  
		Size: 11.7 MB (11734764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a42eb16fe9637037091596145b07dbd6c26d5a89f0f60752ad47e9c6a4cc9`  
		Last Modified: Tue, 04 Nov 2025 01:38:58 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c465762ff747abccb8f26f7940310315ad22c0fc83643d9a17eb2e44999632`  
		Last Modified: Tue, 04 Nov 2025 01:38:58 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a908abcd3ddc1a45d84a8a1ee749cc706039c754ffc9b248a425d41c76ae1e`  
		Last Modified: Tue, 04 Nov 2025 01:38:57 GMT  
		Size: 90.2 KB (90198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1814fb1bc1df679152afd6fd24901df7384befe85816a664b3bda4f764d0fe97`  
		Last Modified: Tue, 04 Nov 2025 01:38:58 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c777d330b6ca4603bc533b8b59a2d655e01875d5366fb0e49a18efb61c8a4223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaf32981d88398acb2c6917a96cc42b7e3624895dc4ae282c20da5a261302cb`

```dockerfile
```

-	Layers:
	-	`sha256:f22f145d2d10c0e5d330f0abab2f7ca18e0529f5bb7a1ef06a8b9c9b96ceb661`  
		Last Modified: Tue, 04 Nov 2025 11:08:41 GMT  
		Size: 3.6 MB (3575404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c492288d345222064869611f8283ff114449640050c12d23dcde88c37772b53`  
		Last Modified: Tue, 04 Nov 2025 11:08:42 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:0e98bbc3daae66df44ae11a5588f2309b4d0b0a3d5759a236557a26319c2c5b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:e6772d070a574f00e1ad07efb0f799b7e9d9020fccf9887c7f6378c50bdbe816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d6aeb77e4a5a773edcad5fc10b5e08d8f387161a9b7b5d93e1cb1aac4e3735`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3881e591a9050bd6250b7975f2a62d69ce9d4bc181a569e43d583973bfffafd6`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 3.6 MB (3625726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7763c1732252c316b49e1a5ebe3d01e0ad636198993b3e20e7267f9fe62d4283`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59987cb0b364dad0627b12e7ef72104aea08b23fff39930f94dac5b79cf2585`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91714d8e9de2a6eab65bf534a21daeac5f710d6f823714736754481479f25eb`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 111.3 KB (111253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74faf561f221e4ff0722a9a6a5469d286311b0d29d710a50c1c2f2d408089335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5093bdb0233d5e701687d2c9157af64b57724e81b512be660289bb7a4c8f7216`

```dockerfile
```

-	Layers:
	-	`sha256:288a50939bde1611937533ae039c8544b98d95d75331e8bde2456927a7ddea17`  
		Last Modified: Fri, 14 Nov 2025 02:07:40 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941444796f9904d69ff28378466addce903b01de5df5c0c291ea8d117c6aff74`  
		Last Modified: Fri, 14 Nov 2025 02:07:41 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:09ed49f28825e5330d749e8aa583e2f0c2c88ace7f935f79fd1b4ee7cfd6502a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31094789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170be1c0c9e62fba389535f45096cb097ffcd73e82e10f8e5f2bbeb7101e7716`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:30:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:30:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:30:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:30:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4fc061e7db4abc03b992399d4d51a6e96a401904e29c8c7cfff6c2b0ef4cbc`  
		Last Modified: Thu, 13 Nov 2025 23:31:03 GMT  
		Size: 3.6 MB (3598146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e356cef2bd87e42a124fc4d5e82057772ca5cf202c6c194f6884f04283430a`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7f921b9372d265e8d3805815b0e98436f5f4b92fc0dae86070b7f4f269f992`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562a8628e6dc417f84896302f26a4b6c43f921ca7ce9b73b785936f7e5d51be2`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 110.6 KB (110588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4d3a9691d374823b1b504cf09f6f82049355ef10aa41d07d3be46ed00124eda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb368a6d54f82c2cad7c303b49a01491c62b68e3a47065952793b1df828ae`

```dockerfile
```

-	Layers:
	-	`sha256:c8a0004225abd4f8c618461be1e72c1192172f7ccfd4fa7f0839dbdc35d24f43`  
		Last Modified: Fri, 14 Nov 2025 02:07:45 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200a3136b60277a7c0dac564342f17944ff690ca89305553d8bd0bcd74108f3a`  
		Last Modified: Fri, 14 Nov 2025 02:07:46 GMT  
		Size: 14.1 KB (14056 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:120b8715dd3a26a2af4049512591dcbb112d36e4accff9d7fded93e27ce47062
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ef9dcfb5426525d36ca828760110823e06e065cca0c4ac0682d0a506e9cf12e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33276245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abbe750921d6da2c2bf91fa655875aa86d26da7d2c93cd08dc4d8b4f91445af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3881e591a9050bd6250b7975f2a62d69ce9d4bc181a569e43d583973bfffafd6`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 3.6 MB (3625726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7763c1732252c316b49e1a5ebe3d01e0ad636198993b3e20e7267f9fe62d4283`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59987cb0b364dad0627b12e7ef72104aea08b23fff39930f94dac5b79cf2585`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91714d8e9de2a6eab65bf534a21daeac5f710d6f823714736754481479f25eb`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 111.3 KB (111253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87663c843a43743cb4efbfd154e030c6591b4085d0c1d047a156158b9c47142a`  
		Last Modified: Thu, 13 Nov 2025 23:31:58 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8b9b5e291adc948bf145496030828a9a408c3399355380347b0ff72c16e2a880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970a1d784b637f4a06999658bbd7cfd5f71517ef14610d1888be4fc2d5614399`

```dockerfile
```

-	Layers:
	-	`sha256:19ad39194fba9b75b47c96c260e5431b390f0c1f40747e8857c995d53dd228f0`  
		Last Modified: Fri, 14 Nov 2025 02:07:48 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd46be2a48617b0b0891f5fe27958f8e2350a649da215ce9a4995e5a9a62d43d`  
		Last Modified: Fri, 14 Nov 2025 02:07:48 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8c05f54ab64c544f5b1833f0d31ef94804c914c6debd693acfce0dc0320660cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31095110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2b987bf931381f750375f7be732736b38d67dd928c373fb3ac7f7703364fd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608dccde847e272476e52044e62fdf40902fdf981eba3f9e853d9bb36c3ebdf5`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 3.6 MB (3598157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff367c25857e7c190e4c69803b560c6e428a2f6fdcdef7291ed9c54595fd3a7`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d785e7ece3388bd939c0607e15ed02803f8e48b590bbf43d7b628f2275ed86`  
		Last Modified: Thu, 13 Nov 2025 23:31:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411f09f71214f6303934a66000e111fee3918961b6f6726ed9b784feeceb7fcf`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 110.6 KB (110611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa2aa73e9807dfaff0d65e73fea59b7275dac6754311bac380e78c75cf4c922`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f02cab47a327aef8e9eea19cc7a8da708ad76b7fd1cee2ccdc47f302f2cade08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5d2870c8ff27e82579456117c17077c9ecc56cf9812adeb91b20dcd8fdb489`

```dockerfile
```

-	Layers:
	-	`sha256:196e2a812f54eccdc16bfcfe68a337ef2397641ccf3672d5f6846a2c19b4a34d`  
		Last Modified: Fri, 14 Nov 2025 02:07:52 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be4dac85cb072f2caede51d4767494f8e063e10991e49a2febf5e030defd53e2`  
		Last Modified: Fri, 14 Nov 2025 02:07:53 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:c2360b59f5cd07c356ea19ed3cdc88006759a1c0012203558eabacf878b94db7
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
$ docker pull neurodebian@sha256:cc62f8a2b909a4a621f695fb23ddfd2f55abe99c1107ea422ddbc9493ed29c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59668516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58c9d81054ebb46f7a713bc03b050382ac159d061b22d7c255322f1b7f34f30`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:17:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:17:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 04:17:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 04:17:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a97f52bf44b7c35c2c3dde0b10f67fac3048c89ac6322097bbe246677a0d380`  
		Last Modified: Tue, 04 Nov 2025 04:17:37 GMT  
		Size: 10.3 MB (10289768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eeeebbd965732bf90942a1ebed2be9c5db1bfbae37f79d18df48b59aca1094e`  
		Last Modified: Tue, 04 Nov 2025 04:17:36 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1715ac06925051c0dc44b303a59854227464617274e4399c7c3f7ed42d3b728`  
		Last Modified: Tue, 04 Nov 2025 04:17:36 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c90e3669c8b11bf12b32885c25bb7005fc7657659840b3143510e4019e3f87`  
		Last Modified: Tue, 04 Nov 2025 04:17:37 GMT  
		Size: 90.2 KB (90219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:36e5e12cc006b9c643190e4e94c3c9be24cdbc7ab1ec5ce2a37eddbf5d3ba551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499dc65ca82ef280131d7296a24026b6d9c9a045d868f46c496b60250fd68b51`

```dockerfile
```

-	Layers:
	-	`sha256:9693e52244e9d6cb3776573b396e8ad9c1541b70da98119a48d0f73cebb9b960`  
		Last Modified: Tue, 04 Nov 2025 11:08:43 GMT  
		Size: 3.6 MB (3613035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc75a15b38b24dca33cd177d886bd1cdc06cc59a5a50cded16bab45890c0f3f3`  
		Last Modified: Tue, 04 Nov 2025 11:08:44 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e88a59a8eb59c283f7ceee4aa5edff9e76424daabdd909cbcfd68c99440707bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a592f978047a6bc3cfa14fa679b85d9abaf32c5c31f72dce1954eed1d6b74070`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:32:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f261ede3c228ffdcf1af64259b67759d9a002314294a6000401de78dec7fb6`  
		Last Modified: Tue, 04 Nov 2025 01:32:37 GMT  
		Size: 10.1 MB (10073302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6646aea08c3732bf73a2e6f46ff98544770e90860b4a0866fccca039070f3971`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44013910ff33d14f15aaed9be503bd613a4c1ecf18b98392429751d3e1fc2010`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7fc94592c535b9c56ba976c47ab0d65065ab60188dfa41ea53a0384e5650fe`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 90.9 KB (90885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:67a7caeac0b108a3854951a85b61cea2cbf3694ba8b127f21abb057acc37ade8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748332e676c636a5998508a3d059c676a2b871719d4db0d6cb4ea97debe4bd2e`

```dockerfile
```

-	Layers:
	-	`sha256:2b1e3c4221c421d4c252a44448f8148f38f4bdac55bd98dbbf9db0660257507a`  
		Last Modified: Tue, 04 Nov 2025 11:08:48 GMT  
		Size: 3.6 MB (3614562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74244bc19fbb24f3845e801cde56e470597db35a2cee721033aa920b9e5a27f2`  
		Last Modified: Tue, 04 Nov 2025 11:08:49 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:f1f7bf3923b89f2692a55d2ef2edee2bd82dbdc0d1d0b02b9b061c57f1e36040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61357599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db97c9f327dffd9682c36f7aea893d03e88502d815f95f1d27f8b9709dd0e9e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:38:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:933c2eb03a495d1bdbab772ff092366c6df6bb75cafd8749623e94908401abca`  
		Last Modified: Tue, 04 Nov 2025 00:13:58 GMT  
		Size: 50.8 MB (50801238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2c10dd39d3ea1b7fcb9ac6e3da6cd2c85fa478453556608f507a3d8d1f3de8`  
		Last Modified: Tue, 04 Nov 2025 01:38:36 GMT  
		Size: 10.5 MB (10462886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9376d28a0149ab43591656335468744f02197d038449d77f9079e5468990880e`  
		Last Modified: Tue, 04 Nov 2025 01:38:35 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca789b0bcf3530d0cfe0bec7d39ca51f45bcff2c8d4b4b423d21a5202dba138`  
		Last Modified: Tue, 04 Nov 2025 01:38:35 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8321b60075f8d7fed5d7ca2c9196cdb5c999eed080f68586d1e00a229d684962`  
		Last Modified: Tue, 04 Nov 2025 01:38:35 GMT  
		Size: 90.6 KB (90574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cda8f897e235f9ee79691e1bc08a3297a011b8bc61f86a081bf28301e8682a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c691882c13ae6f1a1774af6d1a3247c9e387f56355f7cb056f38ff5955ad54`

```dockerfile
```

-	Layers:
	-	`sha256:166ffe9a4c84e31de85225508329baa1a1ba0f7231e235931fc77f822846d3db`  
		Last Modified: Tue, 04 Nov 2025 11:08:53 GMT  
		Size: 3.6 MB (3610984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dca0d5a4a061e7f9961f25762a0315f1d2bbbfb9720f451af5e672c5ffba9d26`  
		Last Modified: Tue, 04 Nov 2025 11:08:53 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:cfbe31e8f8216a29bec1d84ffe30e9154e7006818f7e0fe5af624b8073a5e896
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
$ docker pull neurodebian@sha256:722b3734a074f52b537930b8d13d96a90c23904dea0de135834085857118a3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60161613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9e6e7067e1ace693bcb1daa4cb49007ce4c30aba88f93332e4d3297eef23fe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 00:33:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2e77f12282fcde2c6f54d54624e8a7eef59205bf9001d755b40c1e76ea8e3238`  
		Last Modified: Tue, 04 Nov 2025 00:13:00 GMT  
		Size: 48.5 MB (48485640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a5b96440cbeeb7769517ff329ed0883771f1e3a99f7933b2173145cc5480cc`  
		Last Modified: Tue, 04 Nov 2025 00:34:04 GMT  
		Size: 11.6 MB (11583255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4375310c6ed16655ad67365cd813771aabbbe8573c45b873213c2074e78f4528`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f426f31085761e6a46465387404baada1a21b1249625e208e4bf18e8596c6d`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e900ba29d98519727c17183e473955bf493815c7da5e3103020a8176f31fc356`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 89.8 KB (89813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e4a85c3da567c9a45c5c7f1618d5098c8ee258bf7ea9c83695d83dcd6a8f4c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c45e24afa3b99e6ff745dcae8421698af0fa6919177fa5959f32b08970e1c16`

```dockerfile
```

-	Layers:
	-	`sha256:45cac87f230eb98aa986ff794a77ff43a15a3bc71644de748398a4360351376f`  
		Last Modified: Tue, 04 Nov 2025 11:08:52 GMT  
		Size: 3.6 MB (3577395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c589fd0990d047638dae2719c765f5e3f9f00abad8733ec51451217ce909976`  
		Last Modified: Tue, 04 Nov 2025 11:08:53 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c7cce04f019cdaad0ced550dca9af4ce069da69a580048487ac8e45f4dfad4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59938487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792e7d0dd2ec4ae27f7d32f4408e7344a709b1185f2c60131cba267efb2d3fe0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:32:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e6429e9e41ca9e14d8856af7a396ce50bc2b9896b4f4cd83c36fd480cd4514de`  
		Last Modified: Tue, 04 Nov 2025 00:13:31 GMT  
		Size: 48.6 MB (48586018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e357ec5b83e5625b9f94d5fc603d2031b8514071e4bd32938375326d1cc6c9d9`  
		Last Modified: Tue, 04 Nov 2025 01:33:04 GMT  
		Size: 11.3 MB (11259052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d225e2c5c4d55a1eeedd7d833cce1246eb8fa46211165fba4866d1f770d13666`  
		Last Modified: Tue, 04 Nov 2025 01:33:03 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d0a3c87f92b126ad11f68b5e3d11fc24562344b0b4d492241f33509c2acf11`  
		Last Modified: Tue, 04 Nov 2025 01:33:03 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f467de9381fac753e2f32ec130c3fdc5bd52c38944cf43855a312828900bb2`  
		Last Modified: Tue, 04 Nov 2025 01:33:03 GMT  
		Size: 90.5 KB (90516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b5a2152fc41ed9eea92688f57fddcb38f01656a94abf50490022d188d6e5d609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69957ad7a64f6286d83d10828ce2f0c30cc145aff8c0291731392884594992a`

```dockerfile
```

-	Layers:
	-	`sha256:5df592788eddb75c428d5fba029ca483e1a5adc0e0e03f142b8455a9f3235ce5`  
		Last Modified: Tue, 04 Nov 2025 11:08:58 GMT  
		Size: 3.6 MB (3578271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fc7a61a4a383f5b356e7bb4721d7e94c544d6ea8839c32df57b0b84c4e15cf6`  
		Last Modified: Tue, 04 Nov 2025 11:08:58 GMT  
		Size: 14.0 KB (14028 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:9b677e080c119eb4a17717438cd0c8483c91f4ea704a02c34b6f6506c58b0ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61636868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4883a56e806041e69ea01712a928a707f955a2916bc0a6ddf0f9111af750ddf9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:38:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:37a822686dc57d9a439e8fe6f90a9020bbd58f684341d3cac6e3e13c68f3344e`  
		Last Modified: Tue, 04 Nov 2025 00:13:36 GMT  
		Size: 49.8 MB (49809007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3095763312556ed24fdf8414a87f3df47e55ade17984072746abeb95af700d7`  
		Last Modified: Tue, 04 Nov 2025 01:39:06 GMT  
		Size: 11.7 MB (11734751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20daa1451a1c5e4864905084a53cb50a8ea4ecc7152fe1f07eec291ef587bedc`  
		Last Modified: Tue, 04 Nov 2025 01:39:05 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a436f1558d69b26b0f120fbf5cb58bc87b6656499820ecab74b4cfba29a4f5`  
		Last Modified: Tue, 04 Nov 2025 01:39:05 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d31efbac8a3de9856fb31500c282ed7ac97967a0bfb99748f45785bf8ff335`  
		Last Modified: Tue, 04 Nov 2025 01:39:05 GMT  
		Size: 90.2 KB (90206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d42fe0312df5575f7895f36d60444890b9d1945492b4ebf532dd5fe409a8b2d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8feb1ed938280b209b67281e45960fad0d7b9e3883af43573db10eb3d7a4438c`

```dockerfile
```

-	Layers:
	-	`sha256:c8c06839190cbb474a9a1105dae3eba7bf063e0ec0058bdb7f336eb8fa3fbb48`  
		Last Modified: Tue, 04 Nov 2025 11:09:02 GMT  
		Size: 3.6 MB (3575358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a58ee565df700715f4dc6eb2260eab6c98353f3ffcaa0425fa571731b9f3a9a5`  
		Last Modified: Tue, 04 Nov 2025 11:09:03 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:fc69386df37f5bf119ef83293196dd59e80a4792d08d52e437c64ab8dbd886b1
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
$ docker pull neurodebian@sha256:6879037c817de6fcd44e5e3e5669da89e8ba81a5efb8d55e046fb7cfa1155c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60161908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5d45b5bb82dce6fc9c4f872667cc486b1620d53b2513cab6da3ab558efb16d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 00:33:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:52 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2e77f12282fcde2c6f54d54624e8a7eef59205bf9001d755b40c1e76ea8e3238`  
		Last Modified: Tue, 04 Nov 2025 00:13:00 GMT  
		Size: 48.5 MB (48485640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c43c0422b532d4f7fd4389c7bcce79bb8e16a074d6cb2363789e53874b7bdda`  
		Last Modified: Tue, 04 Nov 2025 00:34:13 GMT  
		Size: 11.6 MB (11583123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704df9e7d2a22ca832d66d121411d6707d4ada86bc43ec80f2a555fa1d72697b`  
		Last Modified: Tue, 04 Nov 2025 00:34:10 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb42e9230b83fcf84ee0a600f12e4cd26a55217ec3de7dd0c6c0aa252771704`  
		Last Modified: Tue, 04 Nov 2025 00:34:10 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2947d93c1659c1730f645265acceb08d999ef27b66b5b7f95b9c3823fa6e88`  
		Last Modified: Tue, 04 Nov 2025 00:34:10 GMT  
		Size: 89.8 KB (89825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2f35ee62eb9b30a2febc3d098c370d6d0e830d7b7067075dd4621db81923a7`  
		Last Modified: Tue, 04 Nov 2025 00:34:10 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7d110273275d3a0b927c7c495a117dfbbbbb6b6b74e02853e56c4279a552beb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c438b5523469c0a8d160ad1023753bef5cb1b88ad7079cb2054bb8819965a85`

```dockerfile
```

-	Layers:
	-	`sha256:5954562b8f15d556fd976802885c845f79a74767c4ad3b3c218918e01ff0066a`  
		Last Modified: Tue, 04 Nov 2025 11:09:05 GMT  
		Size: 3.6 MB (3577431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:389702f3e48418c9722705566d3d18e849d8d1444d2ac1cc0091dbf590eab8a4`  
		Last Modified: Tue, 04 Nov 2025 11:09:06 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:48e130fd3a3c32aa03d0a2768b47cac94653fe00c02852bea9f52c13ba2c2fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59938919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e45f4e9facb1ca6907f02bd36142baf06f206143422bb34218818416844b338`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:32:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e6429e9e41ca9e14d8856af7a396ce50bc2b9896b4f4cd83c36fd480cd4514de`  
		Last Modified: Tue, 04 Nov 2025 00:13:31 GMT  
		Size: 48.6 MB (48586018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6ea727459d544c8517f0c8256aa0fedcebc648fb6af23c240b500415196ac`  
		Last Modified: Tue, 04 Nov 2025 01:33:08 GMT  
		Size: 11.3 MB (11259082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9af8ac4e367a30a0f111ac0e743568cdd4e5bfa5d7d54d501aca01d1a3f256`  
		Last Modified: Tue, 04 Nov 2025 01:33:07 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d30811e3c51ec44c6a3a5af602fb03cd9579ed244d07f4a14a48b57d498929`  
		Last Modified: Tue, 04 Nov 2025 01:33:07 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4881ad860dbb9016aee3cc5779892b19a2e87de7a876fd0a2cdc004d197ce1cf`  
		Last Modified: Tue, 04 Nov 2025 01:33:06 GMT  
		Size: 90.5 KB (90502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246186e66c3a37ef6fd03b09e40ddf97ef52d732a09918e66e3fda666c327633`  
		Last Modified: Tue, 04 Nov 2025 01:33:06 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aa87ac3b4e56d1bbfc35a9e5af42aa76a5a321b219af7edd9177a076ddacb30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3525b0eb3432852f9349a598e3788fce3d01885c6d090fd8d04bbfc8966b4e15`

```dockerfile
```

-	Layers:
	-	`sha256:057302c439195291f1f16521b5f2283e18bfc246a8541b2478b4450684dc0cca`  
		Last Modified: Tue, 04 Nov 2025 11:09:10 GMT  
		Size: 3.6 MB (3578307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc4152efdfe5c56849b62b14de3352fe4dc0777258fd7875529be85a2cfc9d10`  
		Last Modified: Tue, 04 Nov 2025 11:09:11 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:c3fab4fa9ef2cd84bdfd791b0cdc2d4a41c22f90d873cf4f90dea71809f0c3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61637272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf02c6051aadb5284db513d6637e4ba5b536869da5a033f89fe262ecf18ca95`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:38:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:48 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:37a822686dc57d9a439e8fe6f90a9020bbd58f684341d3cac6e3e13c68f3344e`  
		Last Modified: Tue, 04 Nov 2025 00:13:36 GMT  
		Size: 49.8 MB (49809007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892d3fb4efe2a3e137aad659f9e65e47845c46362dfc05bc72e794dc3de155ce`  
		Last Modified: Tue, 04 Nov 2025 01:39:04 GMT  
		Size: 11.7 MB (11734755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e050807cf2c0cd74803b8a7acb3e0a4faeba92aabe9414adf78a10fe10f332`  
		Last Modified: Tue, 04 Nov 2025 01:39:03 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c87cc361f91116017b998780cad41ea0d6555df2d7cc1f06ef61aa5519e9c4`  
		Last Modified: Tue, 04 Nov 2025 01:39:03 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3311ee8f1fc40c74890bd5bcac1450256d6640b97d8f38ef6cd89a603849651`  
		Last Modified: Tue, 04 Nov 2025 01:39:03 GMT  
		Size: 90.2 KB (90192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f0e7037e9d028f6faa7a5822186818bc2adca9d82fafea7ca41d47a9bf58c9`  
		Last Modified: Tue, 04 Nov 2025 01:39:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7e55f505f925899d82e80d8b2c41f2e678958bb8a00f26f80bc93f422c763675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a94c61d7822dc33f6b22948d79ce5a82743c7b588d101fdfbaf8baf9fe96c67`

```dockerfile
```

-	Layers:
	-	`sha256:4e87a0cc8fb757426409cc233a258fea1c63f39172d90e807f21e239d4204dc7`  
		Last Modified: Tue, 04 Nov 2025 11:09:15 GMT  
		Size: 3.6 MB (3575394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac7bb0e2883695d8a9dc27bf4b5f90cec47a720f2c163d3e1c5bfb39eb5c4bf`  
		Last Modified: Tue, 04 Nov 2025 11:09:16 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:58df9431de6dac5cace8bca542030e9e935a3dbdd32255741b4a4aaac8903cf9
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
$ docker pull neurodebian@sha256:e8a290457fdcb25fd97add176a89aaf05448fa1604f033e5576c669df662fc09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed0150829bee747c74417bc49a1a7ae7b385f0b3d92929c5e18981faa5aa3e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:33:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10fd61e59bab2fc94cf6c8ece723b5b01be52abf9287e8ad4a9e0325bbda9f7`  
		Last Modified: Tue, 04 Nov 2025 00:33:36 GMT  
		Size: 11.1 MB (11105086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53069f91061c1664412e1de03713f16511af4421fb26b3cf5c0834cc5e0f5956`  
		Last Modified: Tue, 04 Nov 2025 00:33:35 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0348217f8861b15dbc928cb9ec299642abee403d4f1c9cdcb54a77fb280929c`  
		Last Modified: Tue, 04 Nov 2025 00:33:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d3db1b8d2466e54a0c98cba6586dee43d21bf61cc29a2d1c31fd2eaf958935`  
		Last Modified: Tue, 04 Nov 2025 00:33:35 GMT  
		Size: 101.4 KB (101387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f2ed622434305153bd8f685c0c5c146c9084bb854c75f81b6c8c0cd8f6616eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a0c559cc49adbfeaa5e73e9f4d74b43be50b2306a5313e2cc008d4ebcc919a`

```dockerfile
```

-	Layers:
	-	`sha256:973ef639fc1a7924a61cc483a9a3391689161787e52c26c8a30c0058f8d90b7a`  
		Last Modified: Tue, 04 Nov 2025 11:09:09 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939958c021b8d787652bb54951123245124f215e3944b7525f94d08aef60a918`  
		Last Modified: Tue, 04 Nov 2025 11:09:10 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ad60d79b65d4ee219870c13df5e5115485fdf0e3a15df30a17b5baf80718b5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b05d297144c8eca61ed67371e8a89c5b7f8231da7ce81b6293eceadf964fd3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:34:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:34:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:34:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:34:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a094538342569d02b91d24b808d205b77d9c9fbf852b9fcd0ca7903bad0bf75c`  
		Last Modified: Tue, 04 Nov 2025 00:35:02 GMT  
		Size: 11.1 MB (11105999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dab4fb4d007e63ce04d999f679515216a96e37397441dbfd194691445fdc850`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab95f778dc7d395951c5fc9a7171fbcb2da9219797d0f275f3893baa6d5567`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e461a23e42babff2e43e305785bb9d0dee54499c7cf927103041a5d495519244`  
		Last Modified: Tue, 04 Nov 2025 00:35:05 GMT  
		Size: 101.1 KB (101121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:60f3bec73acc99c31f72c306ebce80ea10d53f94d0a820dcfab64f5172af7f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49be1e79f5f06e2b68c2e08d12bda1fac934f3f4cf4597c22d1a2e2f54cc3dd8`

```dockerfile
```

-	Layers:
	-	`sha256:2c77cdcd1f4462f411c49db74b7815b153f938cbf01a2225e1b8254e06291e1e`  
		Last Modified: Tue, 04 Nov 2025 11:09:15 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8a2c5b00b6acfddf7a7463416c74a5f72f5a43c484a9ba8a9b444cdea70f44`  
		Last Modified: Tue, 04 Nov 2025 11:09:16 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:bffad495fc2e10c9ffdace390212b97040d9dd6fd7a3f3bb36b7a41ccf054306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64afb566d8d555a881c704ad285707871cbed6226050af4b05f957085be2ebc2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 01:37:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:37:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:37:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:37:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e60c3e4fbf8c19df439b90c2a7f7bbd43579378a671c1afe66083570c61159f0`  
		Last Modified: Tue, 04 Nov 2025 00:13:43 GMT  
		Size: 54.7 MB (54699883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11efeb646c81ee09e63cbbd314b45549a0e2d58975c0a2a4d5cf3b176d3a053`  
		Last Modified: Tue, 04 Nov 2025 01:38:00 GMT  
		Size: 11.5 MB (11500313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f18adc21b713d03131791638b3e0e3d1df3afcc168f3a53a98d4642f066adf`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de3fdc0a50f5c4807dccba9afe1e063eee114d6f77728b1ecb923ce3a56a8cf`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349d451c4654669ab44b9d291f3e6be7912fcf85eb2300008ac567b1bf186277`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 101.3 KB (101269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1c23e7716c1929c22ce60b5a211c7486a20034efa59e7f82f8172d21695917a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da420932dd33557839e97964af02cd54f6c3ad003782ab0ffa74bc0e4a5426ca`

```dockerfile
```

-	Layers:
	-	`sha256:b6e13c2e37e1a78a39ee3d6fe22eaf77db826b0afa8e4741f6f1d2c1a68b2547`  
		Last Modified: Tue, 04 Nov 2025 11:09:20 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e5502ab97137ddc1c1d3d9452d22a75de66d48c5b42f805ec6607488ec4efb1`  
		Last Modified: Tue, 04 Nov 2025 11:09:20 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:45c9f19db7fefcd0d7b140ef5c56f23244818d935d631503cbf616bc47053c6d
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
$ docker pull neurodebian@sha256:a45dd0e3386ce95f44f5c4926dd265d443d3d630f4edcc26b882ad3d51dd4e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce557f76a8782cb27f6a937c46475ed73e4bd342c90ee38a0abf344621bcadb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:33:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627c13d45db1bc3627114590a9a572072f259a283e073fabec89b6927460b0e6`  
		Last Modified: Tue, 04 Nov 2025 00:33:47 GMT  
		Size: 11.1 MB (11105106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08637bae51a885f58cd136663fc6922c49e2424cfcea177ea75f7040bdcdef0`  
		Last Modified: Tue, 04 Nov 2025 00:33:46 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace19d11403316e09784bdc28075bf7d7cbfa95b8f520261d963cffa2a418c38`  
		Last Modified: Tue, 04 Nov 2025 00:33:46 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421f1ebf0d0bf7053cbb682ae089001c7bfade44aa1367c2d04be6247af8dd1a`  
		Last Modified: Tue, 04 Nov 2025 00:33:46 GMT  
		Size: 101.4 KB (101402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfaaf8e2a3d6417a25962517c3ecc4093fcc632c6e230edf8be22f23c41dd13`  
		Last Modified: Tue, 04 Nov 2025 00:33:46 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c4fb7ac3fce0ab555c787455ff2a0ec32e5bb0033e6d9980618ff77152743553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc6a968806e1b986e719546bbcdfc39b1421bcf3527b752fba92ad026ecce8c`

```dockerfile
```

-	Layers:
	-	`sha256:18a19dfe3cfac69d2b3ca907adcf30844b15bdfb17df6270677fad851c8d9d61`  
		Last Modified: Tue, 04 Nov 2025 11:08:07 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6273ed50baba0b581f8e5e9c051fb9c6b3c8961818273cdf5f946541d0cc0c27`  
		Last Modified: Tue, 04 Nov 2025 11:08:08 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:57ae5b2253217ac9ae33b55ab55c5360788cc8f216ffd923363708f83617ef95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb427c73de74a9e991f127a33eb1394dba97a3ee16f787a74ada4d217fc0569`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:34:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:34:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:34:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:34:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:34:50 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb8dca10b60e4cad77c222af29c649ff3a5126ea283485ad6c537bae4008456`  
		Last Modified: Tue, 04 Nov 2025 00:35:06 GMT  
		Size: 11.1 MB (11106030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de57a9ad3fe875764e4fbd92ca4e298f4eefbf492ee92887c4fbde5fca730a23`  
		Last Modified: Tue, 04 Nov 2025 00:35:05 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3b09e452de82ebe7de58f5c3ee447695ea6164a28676cfaa3c2725f63a00f6`  
		Last Modified: Tue, 04 Nov 2025 00:35:05 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a00e295f476d7e6317fe37274cd8cc9211229b98fbcc9a872927fb46dec83be`  
		Last Modified: Tue, 04 Nov 2025 00:35:05 GMT  
		Size: 101.1 KB (101115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c366338618a32829891f215d4a2762da10ce1b2d40b4b4582ccabce53735ff6`  
		Last Modified: Tue, 04 Nov 2025 00:35:05 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:271ebb53e8cdad38f8530e5ba91b09e5f4e8f445217eca3b20a8d6201ae9991c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95e8040aadbb5156ea4fe0706203af6f6335ef3922ebfd647454ae60508eefb9`

```dockerfile
```

-	Layers:
	-	`sha256:52a9f7d2fc29ae8cacd332b69f866c721505869a24f567102f48b360f67f9284`  
		Last Modified: Tue, 04 Nov 2025 11:08:15 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfd52c9caf33c39a8a4d52888271a2da0f800be52d634639efcd0ecf36ebbd0`  
		Last Modified: Tue, 04 Nov 2025 11:08:15 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b70e05340f908361cfcb14504eb38d348b67f1385addcb3b71180869cb279b0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66304014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b966eb9bcd46c8924e332ce6d8bb2600aef8489ff46439c0b5a74a67130506b5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 01:37:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:37:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:37:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:37:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:37:59 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e60c3e4fbf8c19df439b90c2a7f7bbd43579378a671c1afe66083570c61159f0`  
		Last Modified: Tue, 04 Nov 2025 00:13:43 GMT  
		Size: 54.7 MB (54699883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11efeb646c81ee09e63cbbd314b45549a0e2d58975c0a2a4d5cf3b176d3a053`  
		Last Modified: Tue, 04 Nov 2025 01:38:00 GMT  
		Size: 11.5 MB (11500313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f18adc21b713d03131791638b3e0e3d1df3afcc168f3a53a98d4642f066adf`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de3fdc0a50f5c4807dccba9afe1e063eee114d6f77728b1ecb923ce3a56a8cf`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349d451c4654669ab44b9d291f3e6be7912fcf85eb2300008ac567b1bf186277`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 101.3 KB (101269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b45ea2828a62da8544d87d0ae49408612b86bc5667196c23cd3008df0aeee5`  
		Last Modified: Tue, 04 Nov 2025 01:38:10 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:995258b08a64bb138022f1c4946d369956d5212553fee8721e22bbce4ec305a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07469cbbf480035470d48b72db1f398d6c102c390ce197dc9fdbd0410fd4d5fa`

```dockerfile
```

-	Layers:
	-	`sha256:75b921e38de9846f770e87307dd1af17529c86aa476baa487b8a92f591c72907`  
		Last Modified: Tue, 04 Nov 2025 11:08:19 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c29747f78e39dd80695f1395d1577f9ca3c0cd4fbb0913f7985cda101a09499`  
		Last Modified: Tue, 04 Nov 2025 11:08:20 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:ec94bf7c865f976be23788ed104ddcba722d2b21b22964883302f3db52f334ee
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
$ docker pull neurodebian@sha256:2b8b12cb107a339fae3a8c5c4f8406b159a03f22fa0ad6d623bd16b49be537df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45016e4b694e24cbc231ee1f05accbb9afb5360d114865d01f0244908c102a2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:33:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d27a9437dd9fc4b0efd290a2bcb6346624c2dd6c60cdc5371306924ff363e6`  
		Last Modified: Tue, 04 Nov 2025 00:33:42 GMT  
		Size: 11.3 MB (11269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663c2d2d90bc6bcc23bd09c4c13c62c2b13f33aa7990a8367683297aca575fa0`  
		Last Modified: Tue, 04 Nov 2025 00:33:41 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae69ff1ea04b61ba0f99224ac7eecbfc020816dc408515a1c4f2687556492e3`  
		Last Modified: Tue, 04 Nov 2025 00:33:41 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103a4eb19871be6279fea378987e872d76dfd7c954a44f4eeaccbf2731d02be1`  
		Last Modified: Tue, 04 Nov 2025 00:33:41 GMT  
		Size: 93.4 KB (93379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4958673bc05f2ecf24b3c3560203043ca1923fec6fbb7b3db2c053d9dd09dbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ddc6fe171c2cafc24b32616ca557363933035f42ff5885d8bafd1af458162f`

```dockerfile
```

-	Layers:
	-	`sha256:62ec6d7f7cd447db60df7966ba8b3ab7b7bcfb5d1bfb634ef231de15d7c9c7fa`  
		Last Modified: Tue, 04 Nov 2025 11:07:24 GMT  
		Size: 4.1 MB (4075236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:067da4b2ed0e3bdb23696defb111cddb528d18310e11a0fce4d129f8305c44c8`  
		Last Modified: Tue, 04 Nov 2025 11:07:25 GMT  
		Size: 14.0 KB (13964 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2ebd3557ce31a6045fd165930762376e37228a68ddbb0cd51d352bf839927a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feed7c361f6454d2ebdca20d62eaa0208f7d77fdfbd2113e9ef339afd892a74a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:35:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:35:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:35:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:35:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a362910b4ff4e83d0dc3b8613b0eb94658f52d229b4411d4f0253056bb192017`  
		Last Modified: Tue, 04 Nov 2025 00:35:27 GMT  
		Size: 11.3 MB (11253369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d168b3317492e8db43d805d74c95ede9223b4334101713d7afe9e3c3cc93f27`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2ef3a583754a79f1f722a9b9976c108f72ba8983ec4bb24bb99010aafd6041`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edecae1bdd0f4220f6dcd6a59736227d042b109c1ecb4f47723783982a721431`  
		Last Modified: Tue, 04 Nov 2025 00:35:26 GMT  
		Size: 93.5 KB (93501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:75feec74e5eac034fa9504f907235aece10e78c0f0ae41090a321ae023ec50fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82ee58d1c3a9e528dee7608a6c72d3042a584b594500f97872e8eec7b2b19ab`

```dockerfile
```

-	Layers:
	-	`sha256:619ddbb9c8584f00313f967f0c11265fe7dcd92403c29673bae6cc5672555029`  
		Last Modified: Tue, 04 Nov 2025 11:07:29 GMT  
		Size: 4.1 MB (4075478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a3294616fef78ed15fd035f53d08d63dc5079f3496cea9faad865804a8324b`  
		Last Modified: Tue, 04 Nov 2025 11:07:30 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:84ec72fe297f615978027618d7a29b7d4fdc7bdf614f6385c71871a006f781df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50834346a5bc41c0b659202fcd7fb0032352323cc91b14829b1accb034ef8750`
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

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5f053bcc51d8e520d03d28889ec38e3fa1eb698e639b24714846c4efd00d88bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aeb4189f2d1c01f722245843d4d06eb85d1f24ba7af1237d67e43be1890b6ea`

```dockerfile
```

-	Layers:
	-	`sha256:64c060ddfa2a6c4b6b512af8c7896620d501066922edecfb857aef9154314d31`  
		Last Modified: Tue, 04 Nov 2025 11:07:34 GMT  
		Size: 4.1 MB (4073204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:def7727632c070776a3a72db4cf217f26b8e0eefb659bbe3bc34da0dbbc5ef53`  
		Last Modified: Tue, 04 Nov 2025 11:07:42 GMT  
		Size: 13.9 KB (13935 bytes)  
		MIME: application/vnd.in-toto+json

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

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:c2360b59f5cd07c356ea19ed3cdc88006759a1c0012203558eabacf878b94db7
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
$ docker pull neurodebian@sha256:cc62f8a2b909a4a621f695fb23ddfd2f55abe99c1107ea422ddbc9493ed29c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59668516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58c9d81054ebb46f7a713bc03b050382ac159d061b22d7c255322f1b7f34f30`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:17:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:17:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 04:17:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 04:17:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a97f52bf44b7c35c2c3dde0b10f67fac3048c89ac6322097bbe246677a0d380`  
		Last Modified: Tue, 04 Nov 2025 04:17:37 GMT  
		Size: 10.3 MB (10289768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eeeebbd965732bf90942a1ebed2be9c5db1bfbae37f79d18df48b59aca1094e`  
		Last Modified: Tue, 04 Nov 2025 04:17:36 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1715ac06925051c0dc44b303a59854227464617274e4399c7c3f7ed42d3b728`  
		Last Modified: Tue, 04 Nov 2025 04:17:36 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c90e3669c8b11bf12b32885c25bb7005fc7657659840b3143510e4019e3f87`  
		Last Modified: Tue, 04 Nov 2025 04:17:37 GMT  
		Size: 90.2 KB (90219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:36e5e12cc006b9c643190e4e94c3c9be24cdbc7ab1ec5ce2a37eddbf5d3ba551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499dc65ca82ef280131d7296a24026b6d9c9a045d868f46c496b60250fd68b51`

```dockerfile
```

-	Layers:
	-	`sha256:9693e52244e9d6cb3776573b396e8ad9c1541b70da98119a48d0f73cebb9b960`  
		Last Modified: Tue, 04 Nov 2025 11:08:43 GMT  
		Size: 3.6 MB (3613035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc75a15b38b24dca33cd177d886bd1cdc06cc59a5a50cded16bab45890c0f3f3`  
		Last Modified: Tue, 04 Nov 2025 11:08:44 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e88a59a8eb59c283f7ceee4aa5edff9e76424daabdd909cbcfd68c99440707bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a592f978047a6bc3cfa14fa679b85d9abaf32c5c31f72dce1954eed1d6b74070`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:32:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f261ede3c228ffdcf1af64259b67759d9a002314294a6000401de78dec7fb6`  
		Last Modified: Tue, 04 Nov 2025 01:32:37 GMT  
		Size: 10.1 MB (10073302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6646aea08c3732bf73a2e6f46ff98544770e90860b4a0866fccca039070f3971`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44013910ff33d14f15aaed9be503bd613a4c1ecf18b98392429751d3e1fc2010`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7fc94592c535b9c56ba976c47ab0d65065ab60188dfa41ea53a0384e5650fe`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 90.9 KB (90885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:67a7caeac0b108a3854951a85b61cea2cbf3694ba8b127f21abb057acc37ade8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748332e676c636a5998508a3d059c676a2b871719d4db0d6cb4ea97debe4bd2e`

```dockerfile
```

-	Layers:
	-	`sha256:2b1e3c4221c421d4c252a44448f8148f38f4bdac55bd98dbbf9db0660257507a`  
		Last Modified: Tue, 04 Nov 2025 11:08:48 GMT  
		Size: 3.6 MB (3614562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74244bc19fbb24f3845e801cde56e470597db35a2cee721033aa920b9e5a27f2`  
		Last Modified: Tue, 04 Nov 2025 11:08:49 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:f1f7bf3923b89f2692a55d2ef2edee2bd82dbdc0d1d0b02b9b061c57f1e36040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61357599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db97c9f327dffd9682c36f7aea893d03e88502d815f95f1d27f8b9709dd0e9e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:38:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:933c2eb03a495d1bdbab772ff092366c6df6bb75cafd8749623e94908401abca`  
		Last Modified: Tue, 04 Nov 2025 00:13:58 GMT  
		Size: 50.8 MB (50801238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2c10dd39d3ea1b7fcb9ac6e3da6cd2c85fa478453556608f507a3d8d1f3de8`  
		Last Modified: Tue, 04 Nov 2025 01:38:36 GMT  
		Size: 10.5 MB (10462886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9376d28a0149ab43591656335468744f02197d038449d77f9079e5468990880e`  
		Last Modified: Tue, 04 Nov 2025 01:38:35 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca789b0bcf3530d0cfe0bec7d39ca51f45bcff2c8d4b4b423d21a5202dba138`  
		Last Modified: Tue, 04 Nov 2025 01:38:35 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8321b60075f8d7fed5d7ca2c9196cdb5c999eed080f68586d1e00a229d684962`  
		Last Modified: Tue, 04 Nov 2025 01:38:35 GMT  
		Size: 90.6 KB (90574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cda8f897e235f9ee79691e1bc08a3297a011b8bc61f86a081bf28301e8682a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c691882c13ae6f1a1774af6d1a3247c9e387f56355f7cb056f38ff5955ad54`

```dockerfile
```

-	Layers:
	-	`sha256:166ffe9a4c84e31de85225508329baa1a1ba0f7231e235931fc77f822846d3db`  
		Last Modified: Tue, 04 Nov 2025 11:08:53 GMT  
		Size: 3.6 MB (3610984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dca0d5a4a061e7f9961f25762a0315f1d2bbbfb9720f451af5e672c5ffba9d26`  
		Last Modified: Tue, 04 Nov 2025 11:08:53 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:054cb83bc13a514b14b0d6d2127811bf8c518e556fd6edf1c54b48aefeaff471
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
$ docker pull neurodebian@sha256:a84e7c70d72128f0303fdb503e24ecd7c72e91d03ce7d2d107f71fd126955cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59669100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ae6b2236202b62a987ca7ce3e3a621ebf3b0ea0f954e6b7b038687bb9f71ab`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:17:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:17:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 04:17:23 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 04:17:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:17:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23386e12d6e309376ac1a14efa640269690dc204b17984b14064c2fd2f49098d`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 10.3 MB (10289939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4a65b6a6351a097123b770a2e0e8e7d5c03b57aa5a1dad26e1c2eadaadfd28`  
		Last Modified: Tue, 04 Nov 2025 04:17:39 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52742b84510725699f7a178b63e604e0d0891893d1f2eb344188531d8636f0e1`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aee8c1d05553c1777be79055a18fea90ee2b8ea9411f6c738c5c18eba8d1c6`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 90.2 KB (90186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2b299738c4e4019fbb06b267440b617ca810b6d56b21bc0afdd3695d852ada`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0089444d554e5cae9f22a559edef3bfd16e1bd0b68860b6c214e2428014781d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba98d48bfb433fb8f9a10e0d06f0d683a5c4944286fdaf551bce2c5892d7022`

```dockerfile
```

-	Layers:
	-	`sha256:3c66055059d16bf03b067f48cf3c4b38abaf5be7f3bd7af8dfaf7d94c8708e01`  
		Last Modified: Tue, 04 Nov 2025 11:09:30 GMT  
		Size: 3.6 MB (3613075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64a75afe777c95a9303af2be30b3244166f9507b5d307bc436cd2c311c33b53`  
		Last Modified: Tue, 04 Nov 2025 11:09:31 GMT  
		Size: 16.3 KB (16280 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1529a63d3b1fd5b20e69752735685aed7551980815e4f5ba9dfeb57bf08a98dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59818048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede29356c99f4ad500f6f92d01d99c80598e7a0ab06e0cba76bb427bec98bcdd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:32:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172872c0ee5e3387027dd024c77e0a566ab9e979918d5d1ae3a862912f9819cb`  
		Last Modified: Tue, 04 Nov 2025 01:32:37 GMT  
		Size: 10.1 MB (10073407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd94c5bde5357bba8d2d736f7e486405a517a770df0fbf2434fff09e3cdfd82`  
		Last Modified: Tue, 04 Nov 2025 01:32:36 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3686e47e17b33cbec471ea4f8d20ee610283524c8e381b60bbe0bca643d3cb`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0201931aec9ab3ac74ff7c1fcb5bbda1b95323d45a16ba0594b8586855f134`  
		Last Modified: Tue, 04 Nov 2025 01:32:36 GMT  
		Size: 90.9 KB (90860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda921f974a2bbf05547e240c45b797d09307a80d64747669b300890b4877699`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:171c082cd86f6d465311384dc89b6f8caef5ba756bac4b22acc5740480c28923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bca970acfe0d4594fdb6fa5375fc79bd72f1c0309d3fcd6644884295e7a995`

```dockerfile
```

-	Layers:
	-	`sha256:e6a4a640a7d1de22f588ad1235c812b9907faedeac55c9b05d4fc71a53fe4317`  
		Last Modified: Tue, 04 Nov 2025 11:09:53 GMT  
		Size: 3.6 MB (3614602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11690b726c377ad7c6177f469ec7805bdb379cb0e37fd6d69b8c57d618893f46`  
		Last Modified: Tue, 04 Nov 2025 11:09:53 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:5771d15f06fa62ffa39ee92437de3260e58824c9c3aca71b930f2340dd55319c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61357929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae41e42556a48153e417d850113110e79e617019f105a3699f765baf91edbacc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:38:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:933c2eb03a495d1bdbab772ff092366c6df6bb75cafd8749623e94908401abca`  
		Last Modified: Tue, 04 Nov 2025 00:13:58 GMT  
		Size: 50.8 MB (50801238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c3eaf959f47b3c81adaab22c02b91552da31d1998da6c88911ad6288b7a9fb`  
		Last Modified: Tue, 04 Nov 2025 01:38:50 GMT  
		Size: 10.5 MB (10462757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e9ef740b4bb48f2974e682a417cb34fceb185aca217d1c2c7f6227a748dd40`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242bf4e4c9cf11d3df4c63f4db58331b50dfdde7542f70fffe6271a6cef67b5c`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7804e0ac9d5bfb67777d18126743dfa3501a6cab30e2779e9c1e882d3931d3b`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 90.6 KB (90584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f31b454367cf57f9fdcbbcbabe35b3a537175a9cbf95e0455aa5c68268299`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fadfe623ab9931f7482ec50383c61bca36e19d1881f7b599d5a47feb0ee6dd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e8ea8d062af83ff955f51cd8b7f77e408cb8628ee432dade259fd59a85c1b7`

```dockerfile
```

-	Layers:
	-	`sha256:088a395d40071397cf8e0032ab14cbcabec0416a8a0a34130b1268e1fe736e89`  
		Last Modified: Tue, 04 Nov 2025 22:51:34 GMT  
		Size: 3.6 MB (3611024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc01ac211e92ee4d0d4707e08a6fb4c64315bf3561a027a8594a15e46d12b72`  
		Last Modified: Tue, 04 Nov 2025 22:51:35 GMT  
		Size: 16.2 KB (16246 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:b0fa219b2f2b0e1ef0ebc2ff181ea60aae3e67618dec06fd14784d22c9a9e076
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
$ docker pull neurodebian@sha256:a95a11b0f551d6c581069697c60e42099b556195747382af9b33a2a1e8ce93f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60157262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f25047aef6c2ed146b0d840b041672aafe2ed858eac68e294f3fc82a423e757`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 00:33:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:186ca733686ffcaca03fdc512b51c9498f39b93235775cf08154b1ff0b143901`  
		Last Modified: Tue, 04 Nov 2025 00:12:56 GMT  
		Size: 48.5 MB (48481364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49a1e0dc0b376f0cc4e1d2e12f628424d11aef8cc2b87d1861a241e7b56be80`  
		Last Modified: Tue, 04 Nov 2025 00:34:08 GMT  
		Size: 11.6 MB (11583245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e442443001bb507838d0ace541f13041b1411d5710f72f823ddc28e99d3f80`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631c24460ba15377fa27b5a824758985f589cc6a8e3d9ceb6081711d0313984c`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511bd2e44a8ef113bd55092f7a48daf15c7c5e2d7bddd9c74aff0b231be4e6f5`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 89.8 KB (89752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8159857513732c8d6ec476797d1e7a3eef95188b2f790e79a3bfd35e97222999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93865f95e0647d34d373da23c19eb0a62c166b34d1df3251cd841853a38b981f`

```dockerfile
```

-	Layers:
	-	`sha256:5af3592e7343b7b1c38b837a1377c054ee4e28a40b2baf57476265e9d958e93b`  
		Last Modified: Tue, 04 Nov 2025 11:08:17 GMT  
		Size: 3.6 MB (3577405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ac2d7114b70f666f54881e4a50c6b5c386f5e319cf9276fa4e75dafc807c90`  
		Last Modified: Tue, 04 Nov 2025 11:08:18 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4a1ab300e12ac91c2e44ad39a108a5bb56a3e906ecf1787492a800e49671056a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59936207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c3dba418be4e19359f1b1f1eb385c8c079ccd6229a6cbf94f21c326c33ff0f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:32:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:52d2706ca00f3431b3c37b306b3eb6cc4989781e31180bfdf93c4dd4108e1e3c`  
		Last Modified: Tue, 04 Nov 2025 00:13:40 GMT  
		Size: 48.6 MB (48583638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de1bec0d095ae1671e8e93b5fd0c690333dc3cec029fee404c8ff0ffd5d47fc`  
		Last Modified: Tue, 04 Nov 2025 01:32:59 GMT  
		Size: 11.3 MB (11259161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9e5a0ec4a83df31c8df66ded76dd9f5aaea5fcc1317ed2a8b9dd1503fbf203`  
		Last Modified: Tue, 04 Nov 2025 01:32:58 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ded840b50c25703b8cedff47124e880b4c80660332cde3bd23f80cfbc0cbd6`  
		Last Modified: Tue, 04 Nov 2025 01:32:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d602e5443e53d9509a8ef31c9c5f0b5a2a09fdd1fde958bb31acffa342d92c29`  
		Last Modified: Tue, 04 Nov 2025 01:32:59 GMT  
		Size: 90.5 KB (90502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:682a6d16a7ae5f71baffd961e48cf81d51aba52c6b06868e211e1088afa97f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba6e63f0527eb6106a462f2be1815978786ac89575942a8b59bf6211fa5d013`

```dockerfile
```

-	Layers:
	-	`sha256:650e9ae2490715384b193964e2a59ed8052365d101979d7893dda65ced07355c`  
		Last Modified: Tue, 04 Nov 2025 11:08:22 GMT  
		Size: 3.6 MB (3578281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5bbc6dac0e2c65a14b10e33477ca40edf0246b43d3b141e56450f889368557`  
		Last Modified: Tue, 04 Nov 2025 11:08:23 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; 386

```console
$ docker pull neurodebian@sha256:7462d5da772e47bc5cfc2c6b321eff341fee7f8d8ed083e68bb4e6258a89b660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61637327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5ebe96ca47d62929b0f9496e4a90f8ce2a9a78c613cae09a60d476ca7eca4b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:38:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bd86ecb6d3ac97cad4df6e0aeedefdf1790afb18f99112bd09ea68844e318978`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 49.8 MB (49809500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9d5279884080b3a9cc53b22c9970ff61131076fa40ed02a21823c040bc3f88`  
		Last Modified: Tue, 04 Nov 2025 01:38:53 GMT  
		Size: 11.7 MB (11734742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea45ef2b067c6f619d817ae565ce3ae8487840b2727b980c0ac37f18cb60a7d6`  
		Last Modified: Tue, 04 Nov 2025 01:38:52 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354665d7d7917d747ec260c4a0e42a1cdf7ced8f50f34d8515da774536057834`  
		Last Modified: Tue, 04 Nov 2025 01:38:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5fdc3252598c0dc204c07be13ef748ce0649e55a32aa7459d22b41f1a045e9`  
		Last Modified: Tue, 04 Nov 2025 01:38:52 GMT  
		Size: 90.2 KB (90180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d6c19633e7dccb24a6f423af4036e5c7dc575df68786e1782a2eaaa76b2fa17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da159b3b8e0dcdad52660ec976ef25d34304e4e14a84e443061cb6d6a9c35926`

```dockerfile
```

-	Layers:
	-	`sha256:d508ed6522322ff57ccb321b54a299fe8ca0df639f7366551a61a05657dc3119`  
		Last Modified: Tue, 04 Nov 2025 11:08:26 GMT  
		Size: 3.6 MB (3575368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb005d7845f49e8616299d2fcf67924720febfa2686753c18f7ac4e8677f8ca`  
		Last Modified: Tue, 04 Nov 2025 11:08:27 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:384828113ce018b109587fdbd0eed3455ed127d24c20f4cd7b567279f645e467
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
$ docker pull neurodebian@sha256:70189282e254301c784925ce371e2d46b8803e68c3bf317555ba516f7f30faf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60157762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc773844b4e251440616e054ab18d55d4fe865140e940d5f110fc8e0a61fd01d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 00:33:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:50 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:186ca733686ffcaca03fdc512b51c9498f39b93235775cf08154b1ff0b143901`  
		Last Modified: Tue, 04 Nov 2025 00:12:56 GMT  
		Size: 48.5 MB (48481364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2ed7e1eb66e73be7a81904f625e8af8e27bdbcb556d412220b4dd47da85a13`  
		Last Modified: Tue, 04 Nov 2025 00:34:04 GMT  
		Size: 11.6 MB (11583251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a2103db929aa61129b750d42223222a7b4692b76c2285cf0445cdad7ce42d2`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af62a6155153d6cdb65922ed9f2501a9399acd5dc27bd108f4abbeaf8a7ce14`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deca5aeb491ce74b8f40489e25bd1cb7d95e88698917d60cd807d9a6c68db73d`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 89.8 KB (89793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d896b07b7e37a7203598f231523daf17e786b9ab694595a4aff3f90eacaab6a7`  
		Last Modified: Tue, 04 Nov 2025 00:34:04 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bf76392847b143d89f63d547ccd03be8ce62c9af5bb9f0820a2cb949ff456788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfb5753a33312ff7862b3b9d32e1577419c78d795b37b5b5e3ab360f8743e80`

```dockerfile
```

-	Layers:
	-	`sha256:fb10025220538f30c02045c8f5d88fded55d77d4fdd339040983116e4d90af1d`  
		Last Modified: Tue, 04 Nov 2025 11:08:30 GMT  
		Size: 3.6 MB (3577441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b43e03910d7abc9bade8c2dd90b348ebcaa7ff7efcbb066f238608850dbf151`  
		Last Modified: Tue, 04 Nov 2025 11:08:31 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bc8ce6ed3e3c776152f99cb1104daea078494d0b923198a6c142487c62eace11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59936579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c69131f270dca8fcbfd32858708e9d91d5ac087ac5e89454675950b29f061c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:32:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:52d2706ca00f3431b3c37b306b3eb6cc4989781e31180bfdf93c4dd4108e1e3c`  
		Last Modified: Tue, 04 Nov 2025 00:13:40 GMT  
		Size: 48.6 MB (48583638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cd34f0ce98712d55741951246c28dc8f4fb5749fe6f009be810a15bc39e7c7`  
		Last Modified: Tue, 04 Nov 2025 01:32:56 GMT  
		Size: 11.3 MB (11259085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37370e1cb03e1aec0bca31b7c63d049563f347f1cbafba5f70d06d99e86b5dbe`  
		Last Modified: Tue, 04 Nov 2025 01:32:56 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17eba42e5d505fc3a5d3fd9987372e50964fc3542c2cdf1d4a193649b6d79dc7`  
		Last Modified: Tue, 04 Nov 2025 01:32:55 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b804357151b1a683a4a79a6e6c1980ecfd72123c62be18c932e14d3bd0684a`  
		Last Modified: Tue, 04 Nov 2025 01:32:55 GMT  
		Size: 90.5 KB (90502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897b8e80528e0ef186efb3269fdf4ee30234c872372be7fa36d91d07b30d7ca`  
		Last Modified: Tue, 04 Nov 2025 01:32:55 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:47773bc2f2c9cf5068f8d72bdcd2fdb869f026c1927d9f695c39218b8917e292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767d0a3d4a306c0a128156ad9700a3ad79383bdacbd5764b54d4bfa729dd9191`

```dockerfile
```

-	Layers:
	-	`sha256:b40777566d143b66e58a9a658fe6e101d5e37c7b56860fb660b7f69556471886`  
		Last Modified: Tue, 04 Nov 2025 11:08:35 GMT  
		Size: 3.6 MB (3578317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30961153f32eea93b5027e2061824753dd9f37ace2199e650c0e21c4c49e8c64`  
		Last Modified: Tue, 04 Nov 2025 11:08:37 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:63d7073757f8af8afe32eadcc816f9af8a1235863947854f3cec2f8cf7759d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61637813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f76ec57eee1b56c541332f031778cdd216e88f6085d0c30b6e631b2600449bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:38:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bd86ecb6d3ac97cad4df6e0aeedefdf1790afb18f99112bd09ea68844e318978`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 49.8 MB (49809500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3fb4596c99fe5762ade8fb8b49b83646c2974bd279b25a5242783b6be97fa4`  
		Last Modified: Tue, 04 Nov 2025 01:38:58 GMT  
		Size: 11.7 MB (11734764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a42eb16fe9637037091596145b07dbd6c26d5a89f0f60752ad47e9c6a4cc9`  
		Last Modified: Tue, 04 Nov 2025 01:38:58 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c465762ff747abccb8f26f7940310315ad22c0fc83643d9a17eb2e44999632`  
		Last Modified: Tue, 04 Nov 2025 01:38:58 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a908abcd3ddc1a45d84a8a1ee749cc706039c754ffc9b248a425d41c76ae1e`  
		Last Modified: Tue, 04 Nov 2025 01:38:57 GMT  
		Size: 90.2 KB (90198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1814fb1bc1df679152afd6fd24901df7384befe85816a664b3bda4f764d0fe97`  
		Last Modified: Tue, 04 Nov 2025 01:38:58 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c777d330b6ca4603bc533b8b59a2d655e01875d5366fb0e49a18efb61c8a4223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caaf32981d88398acb2c6917a96cc42b7e3624895dc4ae282c20da5a261302cb`

```dockerfile
```

-	Layers:
	-	`sha256:f22f145d2d10c0e5d330f0abab2f7ca18e0529f5bb7a1ef06a8b9c9b96ceb661`  
		Last Modified: Tue, 04 Nov 2025 11:08:41 GMT  
		Size: 3.6 MB (3575404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c492288d345222064869611f8283ff114449640050c12d23dcde88c37772b53`  
		Last Modified: Tue, 04 Nov 2025 11:08:42 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:0e98bbc3daae66df44ae11a5588f2309b4d0b0a3d5759a236557a26319c2c5b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:e6772d070a574f00e1ad07efb0f799b7e9d9020fccf9887c7f6378c50bdbe816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d6aeb77e4a5a773edcad5fc10b5e08d8f387161a9b7b5d93e1cb1aac4e3735`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3881e591a9050bd6250b7975f2a62d69ce9d4bc181a569e43d583973bfffafd6`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 3.6 MB (3625726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7763c1732252c316b49e1a5ebe3d01e0ad636198993b3e20e7267f9fe62d4283`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59987cb0b364dad0627b12e7ef72104aea08b23fff39930f94dac5b79cf2585`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91714d8e9de2a6eab65bf534a21daeac5f710d6f823714736754481479f25eb`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 111.3 KB (111253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74faf561f221e4ff0722a9a6a5469d286311b0d29d710a50c1c2f2d408089335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5093bdb0233d5e701687d2c9157af64b57724e81b512be660289bb7a4c8f7216`

```dockerfile
```

-	Layers:
	-	`sha256:288a50939bde1611937533ae039c8544b98d95d75331e8bde2456927a7ddea17`  
		Last Modified: Fri, 14 Nov 2025 02:07:40 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941444796f9904d69ff28378466addce903b01de5df5c0c291ea8d117c6aff74`  
		Last Modified: Fri, 14 Nov 2025 02:07:41 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:09ed49f28825e5330d749e8aa583e2f0c2c88ace7f935f79fd1b4ee7cfd6502a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31094789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170be1c0c9e62fba389535f45096cb097ffcd73e82e10f8e5f2bbeb7101e7716`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:30:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:30:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:30:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:30:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4fc061e7db4abc03b992399d4d51a6e96a401904e29c8c7cfff6c2b0ef4cbc`  
		Last Modified: Thu, 13 Nov 2025 23:31:03 GMT  
		Size: 3.6 MB (3598146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e356cef2bd87e42a124fc4d5e82057772ca5cf202c6c194f6884f04283430a`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7f921b9372d265e8d3805815b0e98436f5f4b92fc0dae86070b7f4f269f992`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562a8628e6dc417f84896302f26a4b6c43f921ca7ce9b73b785936f7e5d51be2`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 110.6 KB (110588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4d3a9691d374823b1b504cf09f6f82049355ef10aa41d07d3be46ed00124eda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb368a6d54f82c2cad7c303b49a01491c62b68e3a47065952793b1df828ae`

```dockerfile
```

-	Layers:
	-	`sha256:c8a0004225abd4f8c618461be1e72c1192172f7ccfd4fa7f0839dbdc35d24f43`  
		Last Modified: Fri, 14 Nov 2025 02:07:45 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200a3136b60277a7c0dac564342f17944ff690ca89305553d8bd0bcd74108f3a`  
		Last Modified: Fri, 14 Nov 2025 02:07:46 GMT  
		Size: 14.1 KB (14056 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:120b8715dd3a26a2af4049512591dcbb112d36e4accff9d7fded93e27ce47062
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ef9dcfb5426525d36ca828760110823e06e065cca0c4ac0682d0a506e9cf12e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33276245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abbe750921d6da2c2bf91fa655875aa86d26da7d2c93cd08dc4d8b4f91445af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3881e591a9050bd6250b7975f2a62d69ce9d4bc181a569e43d583973bfffafd6`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 3.6 MB (3625726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7763c1732252c316b49e1a5ebe3d01e0ad636198993b3e20e7267f9fe62d4283`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59987cb0b364dad0627b12e7ef72104aea08b23fff39930f94dac5b79cf2585`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91714d8e9de2a6eab65bf534a21daeac5f710d6f823714736754481479f25eb`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 111.3 KB (111253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87663c843a43743cb4efbfd154e030c6591b4085d0c1d047a156158b9c47142a`  
		Last Modified: Thu, 13 Nov 2025 23:31:58 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8b9b5e291adc948bf145496030828a9a408c3399355380347b0ff72c16e2a880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970a1d784b637f4a06999658bbd7cfd5f71517ef14610d1888be4fc2d5614399`

```dockerfile
```

-	Layers:
	-	`sha256:19ad39194fba9b75b47c96c260e5431b390f0c1f40747e8857c995d53dd228f0`  
		Last Modified: Fri, 14 Nov 2025 02:07:48 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd46be2a48617b0b0891f5fe27958f8e2350a649da215ce9a4995e5a9a62d43d`  
		Last Modified: Fri, 14 Nov 2025 02:07:48 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8c05f54ab64c544f5b1833f0d31ef94804c914c6debd693acfce0dc0320660cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31095110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2b987bf931381f750375f7be732736b38d67dd928c373fb3ac7f7703364fd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608dccde847e272476e52044e62fdf40902fdf981eba3f9e853d9bb36c3ebdf5`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 3.6 MB (3598157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff367c25857e7c190e4c69803b560c6e428a2f6fdcdef7291ed9c54595fd3a7`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d785e7ece3388bd939c0607e15ed02803f8e48b590bbf43d7b628f2275ed86`  
		Last Modified: Thu, 13 Nov 2025 23:31:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411f09f71214f6303934a66000e111fee3918961b6f6726ed9b784feeceb7fcf`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 110.6 KB (110611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa2aa73e9807dfaff0d65e73fea59b7275dac6754311bac380e78c75cf4c922`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f02cab47a327aef8e9eea19cc7a8da708ad76b7fd1cee2ccdc47f302f2cade08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5d2870c8ff27e82579456117c17077c9ecc56cf9812adeb91b20dcd8fdb489`

```dockerfile
```

-	Layers:
	-	`sha256:196e2a812f54eccdc16bfcfe68a337ef2397641ccf3672d5f6846a2c19b4a34d`  
		Last Modified: Fri, 14 Nov 2025 02:07:52 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be4dac85cb072f2caede51d4767494f8e063e10991e49a2febf5e030defd53e2`  
		Last Modified: Fri, 14 Nov 2025 02:07:53 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:86ac08e0cbf2640750a131de8ddf9bb285ed3c0359b84a4489b870b5bd4b9d73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:2f888be4d7159ed9a03884f72b0a18d428983c3c093c51acf701c4f3a8f58db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33394268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e41a68f6806fe09a43691a06544a172872ab66d56d34fd116ac854f53aa973a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:32:05 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a0ad9b4aaae6e7e946573addf6867a419111a60fc9323198684be47d29ab8e`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 3.6 MB (3562811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2192c9cd8ae78f10eb620c49dd6c3f1c97dbc3a99b8e0e54442bf4c4085d50be`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3fd385eef297b7ab043fbd27de442eb44e742de653f6f0beec541e5624920c`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9ba4094a4680b7c79b70bf18ec8e50552bb4bcde925a278b84fdf831ae1ce`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 103.9 KB (103855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:30e09776cbad0fdeb6250eeb59b6c85db722439c89e9ea463b8846b520362ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fcd14e1e482b89c9f2956dd0d711c27c1041d1eecbc57b8cee5f200fb7e014`

```dockerfile
```

-	Layers:
	-	`sha256:7cb594c99ab7f7379858b0869eccc55ee5d16dd0c7a117ec2ea6286621e09d2e`  
		Last Modified: Fri, 14 Nov 2025 02:08:05 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874d5cd16621b1ee0eb69f6c404dabe165681b10474bdb7a0c987170e3243da9`  
		Last Modified: Fri, 14 Nov 2025 02:08:06 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:96b42b877a4656e7863be6795ffe062410d426123d20fcbe050944554329e1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79a782002d75afde88daf47c99b398edb58da7b5d5cca3827577832434b8abc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a253dba035401f762d0613aa4d977ce12d945bc1918bfb08a17ba7331fe815`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 3.6 MB (3561049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bd3e1c5570e7cd4878353726e4bd0fe6a358ae3cd2dad02e393d59d98803f9`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 2.6 KB (2640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b495cbf000ce9a258736ce76444ca683648a9ba468ca5d3d6cfde0d8bc89402`  
		Last Modified: Thu, 13 Nov 2025 23:31:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a7199ab9252b8ed239c8c34dd3a013dd0b7c2c06d87c00c361824931df4c86`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 104.6 KB (104607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5f3d14db57b4fa3eeb6cbb447024bf03395dfe359f372b7f4917ee462f439907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe6e66c6e7d0f92c843a2215edea604807c6be3f7f5ff9f9929c74d8d3d52f9`

```dockerfile
```

-	Layers:
	-	`sha256:ad647f1003e7e0dec3bdc34b289daefb923cc8e0c1305ba7b14f3a2108d14a3a`  
		Last Modified: Fri, 14 Nov 2025 02:08:10 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c6007dbe7aee0b4fb818dc38799ebc8efd1b7438bf95762182955214aecc0d`  
		Last Modified: Fri, 14 Nov 2025 02:08:11 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:184659c45ef82521389ee748e1ee4bbe1449f0946581307e3e93d86e0e058f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c299aad60e1e7f11d4286835ce579930df7f598ed9b1015fcaa7c79713c42957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33394810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ed87def879102b787b9246c739018511b4b589c34932b0ef713c6c61de668d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:32:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c0e1d7b3f111e4566e1d12f6c0632e153c201260a9826542321f8ea23bcafa`  
		Last Modified: Thu, 13 Nov 2025 23:32:28 GMT  
		Size: 3.6 MB (3562936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b40e8d70ead7cc4f0cd07dae1ee6920efb006cb20528bcc7de39094ddf9874`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5ee6c709ae7dad0afff7391eaaa68296673cf0205a608f9bce6d4f7500e650`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd86eb2b24e5478ee0f7d4c55df8e6c357a999c4083997d6162434e36abba3f`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 103.8 KB (103841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b41bb95e32d18baa23088cddd23dfe1c3c097445ffe768613d34800b4c0c5`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93bbbca7ef64d9156a3013b0c4e3fa3312e91da86a098db01ea9d83029661afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2465328c5c5e8df05ad265eb773fbf3e584134d29936e5a21430c0d9164a3e3`

```dockerfile
```

-	Layers:
	-	`sha256:aabcb977352301fab1d6dabefc144dcce2ebf0a3030cecf40cf83bc2aa92770b`  
		Last Modified: Fri, 14 Nov 2025 02:08:20 GMT  
		Size: 2.1 MB (2120901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82c114f49a06e6a45987c7131d46b1fe1220101c4997f7726a576f2a5543d25b`  
		Last Modified: Fri, 14 Nov 2025 02:08:21 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c6af2ae93699e738b6c0895055144b4bb347920aca7f91e4451aa75dde146236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32531089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989acad9c141ce3dcea15e9a18df4c3ea56ceedb189ef7a6b8b8dfac6823e87c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876648f4bcbbd9a79fe03bc85730393c6e24075dde48714e37bee27c5e932691`  
		Last Modified: Thu, 13 Nov 2025 23:32:17 GMT  
		Size: 3.6 MB (3561120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c874b0b5bacc6d952a7735777f05b95f3c5bcbe6b7f7d50b6dabee2398abad59`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660eaa03fbbddfa884bad13382570eba092d15224cbac502584ceb4f39f1bc8c`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05849e9ea827053df3f7378003dad6aefab958b313dcfc532a8b8cd4826355d`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 104.7 KB (104669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa5566c0de4309a0ef6703f3bee20e95197bb23f5d2a711b7cd280db22508a1`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:da8153a7c5dabd74fc895825a81e69cddc07810acc5675ecc956059d31108d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71031b6901d4ed1fbb3d94ff534deb64c3c8c0902724a95d29584e35420ca5f2`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ac3e4bbdc32139f4d1a5d2b49adbffdd230b9c2f1f6cbc7952707749b342d`  
		Last Modified: Fri, 14 Nov 2025 02:08:25 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:024cf6e9493f7a6f8cac5b000f292b1bc84bfbbc6fb5d69d25b04d6d3c090a55`  
		Last Modified: Fri, 14 Nov 2025 02:08:26 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd25.04`

```console
$ docker pull neurodebian@sha256:ab139e2ef8b811558941eff017d1f467deaa77fcebcdf3189633727ef717dc92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd25.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdc67ac4dd0d651097ba75d3f513b34e66af0bdfa85db80045d15880faf9ef04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36682742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc9a62b14ecbd0c50b253059091a66a5c95e0809527bce9cdece2619b81e21`
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
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
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
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807958f6dce95c2cf132ab919d751d642e0834efea8afabde5dd80a06382164`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 6.9 MB (6862222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d85781ba57065c27119c5b829ede85b21f4be4c79ed21b52b5dd18e69324e`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6000f4f29de58b9c57f46bf4c2915a41aecfde0ffe93b519dc150c2e05839`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b298e1353c735a6385e6a62cecbfe1d1b59a32feea6c006fe2970e9a377fb0`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 103.6 KB (103644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:87fb8fcdc3533806d68ebce00bcfcf60c95a4fd2ca27173aa2131f4e12b9a92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7aa5c68eb77711d7c5504ea0dd43319dc6ba5a495e2a39b29e42dd4613450`

```dockerfile
```

-	Layers:
	-	`sha256:34e86114d346aa4146ae590dee647494234ddff44dc9bf93ed557394aed25887`  
		Last Modified: Fri, 10 Oct 2025 01:07:52 GMT  
		Size: 2.1 MB (2129387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb29516268d88fbe0487f9e71585d01a2863eda154c3b84c932731ccf47ffd8`  
		Last Modified: Fri, 10 Oct 2025 01:07:54 GMT  
		Size: 14.0 KB (13987 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd25.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d0215dbda4b85ac69b750d98f8f3eb9aba18829cafe490ef6c04e7f1b5d3575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34803835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6196b8372a58dd339a5cd7b297736021c12b067eaa196975ee6481a581ec22`
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
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
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
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b8d7c0516946e6186f0c1918a80da44ccc80465d586f0db577e9c5e3fa309`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 6.4 MB (6392372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccd7c148caa4ff621b2e8f1407d0680d8b216fd3b91aade2da4e3bcf67242ab`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63a7c688f7b81b2251c0096fc2033ac1c2243330fd41da718cf8002ec93dae1`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a8bb23e4d96a15bc63dda952317ea8ba3a8efd39c025f4e5d59b26d5afc57c`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b6e0e2468e055fd3994fdd22716a6516ca822a0b893af378cfe9b7c8c92ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b634830ed4e5ae3eba300cf243790465b87b6d976898e0bdc93781f17d3473b`

```dockerfile
```

-	Layers:
	-	`sha256:73f73f1097d47935c4c36115e56c20ae5811fee70906bb8d0100cacf857414df`  
		Last Modified: Fri, 10 Oct 2025 01:07:59 GMT  
		Size: 2.1 MB (2129631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3369301dca599eb9decd9b13cef9db3cbe5da13f1a35be39a2983729b9cd67db`  
		Last Modified: Fri, 10 Oct 2025 01:08:00 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd25.04-non-free`

```console
$ docker pull neurodebian@sha256:843d307ce6bc09a7cd1b57e44466adef4c4764ea1c793ae5816c4c23f5fd2e42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd25.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7e3b0aa3a1e9664cb5a8951141d1855604212beb174f638ffd32f46742ed4bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36683143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b635066dc43129e20e37c95f2235d3e316b7d3b9c2aba40f0ffde2b54e2e6e2d`
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
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
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
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e95813fe4718cf415f65b5a2a6aff41cf1ca472b75f81f0e71c88a2c1e75e9`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 6.9 MB (6862197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c069ba67e04af50034555225735086ac2d283d240d8ce7e46a9d3308c6398c25`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7163aa66b2f0788a2fd8bfb24efa8a573ed390b32865ae0266981836fb3f2a`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744d7aa582d29cc5ee3a878017b70e760a48aaf077eeaf1aa5c0b98f225a81b`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 103.6 KB (103637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709942cf2f7b8bc52d31c967ec725251f89630a82eb3debdaafff34b2502aec6`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b03d30cc46e85e007f546cd2c4a415622d8016571f0fcd74004ece8a9d69a9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b1b3d34374f9d8719267a2de2de8be8524966deb0e192f3a0d0b9e95bbf7e6`

```dockerfile
```

-	Layers:
	-	`sha256:75abe1e107a33427871261a37ffd5362e38bd76021a38d45be8b8ecfd67cf1a7`  
		Last Modified: Fri, 10 Oct 2025 01:08:09 GMT  
		Size: 2.1 MB (2129423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f0d6a23d261b81b7b10446e66dbf147c195e56727be3c4c4095beb8744927b`  
		Last Modified: Fri, 10 Oct 2025 01:08:10 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd25.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8bb52949ffdc66d1b1c45b166770d0321d7082209a408f0dde0ce50355c437d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34804334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6029e77c7f8a48311858bca5d16c501aebcd7dbababb443b3c892392f8506a5`
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
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
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
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d08ff3fe3897ede8ef5bf7e75a8c754e9da90066ad638138411914e6569fcb`  
		Last Modified: Thu, 09 Oct 2025 21:22:12 GMT  
		Size: 6.4 MB (6392412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87458cf3c50f45fec6029a8e2d31f7dc2c30d63c5e92c7e4f4d7ddbf1fd1fb4`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fabfa39ef821d160c97bf91453f07634d072ad956ea83de4da94873f2b71a97`  
		Last Modified: Thu, 09 Oct 2025 21:22:12 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d80fbf3cdda43cd93b73ef0b7215c959689c5073a718bc28b1a88b435aeda`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 104.2 KB (104235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3181f804aca7e1622946b1391b32ee30ccebfbdb03426caab02bcd300d54cd8b`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:29ea36baad60d33ffbfb5fd8152d415e121532b4008b174a68251c71851548a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5656dffee277d964d7af531bee03d767b53dc21bddc33bbedf5b7d1e0c3a1668`

```dockerfile
```

-	Layers:
	-	`sha256:a897c9f03a98ed8cc43baa74786f9234dccd6f6c51fe452db7dab397fb9c66a0`  
		Last Modified: Fri, 10 Oct 2025 01:08:14 GMT  
		Size: 2.1 MB (2129667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0912356738dd5be0731ed4354e13efdb3bb03dfc003407132e1ed93bde4ad42a`  
		Last Modified: Fri, 10 Oct 2025 01:08:15 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:86ac08e0cbf2640750a131de8ddf9bb285ed3c0359b84a4489b870b5bd4b9d73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:2f888be4d7159ed9a03884f72b0a18d428983c3c093c51acf701c4f3a8f58db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33394268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e41a68f6806fe09a43691a06544a172872ab66d56d34fd116ac854f53aa973a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:32:05 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a0ad9b4aaae6e7e946573addf6867a419111a60fc9323198684be47d29ab8e`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 3.6 MB (3562811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2192c9cd8ae78f10eb620c49dd6c3f1c97dbc3a99b8e0e54442bf4c4085d50be`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3fd385eef297b7ab043fbd27de442eb44e742de653f6f0beec541e5624920c`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9ba4094a4680b7c79b70bf18ec8e50552bb4bcde925a278b84fdf831ae1ce`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 103.9 KB (103855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:30e09776cbad0fdeb6250eeb59b6c85db722439c89e9ea463b8846b520362ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fcd14e1e482b89c9f2956dd0d711c27c1041d1eecbc57b8cee5f200fb7e014`

```dockerfile
```

-	Layers:
	-	`sha256:7cb594c99ab7f7379858b0869eccc55ee5d16dd0c7a117ec2ea6286621e09d2e`  
		Last Modified: Fri, 14 Nov 2025 02:08:05 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874d5cd16621b1ee0eb69f6c404dabe165681b10474bdb7a0c987170e3243da9`  
		Last Modified: Fri, 14 Nov 2025 02:08:06 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:96b42b877a4656e7863be6795ffe062410d426123d20fcbe050944554329e1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79a782002d75afde88daf47c99b398edb58da7b5d5cca3827577832434b8abc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a253dba035401f762d0613aa4d977ce12d945bc1918bfb08a17ba7331fe815`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 3.6 MB (3561049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bd3e1c5570e7cd4878353726e4bd0fe6a358ae3cd2dad02e393d59d98803f9`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 2.6 KB (2640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b495cbf000ce9a258736ce76444ca683648a9ba468ca5d3d6cfde0d8bc89402`  
		Last Modified: Thu, 13 Nov 2025 23:31:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a7199ab9252b8ed239c8c34dd3a013dd0b7c2c06d87c00c361824931df4c86`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 104.6 KB (104607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5f3d14db57b4fa3eeb6cbb447024bf03395dfe359f372b7f4917ee462f439907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe6e66c6e7d0f92c843a2215edea604807c6be3f7f5ff9f9929c74d8d3d52f9`

```dockerfile
```

-	Layers:
	-	`sha256:ad647f1003e7e0dec3bdc34b289daefb923cc8e0c1305ba7b14f3a2108d14a3a`  
		Last Modified: Fri, 14 Nov 2025 02:08:10 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c6007dbe7aee0b4fb818dc38799ebc8efd1b7438bf95762182955214aecc0d`  
		Last Modified: Fri, 14 Nov 2025 02:08:11 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:184659c45ef82521389ee748e1ee4bbe1449f0946581307e3e93d86e0e058f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c299aad60e1e7f11d4286835ce579930df7f598ed9b1015fcaa7c79713c42957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33394810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ed87def879102b787b9246c739018511b4b589c34932b0ef713c6c61de668d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:32:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c0e1d7b3f111e4566e1d12f6c0632e153c201260a9826542321f8ea23bcafa`  
		Last Modified: Thu, 13 Nov 2025 23:32:28 GMT  
		Size: 3.6 MB (3562936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b40e8d70ead7cc4f0cd07dae1ee6920efb006cb20528bcc7de39094ddf9874`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5ee6c709ae7dad0afff7391eaaa68296673cf0205a608f9bce6d4f7500e650`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd86eb2b24e5478ee0f7d4c55df8e6c357a999c4083997d6162434e36abba3f`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 103.8 KB (103841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b41bb95e32d18baa23088cddd23dfe1c3c097445ffe768613d34800b4c0c5`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93bbbca7ef64d9156a3013b0c4e3fa3312e91da86a098db01ea9d83029661afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2465328c5c5e8df05ad265eb773fbf3e584134d29936e5a21430c0d9164a3e3`

```dockerfile
```

-	Layers:
	-	`sha256:aabcb977352301fab1d6dabefc144dcce2ebf0a3030cecf40cf83bc2aa92770b`  
		Last Modified: Fri, 14 Nov 2025 02:08:20 GMT  
		Size: 2.1 MB (2120901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82c114f49a06e6a45987c7131d46b1fe1220101c4997f7726a576f2a5543d25b`  
		Last Modified: Fri, 14 Nov 2025 02:08:21 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c6af2ae93699e738b6c0895055144b4bb347920aca7f91e4451aa75dde146236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32531089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989acad9c141ce3dcea15e9a18df4c3ea56ceedb189ef7a6b8b8dfac6823e87c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876648f4bcbbd9a79fe03bc85730393c6e24075dde48714e37bee27c5e932691`  
		Last Modified: Thu, 13 Nov 2025 23:32:17 GMT  
		Size: 3.6 MB (3561120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c874b0b5bacc6d952a7735777f05b95f3c5bcbe6b7f7d50b6dabee2398abad59`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660eaa03fbbddfa884bad13382570eba092d15224cbac502584ceb4f39f1bc8c`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05849e9ea827053df3f7378003dad6aefab958b313dcfc532a8b8cd4826355d`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 104.7 KB (104669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa5566c0de4309a0ef6703f3bee20e95197bb23f5d2a711b7cd280db22508a1`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:da8153a7c5dabd74fc895825a81e69cddc07810acc5675ecc956059d31108d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71031b6901d4ed1fbb3d94ff534deb64c3c8c0902724a95d29584e35420ca5f2`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ac3e4bbdc32139f4d1a5d2b49adbffdd230b9c2f1f6cbc7952707749b342d`  
		Last Modified: Fri, 14 Nov 2025 02:08:25 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:024cf6e9493f7a6f8cac5b000f292b1bc84bfbbc6fb5d69d25b04d6d3c090a55`  
		Last Modified: Fri, 14 Nov 2025 02:08:26 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:054cb83bc13a514b14b0d6d2127811bf8c518e556fd6edf1c54b48aefeaff471
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
$ docker pull neurodebian@sha256:a84e7c70d72128f0303fdb503e24ecd7c72e91d03ce7d2d107f71fd126955cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59669100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ae6b2236202b62a987ca7ce3e3a621ebf3b0ea0f954e6b7b038687bb9f71ab`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:17:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:17:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 04:17:23 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 04:17:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:17:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23386e12d6e309376ac1a14efa640269690dc204b17984b14064c2fd2f49098d`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 10.3 MB (10289939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4a65b6a6351a097123b770a2e0e8e7d5c03b57aa5a1dad26e1c2eadaadfd28`  
		Last Modified: Tue, 04 Nov 2025 04:17:39 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52742b84510725699f7a178b63e604e0d0891893d1f2eb344188531d8636f0e1`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aee8c1d05553c1777be79055a18fea90ee2b8ea9411f6c738c5c18eba8d1c6`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 90.2 KB (90186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2b299738c4e4019fbb06b267440b617ca810b6d56b21bc0afdd3695d852ada`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0089444d554e5cae9f22a559edef3bfd16e1bd0b68860b6c214e2428014781d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba98d48bfb433fb8f9a10e0d06f0d683a5c4944286fdaf551bce2c5892d7022`

```dockerfile
```

-	Layers:
	-	`sha256:3c66055059d16bf03b067f48cf3c4b38abaf5be7f3bd7af8dfaf7d94c8708e01`  
		Last Modified: Tue, 04 Nov 2025 11:09:30 GMT  
		Size: 3.6 MB (3613075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64a75afe777c95a9303af2be30b3244166f9507b5d307bc436cd2c311c33b53`  
		Last Modified: Tue, 04 Nov 2025 11:09:31 GMT  
		Size: 16.3 KB (16280 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1529a63d3b1fd5b20e69752735685aed7551980815e4f5ba9dfeb57bf08a98dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59818048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede29356c99f4ad500f6f92d01d99c80598e7a0ab06e0cba76bb427bec98bcdd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:32:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172872c0ee5e3387027dd024c77e0a566ab9e979918d5d1ae3a862912f9819cb`  
		Last Modified: Tue, 04 Nov 2025 01:32:37 GMT  
		Size: 10.1 MB (10073407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd94c5bde5357bba8d2d736f7e486405a517a770df0fbf2434fff09e3cdfd82`  
		Last Modified: Tue, 04 Nov 2025 01:32:36 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3686e47e17b33cbec471ea4f8d20ee610283524c8e381b60bbe0bca643d3cb`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0201931aec9ab3ac74ff7c1fcb5bbda1b95323d45a16ba0594b8586855f134`  
		Last Modified: Tue, 04 Nov 2025 01:32:36 GMT  
		Size: 90.9 KB (90860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda921f974a2bbf05547e240c45b797d09307a80d64747669b300890b4877699`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:171c082cd86f6d465311384dc89b6f8caef5ba756bac4b22acc5740480c28923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bca970acfe0d4594fdb6fa5375fc79bd72f1c0309d3fcd6644884295e7a995`

```dockerfile
```

-	Layers:
	-	`sha256:e6a4a640a7d1de22f588ad1235c812b9907faedeac55c9b05d4fc71a53fe4317`  
		Last Modified: Tue, 04 Nov 2025 11:09:53 GMT  
		Size: 3.6 MB (3614602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11690b726c377ad7c6177f469ec7805bdb379cb0e37fd6d69b8c57d618893f46`  
		Last Modified: Tue, 04 Nov 2025 11:09:53 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:5771d15f06fa62ffa39ee92437de3260e58824c9c3aca71b930f2340dd55319c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61357929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae41e42556a48153e417d850113110e79e617019f105a3699f765baf91edbacc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:38:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:933c2eb03a495d1bdbab772ff092366c6df6bb75cafd8749623e94908401abca`  
		Last Modified: Tue, 04 Nov 2025 00:13:58 GMT  
		Size: 50.8 MB (50801238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c3eaf959f47b3c81adaab22c02b91552da31d1998da6c88911ad6288b7a9fb`  
		Last Modified: Tue, 04 Nov 2025 01:38:50 GMT  
		Size: 10.5 MB (10462757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e9ef740b4bb48f2974e682a417cb34fceb185aca217d1c2c7f6227a748dd40`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242bf4e4c9cf11d3df4c63f4db58331b50dfdde7542f70fffe6271a6cef67b5c`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7804e0ac9d5bfb67777d18126743dfa3501a6cab30e2779e9c1e882d3931d3b`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 90.6 KB (90584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f31b454367cf57f9fdcbbcbabe35b3a537175a9cbf95e0455aa5c68268299`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fadfe623ab9931f7482ec50383c61bca36e19d1881f7b599d5a47feb0ee6dd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e8ea8d062af83ff955f51cd8b7f77e408cb8628ee432dade259fd59a85c1b7`

```dockerfile
```

-	Layers:
	-	`sha256:088a395d40071397cf8e0032ab14cbcabec0416a8a0a34130b1268e1fe736e89`  
		Last Modified: Tue, 04 Nov 2025 22:51:34 GMT  
		Size: 3.6 MB (3611024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc01ac211e92ee4d0d4707e08a6fb4c64315bf3561a027a8594a15e46d12b72`  
		Last Modified: Tue, 04 Nov 2025 22:51:35 GMT  
		Size: 16.2 KB (16246 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:plucky`

```console
$ docker pull neurodebian@sha256:ab139e2ef8b811558941eff017d1f467deaa77fcebcdf3189633727ef717dc92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdc67ac4dd0d651097ba75d3f513b34e66af0bdfa85db80045d15880faf9ef04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36682742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc9a62b14ecbd0c50b253059091a66a5c95e0809527bce9cdece2619b81e21`
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
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
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
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807958f6dce95c2cf132ab919d751d642e0834efea8afabde5dd80a06382164`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 6.9 MB (6862222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d85781ba57065c27119c5b829ede85b21f4be4c79ed21b52b5dd18e69324e`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6000f4f29de58b9c57f46bf4c2915a41aecfde0ffe93b519dc150c2e05839`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b298e1353c735a6385e6a62cecbfe1d1b59a32feea6c006fe2970e9a377fb0`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 103.6 KB (103644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:87fb8fcdc3533806d68ebce00bcfcf60c95a4fd2ca27173aa2131f4e12b9a92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7aa5c68eb77711d7c5504ea0dd43319dc6ba5a495e2a39b29e42dd4613450`

```dockerfile
```

-	Layers:
	-	`sha256:34e86114d346aa4146ae590dee647494234ddff44dc9bf93ed557394aed25887`  
		Last Modified: Fri, 10 Oct 2025 01:07:52 GMT  
		Size: 2.1 MB (2129387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb29516268d88fbe0487f9e71585d01a2863eda154c3b84c932731ccf47ffd8`  
		Last Modified: Fri, 10 Oct 2025 01:07:54 GMT  
		Size: 14.0 KB (13987 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:plucky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d0215dbda4b85ac69b750d98f8f3eb9aba18829cafe490ef6c04e7f1b5d3575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34803835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6196b8372a58dd339a5cd7b297736021c12b067eaa196975ee6481a581ec22`
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
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
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
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b8d7c0516946e6186f0c1918a80da44ccc80465d586f0db577e9c5e3fa309`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 6.4 MB (6392372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccd7c148caa4ff621b2e8f1407d0680d8b216fd3b91aade2da4e3bcf67242ab`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63a7c688f7b81b2251c0096fc2033ac1c2243330fd41da718cf8002ec93dae1`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a8bb23e4d96a15bc63dda952317ea8ba3a8efd39c025f4e5d59b26d5afc57c`  
		Last Modified: Thu, 09 Oct 2025 21:22:05 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b6e0e2468e055fd3994fdd22716a6516ca822a0b893af378cfe9b7c8c92ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b634830ed4e5ae3eba300cf243790465b87b6d976898e0bdc93781f17d3473b`

```dockerfile
```

-	Layers:
	-	`sha256:73f73f1097d47935c4c36115e56c20ae5811fee70906bb8d0100cacf857414df`  
		Last Modified: Fri, 10 Oct 2025 01:07:59 GMT  
		Size: 2.1 MB (2129631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3369301dca599eb9decd9b13cef9db3cbe5da13f1a35be39a2983729b9cd67db`  
		Last Modified: Fri, 10 Oct 2025 01:08:00 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:plucky-non-free`

```console
$ docker pull neurodebian@sha256:843d307ce6bc09a7cd1b57e44466adef4c4764ea1c793ae5816c4c23f5fd2e42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7e3b0aa3a1e9664cb5a8951141d1855604212beb174f638ffd32f46742ed4bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36683143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b635066dc43129e20e37c95f2235d3e316b7d3b9c2aba40f0ffde2b54e2e6e2d`
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
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
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
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e95813fe4718cf415f65b5a2a6aff41cf1ca472b75f81f0e71c88a2c1e75e9`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 6.9 MB (6862197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c069ba67e04af50034555225735086ac2d283d240d8ce7e46a9d3308c6398c25`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7163aa66b2f0788a2fd8bfb24efa8a573ed390b32865ae0266981836fb3f2a`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744d7aa582d29cc5ee3a878017b70e760a48aaf077eeaf1aa5c0b98f225a81b`  
		Last Modified: Thu, 09 Oct 2025 21:21:04 GMT  
		Size: 103.6 KB (103637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709942cf2f7b8bc52d31c967ec725251f89630a82eb3debdaafff34b2502aec6`  
		Last Modified: Thu, 09 Oct 2025 21:21:05 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b03d30cc46e85e007f546cd2c4a415622d8016571f0fcd74004ece8a9d69a9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b1b3d34374f9d8719267a2de2de8be8524966deb0e192f3a0d0b9e95bbf7e6`

```dockerfile
```

-	Layers:
	-	`sha256:75abe1e107a33427871261a37ffd5362e38bd76021a38d45be8b8ecfd67cf1a7`  
		Last Modified: Fri, 10 Oct 2025 01:08:09 GMT  
		Size: 2.1 MB (2129423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f0d6a23d261b81b7b10446e66dbf147c195e56727be3c4c4095beb8744927b`  
		Last Modified: Fri, 10 Oct 2025 01:08:10 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:plucky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8bb52949ffdc66d1b1c45b166770d0321d7082209a408f0dde0ce50355c437d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34804334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6029e77c7f8a48311858bca5d16c501aebcd7dbababb443b3c892392f8506a5`
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
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
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
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Fri, 03 Oct 2025 12:41:25 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d08ff3fe3897ede8ef5bf7e75a8c754e9da90066ad638138411914e6569fcb`  
		Last Modified: Thu, 09 Oct 2025 21:22:12 GMT  
		Size: 6.4 MB (6392412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87458cf3c50f45fec6029a8e2d31f7dc2c30d63c5e92c7e4f4d7ddbf1fd1fb4`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fabfa39ef821d160c97bf91453f07634d072ad956ea83de4da94873f2b71a97`  
		Last Modified: Thu, 09 Oct 2025 21:22:12 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d80fbf3cdda43cd93b73ef0b7215c959689c5073a718bc28b1a88b435aeda`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 104.2 KB (104235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3181f804aca7e1622946b1391b32ee30ccebfbdb03426caab02bcd300d54cd8b`  
		Last Modified: Thu, 09 Oct 2025 21:22:11 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:29ea36baad60d33ffbfb5fd8152d415e121532b4008b174a68251c71851548a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5656dffee277d964d7af531bee03d767b53dc21bddc33bbedf5b7d1e0c3a1668`

```dockerfile
```

-	Layers:
	-	`sha256:a897c9f03a98ed8cc43baa74786f9234dccd6f6c51fe452db7dab397fb9c66a0`  
		Last Modified: Fri, 10 Oct 2025 01:08:14 GMT  
		Size: 2.1 MB (2129667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0912356738dd5be0731ed4354e13efdb3bb03dfc003407132e1ed93bde4ad42a`  
		Last Modified: Fri, 10 Oct 2025 01:08:15 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:cfbe31e8f8216a29bec1d84ffe30e9154e7006818f7e0fe5af624b8073a5e896
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
$ docker pull neurodebian@sha256:722b3734a074f52b537930b8d13d96a90c23904dea0de135834085857118a3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60161613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9e6e7067e1ace693bcb1daa4cb49007ce4c30aba88f93332e4d3297eef23fe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 00:33:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2e77f12282fcde2c6f54d54624e8a7eef59205bf9001d755b40c1e76ea8e3238`  
		Last Modified: Tue, 04 Nov 2025 00:13:00 GMT  
		Size: 48.5 MB (48485640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a5b96440cbeeb7769517ff329ed0883771f1e3a99f7933b2173145cc5480cc`  
		Last Modified: Tue, 04 Nov 2025 00:34:04 GMT  
		Size: 11.6 MB (11583255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4375310c6ed16655ad67365cd813771aabbbe8573c45b873213c2074e78f4528`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f426f31085761e6a46465387404baada1a21b1249625e208e4bf18e8596c6d`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e900ba29d98519727c17183e473955bf493815c7da5e3103020a8176f31fc356`  
		Last Modified: Tue, 04 Nov 2025 00:34:03 GMT  
		Size: 89.8 KB (89813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e4a85c3da567c9a45c5c7f1618d5098c8ee258bf7ea9c83695d83dcd6a8f4c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c45e24afa3b99e6ff745dcae8421698af0fa6919177fa5959f32b08970e1c16`

```dockerfile
```

-	Layers:
	-	`sha256:45cac87f230eb98aa986ff794a77ff43a15a3bc71644de748398a4360351376f`  
		Last Modified: Tue, 04 Nov 2025 11:08:52 GMT  
		Size: 3.6 MB (3577395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c589fd0990d047638dae2719c765f5e3f9f00abad8733ec51451217ce909976`  
		Last Modified: Tue, 04 Nov 2025 11:08:53 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c7cce04f019cdaad0ced550dca9af4ce069da69a580048487ac8e45f4dfad4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59938487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792e7d0dd2ec4ae27f7d32f4408e7344a709b1185f2c60131cba267efb2d3fe0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:32:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e6429e9e41ca9e14d8856af7a396ce50bc2b9896b4f4cd83c36fd480cd4514de`  
		Last Modified: Tue, 04 Nov 2025 00:13:31 GMT  
		Size: 48.6 MB (48586018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e357ec5b83e5625b9f94d5fc603d2031b8514071e4bd32938375326d1cc6c9d9`  
		Last Modified: Tue, 04 Nov 2025 01:33:04 GMT  
		Size: 11.3 MB (11259052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d225e2c5c4d55a1eeedd7d833cce1246eb8fa46211165fba4866d1f770d13666`  
		Last Modified: Tue, 04 Nov 2025 01:33:03 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d0a3c87f92b126ad11f68b5e3d11fc24562344b0b4d492241f33509c2acf11`  
		Last Modified: Tue, 04 Nov 2025 01:33:03 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f467de9381fac753e2f32ec130c3fdc5bd52c38944cf43855a312828900bb2`  
		Last Modified: Tue, 04 Nov 2025 01:33:03 GMT  
		Size: 90.5 KB (90516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b5a2152fc41ed9eea92688f57fddcb38f01656a94abf50490022d188d6e5d609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69957ad7a64f6286d83d10828ce2f0c30cc145aff8c0291731392884594992a`

```dockerfile
```

-	Layers:
	-	`sha256:5df592788eddb75c428d5fba029ca483e1a5adc0e0e03f142b8455a9f3235ce5`  
		Last Modified: Tue, 04 Nov 2025 11:08:58 GMT  
		Size: 3.6 MB (3578271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fc7a61a4a383f5b356e7bb4721d7e94c544d6ea8839c32df57b0b84c4e15cf6`  
		Last Modified: Tue, 04 Nov 2025 11:08:58 GMT  
		Size: 14.0 KB (14028 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:9b677e080c119eb4a17717438cd0c8483c91f4ea704a02c34b6f6506c58b0ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61636868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4883a56e806041e69ea01712a928a707f955a2916bc0a6ddf0f9111af750ddf9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:38:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:37a822686dc57d9a439e8fe6f90a9020bbd58f684341d3cac6e3e13c68f3344e`  
		Last Modified: Tue, 04 Nov 2025 00:13:36 GMT  
		Size: 49.8 MB (49809007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3095763312556ed24fdf8414a87f3df47e55ade17984072746abeb95af700d7`  
		Last Modified: Tue, 04 Nov 2025 01:39:06 GMT  
		Size: 11.7 MB (11734751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20daa1451a1c5e4864905084a53cb50a8ea4ecc7152fe1f07eec291ef587bedc`  
		Last Modified: Tue, 04 Nov 2025 01:39:05 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a436f1558d69b26b0f120fbf5cb58bc87b6656499820ecab74b4cfba29a4f5`  
		Last Modified: Tue, 04 Nov 2025 01:39:05 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d31efbac8a3de9856fb31500c282ed7ac97967a0bfb99748f45785bf8ff335`  
		Last Modified: Tue, 04 Nov 2025 01:39:05 GMT  
		Size: 90.2 KB (90206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d42fe0312df5575f7895f36d60444890b9d1945492b4ebf532dd5fe409a8b2d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8feb1ed938280b209b67281e45960fad0d7b9e3883af43573db10eb3d7a4438c`

```dockerfile
```

-	Layers:
	-	`sha256:c8c06839190cbb474a9a1105dae3eba7bf063e0ec0058bdb7f336eb8fa3fbb48`  
		Last Modified: Tue, 04 Nov 2025 11:09:02 GMT  
		Size: 3.6 MB (3575358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a58ee565df700715f4dc6eb2260eab6c98353f3ffcaa0425fa571731b9f3a9a5`  
		Last Modified: Tue, 04 Nov 2025 11:09:03 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:fc69386df37f5bf119ef83293196dd59e80a4792d08d52e437c64ab8dbd886b1
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
$ docker pull neurodebian@sha256:6879037c817de6fcd44e5e3e5669da89e8ba81a5efb8d55e046fb7cfa1155c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60161908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5d45b5bb82dce6fc9c4f872667cc486b1620d53b2513cab6da3ab558efb16d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 00:33:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:52 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2e77f12282fcde2c6f54d54624e8a7eef59205bf9001d755b40c1e76ea8e3238`  
		Last Modified: Tue, 04 Nov 2025 00:13:00 GMT  
		Size: 48.5 MB (48485640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c43c0422b532d4f7fd4389c7bcce79bb8e16a074d6cb2363789e53874b7bdda`  
		Last Modified: Tue, 04 Nov 2025 00:34:13 GMT  
		Size: 11.6 MB (11583123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704df9e7d2a22ca832d66d121411d6707d4ada86bc43ec80f2a555fa1d72697b`  
		Last Modified: Tue, 04 Nov 2025 00:34:10 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb42e9230b83fcf84ee0a600f12e4cd26a55217ec3de7dd0c6c0aa252771704`  
		Last Modified: Tue, 04 Nov 2025 00:34:10 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2947d93c1659c1730f645265acceb08d999ef27b66b5b7f95b9c3823fa6e88`  
		Last Modified: Tue, 04 Nov 2025 00:34:10 GMT  
		Size: 89.8 KB (89825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2f35ee62eb9b30a2febc3d098c370d6d0e830d7b7067075dd4621db81923a7`  
		Last Modified: Tue, 04 Nov 2025 00:34:10 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7d110273275d3a0b927c7c495a117dfbbbbb6b6b74e02853e56c4279a552beb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c438b5523469c0a8d160ad1023753bef5cb1b88ad7079cb2054bb8819965a85`

```dockerfile
```

-	Layers:
	-	`sha256:5954562b8f15d556fd976802885c845f79a74767c4ad3b3c218918e01ff0066a`  
		Last Modified: Tue, 04 Nov 2025 11:09:05 GMT  
		Size: 3.6 MB (3577431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:389702f3e48418c9722705566d3d18e849d8d1444d2ac1cc0091dbf590eab8a4`  
		Last Modified: Tue, 04 Nov 2025 11:09:06 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:48e130fd3a3c32aa03d0a2768b47cac94653fe00c02852bea9f52c13ba2c2fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59938919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e45f4e9facb1ca6907f02bd36142baf06f206143422bb34218818416844b338`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:32:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e6429e9e41ca9e14d8856af7a396ce50bc2b9896b4f4cd83c36fd480cd4514de`  
		Last Modified: Tue, 04 Nov 2025 00:13:31 GMT  
		Size: 48.6 MB (48586018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe6ea727459d544c8517f0c8256aa0fedcebc648fb6af23c240b500415196ac`  
		Last Modified: Tue, 04 Nov 2025 01:33:08 GMT  
		Size: 11.3 MB (11259082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9af8ac4e367a30a0f111ac0e743568cdd4e5bfa5d7d54d501aca01d1a3f256`  
		Last Modified: Tue, 04 Nov 2025 01:33:07 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d30811e3c51ec44c6a3a5af602fb03cd9579ed244d07f4a14a48b57d498929`  
		Last Modified: Tue, 04 Nov 2025 01:33:07 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4881ad860dbb9016aee3cc5779892b19a2e87de7a876fd0a2cdc004d197ce1cf`  
		Last Modified: Tue, 04 Nov 2025 01:33:06 GMT  
		Size: 90.5 KB (90502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246186e66c3a37ef6fd03b09e40ddf97ef52d732a09918e66e3fda666c327633`  
		Last Modified: Tue, 04 Nov 2025 01:33:06 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aa87ac3b4e56d1bbfc35a9e5af42aa76a5a321b219af7edd9177a076ddacb30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3525b0eb3432852f9349a598e3788fce3d01885c6d090fd8d04bbfc8966b4e15`

```dockerfile
```

-	Layers:
	-	`sha256:057302c439195291f1f16521b5f2283e18bfc246a8541b2478b4450684dc0cca`  
		Last Modified: Tue, 04 Nov 2025 11:09:10 GMT  
		Size: 3.6 MB (3578307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc4152efdfe5c56849b62b14de3352fe4dc0777258fd7875529be85a2cfc9d10`  
		Last Modified: Tue, 04 Nov 2025 11:09:11 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:c3fab4fa9ef2cd84bdfd791b0cdc2d4a41c22f90d873cf4f90dea71809f0c3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61637272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf02c6051aadb5284db513d6637e4ba5b536869da5a033f89fe262ecf18ca95`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1762202650'
# Tue, 04 Nov 2025 01:38:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:48 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:37a822686dc57d9a439e8fe6f90a9020bbd58f684341d3cac6e3e13c68f3344e`  
		Last Modified: Tue, 04 Nov 2025 00:13:36 GMT  
		Size: 49.8 MB (49809007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892d3fb4efe2a3e137aad659f9e65e47845c46362dfc05bc72e794dc3de155ce`  
		Last Modified: Tue, 04 Nov 2025 01:39:04 GMT  
		Size: 11.7 MB (11734755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e050807cf2c0cd74803b8a7acb3e0a4faeba92aabe9414adf78a10fe10f332`  
		Last Modified: Tue, 04 Nov 2025 01:39:03 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c87cc361f91116017b998780cad41ea0d6555df2d7cc1f06ef61aa5519e9c4`  
		Last Modified: Tue, 04 Nov 2025 01:39:03 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3311ee8f1fc40c74890bd5bcac1450256d6640b97d8f38ef6cd89a603849651`  
		Last Modified: Tue, 04 Nov 2025 01:39:03 GMT  
		Size: 90.2 KB (90192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f0e7037e9d028f6faa7a5822186818bc2adca9d82fafea7ca41d47a9bf58c9`  
		Last Modified: Tue, 04 Nov 2025 01:39:03 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7e55f505f925899d82e80d8b2c41f2e678958bb8a00f26f80bc93f422c763675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a94c61d7822dc33f6b22948d79ce5a82743c7b588d101fdfbaf8baf9fe96c67`

```dockerfile
```

-	Layers:
	-	`sha256:4e87a0cc8fb757426409cc233a258fea1c63f39172d90e807f21e239d4204dc7`  
		Last Modified: Tue, 04 Nov 2025 11:09:15 GMT  
		Size: 3.6 MB (3575394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac7bb0e2883695d8a9dc27bf4b5f90cec47a720f2c163d3e1c5bfb39eb5c4bf`  
		Last Modified: Tue, 04 Nov 2025 11:09:16 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:c2360b59f5cd07c356ea19ed3cdc88006759a1c0012203558eabacf878b94db7
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
$ docker pull neurodebian@sha256:cc62f8a2b909a4a621f695fb23ddfd2f55abe99c1107ea422ddbc9493ed29c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59668516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58c9d81054ebb46f7a713bc03b050382ac159d061b22d7c255322f1b7f34f30`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:17:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:17:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 04:17:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 04:17:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a97f52bf44b7c35c2c3dde0b10f67fac3048c89ac6322097bbe246677a0d380`  
		Last Modified: Tue, 04 Nov 2025 04:17:37 GMT  
		Size: 10.3 MB (10289768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eeeebbd965732bf90942a1ebed2be9c5db1bfbae37f79d18df48b59aca1094e`  
		Last Modified: Tue, 04 Nov 2025 04:17:36 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1715ac06925051c0dc44b303a59854227464617274e4399c7c3f7ed42d3b728`  
		Last Modified: Tue, 04 Nov 2025 04:17:36 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c90e3669c8b11bf12b32885c25bb7005fc7657659840b3143510e4019e3f87`  
		Last Modified: Tue, 04 Nov 2025 04:17:37 GMT  
		Size: 90.2 KB (90219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:36e5e12cc006b9c643190e4e94c3c9be24cdbc7ab1ec5ce2a37eddbf5d3ba551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499dc65ca82ef280131d7296a24026b6d9c9a045d868f46c496b60250fd68b51`

```dockerfile
```

-	Layers:
	-	`sha256:9693e52244e9d6cb3776573b396e8ad9c1541b70da98119a48d0f73cebb9b960`  
		Last Modified: Tue, 04 Nov 2025 11:08:43 GMT  
		Size: 3.6 MB (3613035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc75a15b38b24dca33cd177d886bd1cdc06cc59a5a50cded16bab45890c0f3f3`  
		Last Modified: Tue, 04 Nov 2025 11:08:44 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e88a59a8eb59c283f7ceee4aa5edff9e76424daabdd909cbcfd68c99440707bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a592f978047a6bc3cfa14fa679b85d9abaf32c5c31f72dce1954eed1d6b74070`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:32:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f261ede3c228ffdcf1af64259b67759d9a002314294a6000401de78dec7fb6`  
		Last Modified: Tue, 04 Nov 2025 01:32:37 GMT  
		Size: 10.1 MB (10073302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6646aea08c3732bf73a2e6f46ff98544770e90860b4a0866fccca039070f3971`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44013910ff33d14f15aaed9be503bd613a4c1ecf18b98392429751d3e1fc2010`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7fc94592c535b9c56ba976c47ab0d65065ab60188dfa41ea53a0384e5650fe`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 90.9 KB (90885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:67a7caeac0b108a3854951a85b61cea2cbf3694ba8b127f21abb057acc37ade8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748332e676c636a5998508a3d059c676a2b871719d4db0d6cb4ea97debe4bd2e`

```dockerfile
```

-	Layers:
	-	`sha256:2b1e3c4221c421d4c252a44448f8148f38f4bdac55bd98dbbf9db0660257507a`  
		Last Modified: Tue, 04 Nov 2025 11:08:48 GMT  
		Size: 3.6 MB (3614562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74244bc19fbb24f3845e801cde56e470597db35a2cee721033aa920b9e5a27f2`  
		Last Modified: Tue, 04 Nov 2025 11:08:49 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:f1f7bf3923b89f2692a55d2ef2edee2bd82dbdc0d1d0b02b9b061c57f1e36040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61357599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db97c9f327dffd9682c36f7aea893d03e88502d815f95f1d27f8b9709dd0e9e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:38:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:933c2eb03a495d1bdbab772ff092366c6df6bb75cafd8749623e94908401abca`  
		Last Modified: Tue, 04 Nov 2025 00:13:58 GMT  
		Size: 50.8 MB (50801238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2c10dd39d3ea1b7fcb9ac6e3da6cd2c85fa478453556608f507a3d8d1f3de8`  
		Last Modified: Tue, 04 Nov 2025 01:38:36 GMT  
		Size: 10.5 MB (10462886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9376d28a0149ab43591656335468744f02197d038449d77f9079e5468990880e`  
		Last Modified: Tue, 04 Nov 2025 01:38:35 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca789b0bcf3530d0cfe0bec7d39ca51f45bcff2c8d4b4b423d21a5202dba138`  
		Last Modified: Tue, 04 Nov 2025 01:38:35 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8321b60075f8d7fed5d7ca2c9196cdb5c999eed080f68586d1e00a229d684962`  
		Last Modified: Tue, 04 Nov 2025 01:38:35 GMT  
		Size: 90.6 KB (90574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cda8f897e235f9ee79691e1bc08a3297a011b8bc61f86a081bf28301e8682a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c691882c13ae6f1a1774af6d1a3247c9e387f56355f7cb056f38ff5955ad54`

```dockerfile
```

-	Layers:
	-	`sha256:166ffe9a4c84e31de85225508329baa1a1ba0f7231e235931fc77f822846d3db`  
		Last Modified: Tue, 04 Nov 2025 11:08:53 GMT  
		Size: 3.6 MB (3610984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dca0d5a4a061e7f9961f25762a0315f1d2bbbfb9720f451af5e672c5ffba9d26`  
		Last Modified: Tue, 04 Nov 2025 11:08:53 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:054cb83bc13a514b14b0d6d2127811bf8c518e556fd6edf1c54b48aefeaff471
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
$ docker pull neurodebian@sha256:a84e7c70d72128f0303fdb503e24ecd7c72e91d03ce7d2d107f71fd126955cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59669100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ae6b2236202b62a987ca7ce3e3a621ebf3b0ea0f954e6b7b038687bb9f71ab`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:17:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:17:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 04:17:23 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 04:17:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:17:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23386e12d6e309376ac1a14efa640269690dc204b17984b14064c2fd2f49098d`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 10.3 MB (10289939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4a65b6a6351a097123b770a2e0e8e7d5c03b57aa5a1dad26e1c2eadaadfd28`  
		Last Modified: Tue, 04 Nov 2025 04:17:39 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52742b84510725699f7a178b63e604e0d0891893d1f2eb344188531d8636f0e1`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aee8c1d05553c1777be79055a18fea90ee2b8ea9411f6c738c5c18eba8d1c6`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 90.2 KB (90186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2b299738c4e4019fbb06b267440b617ca810b6d56b21bc0afdd3695d852ada`  
		Last Modified: Tue, 04 Nov 2025 04:17:40 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0089444d554e5cae9f22a559edef3bfd16e1bd0b68860b6c214e2428014781d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ba98d48bfb433fb8f9a10e0d06f0d683a5c4944286fdaf551bce2c5892d7022`

```dockerfile
```

-	Layers:
	-	`sha256:3c66055059d16bf03b067f48cf3c4b38abaf5be7f3bd7af8dfaf7d94c8708e01`  
		Last Modified: Tue, 04 Nov 2025 11:09:30 GMT  
		Size: 3.6 MB (3613075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64a75afe777c95a9303af2be30b3244166f9507b5d307bc436cd2c311c33b53`  
		Last Modified: Tue, 04 Nov 2025 11:09:31 GMT  
		Size: 16.3 KB (16280 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1529a63d3b1fd5b20e69752735685aed7551980815e4f5ba9dfeb57bf08a98dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59818048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede29356c99f4ad500f6f92d01d99c80598e7a0ab06e0cba76bb427bec98bcdd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:32:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:32:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:32:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:32:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172872c0ee5e3387027dd024c77e0a566ab9e979918d5d1ae3a862912f9819cb`  
		Last Modified: Tue, 04 Nov 2025 01:32:37 GMT  
		Size: 10.1 MB (10073407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd94c5bde5357bba8d2d736f7e486405a517a770df0fbf2434fff09e3cdfd82`  
		Last Modified: Tue, 04 Nov 2025 01:32:36 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3686e47e17b33cbec471ea4f8d20ee610283524c8e381b60bbe0bca643d3cb`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0201931aec9ab3ac74ff7c1fcb5bbda1b95323d45a16ba0594b8586855f134`  
		Last Modified: Tue, 04 Nov 2025 01:32:36 GMT  
		Size: 90.9 KB (90860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda921f974a2bbf05547e240c45b797d09307a80d64747669b300890b4877699`  
		Last Modified: Tue, 04 Nov 2025 01:32:35 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:171c082cd86f6d465311384dc89b6f8caef5ba756bac4b22acc5740480c28923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bca970acfe0d4594fdb6fa5375fc79bd72f1c0309d3fcd6644884295e7a995`

```dockerfile
```

-	Layers:
	-	`sha256:e6a4a640a7d1de22f588ad1235c812b9907faedeac55c9b05d4fc71a53fe4317`  
		Last Modified: Tue, 04 Nov 2025 11:09:53 GMT  
		Size: 3.6 MB (3614602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11690b726c377ad7c6177f469ec7805bdb379cb0e37fd6d69b8c57d618893f46`  
		Last Modified: Tue, 04 Nov 2025 11:09:53 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:5771d15f06fa62ffa39ee92437de3260e58824c9c3aca71b930f2340dd55319c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61357929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae41e42556a48153e417d850113110e79e617019f105a3699f765baf91edbacc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:38:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:38:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:38:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:38:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:933c2eb03a495d1bdbab772ff092366c6df6bb75cafd8749623e94908401abca`  
		Last Modified: Tue, 04 Nov 2025 00:13:58 GMT  
		Size: 50.8 MB (50801238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c3eaf959f47b3c81adaab22c02b91552da31d1998da6c88911ad6288b7a9fb`  
		Last Modified: Tue, 04 Nov 2025 01:38:50 GMT  
		Size: 10.5 MB (10462757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e9ef740b4bb48f2974e682a417cb34fceb185aca217d1c2c7f6227a748dd40`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242bf4e4c9cf11d3df4c63f4db58331b50dfdde7542f70fffe6271a6cef67b5c`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7804e0ac9d5bfb67777d18126743dfa3501a6cab30e2779e9c1e882d3931d3b`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 90.6 KB (90584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f31b454367cf57f9fdcbbcbabe35b3a537175a9cbf95e0455aa5c68268299`  
		Last Modified: Tue, 04 Nov 2025 01:38:49 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fadfe623ab9931f7482ec50383c61bca36e19d1881f7b599d5a47feb0ee6dd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e8ea8d062af83ff955f51cd8b7f77e408cb8628ee432dade259fd59a85c1b7`

```dockerfile
```

-	Layers:
	-	`sha256:088a395d40071397cf8e0032ab14cbcabec0416a8a0a34130b1268e1fe736e89`  
		Last Modified: Tue, 04 Nov 2025 22:51:34 GMT  
		Size: 3.6 MB (3611024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc01ac211e92ee4d0d4707e08a6fb4c64315bf3561a027a8594a15e46d12b72`  
		Last Modified: Tue, 04 Nov 2025 22:51:35 GMT  
		Size: 16.2 KB (16246 bytes)  
		MIME: application/vnd.in-toto+json
