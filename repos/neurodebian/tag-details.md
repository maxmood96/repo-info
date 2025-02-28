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
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd20.04`](#neurodebiannd2004)
-	[`neurodebian:nd20.04-non-free`](#neurodebiannd2004-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:nd24.04`](#neurodebiannd2404)
-	[`neurodebian:nd24.04-non-free`](#neurodebiannd2404-non-free)
-	[`neurodebian:noble`](#neurodebiannoble)
-	[`neurodebian:noble-non-free`](#neurodebiannoble-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:892145a819ec106bc50f378387b90c02c8bcb7d45bcb557ad8135bbbc0ed2de6
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
$ docker pull neurodebian@sha256:4734a0d13d4bcbec3944f83770c629cdd4f87c9367e50e71caa37ed96091fa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59838027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12437e9e000486e4e0471e98d352f9a11d3578f484445258e1c2e9285550b86`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1aa091210c71c21e513181372a894d1632574508fffe7828fdd4fe7f4960f5`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 11.3 MB (11266798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea57e78d1797cbd6beb44d0bb0091099cd91eb9a3b52f0df3748bf68fe6e4da7`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015f278840a5a2073510c8fa50bc3fd105b5eabb2c21586361b9261929f4eace`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1577d1efc8f42721fbde6322fa7aaf7ff9e8cfb0e9903554fd38219451b6db`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 93.1 KB (93140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5856d03fa8bd4c96dff4f6fdf7039b126daadec1708eadfb4e0120c80f6213e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05e0d25ea294b77017f8e39123bb2441d9948c72705f235e05048054bc0cb96`

```dockerfile
```

-	Layers:
	-	`sha256:9d54ad43f4fe81b1e5911165dc8a9c05b70075c2c167a57a1fa431b05759b31b`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 3.9 MB (3932828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7862e59544d59e1dd343e6096106c4e4f32c6092bc8837175f5e0999ede6d94`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 14.0 KB (14000 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:33273b79aef6b560450f7930e7d5b2aab0ed20171f2ccfdcfe08f4b44c39b77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59636006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9056e9d1bc0fa6d68726bb1e713d5c2bf109be7a38765b58ec83751d255bd57`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4268effafc2bde885b308f4884da9a5675b21ea9dd10510af4cc390b22435225`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 11.2 MB (11232612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc8fd8ac1e89535a292d7b52efd5bea69c5f5c3851d37b9929659c0c6c042e`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe958a62bf286f5dab55b9feda9c4012922a2405bd34a8e0570b16801e9f1257`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeac118fe924197167da22818e9394a97999867f5e156777e4fcae652229797`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5bf0cf8bbd1552b5d307d189245c140355110008ba5b6d9832c6ac1e62ba330c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525930528ba4ba80cfc5b521e56fa2ac63fc986653c44edb81e1e2b88c04ec1f`

```dockerfile
```

-	Layers:
	-	`sha256:e3d84d2a8929cbdbcfd209768df78069a10fef211f62d7e294dfde2623c7f6aa`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 3.9 MB (3933082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8dd43cbc32f3db75eeb3b3f29b6c6352e2df38a36dd0feb09ea39aa4c04adaf`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 14.1 KB (14136 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:045529ad0e1a2323aae87c4f540f6a3b2e88516ed66c40b07b3eeadb82140fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dabf5edb97ea752e3861fe71d5da288dd065365656c1e8d869b79b467ce33f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06db2eb6124e849508d76e7b9f52369bbaf025a9b535513aeb226ec87e4b5c87`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 11.7 MB (11688923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b690958c17f8254fba7767793a8227fc40ea085973d753fe2c39708a9968e024`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d929ae2564cc35ddd3b993dab4283cdf38fa6beaba29c0c1097521d54917bb`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8701c8177798bc525467c9eaca4ad5bdaeb247310c0d2bde0a1e4fbdeecd7c8b`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 93.2 KB (93228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aee2fbc68d1b7fe46dbdc53656f8d02520f4a1f5e9dd90f4c7ed8b9647479428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ec8a2050ee31cf237ed440a821263f7c0c2425ca7aec82f085d506b881e4fa`

```dockerfile
```

-	Layers:
	-	`sha256:ec23be925f2f0bd074b9b75ab63b0cc12ab36b3b34bef80dba01b31642aa6cb1`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 3.9 MB (3930745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de76ded408b913df6c3ad9bef25422985ed7eb4dc3e8ac94e982b459f8f2aca2`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:5f1c4ffb3aaec94eb85ba6d1159dbaa5d6058199f3c0a84887ab78b469a56d94
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
$ docker pull neurodebian@sha256:86d0f1e008c22ef1371791860617d59b2e903a4d642e928b30e47fa6b181da18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59838474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde7ea88b09684b422a1ac05b6b2ad01622129128e5db57512bdd2f99aa342b4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28441ab853fef772e1e1de08ec36f3ed7180ff3c2a9b9c9e671357202dcdd42`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 11.3 MB (11266799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505ff7e6422a09a3eb1a239312fcdaa2044a0e3eefd0c31485b820c54e4b7967`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d76303fdb4aa5d6083836c5414c3e64b7b9e08dfa94e4900c30eba602003b37`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179af51425b94c30d8dc80554e3ef4c9003f44a94784a75458c79f151ab32c10`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 93.2 KB (93157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36083d574b636b75357cbc3e722a118cdd90d3d27dd10a838646f855d03bc976`  
		Last Modified: Tue, 25 Feb 2025 02:27:21 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:672e5a788f4e12dd192919f23b3cdcc8c247268af0e4c265c3b187946806ca98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94236d5f014c5f6d7cd9746c73b7ebabab74fd82e06f0c1da40d26af73f6b90`

```dockerfile
```

-	Layers:
	-	`sha256:31b0617d5bc927443e4c297613d85abb99148b4e4f2e104f826075d993c933b7`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 3.9 MB (3932868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f7b4463e7f6d4ef42c049f42246d69980142348e3e7e3a4ef61fb6eb3128006`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:abb99c9c2f059106da856b9d569b4d8b7ca84af59582e6a68cef696edd394382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59636435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a022a8b30b7ae18ba216b15f04cbe65382f23139ec4b2b210764daa78ad1fbb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4268effafc2bde885b308f4884da9a5675b21ea9dd10510af4cc390b22435225`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 11.2 MB (11232612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc8fd8ac1e89535a292d7b52efd5bea69c5f5c3851d37b9929659c0c6c042e`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe958a62bf286f5dab55b9feda9c4012922a2405bd34a8e0570b16801e9f1257`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeac118fe924197167da22818e9394a97999867f5e156777e4fcae652229797`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd5763534ceb76e91f0383484f364058ab48c26cef0fb32914ddad1372da0f8`  
		Last Modified: Tue, 25 Feb 2025 06:12:50 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e7c7ed56d0e480fae65c8cde83e1d1adbc75c0a9a9fced612884ab3a96416e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0204f4c376b7e83a2ff9a754d837369ce083d2bccb96e91a0b065a72eaf2d6`

```dockerfile
```

-	Layers:
	-	`sha256:1737f3c716a72e8e417e4d27d5f130b9ad3b8d0a1374350ae0b58459419195a8`  
		Last Modified: Tue, 25 Feb 2025 06:12:51 GMT  
		Size: 3.9 MB (3933122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fad213bc7f30b41f083d0ea35cc189d394c753fdac72d9e11045dadb9bb777a`  
		Last Modified: Tue, 25 Feb 2025 06:12:50 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:14ea109b5493111055a5aaa853884637148ae4dc485ea5c4e267bdb1add74a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61243186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a7ea209e5b0e6d013100f17eff90f4100955ab738acde7026b6c79cabce3e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52022fd04bcf4f92943afd60360f0ecc2322d7d18d6a0abe22a2cdfe8bcecf6`  
		Last Modified: Tue, 25 Feb 2025 02:12:30 GMT  
		Size: 11.7 MB (11689076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900a00b32801477083168732fb13544e2003e9538368e35080da03e1b17fb70f`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d197c332a3b1cc7550c3bff0a9d351b9730cc7493035604b55fd1b1407153255`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf3e2f6fb6f036e3845a4a8b6ee926f3c8d48e922eda645aabbe2681ca3fc57`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 93.2 KB (93240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b9cbc42e9997903403815a1064c86c6cb272ea90c7fc977f69733045254639`  
		Last Modified: Tue, 25 Feb 2025 02:12:30 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d24e1d2b84e10d04805b51e11dd0c50d764501f818f8967b77329b63d229d33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021833d77fdeb79557411acea2ed9985e2d023e575a7287135cb2e1166396447`

```dockerfile
```

-	Layers:
	-	`sha256:335ee5030d46d154190ee10eca81ff2e045c93fb885778864658042d9925fc8a`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 3.9 MB (3930785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:578220ae32d85546c71d91eb6f5654e7c4554c058444cf7711da0b069bef4176`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:58a79d16e7a892c7a9b205ac6b6fc5cbaf75dd3abd45011c0495b6c36bb231b4
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
$ docker pull neurodebian@sha256:255fdb245facc56597ae9b5b225347c9299a146aadacd840189b2b52be189ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64949644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b449ad722cd075d476b244aed68df11ef85b5f61cac4ed6190ac5fa6e850df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a21ad05e392fee8d676440be99dd209ac18de59baa992f707e67b7521df0b6f`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 11.1 MB (11105054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a68e13233f02b4104031993a0684cc1d882e1ac9ede7c81ff542bba3753b5d`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea73ea3f21ff7c2c3cd991b901ff12faf26526caf9d030ec0dc48c01494e35d`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a580996243e3cc1edfeab84f80d57b91cfe0c769853ddc306ec0fa2d61b92ce`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 101.2 KB (101201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ee411d1056c0875d426587f84fd261fa8611ad1c3896cfdd5e825889608a4094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235826dffcc85d41f141da43c90b3a0bdd7d9ace4a10e6d8736c35cb0d0e2b85`

```dockerfile
```

-	Layers:
	-	`sha256:b228de3db05de80fd3f25e54a24bc022f75c3fc059ea2b75832bdb6ab25f659b`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 4.2 MB (4232796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92056a0eb241a620f5b51893b1c44746c7a38dd857e05ea98b9a9c29aa54d1da`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 13.7 KB (13693 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7ad9866c68ff2e19c7299cdb0d9878887cad56c503d83edda51a6712b9f1957e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f2001048eb7c80b6aeaa49269443f9792a9706f622822896abbe5a84d57c42`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78070b166a3b33e5e36dba2e5c6120eb0be4da63e2fadac8989546e77ed84127`  
		Last Modified: Tue, 25 Feb 2025 06:12:12 GMT  
		Size: 11.1 MB (11106135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6409cb1b4b20c21ebb839fc02573f587d35015a457c2a28f6ca099e3cb617b6`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addb1300d0acb93feafce5997490005d13990da5be84a9c0439e886cf3f9800e`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a370d124f43fbbdc6183d48f50d75083b3c2260f2deb41bd6be13b1408428247`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 101.1 KB (101121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f8829cd60b8151bb6843bc62acbca2f6215345cecb217996d00299d68001ed9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df58af517ef2c2b0c94f3bf5a81f4d4a8c2ff00b52e3f3cff3dd1164cc0ff7e5`

```dockerfile
```

-	Layers:
	-	`sha256:af2867479a8ea8851fc9af29c621493be023e1e07882b38427000321f7ef7c06`  
		Last Modified: Tue, 25 Feb 2025 11:26:47 GMT  
		Size: 4.2 MB (4232403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ffb769122edce0984f644047190e6eb18719120068faf3447665649c0b7e669`  
		Last Modified: Tue, 25 Feb 2025 11:26:46 GMT  
		Size: 13.8 KB (13817 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:b9b68a2c030f7816a446102efc01b832a31d88e8e1fca95e90b347113d66ebd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66282360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd3b7662aa6fa7dfbcdc31a0f3b16bf895d779ffa358418f30a1c362cbe7835`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ee56fa4339347a5d9819313a3c54d7a27c7cb5b8d5cc000ffd621148a2d4bd`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 11.5 MB (11500400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623551ff0580ebfcd93cda07f359615669ed2b060f30806734fa12c97c1c2d5f`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d499538f85e1b885adb4a58422c8c4e7e67ae2ef1d8610a84f6768bca9ac071`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79821c0508cdb29d85e661e1a99e8f83683500bca6747943a84dd34dde2b1df0`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 101.1 KB (101104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b61186c3d9e091e599ec9124821991256c93bac976bcae94a4daf4813c86c03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9a496f2a67b7d3857b9409a40da1a518023ffb63a34302a3c28bc774f065e6`

```dockerfile
```

-	Layers:
	-	`sha256:60dd1d2a40d86039f2e85dbab1797c9b022a0664a6e0d2b5b87ced8f62ca7ef9`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 4.2 MB (4229258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845bb2b878bc2a3e85eb925ee5bd62253faa04a947f6688ffce7309902fbc387`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 13.7 KB (13665 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:fa14dfb099c1f60f37fcfbb68d24e96c8220648c087c4951b8221c4f15f54651
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
$ docker pull neurodebian@sha256:8d63c53715ca04153f29d307032b15af604a09d09b77f59650cf848a3ff608e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64950026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229aed07a08563adf03dcc3bfcd2e3760f3949366c2d468b1310001d9ae9757b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f6fd7e0223cdb148d5d913c07f6babb1568f0b86b7f9ccfc45369f5e324987`  
		Last Modified: Tue, 25 Feb 2025 02:27:00 GMT  
		Size: 11.1 MB (11105064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c963f1c8f82ad189a5fc4b0f31b35cbde49379ef9b0ea9b811bb4d5a5ca77c6`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8704f813802b2ceaa6dd7637c468ab12a1006422aa69e5e7d489cd115a799ad`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b485ca6b951ab61bb5c0b158a544c43accbda527cad07cc5b9b5220319ceb348`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 101.2 KB (101211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd86c041609621d93bac1450edc528f252eb3ebac4b2f75fa5bdcbc6a2cb473`  
		Last Modified: Tue, 25 Feb 2025 02:27:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0df95cb09083c0e0b21182c4b274d27c968294d38a549738fde69702a1fc62d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c614534c484237f1b3623825e24962fd19d58efc9d22f06240977e3d39cfca`

```dockerfile
```

-	Layers:
	-	`sha256:7485d10d0dccf6932268f1ae0c302116cd9544ae22dbce2bf6d2cb6aa4bcdb78`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 4.2 MB (4232832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f847d9340aa4eae840c9d35f745ee6db4ed0710d06fd2381e5fa4521e0b84b6`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fa0a21fbc593bcd4c4cddecf5566737a05119d0dd75e704154108ca666faaf75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63458252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b67c0a0108ca2e350e62488892e3ffcd76911c2c64c00b2bb86d00f9b017e61`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78070b166a3b33e5e36dba2e5c6120eb0be4da63e2fadac8989546e77ed84127`  
		Last Modified: Tue, 25 Feb 2025 06:12:12 GMT  
		Size: 11.1 MB (11106135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6409cb1b4b20c21ebb839fc02573f587d35015a457c2a28f6ca099e3cb617b6`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addb1300d0acb93feafce5997490005d13990da5be84a9c0439e886cf3f9800e`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a370d124f43fbbdc6183d48f50d75083b3c2260f2deb41bd6be13b1408428247`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 101.1 KB (101121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed13c1be8af2ff3c91844087d22483e86ef6700f90d3abc4ad40b44d327c9802`  
		Last Modified: Tue, 25 Feb 2025 06:12:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:119edf88da61fae4ada4c0e291f86f9231f9c3a19a2e96aab9501610333197db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d0f2788db64938ae99af7035a20a134d5c8b97ab2b0acbf63f2b1260b3c724`

```dockerfile
```

-	Layers:
	-	`sha256:34809246ca54eb8c61ede6a4e92fc0ee570cdc57564d7c18b9ad52b607daad1a`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 4.2 MB (4232439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af4fb6f4bc826f690e2883cbfe1e142b21f2186dc770b02535ac7ccb19b7cc7`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 15.9 KB (15861 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bda7ef7ecd9283b7822b07b53f221a06ba49fe489060c8a9508d82e98f19bb8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66282729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b064cfaa3cf2dab53ecb8c8de999dfc5d23f3c411e2325896a9a89394c8b02c7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484422fd4a1d6ec8ee86b88a25b7b6de58842c0a9766192f8aecc828773d4fb4`  
		Last Modified: Tue, 25 Feb 2025 02:25:41 GMT  
		Size: 11.5 MB (11500408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b0d8ab6eda4034ddfc4abf4375bb7c39167373be9c5b8855cf35709d1ab05f`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8a333b07c35d233d46d7299bb98c76c919c06db1f4b65e5162c094a47a5e45`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630be2d9eda0730b7509b08fc22cc48cb4b2eac0b889ca41056dc7b28e6ac464`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 101.1 KB (101108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99d797416760116642baffb3f545f96399dfdd457f6ee83878d72a6226b27a0`  
		Last Modified: Tue, 25 Feb 2025 02:25:41 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2a099be5c16e0ef0a587fc39e2b0c0256c7e453cc89738defc3c6fb1b01b4435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157a091dddd9c3609266c5ae727ab24372cedd9e442aad30db1105e60ae0cbe3`

```dockerfile
```

-	Layers:
	-	`sha256:cbc827a05c0eb7c5911633103469d0490d1e56755eb0b1b0cf2748ad4eece5b5`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 4.2 MB (4229294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79c2802a2c27fb32ac6e543ac9e274c3da613e921c48a1c00719150e87b37c16`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 15.7 KB (15690 bytes)  
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
$ docker pull neurodebian@sha256:dddd5dfbc7fd007f4a3e728570835205318a059509fe698a32190ff096b1777a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:5f26675bcc90c8758ac288c5e42b178ff48a73e9ab4970f919e5ec4938cbd460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33271586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d5a7ae88d753f13e79fa4bb43d53cbf4cfed9fadba34ab474f4099807fe261`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63336557e3a88e2b6816b75ec69356976ec7a6330214bfa441e5d86b8bcd5fab`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 3.6 MB (3623158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f3b6cde57e753607cb5d03b5f4df97fcabbea0a03734d33c7a056556b608b4`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6389250b72dfd734ad1e61588b821ac38d8a3035405ce0dce0746dc8aa07fd94`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128920b07afa9e2ab5a724db970a1017a3839518a53c5829c82e7a6dce0154eb`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 110.5 KB (110492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c671d1877f1ca886adc735145c09a8b212ebf717dab82aafc170b00ada8f0890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb200fcf794b88cfdfe58fbf9fe7c5df4dd58d5af47ef863b77847b1ce789695`

```dockerfile
```

-	Layers:
	-	`sha256:495ed7fc83baeda0269343c97821047e2c68647a9c3b5d70f448b4caa68577c6`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 2.1 MB (2055319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baa3488be0939d3a148d71befa440ae927009daca74013dc5ec80152a7933da1`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 13.7 KB (13660 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:67728fb8e5cd3818b91715960c1bba0a0c0023bcabcd5671bc64df1d9df72da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f3f7d90cc1fbbefb0d8442ab9c23a806f90fef8b03dc4fdc5f1203b74992d3`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa83e4278dc6cff1ef0b2ddfdcdb95e8b576852125603aff18c4adbd62abfa`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 3.6 MB (3594385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f206a367506b9a6e0da2a087a15345608f59c46aed8faaf14965a2048a684`  
		Last Modified: Tue, 04 Feb 2025 10:12:44 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d2194ff2bd3e4e851f237645c0bd78afd3a389c1df83bc989d3245af146c30`  
		Last Modified: Tue, 04 Feb 2025 10:12:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e4837f465facfb077234adc2a993e2a512c6e94506c37f467ca0d03c95b7d4`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 110.3 KB (110348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9bb6e8c0c274860bac8c67b48375fd3b636f078b902c99d7683b178b98154e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f0655895d6ff3d027802a83acd357d94c7309434a0a7690073fd3df7bb1ef0`

```dockerfile
```

-	Layers:
	-	`sha256:5d3714f689f360f18f642041f406b8692c6373b6cdc03d9b4e616e7686ccb86e`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 2.1 MB (2055579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ad1910f3d5ccf7f20eac6a6cb65c3a203059bb8a4456258e696ec7fdc164d80`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:f03ae0a3cf4075547117b044adb41f16fad47137475cff997d41f3357cde975c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3c4173d5c31f8a53bbc0a2a190f78ae51e471618ee01069ecb2bc9459e952711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33271759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c3eaa4493fd2df3d65ef60c7b8dd8c63eae0ac0c17408e4f82998765182296`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d717b5746fc604b8417f674bfe4b267ccadca9c7c126b92991bb31d94d6d6b7`  
		Last Modified: Tue, 04 Feb 2025 04:25:09 GMT  
		Size: 3.6 MB (3623114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e87505a43c5a5f52ac9d7e93021419084501f715570763864d7f2bdc6068673`  
		Last Modified: Tue, 04 Feb 2025 04:25:09 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053c5ad118ff70f2b8fdd9a491743706d705020d0bfea7c71eaf3310c489a5bf`  
		Last Modified: Tue, 04 Feb 2025 04:25:09 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f757a34e2e1124f50485ed20bdf68b036a063a9ab34355a1c1676add6b438ae6`  
		Last Modified: Tue, 04 Feb 2025 04:25:09 GMT  
		Size: 110.5 KB (110450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43befb502973bc3768fe50fa6753ba9e0312654b012cf9db16a8f3eec23f6128`  
		Last Modified: Tue, 04 Feb 2025 04:25:10 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d4aee3cf707c745d560848ee49f052f203b32be18254a0bbd7f2ce026eaf6a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819d998f536ecd2c60c7f2c1fae4e361a91cb740ffe9608f690e12a03cc7a946`

```dockerfile
```

-	Layers:
	-	`sha256:f15b7681a6f1a10496fdb2eb02b4e22066edbd9abe4f3efc6912aa38e15e9840`  
		Last Modified: Tue, 04 Feb 2025 04:25:09 GMT  
		Size: 2.1 MB (2055355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f21fdeb65e657559fe924fe74b95df4e2b1157ff5ec18a4818715ed15fc51fe4`  
		Last Modified: Tue, 04 Feb 2025 04:25:09 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6ea935711d8e169b474d27073a01d3e0359878eadd283d1d93c4b577e8865490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31065166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30946598065f707a13ed26bb51018e6af24620a760b2293815ac5fa249b399bd`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa83e4278dc6cff1ef0b2ddfdcdb95e8b576852125603aff18c4adbd62abfa`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 3.6 MB (3594385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f206a367506b9a6e0da2a087a15345608f59c46aed8faaf14965a2048a684`  
		Last Modified: Tue, 04 Feb 2025 10:12:44 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d2194ff2bd3e4e851f237645c0bd78afd3a389c1df83bc989d3245af146c30`  
		Last Modified: Tue, 04 Feb 2025 10:12:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e4837f465facfb077234adc2a993e2a512c6e94506c37f467ca0d03c95b7d4`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 110.3 KB (110348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a2ce10ded06c3c89836d98dfe75aead8f6debf35261552961af34a3119d6b1`  
		Last Modified: Tue, 04 Feb 2025 10:13:04 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:eb6374ed9f5170068bbb23a3e58b7e61160c4e7b470845ee5877ebf2543b918e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb51f2b28516c23cabf829951e9a87e36097ef1710bdd7d6e3751483722042a0`

```dockerfile
```

-	Layers:
	-	`sha256:e4d312d6a85d3cee621fb1e24d7113e9b1fdce62a9b59001e0ebe7e369513403`  
		Last Modified: Tue, 04 Feb 2025 10:13:04 GMT  
		Size: 2.1 MB (2055615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c11f32963ab6bbbf1720c95e40fd72388ca05ebf764915eeca181050b953db0`  
		Last Modified: Tue, 04 Feb 2025 10:13:04 GMT  
		Size: 16.0 KB (16029 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:892145a819ec106bc50f378387b90c02c8bcb7d45bcb557ad8135bbbc0ed2de6
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
$ docker pull neurodebian@sha256:4734a0d13d4bcbec3944f83770c629cdd4f87c9367e50e71caa37ed96091fa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59838027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12437e9e000486e4e0471e98d352f9a11d3578f484445258e1c2e9285550b86`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1aa091210c71c21e513181372a894d1632574508fffe7828fdd4fe7f4960f5`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 11.3 MB (11266798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea57e78d1797cbd6beb44d0bb0091099cd91eb9a3b52f0df3748bf68fe6e4da7`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015f278840a5a2073510c8fa50bc3fd105b5eabb2c21586361b9261929f4eace`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1577d1efc8f42721fbde6322fa7aaf7ff9e8cfb0e9903554fd38219451b6db`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 93.1 KB (93140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5856d03fa8bd4c96dff4f6fdf7039b126daadec1708eadfb4e0120c80f6213e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05e0d25ea294b77017f8e39123bb2441d9948c72705f235e05048054bc0cb96`

```dockerfile
```

-	Layers:
	-	`sha256:9d54ad43f4fe81b1e5911165dc8a9c05b70075c2c167a57a1fa431b05759b31b`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 3.9 MB (3932828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7862e59544d59e1dd343e6096106c4e4f32c6092bc8837175f5e0999ede6d94`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 14.0 KB (14000 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:33273b79aef6b560450f7930e7d5b2aab0ed20171f2ccfdcfe08f4b44c39b77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59636006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9056e9d1bc0fa6d68726bb1e713d5c2bf109be7a38765b58ec83751d255bd57`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4268effafc2bde885b308f4884da9a5675b21ea9dd10510af4cc390b22435225`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 11.2 MB (11232612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc8fd8ac1e89535a292d7b52efd5bea69c5f5c3851d37b9929659c0c6c042e`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe958a62bf286f5dab55b9feda9c4012922a2405bd34a8e0570b16801e9f1257`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeac118fe924197167da22818e9394a97999867f5e156777e4fcae652229797`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5bf0cf8bbd1552b5d307d189245c140355110008ba5b6d9832c6ac1e62ba330c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525930528ba4ba80cfc5b521e56fa2ac63fc986653c44edb81e1e2b88c04ec1f`

```dockerfile
```

-	Layers:
	-	`sha256:e3d84d2a8929cbdbcfd209768df78069a10fef211f62d7e294dfde2623c7f6aa`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 3.9 MB (3933082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8dd43cbc32f3db75eeb3b3f29b6c6352e2df38a36dd0feb09ea39aa4c04adaf`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 14.1 KB (14136 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:045529ad0e1a2323aae87c4f540f6a3b2e88516ed66c40b07b3eeadb82140fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dabf5edb97ea752e3861fe71d5da288dd065365656c1e8d869b79b467ce33f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06db2eb6124e849508d76e7b9f52369bbaf025a9b535513aeb226ec87e4b5c87`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 11.7 MB (11688923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b690958c17f8254fba7767793a8227fc40ea085973d753fe2c39708a9968e024`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d929ae2564cc35ddd3b993dab4283cdf38fa6beaba29c0c1097521d54917bb`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8701c8177798bc525467c9eaca4ad5bdaeb247310c0d2bde0a1e4fbdeecd7c8b`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 93.2 KB (93228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aee2fbc68d1b7fe46dbdc53656f8d02520f4a1f5e9dd90f4c7ed8b9647479428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ec8a2050ee31cf237ed440a821263f7c0c2425ca7aec82f085d506b881e4fa`

```dockerfile
```

-	Layers:
	-	`sha256:ec23be925f2f0bd074b9b75ab63b0cc12ab36b3b34bef80dba01b31642aa6cb1`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 3.9 MB (3930745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de76ded408b913df6c3ad9bef25422985ed7eb4dc3e8ac94e982b459f8f2aca2`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:58a79d16e7a892c7a9b205ac6b6fc5cbaf75dd3abd45011c0495b6c36bb231b4
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
$ docker pull neurodebian@sha256:255fdb245facc56597ae9b5b225347c9299a146aadacd840189b2b52be189ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64949644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b449ad722cd075d476b244aed68df11ef85b5f61cac4ed6190ac5fa6e850df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a21ad05e392fee8d676440be99dd209ac18de59baa992f707e67b7521df0b6f`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 11.1 MB (11105054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a68e13233f02b4104031993a0684cc1d882e1ac9ede7c81ff542bba3753b5d`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea73ea3f21ff7c2c3cd991b901ff12faf26526caf9d030ec0dc48c01494e35d`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a580996243e3cc1edfeab84f80d57b91cfe0c769853ddc306ec0fa2d61b92ce`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 101.2 KB (101201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ee411d1056c0875d426587f84fd261fa8611ad1c3896cfdd5e825889608a4094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235826dffcc85d41f141da43c90b3a0bdd7d9ace4a10e6d8736c35cb0d0e2b85`

```dockerfile
```

-	Layers:
	-	`sha256:b228de3db05de80fd3f25e54a24bc022f75c3fc059ea2b75832bdb6ab25f659b`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 4.2 MB (4232796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92056a0eb241a620f5b51893b1c44746c7a38dd857e05ea98b9a9c29aa54d1da`  
		Last Modified: Tue, 25 Feb 2025 02:26:58 GMT  
		Size: 13.7 KB (13693 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7ad9866c68ff2e19c7299cdb0d9878887cad56c503d83edda51a6712b9f1957e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f2001048eb7c80b6aeaa49269443f9792a9706f622822896abbe5a84d57c42`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78070b166a3b33e5e36dba2e5c6120eb0be4da63e2fadac8989546e77ed84127`  
		Last Modified: Tue, 25 Feb 2025 06:12:12 GMT  
		Size: 11.1 MB (11106135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6409cb1b4b20c21ebb839fc02573f587d35015a457c2a28f6ca099e3cb617b6`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addb1300d0acb93feafce5997490005d13990da5be84a9c0439e886cf3f9800e`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a370d124f43fbbdc6183d48f50d75083b3c2260f2deb41bd6be13b1408428247`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 101.1 KB (101121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f8829cd60b8151bb6843bc62acbca2f6215345cecb217996d00299d68001ed9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df58af517ef2c2b0c94f3bf5a81f4d4a8c2ff00b52e3f3cff3dd1164cc0ff7e5`

```dockerfile
```

-	Layers:
	-	`sha256:af2867479a8ea8851fc9af29c621493be023e1e07882b38427000321f7ef7c06`  
		Last Modified: Tue, 25 Feb 2025 11:26:47 GMT  
		Size: 4.2 MB (4232403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ffb769122edce0984f644047190e6eb18719120068faf3447665649c0b7e669`  
		Last Modified: Tue, 25 Feb 2025 11:26:46 GMT  
		Size: 13.8 KB (13817 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:b9b68a2c030f7816a446102efc01b832a31d88e8e1fca95e90b347113d66ebd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66282360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd3b7662aa6fa7dfbcdc31a0f3b16bf895d779ffa358418f30a1c362cbe7835`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ee56fa4339347a5d9819313a3c54d7a27c7cb5b8d5cc000ffd621148a2d4bd`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 11.5 MB (11500400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623551ff0580ebfcd93cda07f359615669ed2b060f30806734fa12c97c1c2d5f`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d499538f85e1b885adb4a58422c8c4e7e67ae2ef1d8610a84f6768bca9ac071`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79821c0508cdb29d85e661e1a99e8f83683500bca6747943a84dd34dde2b1df0`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 101.1 KB (101104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b61186c3d9e091e599ec9124821991256c93bac976bcae94a4daf4813c86c03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4242923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9a496f2a67b7d3857b9409a40da1a518023ffb63a34302a3c28bc774f065e6`

```dockerfile
```

-	Layers:
	-	`sha256:60dd1d2a40d86039f2e85dbab1797c9b022a0664a6e0d2b5b87ced8f62ca7ef9`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 4.2 MB (4229258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845bb2b878bc2a3e85eb925ee5bd62253faa04a947f6688ffce7309902fbc387`  
		Last Modified: Tue, 25 Feb 2025 02:25:33 GMT  
		Size: 13.7 KB (13665 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:fa14dfb099c1f60f37fcfbb68d24e96c8220648c087c4951b8221c4f15f54651
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
$ docker pull neurodebian@sha256:8d63c53715ca04153f29d307032b15af604a09d09b77f59650cf848a3ff608e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64950026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229aed07a08563adf03dcc3bfcd2e3760f3949366c2d468b1310001d9ae9757b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f6fd7e0223cdb148d5d913c07f6babb1568f0b86b7f9ccfc45369f5e324987`  
		Last Modified: Tue, 25 Feb 2025 02:27:00 GMT  
		Size: 11.1 MB (11105064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c963f1c8f82ad189a5fc4b0f31b35cbde49379ef9b0ea9b811bb4d5a5ca77c6`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8704f813802b2ceaa6dd7637c468ab12a1006422aa69e5e7d489cd115a799ad`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b485ca6b951ab61bb5c0b158a544c43accbda527cad07cc5b9b5220319ceb348`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 101.2 KB (101211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd86c041609621d93bac1450edc528f252eb3ebac4b2f75fa5bdcbc6a2cb473`  
		Last Modified: Tue, 25 Feb 2025 02:27:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0df95cb09083c0e0b21182c4b274d27c968294d38a549738fde69702a1fc62d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c614534c484237f1b3623825e24962fd19d58efc9d22f06240977e3d39cfca`

```dockerfile
```

-	Layers:
	-	`sha256:7485d10d0dccf6932268f1ae0c302116cd9544ae22dbce2bf6d2cb6aa4bcdb78`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 4.2 MB (4232832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f847d9340aa4eae840c9d35f745ee6db4ed0710d06fd2381e5fa4521e0b84b6`  
		Last Modified: Tue, 25 Feb 2025 02:26:59 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fa0a21fbc593bcd4c4cddecf5566737a05119d0dd75e704154108ca666faaf75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63458252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b67c0a0108ca2e350e62488892e3ffcd76911c2c64c00b2bb86d00f9b017e61`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78070b166a3b33e5e36dba2e5c6120eb0be4da63e2fadac8989546e77ed84127`  
		Last Modified: Tue, 25 Feb 2025 06:12:12 GMT  
		Size: 11.1 MB (11106135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6409cb1b4b20c21ebb839fc02573f587d35015a457c2a28f6ca099e3cb617b6`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addb1300d0acb93feafce5997490005d13990da5be84a9c0439e886cf3f9800e`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a370d124f43fbbdc6183d48f50d75083b3c2260f2deb41bd6be13b1408428247`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 101.1 KB (101121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed13c1be8af2ff3c91844087d22483e86ef6700f90d3abc4ad40b44d327c9802`  
		Last Modified: Tue, 25 Feb 2025 06:12:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:119edf88da61fae4ada4c0e291f86f9231f9c3a19a2e96aab9501610333197db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d0f2788db64938ae99af7035a20a134d5c8b97ab2b0acbf63f2b1260b3c724`

```dockerfile
```

-	Layers:
	-	`sha256:34809246ca54eb8c61ede6a4e92fc0ee570cdc57564d7c18b9ad52b607daad1a`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 4.2 MB (4232439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af4fb6f4bc826f690e2883cbfe1e142b21f2186dc770b02535ac7ccb19b7cc7`  
		Last Modified: Tue, 25 Feb 2025 06:12:11 GMT  
		Size: 15.9 KB (15861 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bda7ef7ecd9283b7822b07b53f221a06ba49fe489060c8a9508d82e98f19bb8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66282729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b064cfaa3cf2dab53ecb8c8de999dfc5d23f3c411e2325896a9a89394c8b02c7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484422fd4a1d6ec8ee86b88a25b7b6de58842c0a9766192f8aecc828773d4fb4`  
		Last Modified: Tue, 25 Feb 2025 02:25:41 GMT  
		Size: 11.5 MB (11500408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b0d8ab6eda4034ddfc4abf4375bb7c39167373be9c5b8855cf35709d1ab05f`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8a333b07c35d233d46d7299bb98c76c919c06db1f4b65e5162c094a47a5e45`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630be2d9eda0730b7509b08fc22cc48cb4b2eac0b889ca41056dc7b28e6ac464`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 101.1 KB (101108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99d797416760116642baffb3f545f96399dfdd457f6ee83878d72a6226b27a0`  
		Last Modified: Tue, 25 Feb 2025 02:25:41 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2a099be5c16e0ef0a587fc39e2b0c0256c7e453cc89738defc3c6fb1b01b4435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4244984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157a091dddd9c3609266c5ae727ab24372cedd9e442aad30db1105e60ae0cbe3`

```dockerfile
```

-	Layers:
	-	`sha256:cbc827a05c0eb7c5911633103469d0490d1e56755eb0b1b0cf2748ad4eece5b5`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 4.2 MB (4229294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79c2802a2c27fb32ac6e543ac9e274c3da613e921c48a1c00719150e87b37c16`  
		Last Modified: Tue, 25 Feb 2025 02:25:40 GMT  
		Size: 15.7 KB (15690 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:892145a819ec106bc50f378387b90c02c8bcb7d45bcb557ad8135bbbc0ed2de6
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
$ docker pull neurodebian@sha256:4734a0d13d4bcbec3944f83770c629cdd4f87c9367e50e71caa37ed96091fa90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59838027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12437e9e000486e4e0471e98d352f9a11d3578f484445258e1c2e9285550b86`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1aa091210c71c21e513181372a894d1632574508fffe7828fdd4fe7f4960f5`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 11.3 MB (11266798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea57e78d1797cbd6beb44d0bb0091099cd91eb9a3b52f0df3748bf68fe6e4da7`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015f278840a5a2073510c8fa50bc3fd105b5eabb2c21586361b9261929f4eace`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1577d1efc8f42721fbde6322fa7aaf7ff9e8cfb0e9903554fd38219451b6db`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 93.1 KB (93140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5856d03fa8bd4c96dff4f6fdf7039b126daadec1708eadfb4e0120c80f6213e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05e0d25ea294b77017f8e39123bb2441d9948c72705f235e05048054bc0cb96`

```dockerfile
```

-	Layers:
	-	`sha256:9d54ad43f4fe81b1e5911165dc8a9c05b70075c2c167a57a1fa431b05759b31b`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 3.9 MB (3932828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7862e59544d59e1dd343e6096106c4e4f32c6092bc8837175f5e0999ede6d94`  
		Last Modified: Tue, 25 Feb 2025 02:27:15 GMT  
		Size: 14.0 KB (14000 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:33273b79aef6b560450f7930e7d5b2aab0ed20171f2ccfdcfe08f4b44c39b77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59636006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9056e9d1bc0fa6d68726bb1e713d5c2bf109be7a38765b58ec83751d255bd57`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4268effafc2bde885b308f4884da9a5675b21ea9dd10510af4cc390b22435225`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 11.2 MB (11232612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc8fd8ac1e89535a292d7b52efd5bea69c5f5c3851d37b9929659c0c6c042e`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe958a62bf286f5dab55b9feda9c4012922a2405bd34a8e0570b16801e9f1257`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeac118fe924197167da22818e9394a97999867f5e156777e4fcae652229797`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5bf0cf8bbd1552b5d307d189245c140355110008ba5b6d9832c6ac1e62ba330c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525930528ba4ba80cfc5b521e56fa2ac63fc986653c44edb81e1e2b88c04ec1f`

```dockerfile
```

-	Layers:
	-	`sha256:e3d84d2a8929cbdbcfd209768df78069a10fef211f62d7e294dfde2623c7f6aa`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 3.9 MB (3933082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8dd43cbc32f3db75eeb3b3f29b6c6352e2df38a36dd0feb09ea39aa4c04adaf`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 14.1 KB (14136 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:045529ad0e1a2323aae87c4f540f6a3b2e88516ed66c40b07b3eeadb82140fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dabf5edb97ea752e3861fe71d5da288dd065365656c1e8d869b79b467ce33f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06db2eb6124e849508d76e7b9f52369bbaf025a9b535513aeb226ec87e4b5c87`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 11.7 MB (11688923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b690958c17f8254fba7767793a8227fc40ea085973d753fe2c39708a9968e024`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d929ae2564cc35ddd3b993dab4283cdf38fa6beaba29c0c1097521d54917bb`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8701c8177798bc525467c9eaca4ad5bdaeb247310c0d2bde0a1e4fbdeecd7c8b`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 93.2 KB (93228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aee2fbc68d1b7fe46dbdc53656f8d02520f4a1f5e9dd90f4c7ed8b9647479428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ec8a2050ee31cf237ed440a821263f7c0c2425ca7aec82f085d506b881e4fa`

```dockerfile
```

-	Layers:
	-	`sha256:ec23be925f2f0bd074b9b75ab63b0cc12ab36b3b34bef80dba01b31642aa6cb1`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 3.9 MB (3930745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de76ded408b913df6c3ad9bef25422985ed7eb4dc3e8ac94e982b459f8f2aca2`  
		Last Modified: Tue, 25 Feb 2025 02:30:52 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:5f1c4ffb3aaec94eb85ba6d1159dbaa5d6058199f3c0a84887ab78b469a56d94
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
$ docker pull neurodebian@sha256:86d0f1e008c22ef1371791860617d59b2e903a4d642e928b30e47fa6b181da18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59838474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde7ea88b09684b422a1ac05b6b2ad01622129128e5db57512bdd2f99aa342b4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28441ab853fef772e1e1de08ec36f3ed7180ff3c2a9b9c9e671357202dcdd42`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 11.3 MB (11266799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505ff7e6422a09a3eb1a239312fcdaa2044a0e3eefd0c31485b820c54e4b7967`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d76303fdb4aa5d6083836c5414c3e64b7b9e08dfa94e4900c30eba602003b37`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179af51425b94c30d8dc80554e3ef4c9003f44a94784a75458c79f151ab32c10`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 93.2 KB (93157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36083d574b636b75357cbc3e722a118cdd90d3d27dd10a838646f855d03bc976`  
		Last Modified: Tue, 25 Feb 2025 02:27:21 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:672e5a788f4e12dd192919f23b3cdcc8c247268af0e4c265c3b187946806ca98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94236d5f014c5f6d7cd9746c73b7ebabab74fd82e06f0c1da40d26af73f6b90`

```dockerfile
```

-	Layers:
	-	`sha256:31b0617d5bc927443e4c297613d85abb99148b4e4f2e104f826075d993c933b7`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 3.9 MB (3932868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f7b4463e7f6d4ef42c049f42246d69980142348e3e7e3a4ef61fb6eb3128006`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:abb99c9c2f059106da856b9d569b4d8b7ca84af59582e6a68cef696edd394382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59636435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a022a8b30b7ae18ba216b15f04cbe65382f23139ec4b2b210764daa78ad1fbb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4268effafc2bde885b308f4884da9a5675b21ea9dd10510af4cc390b22435225`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 11.2 MB (11232612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc8fd8ac1e89535a292d7b52efd5bea69c5f5c3851d37b9929659c0c6c042e`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe958a62bf286f5dab55b9feda9c4012922a2405bd34a8e0570b16801e9f1257`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeac118fe924197167da22818e9394a97999867f5e156777e4fcae652229797`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd5763534ceb76e91f0383484f364058ab48c26cef0fb32914ddad1372da0f8`  
		Last Modified: Tue, 25 Feb 2025 06:12:50 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e7c7ed56d0e480fae65c8cde83e1d1adbc75c0a9a9fced612884ab3a96416e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0204f4c376b7e83a2ff9a754d837369ce083d2bccb96e91a0b065a72eaf2d6`

```dockerfile
```

-	Layers:
	-	`sha256:1737f3c716a72e8e417e4d27d5f130b9ad3b8d0a1374350ae0b58459419195a8`  
		Last Modified: Tue, 25 Feb 2025 06:12:51 GMT  
		Size: 3.9 MB (3933122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fad213bc7f30b41f083d0ea35cc189d394c753fdac72d9e11045dadb9bb777a`  
		Last Modified: Tue, 25 Feb 2025 06:12:50 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:14ea109b5493111055a5aaa853884637148ae4dc485ea5c4e267bdb1add74a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61243186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a7ea209e5b0e6d013100f17eff90f4100955ab738acde7026b6c79cabce3e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52022fd04bcf4f92943afd60360f0ecc2322d7d18d6a0abe22a2cdfe8bcecf6`  
		Last Modified: Tue, 25 Feb 2025 02:12:30 GMT  
		Size: 11.7 MB (11689076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900a00b32801477083168732fb13544e2003e9538368e35080da03e1b17fb70f`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d197c332a3b1cc7550c3bff0a9d351b9730cc7493035604b55fd1b1407153255`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf3e2f6fb6f036e3845a4a8b6ee926f3c8d48e922eda645aabbe2681ca3fc57`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 93.2 KB (93240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b9cbc42e9997903403815a1064c86c6cb272ea90c7fc977f69733045254639`  
		Last Modified: Tue, 25 Feb 2025 02:12:30 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d24e1d2b84e10d04805b51e11dd0c50d764501f818f8967b77329b63d229d33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021833d77fdeb79557411acea2ed9985e2d023e575a7287135cb2e1166396447`

```dockerfile
```

-	Layers:
	-	`sha256:335ee5030d46d154190ee10eca81ff2e045c93fb885778864658042d9925fc8a`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 3.9 MB (3930785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:578220ae32d85546c71d91eb6f5654e7c4554c058444cf7711da0b069bef4176`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 16.0 KB (15996 bytes)  
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
$ docker pull neurodebian@sha256:dddd5dfbc7fd007f4a3e728570835205318a059509fe698a32190ff096b1777a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:5f26675bcc90c8758ac288c5e42b178ff48a73e9ab4970f919e5ec4938cbd460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33271586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d5a7ae88d753f13e79fa4bb43d53cbf4cfed9fadba34ab474f4099807fe261`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63336557e3a88e2b6816b75ec69356976ec7a6330214bfa441e5d86b8bcd5fab`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 3.6 MB (3623158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f3b6cde57e753607cb5d03b5f4df97fcabbea0a03734d33c7a056556b608b4`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6389250b72dfd734ad1e61588b821ac38d8a3035405ce0dce0746dc8aa07fd94`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128920b07afa9e2ab5a724db970a1017a3839518a53c5829c82e7a6dce0154eb`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 110.5 KB (110492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c671d1877f1ca886adc735145c09a8b212ebf717dab82aafc170b00ada8f0890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb200fcf794b88cfdfe58fbf9fe7c5df4dd58d5af47ef863b77847b1ce789695`

```dockerfile
```

-	Layers:
	-	`sha256:495ed7fc83baeda0269343c97821047e2c68647a9c3b5d70f448b4caa68577c6`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 2.1 MB (2055319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baa3488be0939d3a148d71befa440ae927009daca74013dc5ec80152a7933da1`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 13.7 KB (13660 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:67728fb8e5cd3818b91715960c1bba0a0c0023bcabcd5671bc64df1d9df72da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f3f7d90cc1fbbefb0d8442ab9c23a806f90fef8b03dc4fdc5f1203b74992d3`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa83e4278dc6cff1ef0b2ddfdcdb95e8b576852125603aff18c4adbd62abfa`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 3.6 MB (3594385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f206a367506b9a6e0da2a087a15345608f59c46aed8faaf14965a2048a684`  
		Last Modified: Tue, 04 Feb 2025 10:12:44 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d2194ff2bd3e4e851f237645c0bd78afd3a389c1df83bc989d3245af146c30`  
		Last Modified: Tue, 04 Feb 2025 10:12:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e4837f465facfb077234adc2a993e2a512c6e94506c37f467ca0d03c95b7d4`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 110.3 KB (110348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9bb6e8c0c274860bac8c67b48375fd3b636f078b902c99d7683b178b98154e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f0655895d6ff3d027802a83acd357d94c7309434a0a7690073fd3df7bb1ef0`

```dockerfile
```

-	Layers:
	-	`sha256:5d3714f689f360f18f642041f406b8692c6373b6cdc03d9b4e616e7686ccb86e`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 2.1 MB (2055579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ad1910f3d5ccf7f20eac6a6cb65c3a203059bb8a4456258e696ec7fdc164d80`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:f03ae0a3cf4075547117b044adb41f16fad47137475cff997d41f3357cde975c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3c4173d5c31f8a53bbc0a2a190f78ae51e471618ee01069ecb2bc9459e952711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33271759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c3eaa4493fd2df3d65ef60c7b8dd8c63eae0ac0c17408e4f82998765182296`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d717b5746fc604b8417f674bfe4b267ccadca9c7c126b92991bb31d94d6d6b7`  
		Last Modified: Tue, 04 Feb 2025 04:25:09 GMT  
		Size: 3.6 MB (3623114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e87505a43c5a5f52ac9d7e93021419084501f715570763864d7f2bdc6068673`  
		Last Modified: Tue, 04 Feb 2025 04:25:09 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053c5ad118ff70f2b8fdd9a491743706d705020d0bfea7c71eaf3310c489a5bf`  
		Last Modified: Tue, 04 Feb 2025 04:25:09 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f757a34e2e1124f50485ed20bdf68b036a063a9ab34355a1c1676add6b438ae6`  
		Last Modified: Tue, 04 Feb 2025 04:25:09 GMT  
		Size: 110.5 KB (110450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43befb502973bc3768fe50fa6753ba9e0312654b012cf9db16a8f3eec23f6128`  
		Last Modified: Tue, 04 Feb 2025 04:25:10 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d4aee3cf707c745d560848ee49f052f203b32be18254a0bbd7f2ce026eaf6a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819d998f536ecd2c60c7f2c1fae4e361a91cb740ffe9608f690e12a03cc7a946`

```dockerfile
```

-	Layers:
	-	`sha256:f15b7681a6f1a10496fdb2eb02b4e22066edbd9abe4f3efc6912aa38e15e9840`  
		Last Modified: Tue, 04 Feb 2025 04:25:09 GMT  
		Size: 2.1 MB (2055355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f21fdeb65e657559fe924fe74b95df4e2b1157ff5ec18a4818715ed15fc51fe4`  
		Last Modified: Tue, 04 Feb 2025 04:25:09 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6ea935711d8e169b474d27073a01d3e0359878eadd283d1d93c4b577e8865490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31065166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30946598065f707a13ed26bb51018e6af24620a760b2293815ac5fa249b399bd`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa83e4278dc6cff1ef0b2ddfdcdb95e8b576852125603aff18c4adbd62abfa`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 3.6 MB (3594385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f206a367506b9a6e0da2a087a15345608f59c46aed8faaf14965a2048a684`  
		Last Modified: Tue, 04 Feb 2025 10:12:44 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d2194ff2bd3e4e851f237645c0bd78afd3a389c1df83bc989d3245af146c30`  
		Last Modified: Tue, 04 Feb 2025 10:12:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e4837f465facfb077234adc2a993e2a512c6e94506c37f467ca0d03c95b7d4`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 110.3 KB (110348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a2ce10ded06c3c89836d98dfe75aead8f6debf35261552961af34a3119d6b1`  
		Last Modified: Tue, 04 Feb 2025 10:13:04 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:eb6374ed9f5170068bbb23a3e58b7e61160c4e7b470845ee5877ebf2543b918e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb51f2b28516c23cabf829951e9a87e36097ef1710bdd7d6e3751483722042a0`

```dockerfile
```

-	Layers:
	-	`sha256:e4d312d6a85d3cee621fb1e24d7113e9b1fdce62a9b59001e0ebe7e369513403`  
		Last Modified: Tue, 04 Feb 2025 10:13:04 GMT  
		Size: 2.1 MB (2055615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c11f32963ab6bbbf1720c95e40fd72388ca05ebf764915eeca181050b953db0`  
		Last Modified: Tue, 04 Feb 2025 10:13:04 GMT  
		Size: 16.0 KB (16029 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:38f9c9c2b8ddcdde1839190b218af5c9636206a49a9b9e4c8456cf358e6e6ce0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:cea428758d59e5c037558c4133b13dcacb1148e28864668c244d661b2523bd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33417241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5890398ac27e560d4c10381f256468967d8b0fbc6d76a82d310df4d15e9268`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1065a20175c23251722dc4127e132e9ae13f1ec1800c748abd3b2e012ce4e35b`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 3.6 MB (3559070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685a25185edaecc67750bb55945a1d64e695cb4b3c7871764a02574e82be323b`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efa89cd8e883848fd2477d5ca3e2dc77111a1ede5baf0624848f26dd3b7c818`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc894a399dda914031caaed968ccafa3fe58734e5abafa23738502812a6d384`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 101.9 KB (101888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:92cb62a10f02dcc605ce37e73ecb53e7933fd5d38ae3f4530603c0fa060d71db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab4e963a55ae2118ceced0141383cc6656135531259fa2174092966efc2589e`

```dockerfile
```

-	Layers:
	-	`sha256:7f56d1ae5d6509efe4576574fa7ae17d8942e0ce6808254e404cca6591a9c9d7`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 2.0 MB (1990198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cea103e1efcbfc9ef35081d135cc8fc06a943c20599f9f6896e855f14bb3d0`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 13.7 KB (13660 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f5b26d64ee884094b3dd5a25ceda8824cfc810e6ffeb3cf77e8a1ecbbf7e0d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537ea799e077829555862da85a0ac66f58e8afe85c93b4e5f8e74392118103b`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064752aea5e7093dffc08088a65b854a8bd1a23f85ea6b642db4eb739d53457f`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 3.6 MB (3558141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8f9bcffbedfa700b80bf2298dfdd9a05077d59e2a3797faa4bdfc933e2f15`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c1f5ec1d6864c339d17b3fa5942c94b2202fdf4caf909b7f0a5da76fe280b0`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b8869a343ba6379e71c8a4bbcc5f7a32b3950017c7b36d3aa0acf8456ad2b3`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 102.5 KB (102513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f559a9bd8251416c5b26c2a5f3c001b693736d8c7bbbe4dcd59aa979fb8a9f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c65c73366b44fe7dd7c1dda3b14d538e785bef2ca4cea4cab47272e7bea69f5`

```dockerfile
```

-	Layers:
	-	`sha256:511f03c5b32d27ce4da4807cd63b1ff5225bad0e3cb78e0d2a40bc71830516f8`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 2.0 MB (1991243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe0f5717d5934dbf47501dae0839de37fefd3a48f84d3b59ee315927bd5af3a1`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:d876f5d2c1a243cec0c367aceb3e984003978978522474f68e39d1560fcd4f8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:46e197e29b09ebdcf8b79f5d4243b7a2ee38de58322e566005687311f02d432e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33417662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63727e014a8b319207be5c3696e3f62c7f30f85182746de8fe5e457e4f26522c`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7437a2bec487e56640d2df97d10d20c5d1dfa27e0e438784633ab110ee53ee36`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 3.6 MB (3559073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bad12c5f1fc20ee11ebf084c7dd8083dedce42a054f7436d654477679aacaf`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec5188e249edf8869e827975c795e8ded14ec5f3814f04ca3c0265087ffb7ba`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617193eaa6a7126b5d2fc3b9e53bbe8c8e36f7cb2b96b13a4a83f55dc3b9af41`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 101.9 KB (101904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a3f3f74ba19973d7a055cd89339fd42e1201d6087d3579224e3c2537d82fc7`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9d45065b62fdb0cd8b64cf598efb96e01258ca787ac6de734ee33575a975525b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2006124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdf6861efa175af6d5346140760fb5dfe8909b8d400074154e6b41f1f4138f4`

```dockerfile
```

-	Layers:
	-	`sha256:a8c721ca171aa98660eda78e17b0b52c586d2d79b6038943078d2d88ca0308d6`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 2.0 MB (1990234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008fb6819e6444684199e2d580536f6842848264a696ed06435ef17f187be07f`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4aa10d174411fad8e477b1bb8500090b9445380e7bbf063c8e06f7c8cc7ec146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92852453dc0aba0666ae7729d1c369ac51aa09bb0c0849cb99244377214ad21`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064752aea5e7093dffc08088a65b854a8bd1a23f85ea6b642db4eb739d53457f`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 3.6 MB (3558141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8f9bcffbedfa700b80bf2298dfdd9a05077d59e2a3797faa4bdfc933e2f15`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c1f5ec1d6864c339d17b3fa5942c94b2202fdf4caf909b7f0a5da76fe280b0`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b8869a343ba6379e71c8a4bbcc5f7a32b3950017c7b36d3aa0acf8456ad2b3`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 102.5 KB (102513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad5bc0311e43e08fc1e9c7d0046b547b2c62efd094a6d6072982f9c11950ac8`  
		Last Modified: Tue, 04 Feb 2025 10:13:41 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb2eee9d42e78b21c675c941959e65270fab2a7c03c8d8db15a1caf822071b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2007309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b42d91068670cdc5c981e68973f6e71e4b7198df0f6453b409990f569967e09`

```dockerfile
```

-	Layers:
	-	`sha256:2acf0ac00dab95682470b9d4204bde19accbd13cfcde77f9be73335039a1892a`  
		Last Modified: Tue, 04 Feb 2025 10:13:42 GMT  
		Size: 2.0 MB (1991279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf4a9723c79445f1d827e6fce3eaa61e41973fbb7f906f83e79296e6fcf0ffa`  
		Last Modified: Tue, 04 Feb 2025 10:13:41 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:38f9c9c2b8ddcdde1839190b218af5c9636206a49a9b9e4c8456cf358e6e6ce0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:cea428758d59e5c037558c4133b13dcacb1148e28864668c244d661b2523bd3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33417241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5890398ac27e560d4c10381f256468967d8b0fbc6d76a82d310df4d15e9268`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1065a20175c23251722dc4127e132e9ae13f1ec1800c748abd3b2e012ce4e35b`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 3.6 MB (3559070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685a25185edaecc67750bb55945a1d64e695cb4b3c7871764a02574e82be323b`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efa89cd8e883848fd2477d5ca3e2dc77111a1ede5baf0624848f26dd3b7c818`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc894a399dda914031caaed968ccafa3fe58734e5abafa23738502812a6d384`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 101.9 KB (101888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:92cb62a10f02dcc605ce37e73ecb53e7933fd5d38ae3f4530603c0fa060d71db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab4e963a55ae2118ceced0141383cc6656135531259fa2174092966efc2589e`

```dockerfile
```

-	Layers:
	-	`sha256:7f56d1ae5d6509efe4576574fa7ae17d8942e0ce6808254e404cca6591a9c9d7`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 2.0 MB (1990198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93cea103e1efcbfc9ef35081d135cc8fc06a943c20599f9f6896e855f14bb3d0`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 13.7 KB (13660 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f5b26d64ee884094b3dd5a25ceda8824cfc810e6ffeb3cf77e8a1ecbbf7e0d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f537ea799e077829555862da85a0ac66f58e8afe85c93b4e5f8e74392118103b`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064752aea5e7093dffc08088a65b854a8bd1a23f85ea6b642db4eb739d53457f`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 3.6 MB (3558141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8f9bcffbedfa700b80bf2298dfdd9a05077d59e2a3797faa4bdfc933e2f15`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c1f5ec1d6864c339d17b3fa5942c94b2202fdf4caf909b7f0a5da76fe280b0`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b8869a343ba6379e71c8a4bbcc5f7a32b3950017c7b36d3aa0acf8456ad2b3`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 102.5 KB (102513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f559a9bd8251416c5b26c2a5f3c001b693736d8c7bbbe4dcd59aa979fb8a9f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c65c73366b44fe7dd7c1dda3b14d538e785bef2ca4cea4cab47272e7bea69f5`

```dockerfile
```

-	Layers:
	-	`sha256:511f03c5b32d27ce4da4807cd63b1ff5225bad0e3cb78e0d2a40bc71830516f8`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 2.0 MB (1991243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe0f5717d5934dbf47501dae0839de37fefd3a48f84d3b59ee315927bd5af3a1`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:d876f5d2c1a243cec0c367aceb3e984003978978522474f68e39d1560fcd4f8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:46e197e29b09ebdcf8b79f5d4243b7a2ee38de58322e566005687311f02d432e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33417662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63727e014a8b319207be5c3696e3f62c7f30f85182746de8fe5e457e4f26522c`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7437a2bec487e56640d2df97d10d20c5d1dfa27e0e438784633ab110ee53ee36`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 3.6 MB (3559073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bad12c5f1fc20ee11ebf084c7dd8083dedce42a054f7436d654477679aacaf`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec5188e249edf8869e827975c795e8ded14ec5f3814f04ca3c0265087ffb7ba`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617193eaa6a7126b5d2fc3b9e53bbe8c8e36f7cb2b96b13a4a83f55dc3b9af41`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 101.9 KB (101904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a3f3f74ba19973d7a055cd89339fd42e1201d6087d3579224e3c2537d82fc7`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9d45065b62fdb0cd8b64cf598efb96e01258ca787ac6de734ee33575a975525b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2006124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdf6861efa175af6d5346140760fb5dfe8909b8d400074154e6b41f1f4138f4`

```dockerfile
```

-	Layers:
	-	`sha256:a8c721ca171aa98660eda78e17b0b52c586d2d79b6038943078d2d88ca0308d6`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 2.0 MB (1990234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008fb6819e6444684199e2d580536f6842848264a696ed06435ef17f187be07f`  
		Last Modified: Tue, 04 Feb 2025 04:25:08 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4aa10d174411fad8e477b1bb8500090b9445380e7bbf063c8e06f7c8cc7ec146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92852453dc0aba0666ae7729d1c369ac51aa09bb0c0849cb99244377214ad21`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064752aea5e7093dffc08088a65b854a8bd1a23f85ea6b642db4eb739d53457f`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 3.6 MB (3558141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b8f9bcffbedfa700b80bf2298dfdd9a05077d59e2a3797faa4bdfc933e2f15`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c1f5ec1d6864c339d17b3fa5942c94b2202fdf4caf909b7f0a5da76fe280b0`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b8869a343ba6379e71c8a4bbcc5f7a32b3950017c7b36d3aa0acf8456ad2b3`  
		Last Modified: Tue, 04 Feb 2025 10:13:29 GMT  
		Size: 102.5 KB (102513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad5bc0311e43e08fc1e9c7d0046b547b2c62efd094a6d6072982f9c11950ac8`  
		Last Modified: Tue, 04 Feb 2025 10:13:41 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb2eee9d42e78b21c675c941959e65270fab2a7c03c8d8db15a1caf822071b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2007309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b42d91068670cdc5c981e68973f6e71e4b7198df0f6453b409990f569967e09`

```dockerfile
```

-	Layers:
	-	`sha256:2acf0ac00dab95682470b9d4204bde19accbd13cfcde77f9be73335039a1892a`  
		Last Modified: Tue, 04 Feb 2025 10:13:42 GMT  
		Size: 2.0 MB (1991279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf4a9723c79445f1d827e6fce3eaa61e41973fbb7f906f83e79296e6fcf0ffa`  
		Last Modified: Tue, 04 Feb 2025 10:13:41 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:5f1c4ffb3aaec94eb85ba6d1159dbaa5d6058199f3c0a84887ab78b469a56d94
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
$ docker pull neurodebian@sha256:86d0f1e008c22ef1371791860617d59b2e903a4d642e928b30e47fa6b181da18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59838474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde7ea88b09684b422a1ac05b6b2ad01622129128e5db57512bdd2f99aa342b4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28441ab853fef772e1e1de08ec36f3ed7180ff3c2a9b9c9e671357202dcdd42`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 11.3 MB (11266799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505ff7e6422a09a3eb1a239312fcdaa2044a0e3eefd0c31485b820c54e4b7967`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d76303fdb4aa5d6083836c5414c3e64b7b9e08dfa94e4900c30eba602003b37`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179af51425b94c30d8dc80554e3ef4c9003f44a94784a75458c79f151ab32c10`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 93.2 KB (93157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36083d574b636b75357cbc3e722a118cdd90d3d27dd10a838646f855d03bc976`  
		Last Modified: Tue, 25 Feb 2025 02:27:21 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:672e5a788f4e12dd192919f23b3cdcc8c247268af0e4c265c3b187946806ca98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94236d5f014c5f6d7cd9746c73b7ebabab74fd82e06f0c1da40d26af73f6b90`

```dockerfile
```

-	Layers:
	-	`sha256:31b0617d5bc927443e4c297613d85abb99148b4e4f2e104f826075d993c933b7`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 3.9 MB (3932868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f7b4463e7f6d4ef42c049f42246d69980142348e3e7e3a4ef61fb6eb3128006`  
		Last Modified: Tue, 25 Feb 2025 02:27:20 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:abb99c9c2f059106da856b9d569b4d8b7ca84af59582e6a68cef696edd394382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59636435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a022a8b30b7ae18ba216b15f04cbe65382f23139ec4b2b210764daa78ad1fbb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4268effafc2bde885b308f4884da9a5675b21ea9dd10510af4cc390b22435225`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 11.2 MB (11232612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc8fd8ac1e89535a292d7b52efd5bea69c5f5c3851d37b9929659c0c6c042e`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe958a62bf286f5dab55b9feda9c4012922a2405bd34a8e0570b16801e9f1257`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeac118fe924197167da22818e9394a97999867f5e156777e4fcae652229797`  
		Last Modified: Tue, 25 Feb 2025 06:12:37 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd5763534ceb76e91f0383484f364058ab48c26cef0fb32914ddad1372da0f8`  
		Last Modified: Tue, 25 Feb 2025 06:12:50 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e7c7ed56d0e480fae65c8cde83e1d1adbc75c0a9a9fced612884ab3a96416e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0204f4c376b7e83a2ff9a754d837369ce083d2bccb96e91a0b065a72eaf2d6`

```dockerfile
```

-	Layers:
	-	`sha256:1737f3c716a72e8e417e4d27d5f130b9ad3b8d0a1374350ae0b58459419195a8`  
		Last Modified: Tue, 25 Feb 2025 06:12:51 GMT  
		Size: 3.9 MB (3933122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fad213bc7f30b41f083d0ea35cc189d394c753fdac72d9e11045dadb9bb777a`  
		Last Modified: Tue, 25 Feb 2025 06:12:50 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:14ea109b5493111055a5aaa853884637148ae4dc485ea5c4e267bdb1add74a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61243186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a7ea209e5b0e6d013100f17eff90f4100955ab738acde7026b6c79cabce3e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52022fd04bcf4f92943afd60360f0ecc2322d7d18d6a0abe22a2cdfe8bcecf6`  
		Last Modified: Tue, 25 Feb 2025 02:12:30 GMT  
		Size: 11.7 MB (11689076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900a00b32801477083168732fb13544e2003e9538368e35080da03e1b17fb70f`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d197c332a3b1cc7550c3bff0a9d351b9730cc7493035604b55fd1b1407153255`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf3e2f6fb6f036e3845a4a8b6ee926f3c8d48e922eda645aabbe2681ca3fc57`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 93.2 KB (93240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b9cbc42e9997903403815a1064c86c6cb272ea90c7fc977f69733045254639`  
		Last Modified: Tue, 25 Feb 2025 02:12:30 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d24e1d2b84e10d04805b51e11dd0c50d764501f818f8967b77329b63d229d33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021833d77fdeb79557411acea2ed9985e2d023e575a7287135cb2e1166396447`

```dockerfile
```

-	Layers:
	-	`sha256:335ee5030d46d154190ee10eca81ff2e045c93fb885778864658042d9925fc8a`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 3.9 MB (3930785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:578220ae32d85546c71d91eb6f5654e7c4554c058444cf7711da0b069bef4176`  
		Last Modified: Tue, 25 Feb 2025 02:12:29 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
