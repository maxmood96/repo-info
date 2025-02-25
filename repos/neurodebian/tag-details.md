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
$ docker pull neurodebian@sha256:9a19c3abb0728fcc0bb71a4b83d27cc0535690af34db1d4565e7a03e766152aa
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
$ docker pull neurodebian@sha256:1e2e435f7f0b62700276be201537841294494dcc75aff3901883ec865502a026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59634462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde46790df52779fab79f8caa47eed9af98b70ac832dcb55b9e3094f3e06e5a4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0890be792eb8cf2c454fe7c038fba6da83a8ef251447a532fa6d4f3108c2f7`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 11.2 MB (11232504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99eec1b3a608d28ef329abdd58a2e25ee524c0453b1269a4668003e0983d49`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86127ee86de4c4cff8e4bdd5c18c3f9d3021d01a9a46fb1e63a786d3c5abab3`  
		Last Modified: Tue, 04 Feb 2025 10:14:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd76384f78a868cb30bf0b964090aebaad99664c593dc1fcb7897c3ca2af13`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aeacc818a0c86df95b4a72372d5b0dac3431692818070177ea7b5e0d005d39ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6b5a02e4de1e4ecb8d92db34b5cb18345e4c90682d2157fa69579f5355fbeb`

```dockerfile
```

-	Layers:
	-	`sha256:2fd92c47f6a7061525a6ef620af7395dc15f4d5c555649a4deb9b9d958fb1217`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 3.9 MB (3933064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096b970f4b1015790b69dee643108090df667b906b9ca0c7985a4ad9e84d6e50`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
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
$ docker pull neurodebian@sha256:1e5336de47c0916153b95b268b167627f1dcbbb014b0dfe948f093a782d4337a
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
$ docker pull neurodebian@sha256:8cd5e6b7bec8b2fb545404fa4ef6bd502469cf4951c316d6e6279f2853160096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59634890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4830671f1f42f572e6707b244573102e521ead223e96423ff85026ae06f25297`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0890be792eb8cf2c454fe7c038fba6da83a8ef251447a532fa6d4f3108c2f7`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 11.2 MB (11232504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99eec1b3a608d28ef329abdd58a2e25ee524c0453b1269a4668003e0983d49`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86127ee86de4c4cff8e4bdd5c18c3f9d3021d01a9a46fb1e63a786d3c5abab3`  
		Last Modified: Tue, 04 Feb 2025 10:14:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd76384f78a868cb30bf0b964090aebaad99664c593dc1fcb7897c3ca2af13`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04417613519d31f6f792cca8327cad6db9d5664fb6531c5c94f92801518ff51d`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5ca00e53e65addbf1adf8782ccd07719cda0df67061120dae1afa0773d8cf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e6e0a88411798e9de89e740aec9110aa51198ec12d4d77b9188f3b5d0ab85a`

```dockerfile
```

-	Layers:
	-	`sha256:2c9e1237745fd9d27f596daf590b01f333c1e6ed5054993d33f0533e77edc71e`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
		Size: 3.9 MB (3933104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3978024698224d9e7ae7a49ba553a6391e10f049df270264dacc9a5d2e8d971`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
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
$ docker pull neurodebian@sha256:de5984f80a6d3e2efaceaf8a67098bedb456a0f5384dd010a1f62b0b9108db4c
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
$ docker pull neurodebian@sha256:32b3eff063928944b21b68fd109e77822f1748d84a34cda4e9386437c9a82e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63454738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb44f4947cda69488a47fb8a06e1b7eeb82303ab2ac4bf3b08ef966610272f1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e95529282fe4b2c53926ffa260e910ca2e7edbe840ec6045501427c2b0fcc2`  
		Last Modified: Tue, 04 Feb 2025 10:14:11 GMT  
		Size: 11.1 MB (11105949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3498b7aa8199bc97f275a3b6d10573f41165c0eb35ce7ff70f2f3ddd65a4f5`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af64b7d26c87753053c75134052452ee120a3493c4d975102854f002f29f65c`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628b5ae84a5cd3de98a4de2b27f64955e4e5e004721258979acdb6b183904370`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 101.1 KB (101102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bda47942c2d20d8e4ddca4dab08bd7153d5cebf4ae5d8dddb697275df70c4751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51080557bc9f2721293cbec4e63725d6cfad190384939d02454baffd49dfa734`

```dockerfile
```

-	Layers:
	-	`sha256:491de11ae23b4dd66b220dcd76c0e275149062203504cb58082e0ee65c6af69d`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 4.2 MB (4232403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7e433bf58ab1e39dd4074bdeb966fedf4b20b0437a949f2c4b52569e2a28987`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 13.8 KB (13818 bytes)  
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
$ docker pull neurodebian@sha256:f6e680a2730aa165430fb7b2397ec4fc7376cfab7606fce027c4da0819ad5cb3
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
$ docker pull neurodebian@sha256:adeffd7d7b4876d93490b45f1bf7db0a31ebe2c91fe557a5ed33e7dcd95afd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e9bc24d7d988dbc1b420003629bdab58a106a6a0f17ca197d784887859b9d3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e95529282fe4b2c53926ffa260e910ca2e7edbe840ec6045501427c2b0fcc2`  
		Last Modified: Tue, 04 Feb 2025 10:14:11 GMT  
		Size: 11.1 MB (11105949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3498b7aa8199bc97f275a3b6d10573f41165c0eb35ce7ff70f2f3ddd65a4f5`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af64b7d26c87753053c75134052452ee120a3493c4d975102854f002f29f65c`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628b5ae84a5cd3de98a4de2b27f64955e4e5e004721258979acdb6b183904370`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 101.1 KB (101102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df83d3c23da0b5df36bdc784ddee25b91909ea0340f81b77341cbd0e75147f18`  
		Last Modified: Tue, 04 Feb 2025 10:14:25 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b1c2a555a093d89edb798b9c41eec081c742e59307253be2f5bd4a5899147d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a9bb42f0dc95e2bf94c144e676c423415a7b1442a83ede8afbd5847ddeea66`

```dockerfile
```

-	Layers:
	-	`sha256:dfae46ead578e6973908c1a2c813a24d46fc554aba3026407ed83cee0b4ddc46`  
		Last Modified: Tue, 04 Feb 2025 10:14:25 GMT  
		Size: 4.2 MB (4232439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5c6fe5fa24a9bafc7f0d161f4b11d10f8578478a0e160fe998a3ec5ac64941`  
		Last Modified: Tue, 04 Feb 2025 10:14:25 GMT  
		Size: 15.9 KB (15859 bytes)  
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
$ docker pull neurodebian@sha256:9a19c3abb0728fcc0bb71a4b83d27cc0535690af34db1d4565e7a03e766152aa
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
$ docker pull neurodebian@sha256:1e2e435f7f0b62700276be201537841294494dcc75aff3901883ec865502a026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59634462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde46790df52779fab79f8caa47eed9af98b70ac832dcb55b9e3094f3e06e5a4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0890be792eb8cf2c454fe7c038fba6da83a8ef251447a532fa6d4f3108c2f7`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 11.2 MB (11232504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99eec1b3a608d28ef329abdd58a2e25ee524c0453b1269a4668003e0983d49`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86127ee86de4c4cff8e4bdd5c18c3f9d3021d01a9a46fb1e63a786d3c5abab3`  
		Last Modified: Tue, 04 Feb 2025 10:14:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd76384f78a868cb30bf0b964090aebaad99664c593dc1fcb7897c3ca2af13`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aeacc818a0c86df95b4a72372d5b0dac3431692818070177ea7b5e0d005d39ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6b5a02e4de1e4ecb8d92db34b5cb18345e4c90682d2157fa69579f5355fbeb`

```dockerfile
```

-	Layers:
	-	`sha256:2fd92c47f6a7061525a6ef620af7395dc15f4d5c555649a4deb9b9d958fb1217`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 3.9 MB (3933064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096b970f4b1015790b69dee643108090df667b906b9ca0c7985a4ad9e84d6e50`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
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

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:396c89536fe6db1bc27165b5b3b01c1c141024b20e94ed056ca001ee7d489199
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
$ docker pull neurodebian@sha256:11f1d8a2c1ba5807309a84fe53239c15644decd7e0f952223fcfe8e28b9d40ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58544043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d931e73790091e29816ecd8a3b3bd13e50c1b635e8ec66b670304f41e9377f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
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
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e623044ed6d226bb08223597c0f380daf46067df42de48e52515dd8b6015bd9`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 6.3 MB (6309037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df34ef8a3df44564cff9f91477c96045ed1348d5c6bacebb2c30da5ed1d67729`  
		Last Modified: Tue, 03 Dec 2024 02:32:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d9ecdc74a71cc7cfaf2b1635937b88fc90e48932874568379bd4948b83d9c0`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4420bbd6a1e5e4067d6048b9cfc560b9b39df72d87d4ed9e93ebb3c7f8be97e6`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 91.4 KB (91417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:813cab0e7d8d6a6d32eb156bb2a98ba13135a9efdefa45445c299cff634bb3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eddb8c244b0b5047058b014b003d153a1b272ae2e55f50361d6707a657d0ca`

```dockerfile
```

-	Layers:
	-	`sha256:c07968d16a78367e1d48530eb27283dfe91c39751a8b135ec9af329cb9dda337`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 3.6 MB (3559094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ddfa355e9e60cc21afc4f6d9b0f6907ad2cd79edba64fdeafb408ff1ebf336c`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 13.6 KB (13627 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f70ccf1c4f8e34348cbd6dbdfdf30069e43ae372c6d6ae4183ee57c6cf6e7f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58746356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe90355c453a718b5f375561fdd4ffe5ee6d55f7254cf1b2b706984bfcd91d9a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
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
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:37cfe9a0d72ee56ff9cfbd3d6f54367b57a516bedd5b30b0d1a598123957ab2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3355433a01c656d9187644992eb02f399b926fd6998309ff3152bdd174664e0`

```dockerfile
```

-	Layers:
	-	`sha256:f01a69ba873a649d16109246e36645e9293f212711280454988268bed4add197`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 3.6 MB (3563973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bcd735f99065db42e22a630fcbdde19cc6d75b63789503857eba2885a0de8be`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 13.8 KB (13752 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:a6e34b9b3ef10febb3e68cb59e5d43a9cd4518aaaec42c9fb0eb764661ebac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59703235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356823f088987741ec801961eaf46491d407c63f5df550066164acb83a595dcd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
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
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c500b7e81fb48a2ca8dfb944bf05a4434b38906509b44c8230cb468350330652`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 6.6 MB (6636172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cba7baac1bbf19c4eff6cba1e463e4514023f61e5e4f99eabf003c60f53789`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bbc8c8ecf4c50fb1afe9f838e8684a9f8283e6edf3aea752fba90ecdfb953c`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38faa38e98066ab42e204ada314c609783c4d1432e9755b2bcb597ed43dd599b`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 91.7 KB (91657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a39472daab1f7ad10eddf0cd67f8453f4675bbd31ed229cb77f9a601729e442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5077173fa2b440d42065a12b5c4ecbf78be9444e400aa418924ffe9cdeb599`

```dockerfile
```

-	Layers:
	-	`sha256:b9520b672b857555a8f6a7d165f2b5323247148278f458a7278373f979f2088f`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 3.6 MB (3556335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a715947ef1aeb942d19d5f3d425c0a032538f9e6b2ee6340f7ab1c249910cdb`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 13.6 KB (13599 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:e7c0d77acdd38391058bb428da4b25ac4b5d5b17dbc921ee7afb854783a1cc48
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
$ docker pull neurodebian@sha256:9cdfe6f90f096c5886af048cddf57f84f7131abc4faa5f65638d66c77660e090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58544425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29dae39f0e2a61e2773abfc9d19efaff6e24355ae35e8f376529d52c260d4529`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
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
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114eb8c7559544e979c7bc06d71d09eaa2cd00debd8cf4f03a56d8104b7699b3`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 6.3 MB (6308996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff80e11993394c1dc9aaa17af36dfa33cca39fa8e0caabe1b3bf52e80a34369c`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4eb1dc4c12753dfe02a45cea97e094916913c37268158aa3b340700e68143f`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12f43e28b0e223dee7e963ea7a4ad3a48f843457e481ee84cfb74772191cd9`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 91.4 KB (91443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405db61dc15551d8850b73eec4f6ecee2d15504c5d277afd2c8128e17ecf6611`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1bf2d8e93155ae981f2f562f22bf9918fdb877c66cffd35655fec1d9b1f39938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffd90ef4d3ae1ed5361af576f9d3f2c0d2a5754f07e470e32f3a78bc8bd6096`

```dockerfile
```

-	Layers:
	-	`sha256:9702d640d901ef7903e74e7c2b43af913d4f418a939adc866950dcedaf2a783a`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 3.6 MB (3559130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7bb223c6e89608e9722bf8101c7626ae5724ae67e6be3bab333911378929ca4`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 15.7 KB (15653 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c7ac4ef4afbf39509f7a22b31591f646ef72bc02b766b53e5fd512cdd67e0175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58746750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed54a230a0fd8bfde46f98be15f4d3b97ce2d877b842da7ab902c830cee5c0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
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
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c880850a32196b5042f578dfb72c4fa93d1ee7ebd60d71fa4d5fbe19814c1ac`  
		Last Modified: Tue, 03 Dec 2024 06:18:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:22661e3cbf436b44b80103996ca2bd6577e74d6b1b8bebb5202171aadd46a284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d846bb8b6f1144a2d45721e8f45c30c3f32192c7a1ac72ca6b7268efa446fe48`

```dockerfile
```

-	Layers:
	-	`sha256:96771062d69621936e46943c2483b9fbc12aa2771b6c3722cb1035b36ef91682`  
		Last Modified: Tue, 03 Dec 2024 06:18:32 GMT  
		Size: 3.6 MB (3564009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c24f5aff628042c5046d45e533873a264167660d2769d5c6aa4aad04528fe9`  
		Last Modified: Tue, 03 Dec 2024 06:18:31 GMT  
		Size: 15.8 KB (15793 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a7f28e60fef8ae8c66fd2dba17b3f842cc070ff0f190ebc2bdf9a7a8be76fe7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59703410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a1f70a2c0871c021a308aded3c9b948de0de66faaa7121a2d269e4640fc96`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
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
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998bde38fb7afd531148bc5ada8932ba6909774db1014c810250d2fed9705c28`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 6.6 MB (6635982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff379f8e9bb8d25d6e0f0189f738f8b022e1073b791de493bf8117cc6d281ae`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863c1b51d89e4dd4797ba1c7a7da71a5c460240254b1e7853212c5b2e920c1af`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bc6338d9947bdf727b4f355b78ec884ccc098bacc03deb3d7965d5d04398bb`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 91.6 KB (91629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deb6e8c73557a116710e67686758ffb933b5075a0bed69a3dae3ca0be59627d`  
		Last Modified: Tue, 03 Dec 2024 02:28:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74f05ff960ca0068515281f926b0c25dbcf76375b4f99e58125b16a689b862ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d55b24693960716604398d554cbad7c385b5f86da205d5292975eeb67833ff`

```dockerfile
```

-	Layers:
	-	`sha256:74ca85f2e86db85f7b30f20d46e8e42be283a7b27e1b60976e0ff56e761fd5f2`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 3.6 MB (3556371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d03ff36e1583fd5288b7e43255d4ae49d2af7984f1801d3d5ea02eae17b0cc6`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:de5984f80a6d3e2efaceaf8a67098bedb456a0f5384dd010a1f62b0b9108db4c
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
$ docker pull neurodebian@sha256:32b3eff063928944b21b68fd109e77822f1748d84a34cda4e9386437c9a82e34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63454738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb44f4947cda69488a47fb8a06e1b7eeb82303ab2ac4bf3b08ef966610272f1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e95529282fe4b2c53926ffa260e910ca2e7edbe840ec6045501427c2b0fcc2`  
		Last Modified: Tue, 04 Feb 2025 10:14:11 GMT  
		Size: 11.1 MB (11105949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3498b7aa8199bc97f275a3b6d10573f41165c0eb35ce7ff70f2f3ddd65a4f5`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af64b7d26c87753053c75134052452ee120a3493c4d975102854f002f29f65c`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628b5ae84a5cd3de98a4de2b27f64955e4e5e004721258979acdb6b183904370`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 101.1 KB (101102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bda47942c2d20d8e4ddca4dab08bd7153d5cebf4ae5d8dddb697275df70c4751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51080557bc9f2721293cbec4e63725d6cfad190384939d02454baffd49dfa734`

```dockerfile
```

-	Layers:
	-	`sha256:491de11ae23b4dd66b220dcd76c0e275149062203504cb58082e0ee65c6af69d`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 4.2 MB (4232403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7e433bf58ab1e39dd4074bdeb966fedf4b20b0437a949f2c4b52569e2a28987`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 13.8 KB (13818 bytes)  
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
$ docker pull neurodebian@sha256:f6e680a2730aa165430fb7b2397ec4fc7376cfab7606fce027c4da0819ad5cb3
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
$ docker pull neurodebian@sha256:adeffd7d7b4876d93490b45f1bf7db0a31ebe2c91fe557a5ed33e7dcd95afd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e9bc24d7d988dbc1b420003629bdab58a106a6a0f17ca197d784887859b9d3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e95529282fe4b2c53926ffa260e910ca2e7edbe840ec6045501427c2b0fcc2`  
		Last Modified: Tue, 04 Feb 2025 10:14:11 GMT  
		Size: 11.1 MB (11105949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3498b7aa8199bc97f275a3b6d10573f41165c0eb35ce7ff70f2f3ddd65a4f5`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af64b7d26c87753053c75134052452ee120a3493c4d975102854f002f29f65c`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628b5ae84a5cd3de98a4de2b27f64955e4e5e004721258979acdb6b183904370`  
		Last Modified: Tue, 04 Feb 2025 10:14:10 GMT  
		Size: 101.1 KB (101102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df83d3c23da0b5df36bdc784ddee25b91909ea0340f81b77341cbd0e75147f18`  
		Last Modified: Tue, 04 Feb 2025 10:14:25 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b1c2a555a093d89edb798b9c41eec081c742e59307253be2f5bd4a5899147d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a9bb42f0dc95e2bf94c144e676c423415a7b1442a83ede8afbd5847ddeea66`

```dockerfile
```

-	Layers:
	-	`sha256:dfae46ead578e6973908c1a2c813a24d46fc554aba3026407ed83cee0b4ddc46`  
		Last Modified: Tue, 04 Feb 2025 10:14:25 GMT  
		Size: 4.2 MB (4232439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5c6fe5fa24a9bafc7f0d161f4b11d10f8578478a0e160fe998a3ec5ac64941`  
		Last Modified: Tue, 04 Feb 2025 10:14:25 GMT  
		Size: 15.9 KB (15859 bytes)  
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
$ docker pull neurodebian@sha256:9a19c3abb0728fcc0bb71a4b83d27cc0535690af34db1d4565e7a03e766152aa
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
$ docker pull neurodebian@sha256:1e2e435f7f0b62700276be201537841294494dcc75aff3901883ec865502a026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59634462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde46790df52779fab79f8caa47eed9af98b70ac832dcb55b9e3094f3e06e5a4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0890be792eb8cf2c454fe7c038fba6da83a8ef251447a532fa6d4f3108c2f7`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 11.2 MB (11232504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99eec1b3a608d28ef329abdd58a2e25ee524c0453b1269a4668003e0983d49`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86127ee86de4c4cff8e4bdd5c18c3f9d3021d01a9a46fb1e63a786d3c5abab3`  
		Last Modified: Tue, 04 Feb 2025 10:14:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd76384f78a868cb30bf0b964090aebaad99664c593dc1fcb7897c3ca2af13`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:aeacc818a0c86df95b4a72372d5b0dac3431692818070177ea7b5e0d005d39ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6b5a02e4de1e4ecb8d92db34b5cb18345e4c90682d2157fa69579f5355fbeb`

```dockerfile
```

-	Layers:
	-	`sha256:2fd92c47f6a7061525a6ef620af7395dc15f4d5c555649a4deb9b9d958fb1217`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 3.9 MB (3933064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096b970f4b1015790b69dee643108090df667b906b9ca0c7985a4ad9e84d6e50`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
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
$ docker pull neurodebian@sha256:1e5336de47c0916153b95b268b167627f1dcbbb014b0dfe948f093a782d4337a
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
$ docker pull neurodebian@sha256:8cd5e6b7bec8b2fb545404fa4ef6bd502469cf4951c316d6e6279f2853160096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59634890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4830671f1f42f572e6707b244573102e521ead223e96423ff85026ae06f25297`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0890be792eb8cf2c454fe7c038fba6da83a8ef251447a532fa6d4f3108c2f7`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 11.2 MB (11232504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99eec1b3a608d28ef329abdd58a2e25ee524c0453b1269a4668003e0983d49`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86127ee86de4c4cff8e4bdd5c18c3f9d3021d01a9a46fb1e63a786d3c5abab3`  
		Last Modified: Tue, 04 Feb 2025 10:14:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd76384f78a868cb30bf0b964090aebaad99664c593dc1fcb7897c3ca2af13`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04417613519d31f6f792cca8327cad6db9d5664fb6531c5c94f92801518ff51d`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5ca00e53e65addbf1adf8782ccd07719cda0df67061120dae1afa0773d8cf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e6e0a88411798e9de89e740aec9110aa51198ec12d4d77b9188f3b5d0ab85a`

```dockerfile
```

-	Layers:
	-	`sha256:2c9e1237745fd9d27f596daf590b01f333c1e6ed5054993d33f0533e77edc71e`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
		Size: 3.9 MB (3933104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3978024698224d9e7ae7a49ba553a6391e10f049df270264dacc9a5d2e8d971`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
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

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:bbc3ded260e52ab68dea79f0a8860a9853977c5b81a7cbc61da66dd3e73e464d
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
$ docker pull neurodebian@sha256:22ba4c69dfacb7993f7fcf3708c2ec38e7a15ed1bed206d226c5160e47273847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58516023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fd9c4b14dc331719047f53a409b7b3093d384a6ff135c95b14e664c6b43885`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
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
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31fa211153a834040c35ecc855708df74ae143e0f067f5f29d4299bec783171`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 6.3 MB (6309046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759be46808786c18908d758383834044fed05ddaf818585877931072aaa3bea3`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9340f215c3f9e9497b17c7dcc21314a53d5553d70c1a45f9ecd9663aa523c`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809dd25b48752fba0eeac0fcf5c38a88f0e12b0db0b022acf82ae7fafd98800f`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 91.4 KB (91435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b22d1f83ebacbb4392e9e1ec31a9e0902f3f7a2cde703ee063fc39bfcd1b648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9d1493dabbbd58df5573fa3c3dc733bfb235815353be42c104a85da39f4758`

```dockerfile
```

-	Layers:
	-	`sha256:8cfad2f41e51e9ca8348d9d7852f9a0f81c5d0a482874503181c168442d46e8d`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 3.6 MB (3564266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291ee8d275476a4f56b64a69bb3c484a527878d207b0f47533dc5df2c24f9458`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1401e84e1f34ba3fec0eccc60bfdb562ec886b1705aeb33459074a37aed25700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58723605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547bcc904f8cc765088dc02b9c5eac15bece1c36242ba056fa8894fa557231aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
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
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8640b31431e2f1a1a2b65b6fed2b7a4bcd6826c4d1cb17e4d8e1e9e2bf2ec5`  
		Last Modified: Tue, 03 Dec 2024 06:17:43 GMT  
		Size: 6.3 MB (6288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f67a6b589fb5f0c9202e6eb9aa7cc5ec0a7c2e67c81df4d2e3f8bc9603c4e9`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96d02cd9c1d5c2742decbe351e194414adec825bee6bbd6263521be0a514665`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d38c51092ac20a5bcd1dfc533de43a738889d192e62656482dc22f1505a79`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 92.2 KB (92158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d4b78788290c99294a51ceca1957d8eb6e9e849177decb1f820324a7d85b171a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3582936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c170b6bf1352da87527070a521d5bca904ee0e113091bee7260deb2c47e958`

```dockerfile
```

-	Layers:
	-	`sha256:60730bef667d6b97b826f735f2547ce96c7c51f072bed45993eb690ead280fc9`  
		Last Modified: Tue, 03 Dec 2024 06:17:43 GMT  
		Size: 3.6 MB (3569145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a78c16c7a4e8d937b184fa40339df44fa15f714b5d50ea63d627b3763ab773`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 13.8 KB (13791 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:0c302d3d91a06e0de1ae44728e6c238af8f332b079b0dde357761280c7738727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59685891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eda70426935cafff4ae79341debf8d16acdb137a79c79aaf95a4e89287e257`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
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
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07d21ec843fdae56608290e710928213278f433f216169549f4105b0b7adcde`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 6.6 MB (6636002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790ba6a36bbd0ddde077446c337522dff4905079f146ba4f81c5f1b1ba01508e`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f988e696d1fd940f6f8a41f61db71109214ffa05a741e7ad19280fab3317b7a6`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7105d8b802d7cbbf45432b1a9323e287ee890f7b63ac52b16e684f8aa59aa436`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 91.6 KB (91615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:640e8a6c2b29256a11a97f4fab868b83769f471a9a56a787f0520ea21d8560d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0a2cb4139fdbf18dfb086e8db81f463979da7309ce33c42798424276477172`

```dockerfile
```

-	Layers:
	-	`sha256:13a56528e8fb58e39de0f1b02fd41e36f2ce6114df32afe325634c478c2d46c0`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 3.6 MB (3561502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda46b32b1387c0fd07559cd518cb696c94a4a839d171f21cf6124f57cee113a`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 13.6 KB (13638 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:a78a1c95462db7bf414f96ce328616fe968aac57b876af3362c3e4b47cdb81f1
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
$ docker pull neurodebian@sha256:dc2ee078717e5cd6782de72121bcc9936ef63cb0981ca8e921754737a77980e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58516479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf94ef9a8ab87a336dec4a29f001d654de0e935525f16a071a00515579aff5be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
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
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507e5811b953238ff193b1168d33f51c6e9d529f200a09d5a7cacc81a3cc8c3`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 6.3 MB (6309097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53110b5d9fe921d17db007a1ddcf5a14b209223be44404d7367639af0432a720`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073121ed00d2745775e339f48a955b95fe1cf8f720671dcb447fc1ed84db92f`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a4d13654e7924d6b2b37ec66b136d37c2be5c0336ea4c05ed6c366e2a4fd3f`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 91.4 KB (91421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8461a91abccfb6a0564642a71b515e4966ed0f07a5adb19dea1de7fda249aaf0`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 422.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7de7481f3bac1a3622e0eed2ca47e8f02312431429159b58502dfc6e1b23d76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bcddfe5efc17cf322b5dd0859093bb6b3567c32ae516fe9b443b80a0541765`

```dockerfile
```

-	Layers:
	-	`sha256:70ad6f08346ad337d0f9e32f7ec11b22ad0d818d1df8a6aee0a4052c1cd75b1d`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 3.6 MB (3564302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97d1de4b535410fddab63f0e6af15dfaa00cec28ba8c0fde0a15678db848775`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 15.7 KB (15692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:17fe10b8e293faa659d945422ff3aaf4c7e6e1f387d707d314802beb80b71a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58724028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85d39b737a8ff196e533cfc0ffb9a1412e43594be8673e8c0da6c05751f91ce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
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
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8640b31431e2f1a1a2b65b6fed2b7a4bcd6826c4d1cb17e4d8e1e9e2bf2ec5`  
		Last Modified: Tue, 03 Dec 2024 06:17:43 GMT  
		Size: 6.3 MB (6288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f67a6b589fb5f0c9202e6eb9aa7cc5ec0a7c2e67c81df4d2e3f8bc9603c4e9`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96d02cd9c1d5c2742decbe351e194414adec825bee6bbd6263521be0a514665`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d38c51092ac20a5bcd1dfc533de43a738889d192e62656482dc22f1505a79`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 92.2 KB (92158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da18a25c93d7133b2d4097e549a323142182e4dd20d54315927b6bd6573eb0f1`  
		Last Modified: Tue, 03 Dec 2024 06:17:54 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c77a0b2714832915027f323e1b1215a7ec8179d2324362662d8283e9cad88fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7509c00ee24dafaacefc91ed80721178d33398b768fb59515c8052afde5a23`

```dockerfile
```

-	Layers:
	-	`sha256:27c4680740117658f3a6d274e90c1bc193f9aed297af2e9c8658296f77a30654`  
		Last Modified: Tue, 03 Dec 2024 06:17:55 GMT  
		Size: 3.6 MB (3569181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37b47d54c077c2ac6d602d5b546c068ab8e54b2c34442bb70ec6ca92ca86216`  
		Last Modified: Tue, 03 Dec 2024 06:17:54 GMT  
		Size: 15.8 KB (15832 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:58259995e2bf23d42df018ba25ba3a67372a2422fdc7914cc5a132eee35433fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59686248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2739463941d7f2c81e9dcf2985fa548a020146336a6608a92ab4a327c6ebdf7a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
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
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e886790f9afca68021d7c75698a1217a115b9cc1ad35a2810b2d8b0ad55f3`  
		Last Modified: Tue, 03 Dec 2024 02:28:32 GMT  
		Size: 6.6 MB (6635953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7250eb870a6e7d1ba2c1af2ca41ebfa2fb763a5be83d1710296ff798161459c4`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143e50a785fba3cd83cef1e55edff4f0d54e965cede0048ee57f596d5735e0a`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd92cccb8507bf0ea24147acd06ddac399895aa65bc91c02c25f650bd8c41174`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 91.6 KB (91598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c62cefd1610f7333f6f871c1794e559b2115e00c5863260f9ddedd99769cf8`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7260c43f0f9e6c3c34410fdfc970a0d4fcc49429c791e26905b3e6bfca89798c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c94c1a91810b80643dc3cac6052e446072381fd31485d5f5196bd3ea6e0cb1`

```dockerfile
```

-	Layers:
	-	`sha256:deab7f2dbd81f35b295f26a1874c4c6ce9cea7f2c767ec20cdf21e9e17c46086`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 3.6 MB (3561538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2606e6a1a87f3ded6407b0d5258d8218f3da05be49ac5201a62941c4296cdb35`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 15.7 KB (15662 bytes)  
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
$ docker pull neurodebian@sha256:1e5336de47c0916153b95b268b167627f1dcbbb014b0dfe948f093a782d4337a
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
$ docker pull neurodebian@sha256:8cd5e6b7bec8b2fb545404fa4ef6bd502469cf4951c316d6e6279f2853160096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59634890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4830671f1f42f572e6707b244573102e521ead223e96423ff85026ae06f25297`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0890be792eb8cf2c454fe7c038fba6da83a8ef251447a532fa6d4f3108c2f7`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 11.2 MB (11232504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99eec1b3a608d28ef329abdd58a2e25ee524c0453b1269a4668003e0983d49`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86127ee86de4c4cff8e4bdd5c18c3f9d3021d01a9a46fb1e63a786d3c5abab3`  
		Last Modified: Tue, 04 Feb 2025 10:14:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd76384f78a868cb30bf0b964090aebaad99664c593dc1fcb7897c3ca2af13`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04417613519d31f6f792cca8327cad6db9d5664fb6531c5c94f92801518ff51d`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5ca00e53e65addbf1adf8782ccd07719cda0df67061120dae1afa0773d8cf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e6e0a88411798e9de89e740aec9110aa51198ec12d4d77b9188f3b5d0ab85a`

```dockerfile
```

-	Layers:
	-	`sha256:2c9e1237745fd9d27f596daf590b01f333c1e6ed5054993d33f0533e77edc71e`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
		Size: 3.9 MB (3933104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3978024698224d9e7ae7a49ba553a6391e10f049df270264dacc9a5d2e8d971`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
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

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:396c89536fe6db1bc27165b5b3b01c1c141024b20e94ed056ca001ee7d489199
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
$ docker pull neurodebian@sha256:11f1d8a2c1ba5807309a84fe53239c15644decd7e0f952223fcfe8e28b9d40ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58544043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d931e73790091e29816ecd8a3b3bd13e50c1b635e8ec66b670304f41e9377f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
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
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e623044ed6d226bb08223597c0f380daf46067df42de48e52515dd8b6015bd9`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 6.3 MB (6309037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df34ef8a3df44564cff9f91477c96045ed1348d5c6bacebb2c30da5ed1d67729`  
		Last Modified: Tue, 03 Dec 2024 02:32:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d9ecdc74a71cc7cfaf2b1635937b88fc90e48932874568379bd4948b83d9c0`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4420bbd6a1e5e4067d6048b9cfc560b9b39df72d87d4ed9e93ebb3c7f8be97e6`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 91.4 KB (91417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:813cab0e7d8d6a6d32eb156bb2a98ba13135a9efdefa45445c299cff634bb3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eddb8c244b0b5047058b014b003d153a1b272ae2e55f50361d6707a657d0ca`

```dockerfile
```

-	Layers:
	-	`sha256:c07968d16a78367e1d48530eb27283dfe91c39751a8b135ec9af329cb9dda337`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 3.6 MB (3559094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ddfa355e9e60cc21afc4f6d9b0f6907ad2cd79edba64fdeafb408ff1ebf336c`  
		Last Modified: Tue, 03 Dec 2024 02:32:02 GMT  
		Size: 13.6 KB (13627 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f70ccf1c4f8e34348cbd6dbdfdf30069e43ae372c6d6ae4183ee57c6cf6e7f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58746356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe90355c453a718b5f375561fdd4ffe5ee6d55f7254cf1b2b706984bfcd91d9a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
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
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:37cfe9a0d72ee56ff9cfbd3d6f54367b57a516bedd5b30b0d1a598123957ab2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3355433a01c656d9187644992eb02f399b926fd6998309ff3152bdd174664e0`

```dockerfile
```

-	Layers:
	-	`sha256:f01a69ba873a649d16109246e36645e9293f212711280454988268bed4add197`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 3.6 MB (3563973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bcd735f99065db42e22a630fcbdde19cc6d75b63789503857eba2885a0de8be`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 13.8 KB (13752 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:a6e34b9b3ef10febb3e68cb59e5d43a9cd4518aaaec42c9fb0eb764661ebac95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59703235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356823f088987741ec801961eaf46491d407c63f5df550066164acb83a595dcd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
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
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c500b7e81fb48a2ca8dfb944bf05a4434b38906509b44c8230cb468350330652`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 6.6 MB (6636172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cba7baac1bbf19c4eff6cba1e463e4514023f61e5e4f99eabf003c60f53789`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bbc8c8ecf4c50fb1afe9f838e8684a9f8283e6edf3aea752fba90ecdfb953c`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38faa38e98066ab42e204ada314c609783c4d1432e9755b2bcb597ed43dd599b`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 91.7 KB (91657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a39472daab1f7ad10eddf0cd67f8453f4675bbd31ed229cb77f9a601729e442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5077173fa2b440d42065a12b5c4ecbf78be9444e400aa418924ffe9cdeb599`

```dockerfile
```

-	Layers:
	-	`sha256:b9520b672b857555a8f6a7d165f2b5323247148278f458a7278373f979f2088f`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 3.6 MB (3556335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a715947ef1aeb942d19d5f3d425c0a032538f9e6b2ee6340f7ab1c249910cdb`  
		Last Modified: Tue, 03 Dec 2024 02:15:30 GMT  
		Size: 13.6 KB (13599 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:e7c0d77acdd38391058bb428da4b25ac4b5d5b17dbc921ee7afb854783a1cc48
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
$ docker pull neurodebian@sha256:9cdfe6f90f096c5886af048cddf57f84f7131abc4faa5f65638d66c77660e090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58544425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29dae39f0e2a61e2773abfc9d19efaff6e24355ae35e8f376529d52c260d4529`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
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
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114eb8c7559544e979c7bc06d71d09eaa2cd00debd8cf4f03a56d8104b7699b3`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 6.3 MB (6308996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff80e11993394c1dc9aaa17af36dfa33cca39fa8e0caabe1b3bf52e80a34369c`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4eb1dc4c12753dfe02a45cea97e094916913c37268158aa3b340700e68143f`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12f43e28b0e223dee7e963ea7a4ad3a48f843457e481ee84cfb74772191cd9`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 91.4 KB (91443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405db61dc15551d8850b73eec4f6ecee2d15504c5d277afd2c8128e17ecf6611`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1bf2d8e93155ae981f2f562f22bf9918fdb877c66cffd35655fec1d9b1f39938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffd90ef4d3ae1ed5361af576f9d3f2c0d2a5754f07e470e32f3a78bc8bd6096`

```dockerfile
```

-	Layers:
	-	`sha256:9702d640d901ef7903e74e7c2b43af913d4f418a939adc866950dcedaf2a783a`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 3.6 MB (3559130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7bb223c6e89608e9722bf8101c7626ae5724ae67e6be3bab333911378929ca4`  
		Last Modified: Tue, 03 Dec 2024 02:32:03 GMT  
		Size: 15.7 KB (15653 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c7ac4ef4afbf39509f7a22b31591f646ef72bc02b766b53e5fd512cdd67e0175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58746750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed54a230a0fd8bfde46f98be15f4d3b97ce2d877b842da7ab902c830cee5c0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
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
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Tue, 03 Dec 2024 06:18:20 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Tue, 03 Dec 2024 06:18:19 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c880850a32196b5042f578dfb72c4fa93d1ee7ebd60d71fa4d5fbe19814c1ac`  
		Last Modified: Tue, 03 Dec 2024 06:18:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:22661e3cbf436b44b80103996ca2bd6577e74d6b1b8bebb5202171aadd46a284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d846bb8b6f1144a2d45721e8f45c30c3f32192c7a1ac72ca6b7268efa446fe48`

```dockerfile
```

-	Layers:
	-	`sha256:96771062d69621936e46943c2483b9fbc12aa2771b6c3722cb1035b36ef91682`  
		Last Modified: Tue, 03 Dec 2024 06:18:32 GMT  
		Size: 3.6 MB (3564009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c24f5aff628042c5046d45e533873a264167660d2769d5c6aa4aad04528fe9`  
		Last Modified: Tue, 03 Dec 2024 06:18:31 GMT  
		Size: 15.8 KB (15793 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a7f28e60fef8ae8c66fd2dba17b3f842cc070ff0f190ebc2bdf9a7a8be76fe7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59703410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991a1f70a2c0871c021a308aded3c9b948de0de66faaa7121a2d269e4640fc96`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
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
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998bde38fb7afd531148bc5ada8932ba6909774db1014c810250d2fed9705c28`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 6.6 MB (6635982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff379f8e9bb8d25d6e0f0189f738f8b022e1073b791de493bf8117cc6d281ae`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863c1b51d89e4dd4797ba1c7a7da71a5c460240254b1e7853212c5b2e920c1af`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bc6338d9947bdf727b4f355b78ec884ccc098bacc03deb3d7965d5d04398bb`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 91.6 KB (91629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deb6e8c73557a116710e67686758ffb933b5075a0bed69a3dae3ca0be59627d`  
		Last Modified: Tue, 03 Dec 2024 02:28:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74f05ff960ca0068515281f926b0c25dbcf76375b4f99e58125b16a689b862ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d55b24693960716604398d554cbad7c385b5f86da205d5292975eeb67833ff`

```dockerfile
```

-	Layers:
	-	`sha256:74ca85f2e86db85f7b30f20d46e8e42be283a7b27e1b60976e0ff56e761fd5f2`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 3.6 MB (3556371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d03ff36e1583fd5288b7e43255d4ae49d2af7984f1801d3d5ea02eae17b0cc6`  
		Last Modified: Tue, 03 Dec 2024 02:28:45 GMT  
		Size: 15.6 KB (15623 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:bbc3ded260e52ab68dea79f0a8860a9853977c5b81a7cbc61da66dd3e73e464d
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
$ docker pull neurodebian@sha256:22ba4c69dfacb7993f7fcf3708c2ec38e7a15ed1bed206d226c5160e47273847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58516023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6fd9c4b14dc331719047f53a409b7b3093d384a6ff135c95b14e664c6b43885`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
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
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31fa211153a834040c35ecc855708df74ae143e0f067f5f29d4299bec783171`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 6.3 MB (6309046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759be46808786c18908d758383834044fed05ddaf818585877931072aaa3bea3`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9340f215c3f9e9497b17c7dcc21314a53d5553d70c1a45f9ecd9663aa523c`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809dd25b48752fba0eeac0fcf5c38a88f0e12b0db0b022acf82ae7fafd98800f`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 91.4 KB (91435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b22d1f83ebacbb4392e9e1ec31a9e0902f3f7a2cde703ee063fc39bfcd1b648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9d1493dabbbd58df5573fa3c3dc733bfb235815353be42c104a85da39f4758`

```dockerfile
```

-	Layers:
	-	`sha256:8cfad2f41e51e9ca8348d9d7852f9a0f81c5d0a482874503181c168442d46e8d`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 3.6 MB (3564266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291ee8d275476a4f56b64a69bb3c484a527878d207b0f47533dc5df2c24f9458`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1401e84e1f34ba3fec0eccc60bfdb562ec886b1705aeb33459074a37aed25700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58723605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547bcc904f8cc765088dc02b9c5eac15bece1c36242ba056fa8894fa557231aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
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
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8640b31431e2f1a1a2b65b6fed2b7a4bcd6826c4d1cb17e4d8e1e9e2bf2ec5`  
		Last Modified: Tue, 03 Dec 2024 06:17:43 GMT  
		Size: 6.3 MB (6288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f67a6b589fb5f0c9202e6eb9aa7cc5ec0a7c2e67c81df4d2e3f8bc9603c4e9`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96d02cd9c1d5c2742decbe351e194414adec825bee6bbd6263521be0a514665`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d38c51092ac20a5bcd1dfc533de43a738889d192e62656482dc22f1505a79`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 92.2 KB (92158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d4b78788290c99294a51ceca1957d8eb6e9e849177decb1f820324a7d85b171a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3582936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c170b6bf1352da87527070a521d5bca904ee0e113091bee7260deb2c47e958`

```dockerfile
```

-	Layers:
	-	`sha256:60730bef667d6b97b826f735f2547ce96c7c51f072bed45993eb690ead280fc9`  
		Last Modified: Tue, 03 Dec 2024 06:17:43 GMT  
		Size: 3.6 MB (3569145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a78c16c7a4e8d937b184fa40339df44fa15f714b5d50ea63d627b3763ab773`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 13.8 KB (13791 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:0c302d3d91a06e0de1ae44728e6c238af8f332b079b0dde357761280c7738727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59685891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eda70426935cafff4ae79341debf8d16acdb137a79c79aaf95a4e89287e257`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
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
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07d21ec843fdae56608290e710928213278f433f216169549f4105b0b7adcde`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 6.6 MB (6636002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790ba6a36bbd0ddde077446c337522dff4905079f146ba4f81c5f1b1ba01508e`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f988e696d1fd940f6f8a41f61db71109214ffa05a741e7ad19280fab3317b7a6`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7105d8b802d7cbbf45432b1a9323e287ee890f7b63ac52b16e684f8aa59aa436`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 91.6 KB (91615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:640e8a6c2b29256a11a97f4fab868b83769f471a9a56a787f0520ea21d8560d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0a2cb4139fdbf18dfb086e8db81f463979da7309ce33c42798424276477172`

```dockerfile
```

-	Layers:
	-	`sha256:13a56528e8fb58e39de0f1b02fd41e36f2ce6114df32afe325634c478c2d46c0`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 3.6 MB (3561502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda46b32b1387c0fd07559cd518cb696c94a4a839d171f21cf6124f57cee113a`  
		Last Modified: Tue, 03 Dec 2024 02:15:10 GMT  
		Size: 13.6 KB (13638 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:a78a1c95462db7bf414f96ce328616fe968aac57b876af3362c3e4b47cdb81f1
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
$ docker pull neurodebian@sha256:dc2ee078717e5cd6782de72121bcc9936ef63cb0981ca8e921754737a77980e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58516479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf94ef9a8ab87a336dec4a29f001d654de0e935525f16a071a00515579aff5be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
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
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507e5811b953238ff193b1168d33f51c6e9d529f200a09d5a7cacc81a3cc8c3`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 6.3 MB (6309097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53110b5d9fe921d17db007a1ddcf5a14b209223be44404d7367639af0432a720`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073121ed00d2745775e339f48a955b95fe1cf8f720671dcb447fc1ed84db92f`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a4d13654e7924d6b2b37ec66b136d37c2be5c0336ea4c05ed6c366e2a4fd3f`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 91.4 KB (91421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8461a91abccfb6a0564642a71b515e4966ed0f07a5adb19dea1de7fda249aaf0`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 422.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7de7481f3bac1a3622e0eed2ca47e8f02312431429159b58502dfc6e1b23d76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bcddfe5efc17cf322b5dd0859093bb6b3567c32ae516fe9b443b80a0541765`

```dockerfile
```

-	Layers:
	-	`sha256:70ad6f08346ad337d0f9e32f7ec11b22ad0d818d1df8a6aee0a4052c1cd75b1d`  
		Last Modified: Tue, 03 Dec 2024 02:31:57 GMT  
		Size: 3.6 MB (3564302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97d1de4b535410fddab63f0e6af15dfaa00cec28ba8c0fde0a15678db848775`  
		Last Modified: Tue, 03 Dec 2024 02:31:58 GMT  
		Size: 15.7 KB (15692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:17fe10b8e293faa659d945422ff3aaf4c7e6e1f387d707d314802beb80b71a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58724028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85d39b737a8ff196e533cfc0ffb9a1412e43594be8673e8c0da6c05751f91ce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
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
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8640b31431e2f1a1a2b65b6fed2b7a4bcd6826c4d1cb17e4d8e1e9e2bf2ec5`  
		Last Modified: Tue, 03 Dec 2024 06:17:43 GMT  
		Size: 6.3 MB (6288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f67a6b589fb5f0c9202e6eb9aa7cc5ec0a7c2e67c81df4d2e3f8bc9603c4e9`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96d02cd9c1d5c2742decbe351e194414adec825bee6bbd6263521be0a514665`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d38c51092ac20a5bcd1dfc533de43a738889d192e62656482dc22f1505a79`  
		Last Modified: Tue, 03 Dec 2024 06:17:42 GMT  
		Size: 92.2 KB (92158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da18a25c93d7133b2d4097e549a323142182e4dd20d54315927b6bd6573eb0f1`  
		Last Modified: Tue, 03 Dec 2024 06:17:54 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c77a0b2714832915027f323e1b1215a7ec8179d2324362662d8283e9cad88fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7509c00ee24dafaacefc91ed80721178d33398b768fb59515c8052afde5a23`

```dockerfile
```

-	Layers:
	-	`sha256:27c4680740117658f3a6d274e90c1bc193f9aed297af2e9c8658296f77a30654`  
		Last Modified: Tue, 03 Dec 2024 06:17:55 GMT  
		Size: 3.6 MB (3569181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37b47d54c077c2ac6d602d5b546c068ab8e54b2c34442bb70ec6ca92ca86216`  
		Last Modified: Tue, 03 Dec 2024 06:17:54 GMT  
		Size: 15.8 KB (15832 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:58259995e2bf23d42df018ba25ba3a67372a2422fdc7914cc5a132eee35433fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59686248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2739463941d7f2c81e9dcf2985fa548a020146336a6608a92ab4a327c6ebdf7a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
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
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e886790f9afca68021d7c75698a1217a115b9cc1ad35a2810b2d8b0ad55f3`  
		Last Modified: Tue, 03 Dec 2024 02:28:32 GMT  
		Size: 6.6 MB (6635953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7250eb870a6e7d1ba2c1af2ca41ebfa2fb763a5be83d1710296ff798161459c4`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143e50a785fba3cd83cef1e55edff4f0d54e965cede0048ee57f596d5735e0a`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd92cccb8507bf0ea24147acd06ddac399895aa65bc91c02c25f650bd8c41174`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 91.6 KB (91598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c62cefd1610f7333f6f871c1794e559b2115e00c5863260f9ddedd99769cf8`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7260c43f0f9e6c3c34410fdfc970a0d4fcc49429c791e26905b3e6bfca89798c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c94c1a91810b80643dc3cac6052e446072381fd31485d5f5196bd3ea6e0cb1`

```dockerfile
```

-	Layers:
	-	`sha256:deab7f2dbd81f35b295f26a1874c4c6ce9cea7f2c767ec20cdf21e9e17c46086`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 3.6 MB (3561538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2606e6a1a87f3ded6407b0d5258d8218f3da05be49ac5201a62941c4296cdb35`  
		Last Modified: Tue, 03 Dec 2024 02:28:31 GMT  
		Size: 15.7 KB (15662 bytes)  
		MIME: application/vnd.in-toto+json
