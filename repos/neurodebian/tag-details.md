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
-	[`neurodebian:noble`](#neurodebiannoble)
-	[`neurodebian:noble-non-free`](#neurodebiannoble-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:trixie`](#neurodebiantrixie)
-	[`neurodebian:trixie-non-free`](#neurodebiantrixie-non-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:a2f6c6c17cbff7230acda8ba612accec5e349bc96bee30683331819139123c5e
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
$ docker pull neurodebian@sha256:5f1edf985e61cbf97efde486919a11cdd1321784ec5b689c0f663a239d432930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59864512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1cc70e97c70e7365943b885250206fc0d0c006c184e0b4575b525b62313409`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0b13f85cef1bc2ce7a76cce6ee029b8243a25927e76e49c158f666b198ab34`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 11.3 MB (11273489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92465114cfa19af1e7d1465a6f07aad31ab6a7f79430a86503f930f75bcd8e`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb5eea44fd635d732ce776ec41e954350fd60febd30f2535ff90a95f02e694f`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65045d6e9755b4521bff489a4cfe874d64afb12913afd6f9409b4db8e75815bb`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 93.4 KB (93418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c9485f81f0ed7a82857ed2e106a72658d92a0a5832d2579c9f4a82793447f3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e762b972906fe4849f770c267338ecc5808183adfbef8b29e5e2a57621bf3a82`

```dockerfile
```

-	Layers:
	-	`sha256:4c8c3519546430d89e9b45731f379793f0aaece5a5b1f8d2226cce0a72c3d9c1`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 4.1 MB (4075897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf2d39b2b10172be44e16176c499bbedcfe866819416458e1e92f0cdf558f0db`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e09ea831c61b1599fee2f299d7b74d41da8949d4716e00c7070574df27d2ec77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59727931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4d565a6c8435852e6e559d6b02681dec3672d38d0a85f01c31ae36fc3d1df8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:30:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afb329fa1729a6052cb601fa1fd906fb64972f64a4d5d5ef8bbbec2a906fe06`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 11.3 MB (11252799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec52cdc62034f3ec44c096f32d8778424dfc37eba422546e223cd08f6eed2d8`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09da1e782941a6a1a9e1201cc009fac57339572ac8dd69850a04fc1a351f594`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f636239c1baebf36cadcf17254c8afd9c5f67cc9c85dbbd502825029a7cafce8`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 93.5 KB (93528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:190c613f459064bb90444e69cf51a087c870c70a443ed2bf9ef5dec9c4725c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd59ed66a025e7638acec0af37cc2fef4495c82bd69e9d16fa6bb0b869682bdb`

```dockerfile
```

-	Layers:
	-	`sha256:d3b2aa904e74e6dcc427cceb1d8b8356233433b22667cb251cee74b1eb2bf7d4`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 4.1 MB (4076139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48223a98ca62724d50b0bd324d3ed7f9901ed2539707511cf2294f84e096fe82`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:06efd2617c2deff0de78668a4b93e2de94a16cd6c1e9cb08d532101a29937c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61271862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48850400bca13d7fdf7526618a52ed599cf2e3bd747447233f88108c81435917`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566da1b3f80bb347d6012fd5fb6da173dfe240808cde5ab901fcade81dcaa9c7`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 11.7 MB (11693150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb3ca3fa9e5e3255de5568039d480a7f42aae72daa70e9876f9d7928795d9ee`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4126cfc6ef24413ff78a87e200613bcccde45c97c74be127627edd576f7af08f`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5d7d17adcbb67f3ad0df7a77b50d4294d8881831996e1cb11f0ef6165ea3f4`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 93.4 KB (93420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c39f6c8b1cdf8815739b276741eaa50ed5c76dfbde1f1835cdc41dea44ad9874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9eaecb3bea7efa86360330985d1ec29e0985e05710bf2a09b60d3ace766fd51`

```dockerfile
```

-	Layers:
	-	`sha256:6587da0d5f807f38b05ab0f76a42070423152338f48345c24225c80a2a938790`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 4.1 MB (4073864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b0fcfbd3941a2122b6c9144f53972601b6d65978393a60dfe8aa09b6228a1a`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:791e12aca1a39722b6d5ae4fba3f0a01bca8d358c1bbc2d4f26ca249dc87b16f
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
$ docker pull neurodebian@sha256:a68c734c00b3698e7b11888eadb04a8991624b39bcf23290d300838be1056578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59864739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b109e02369ad91c522bb9e160852fce154742b03780232bf4cc904c120daf43`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b209413f350467a5ae5c418b73ac48d809463e6e3a290d3c1208cba9f34ab3c4`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 11.3 MB (11273289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958835a82131d9b249019b0445717bd4394054b82052fa141556a6d461bc9f80`  
		Last Modified: Tue, 19 May 2026 23:26:49 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac5731f71ed9fc336e58efcce2de819cd14828671adaff420902f9ea091455`  
		Last Modified: Tue, 19 May 2026 23:26:49 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482b13f29d6faade6a1f514b290c009e4e3359f58d34d63eb1216860ad993e07`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129025ba31fda6ce65a428088c21ea0cea14bd38c373c8fd604bfd5a37d1e73a`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4e94433e88f2b411bb7b941a087ce937c99b12e028a35ad7e2ff891096fb5a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93eeca15a1daefa3344c6cee6c1ebd5491b3d9d6cd9da0063c9d72949d646ec`

```dockerfile
```

-	Layers:
	-	`sha256:aac31dcc3ceeda2a52871716697b75acce365af34fa105b8e1b5f4300226f219`  
		Last Modified: Tue, 19 May 2026 23:26:49 GMT  
		Size: 4.1 MB (4075933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ba866a07c775385e7b15a1ddc70d503cab165741c7bdc97dbfe353dc296a8b`  
		Last Modified: Tue, 19 May 2026 23:26:49 GMT  
		Size: 16.0 KB (15991 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:960268a0372f026e30de47583581420aab60507a81b59f30c9ec236c22d8beb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59728479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41ac9c5e150732a2c484624f2b4fa08dd0eea99f7668781be6b9c9dc59d69b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:30:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ea4a2729c69acfa17c3025a40f85513b1f8639dc8170799e6eec54c9c1bcc3`  
		Last Modified: Tue, 19 May 2026 23:30:36 GMT  
		Size: 11.3 MB (11252891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e1bb079ba66989f9a8f05c2354e7fd267fc98337b75e080b077d7f9d41a6e`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b8923883494084dd5136c060256ccf663838d09a4d3d46c8111d1cc801baa4`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad721159bb9271b363502e3e9d13a790c54d04a383ed7b61f4c0934f6812e79`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 93.5 KB (93534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb84a30c185b452bf5a889119a5572594d3c7d011797304bfc7ad44dbb80e29`  
		Last Modified: Tue, 19 May 2026 23:30:36 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cef5a64a1236af4f765b8b55512bf00b5960ae98634a89f831af7a3d3cd27f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49220dd3c313a7622e2379927a6d1d0d7d8298ffd7a53206ce6fbb0c4cb994ea`

```dockerfile
```

-	Layers:
	-	`sha256:183066e63f4513b84fc0147089b908d7f81c70d581695c94ac38738674cba9fe`  
		Last Modified: Tue, 19 May 2026 23:30:36 GMT  
		Size: 4.1 MB (4076175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebffd27b4acf3ef30f36b1a2650a111e7419e0033ca66b64ec53a948a253bc21`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:84f110cbc4ed1d46ffeed162a00e9bb00b38814c6ee85c28c21ec82aaa1d40af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61272369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e517f47cfe4822fb2559e4c5816d14cd178edf81821527e0826c845da942de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce19c0c826a9877ab35c71e19668e7fe552ebc4cbf2dfda44942b387c25f88d`  
		Last Modified: Tue, 19 May 2026 23:26:29 GMT  
		Size: 11.7 MB (11693199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622a94d295eafa3598fc7d9046e7abf0c9c4d1d58b75c75db2a9f8f833ce7516`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779d6106bbf28141a507337cd68918f9d28aa64456b30457ccfc33b407f238ab`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f312fbdefaf85dc165c74188b8c6c551e6c3727ba585a5e4bcb19dc72769878a`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 93.4 KB (93426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86a918356a5e7208590f4ebbe73847002c2a322bf305dbd1e31cbeecf50957`  
		Last Modified: Tue, 19 May 2026 23:26:29 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:69518252dc6ce99e801b80526398eeb44fb77b2c07dc53ad098081f7e56e8491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e83b685d9744d857eab93f333917d66051cc16e7151853030a79f3e9da8273`

```dockerfile
```

-	Layers:
	-	`sha256:a0e03d802fcd6e495e1344cb76893109fffb3fa25bc30b5473032e853cc24ef7`  
		Last Modified: Tue, 19 May 2026 23:26:29 GMT  
		Size: 4.1 MB (4073900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0747c02c4b6d7840f1f3c14525dbfdaa1dca392187513d58dfc3381ccb73941`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:eff8b93f637626ebb59c8def717e00670475023d5c1da61cd0ed6f636aa7ca48
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
$ docker pull neurodebian@sha256:9b243bc24265ea356b0c5be55f8a2b411a2ea2290864a7807b60a51ac5c3a613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64975821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22347b7237e8cb430fe55f5b78738e9a3e2398d013e2c3fe0cca9275a438e078`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7236d1089a039f5ffc6e36f0f0c0fa5d2b327158b4baf949b6f4f2efbb115c29`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 11.1 MB (11103419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c366df488968e5fbfefa6fdf8cf3ef33c7cf8c54f81d98f46f231ac0e483c71e`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad28559cefce11e4196ba5ad2f8f0b8c4357774b782c1f2aa86ef2895221736`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a8c66f53355fe68d5301ab9393eee9d2b137ccae00ce12e24369af94e7723a`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 101.4 KB (101393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8776d4efbdeedad14efaac21ef11495cce5a02a1ab472f4a96f18910e7de4875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2b3dde9dd3c4994b35307a367496f1a17e6b0ce9042130e014da2a15bc404b`

```dockerfile
```

-	Layers:
	-	`sha256:27784bee2552828171717d2107483a4211d66523d613a2e66fa9d272833a0a11`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97356413bd0310cd9473f5ad7ddbbdd00b2ce65ccd309a751c863e33581be74b`  
		Last Modified: Tue, 19 May 2026 23:26:40 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:82b0af26743b912b012739ce6e8c20744e6992a30ce5729c13ff5421683205e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63469957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d8df7d8e955f1470b9f5bb291d5a231550cb0422741a69912a7a532d2b61d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:30:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:02 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0cc4562f1c5f7bb18eebecd9ad923d8d4541d490d5454803267f581a0e747c`  
		Last Modified: Tue, 19 May 2026 23:30:12 GMT  
		Size: 11.1 MB (11109955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c766a489b2eb8d722fb99314aab9123c016e02b6356a91d3bbe1037787cfe592`  
		Last Modified: Tue, 19 May 2026 23:30:12 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b887c9d1e4c3b8b180c3e9d16e8f10ba5d0d185f473b3749a2e18cb162451f7`  
		Last Modified: Tue, 19 May 2026 23:30:12 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57b61e40bf16a60d7d5c3a040961119572d6021db6078d4d3d26f2a4a25890e`  
		Last Modified: Tue, 19 May 2026 23:30:12 GMT  
		Size: 101.3 KB (101265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0ec18ac1afedb8703040b4da626bc389fc02969276be301cfee03a1771101f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae2e6957c59d38736b66da84eb56d10be26eae449f3d9d77dbd2a0b02c85577`

```dockerfile
```

-	Layers:
	-	`sha256:faf74e35773044ccf7896f73ba345067eecc8fb6c573c7d5d0a5e0528a4aa19b`  
		Last Modified: Tue, 19 May 2026 23:30:12 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c332b90e207904b573d2f4aeb7f6e4b7cc662525b6be14551bdf1d563512ab0`  
		Last Modified: Tue, 19 May 2026 23:30:12 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:97ec0a5bc8c4a40c636fd93c1c9fde4a07657b191b94d494d4aba05195fb3fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66315053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf2e159c542858f46e0c17627da7185487e15be8d0598b7d8a797719d782a9a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:25:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:25:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:25:52 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:25:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e09eb609a6245c10b9cb43e597a7ec3d9e4224f925e717a38f2fb36787a4e7c0`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 54.7 MB (54709050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6ef78f35d55a7bdcd4ce51a8250fab7f87447997a985bec19d4f5df93176b7`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 11.5 MB (11502540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381543fb5518886d0decd77840694831287740a98172554d552db0976a629d78`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 1.9 KB (1896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66477593a0b871768cf3a1418cada25d9f4af13c700326cdfd49ab211fcd34ad`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff955a9c4e443cf9f3142612d3ab247200cad20aa22c18cd1409dfd7eca4980`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 101.3 KB (101303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ea456581c23a81a6c38c1653d1c2c94be10f778f8cd85ed42614740430690e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d3e5c7dfc130587ee7865e02dfb567debf1712d918ab299e1430b8ade65e5e`

```dockerfile
```

-	Layers:
	-	`sha256:e307f0838abd851e0cf52756ae65d7aec7e0335039fd55bbcb901812698bafba`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:049f7c47d2e2f1d7d8c5883c6552fb68c7be64c58c35b3dc3549795dd6f1ae98`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:f1f3f65be806cd2e5289859430967fb45d2c86b81d8f9e5647f088472979881a
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
$ docker pull neurodebian@sha256:a31f245a8e23ab333d0cb91a20812909e691960a320848d4ef26b352815a7a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64976262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5f8d51d8fe2e0b29833a6930ee9ed8127229396c7bf674da0550ba14789465`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cb8ccddb7ae905a7c15a308bcc5010fd4a842839e6c4e55aea5037fc2c6f88`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 11.1 MB (11103489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73aec67b21a1a6c0b4dc177a5965f48251ca61285c2843d50601d15bff859db`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f906aead18b295a02b3010f8b914a9b91159b0bda97419216db9f38e2ad3d90b`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60969937977bcc4c5b60c1148c0bc24e73935eb4543bc321604bd0cb403bd1a`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 101.4 KB (101372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dbca80d9daeba4dc863e30e3d1b11e83b590a71f2404c0f81f620de94f8861`  
		Last Modified: Tue, 19 May 2026 23:26:45 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4c7c72ba8aa60242c01595e6c329c6841fdb75347d3a378338e8f79168111c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b351f919e5d6f50af1abf13db25055742b5206b749deb69a8512c9483a9321`

```dockerfile
```

-	Layers:
	-	`sha256:2f85224be519cfcaeecbec362461b06c554dec6c914ac74dc25ea1b39c2399b1`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0003492d33be36dc5b18d246a9b0ceecfcdc28900cc4527fde33b969d8b65b6`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 16.0 KB (15993 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:44ae51ff793f39946038ce5d95af869b3b70558a685f74437925423722dfc75a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63470348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818e4b617c895bb6f2e851ddf2b7aa3e84a209b97a6f73727ac44d87e804840`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:30:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ec49c2c0e7ae149d1217b1064a04894098733733e47129d491b619501080bc`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 11.1 MB (11109941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3221195c4a3803c742597ae3c20c7938603d4225ba8bc12e2a132e14ec3c1534`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3976723b40480b65484fdac4ff3b9cb3f2c4adfaad97bd5fcc0ce764f71730d`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30ea5cadfabf914d41176cf9b67c2e8c84268162895103d5f5a190a1c91f259`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 101.3 KB (101283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f656a055002be466165c33f521121cc4442274cdf721654db837483142b402e`  
		Last Modified: Tue, 19 May 2026 23:30:31 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a1a1bb1d584fd6181b16c73cdf9c96191c3e2364aa67a79031ed79b692977be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e012ba92c198995a31023ae78735740956364723a16b42738cf90b5bf0d33866`

```dockerfile
```

-	Layers:
	-	`sha256:14bbb92d22c5cfb94345cfb92bdf1472efdbc687a191ad6da80b3deb70706234`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:372972fb25a4fc5ab5ca9c1eb667e639300981bf1c0f0ebfe6758a13599a0111`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:dce71c3d3978a2a855abcf1bc5a83a54b0f1eb84afe9c708d37b9945612e3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66315350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0801860e74bdd4e1248165adcc97832ff1397a208cb4e9e22f057ff56cc487c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:25:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:25:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:25:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:25:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:25:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e09eb609a6245c10b9cb43e597a7ec3d9e4224f925e717a38f2fb36787a4e7c0`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 54.7 MB (54709050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95b0b4b40e146641da97fbb635272948b4c269cec26aa79cbfb54c37dbe1649`  
		Last Modified: Tue, 19 May 2026 23:26:05 GMT  
		Size: 11.5 MB (11502477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45354a9aa4ef78b02696ceb5c8a0ef10d0988ccf5c880ada568b69ece7d4c16`  
		Last Modified: Tue, 19 May 2026 23:26:04 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987dc208402f1ea8675711285765d6168b97248acb8af9055c80f2d60ce40408`  
		Last Modified: Tue, 19 May 2026 23:26:04 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6f4d36ca15503abe1f07e2b4c2b1de0779f2c0637b548f8b311632e249513c`  
		Last Modified: Tue, 19 May 2026 23:26:05 GMT  
		Size: 101.3 KB (101276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb5a5de4f9760cf73bff4a94a316eb883b68e28b6e15d06881dcef89e8ea279`  
		Last Modified: Tue, 19 May 2026 23:26:05 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c9a4a7d9ac0a43c6ef88e5f3f498ce786c0ecaea09f7225e425e6ffb3efe7e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b511300d3fa88ec3da28b7d91942be85641b4ee4e5e05658b51c195e548a2da2`

```dockerfile
```

-	Layers:
	-	`sha256:d1b2779cbb92980bf8bab7aece37d6ba04e04f00759c3ad6b8a4de4bec717427`  
		Last Modified: Tue, 19 May 2026 23:26:05 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:715cda405a610752bcc00c2ba1c11215cf139bdc737d545c950bef4d1c5f0117`  
		Last Modified: Tue, 19 May 2026 23:26:04 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:124f3cd766fdb6aaa33675b961fe5dc94a3f9e6a957900ed827264af42cdfdfa
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
$ docker pull neurodebian@sha256:f57061aced5b88df44aa3221139686d245a805cd359f62e3a71f8f7c9c3a9109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60181755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7121d0b3446b9c3052cf5091a7bb78220dedb781a0c3d91d34dabde8f374a7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:27:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30b85315dec2d58f35c416abc0e468c9a5fb485e83af8c76ba1b33292e721633`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48697206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c83530a6b51b03de05e55eaeecb58ea7b7ce335817e7289c21cefc0f862cb3`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 11.4 MB (11392191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d02498190a7406351e8a8b106b0cddb3d47e50d1b7880474dcd87e5dadde74`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f543c19bffe03075382a45dfc91388da45cf11bf12ec5be4f33fb84234947212`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5270106ce715802dd9a6ba52b784375677aa57ea1f908f6657055fc3fa3adc36`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 89.5 KB (89451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:49dce879208c36525248f3b7d81cf77a7e45a99563981099c221033c55baf4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84c58a46f234563da19731d3792446c0a348b39255c47d65573ce856c991ce0`

```dockerfile
```

-	Layers:
	-	`sha256:963280b72f123e9ec9bc34ecc09368955c2c72f6338539252f0cced6feee7527`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 3.6 MB (3555633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d28a7d1dee2b324f02d370f9a9386e5558d48e4da78765b27a72b5a8c9d90b`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d2db333e4115682fce4df1e16d76b6fedc97c62b529c682a706bec75f471d3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59906141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e66451b03a9ef7caea93c64d629129a1f9d1211f13d464924e36243cb619050`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:30:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d4360d64f4e71c17817e39372cada00ee239c7d2715cf79f6e6cdc602a7cd46a`  
		Last Modified: Tue, 19 May 2026 22:36:44 GMT  
		Size: 48.7 MB (48720031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4576c4f7d45466740a199d54662cab12c85d21bc75740a97055a71b74822fb25`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 11.1 MB (11093120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9a7a448cc8b0211eb9bef63518a33e6ab21d9096e89b4d32e81161f1b4437b`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e100d1e87b39987108ee142e1e682902047cbc3339a12200c2f6773805ef3056`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41863c941f5466e882167b32083d10a3cff9cb82e7186de9f4097e6bfb1c557`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 90.1 KB (90082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9c3438fe9c4af5de6d4d80b3d33125a7f7cdcf118c2ee3063e8d7a42175ac858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13987104def2f6995f2fe59b900687cbb3d9f7109576c03d65703666cd98da14`

```dockerfile
```

-	Layers:
	-	`sha256:7db5d6425f8abbb85f4075eeffe58aabf77d9534b67e80f7e686f18ac7c6cb83`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 3.6 MB (3560338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a85afa279224730598bd1b8225f47db376acdec114e15fd4c73c07fe25d2a289`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 14.1 KB (14056 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:5ce574a56b23425bece211570b1ece4c6df414cf625f351a54bf965123f53ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61720477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f2526638ec2933cdadb2da0854e7be0f6f6e3096b2baee6120a885fbe5e431`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:26:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7af1962edabe3d58af5fbd06f3e345528b78b672a4b879b72fcf2e0d92549637`  
		Last Modified: Tue, 19 May 2026 22:36:57 GMT  
		Size: 50.0 MB (50001944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f9c5f81aa30e1e455f4be28ee2b9c7a2f372aa9baad7d1164b050349789042`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 11.6 MB (11625868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289977e8f65a11c099d93af9b5d6100a3be07a1e5230cc672288ad3973b4c79b`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a679fcb6a1b512652aa74206d34f8d5c94d65eb95dba15a6c60df8706b0d7f`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e1363a87009473e2d0e443822d5a07d125247e5297e598a5efe55903304804`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 89.8 KB (89757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4d20751ac6c9509f53f494f8b604eb1c5fb69dcbf005ec453121e82bfac9c4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7eab1ea7fe4a42bf5b8b03524b27b59a22ddcd66cc3c4b3a25af3bcc0ae330`

```dockerfile
```

-	Layers:
	-	`sha256:4058109d32d62eda5118e9f4efd197a8a5e5e43ddd1b17c9b25645a963b9a63f`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 3.6 MB (3553579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ecb7a56e8c9159c1228306bcbd5b31938c520d3edae46de65313aabdab11187`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:fc692782f71ccb077da8611789c9d51663053488c1e1182d5126e93dfda29f1d
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
$ docker pull neurodebian@sha256:dd5bc7f6893df426625b44e21543155e38944c72365cdde75b136cb1114f3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60182055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac711ac0cf19ff39eec3d6b93c2c44ac71263b998019c8ce6d6c3151688edd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:27:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:07 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:30b85315dec2d58f35c416abc0e468c9a5fb485e83af8c76ba1b33292e721633`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48697206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8034887a0bbbfb1d67831fbc844720a3b006206b9e49f7870fb5005bb3c89001`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 11.4 MB (11392061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91ec5878091a1da281fc06f89966a5ce781d30d1cdadb3534b96138fbbca5c`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f543c19bffe03075382a45dfc91388da45cf11bf12ec5be4f33fb84234947212`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399ae341c4077520a588253618e8c4225e95ff6ae9bc4b9e1633da51a6a75100`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 89.4 KB (89436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5bb7d619a42df196180ed8bef0b5f80176bf6f00f546b800c1c31b10d9f9e9`  
		Last Modified: Tue, 19 May 2026 23:27:17 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:044e4a207e873752dda35d4d8cfd81e45c7bbdb7989a0ee0d4311fa09acc29ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e367fda5e18a445afa9fc71877870628f335e4d71a337fc4bdc50de917ca7800`

```dockerfile
```

-	Layers:
	-	`sha256:15a08b05785f1847bd3d3df55e8443c0d80c779856b0862e24ec6c38169d075a`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 3.6 MB (3555669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7dd5aacc2dcb6133d43b785423cf00d00309871d85a776360ceba20e840ce0`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b5343f56c1fb31218429053ffbecc0cdb55062fcd20ecfe9d728041c5c01d50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59906536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c799133513afa7f756207bde3447643a51b965c35cd88008e1a6556f3ffc8999`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:30:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d4360d64f4e71c17817e39372cada00ee239c7d2715cf79f6e6cdc602a7cd46a`  
		Last Modified: Tue, 19 May 2026 22:36:44 GMT  
		Size: 48.7 MB (48720031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec98f49d5e4fa11cebafb79bb6f58fbef7023c8a19fcce5aa94df4a4e7496f9`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 11.1 MB (11093072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9a7a448cc8b0211eb9bef63518a33e6ab21d9096e89b4d32e81161f1b4437b`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e100d1e87b39987108ee142e1e682902047cbc3339a12200c2f6773805ef3056`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c32e23cd1e65b98407dd7e7eb4196697bdb064b3446d752955286f082a89bd2`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 90.1 KB (90077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9bc2b2cf57a5d3f81b2da41573718da95babb252453b4969fc2bfb79f25f89`  
		Last Modified: Tue, 19 May 2026 23:31:02 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8ef9c7076cdb1f64991964c59458038a88cd5185a2cedd92eb15cfe92ddd0946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222b74591ff62cec5f61294bba8e63539d6d288cbfd0767d3ac7f827ed20a158`

```dockerfile
```

-	Layers:
	-	`sha256:5abbd613c8df3b55c925c540eecc65c824e5574b6fb95d4311b7e67d29ef7735`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 3.6 MB (3560374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0379800346bedbe8114baa2a2a59c79880f928a6875b195fcce6d11a9d4d17`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:3b0d1d02630a55a6c377fac8567c347cb626f7b41b37009486d26cc4219a707c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61720915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a46cd04684649a857887b5148ed9863726fbeae7e8cdc8a0c3af9b9e4fb03f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:26:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7af1962edabe3d58af5fbd06f3e345528b78b672a4b879b72fcf2e0d92549637`  
		Last Modified: Tue, 19 May 2026 22:36:57 GMT  
		Size: 50.0 MB (50001944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b022792ab90d17b19c012791d704160e1cb4d9c1094ed5126b1ac93056114f`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 11.6 MB (11625868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80680d0e09afe77e520bc718136fe080de719a24960af381889b5325a007ced5`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a2f99f1f32136fec89aea3b0aaf2aca4477d31c89bde845d0e723a40a5695`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56352ba5cb0918dea97f161038dfd699afb0529bea66b2ba9e35950d31b10132`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 89.7 KB (89747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1ddd8e31b744cbe0b5383cca53cdbaf40687dfc7261d3a1015473b4ff07ac0`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:042aab238d53837875e53c16a3e8ad5d5d5c64f13e80e00a71a6262f9605782e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899c13bc48fc716a0d53b364d858095d8a5fae3ea53f1452ce1e5c91a133f67d`

```dockerfile
```

-	Layers:
	-	`sha256:cbce9fd25812137d4aeb6f43af2ae3016ac0cdc0b3a8a78ff505c25198869c80`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 3.6 MB (3553615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104654a631070bbc809227ff13dd24c16337baf2e2d63f359da294dad41790f9`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:75f904d0c67f4c9858cff6f0103e91027e807518b04fe5f8092efc0c0981aa3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:50424def1a9f9c45659cd9a3c8fd7be20b771d9faf316706d56191817d0a7bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4caa9f0454a8506b06908af40b3180c7ab34e543901a0d141383284031761739`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e965e0cbfb28916191745c6417d4338beea7aec2cb5fd81e10dec40dd2e8366`  
		Last Modified: Fri, 15 May 2026 21:20:18 GMT  
		Size: 3.6 MB (3624588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b460ff363337b53a251fba6ab38f85ae7dbd0d322131f9f7ef3e3e5ec3993841`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c526a5517cd48bc16f89213299da52f9690296195e5ac59667a2bd643e3c5e41`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccf8b1159386b1fd839b78027a3b340ad638ebceb5a5539d309b242933f1831`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 111.2 KB (111232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e412202f26ceb6d4c1bcffdc5575ef0790972dcdd1ad14eaf46f040cac1316cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f887bb03cdd347eeb92f232c6a07d31436a34375b07e390389807dabe87027`

```dockerfile
```

-	Layers:
	-	`sha256:809d99babe923ab2dd062a2f570a5266b242a04c4fafc307c92fed2e3a9b282b`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 2.2 MB (2198324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdea2d028b9d02999d109dc927e7a4f4f2eb569da53527dbaa7364aabe4f58ae`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:97414ed4f59910609b1a9d705b7a3a667c26066208e644efec505f633b47edc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31324763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a849cdc79b65cf626b3b9fcf4493328abde886f8144f0e07b67910f9031ef4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5439fbff57039d8111c79e00db08bd4ce15263bd5b99af9187a4bc0f4e8b3a3f`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 3.6 MB (3604765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4e64fc2883d214a40a57eaf9b537698bd2716c653c6222dcbfe6fe31ae80c9`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16947bc03ead29ec0c191d87407de3718f236783939aab991b0796802259874`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6602ba41307da6865e1f72143c4370a3e8314e6549962b23a911c4258a962097`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 111.2 KB (111196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1b49ffa2049e4591c8f82f011202a785b743c0a435508fa5289cd41580900181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800a7e9d197c9c0dc0a6f3713a812beb76783de250350cd4f1c949813ce36d7b`

```dockerfile
```

-	Layers:
	-	`sha256:6e35d0abb6e3a97793d611df4083460be5d8ca41a0a4a4caad1681ea6c693031`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 2.2 MB (2198584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3059046f1d26c24c93d9cbbebe2a0e41abff976015c5e06bf32a4c00ed72ba5a`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:c15cc5b2609215d38f487ca74d9a0c364fef640456351786ba6ed7ddbdbd9e23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:741e4d235640395bb69af07b20575215e3726c3a51b342d7a6ab63b03f542913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d070a1b4367810c74bf7fd5297d7c2b0bdf28bfb7bf8fb1d2f140a7477eb6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38cc2da34443ee698d2fb5746eeb70d00d8cf9832f5c179c94dd01d32a6c322`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 3.6 MB (3624605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8de9718e2df29fa2d76f88c5bdf5a5d1c67dd9cb2a42ac280a5a11008d6cad`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609c6677ad71bba680f8167c8974b73f8286635b51e89d7e59b83165f5c783e4`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815bfcf7ec7f087a70287169d800d287b5168932caff8ea06f75959b47451481`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 111.2 KB (111242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49aaddb4c43128aebecde25753a0bb923ccbf5ea00aa45045cbaf373d236054`  
		Last Modified: Fri, 15 May 2026 21:20:21 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:81dcf4b3a3c8ea4dc21201c4b401da4547964aa00e40f97394136dfdee1287ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5876d21edff0cea93eac4c36709504c4935003c3b39eff6d3fcb78e2c01670`

```dockerfile
```

-	Layers:
	-	`sha256:fea8fd6c0a0c0ec27d42693017eb03dcb6517cec0badbda611767531ced60f5a`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 2.2 MB (2198360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30444ea650f022aaa5e6707a1d474afb7a85e00f07e9dec8bf133305f85eb69`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ebb7a5aaf051c49d265817b4c21a8f3e1f4340caa4351791250395b45a1daeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f7558d4f7ce8272783cff8b620052a1e42f297365702f22fed127d8fa014ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfba9082861e846762690f8c9061bf0b330a06abe65636c2f7b0cdfb25816ca`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 3.6 MB (3604762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41eec572cc90753bca88496df6fd51ebb6a228bd52acfd45bb858c247fe34c87`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6e73b3568c2e79fee913e8fb0a2417d91340fb6ff38a5a55fd03819c0aa86c`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254233f274bb3fe0fd62162e9a7bd9946f215e74774b49e235310bbef9e524f`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 111.2 KB (111186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7e707bf8653b57bc80f5de25934e155b312dfce4cc4e3277a8dec5b82a3aa0`  
		Last Modified: Fri, 15 May 2026 21:20:40 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:02916722ca03dcac193f1f622dfc12e91bf090281b8072122d1ce4e2b71f5c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba93e33625286cae36e90a26e761bf14cb9cc9a67492eb5aee053c0159c1beeb`

```dockerfile
```

-	Layers:
	-	`sha256:81747f061bbcb86cfb76d061f8c57a6146ba8174df02ef5a65b960be9d7224d6`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 2.2 MB (2198620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb84873f4648ef88e059c7ec03f22b542751d2dea12d0f148bd6cd60c7d624d`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 16.3 KB (16301 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:018480627781c4f09ea274ec1bc621e0efb67169822f7b105e75a89ab96cabf6
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
$ docker pull neurodebian@sha256:5a9a16c21ab86720341c5aac3fc5e19af871a9930ca090419f6362b69f7e711a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59698019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d7ec001bda49b603142553de0e421284e9a4311d4efa7080638b518e8e8322`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba814ed0b2d9a547c76536523b463e06898aebf2aaa398aa74311d3c1dc1a4e`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 10.3 MB (10294107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2e37411de84cbca2fca1ff8d236df88116d475c59a2c69614af55802a9bbf0`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d341991aaa56f761b5dab25eabf016668a7df99acd80b4a859fea4f6f10f1be8`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471d6791181851b02e8005a6a573347bc3343e727010d156ebff951c01f0831c`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 90.4 KB (90385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ffd1de262fda88d420c478f4e125ce39e37a19e9370de15c8b7bb70f87a37b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bec6da167a19c934ae18b41c68d67abd2c272e0af3c4f82ba0dd5e8a0ec9c2`

```dockerfile
```

-	Layers:
	-	`sha256:1b2cd8a742194e30de120f5799fa47218b060ad8e5813ad5e839bd52cd6a49a5`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 3.6 MB (3614146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba7e66993193c71d173a9a88cb6c1f544da27e64f231bbebc5f2d8865c83015`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1ebb7b15628e7e0ebc948ef63b2191b8379dcce522cebccd39a9a2a685b06513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c791dc53a9166c2866017c86f531369092012575d8755081c0e8524e04cfb0b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1942be77793cf7d7768bf84d6eeb2ba5950a28db24f33091ff5994538cf1a6`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 10.1 MB (10079225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3457a9f11dc4e18f12cc7a4005782198f4b79a88a7eb1d887dacf5a49beac32`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864235a4a0107dda08be1df2d9fb91d16a1bf0cb6425d918f3e7f279b47d9f76`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745f6668de60811fd9ba506dd37cf3433b97f825e2890d3c0ec81b413f3cb511`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 91.0 KB (90998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:169b5ce71453916a845776bdb00f54d254a42a8ac82934fc339558f892a93252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a699a5f993dee3ada544a33120f37cc56d20e87c04aa524725f0f702d7fd45c`

```dockerfile
```

-	Layers:
	-	`sha256:025c64ba23493947f035fcbd203e7fb190c05f790a389eccff9d5f2a626187a7`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 3.6 MB (3615036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f2692cf313664fb8d329acb3431b9dcb225150641afdaaad3d858f6add85ff`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:8de903a96a87d453f0f55e59a481d2ecb136af612e7a8cb1af3ebf7b4c4599b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61391247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc3a9c9e96550ad6abb72f0ed19bcd31f13470b3b8d71a1d44e79bde57cf1ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cc7ed761905fe0f613ac0587c2eee5fc88709addaa08848f0c530ec2dce1e0`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 10.5 MB (10468039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa1ede3b3f88be094ea90befe80e469bf334a24ffc05b7f563662d85c89ca2`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae4073214f3081684e7a0498b92c738fed59cbd0bf33dc5834b8b759736dd6`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff35dae5623186c951a120843fa244868f705164a1489437aa109a8d84704d1`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 90.7 KB (90746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6ecaaff4cf9b54e0b165525fe2690467a6733d849e2a0a48eec9d898da7b371d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244fc09bdd8c8364a7de7fad082cb5c2db5b255f52ff05b1dc5e310aa74ad834`

```dockerfile
```

-	Layers:
	-	`sha256:35f4f12874c2ddbd67f0a31a9593a8d28a9987efb0c2eba8d007bf1b9a0f6e0c`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 3.6 MB (3612094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e3a199c0d4b66452cc112a33ebb31826de992764349f3abee5ec027278b2c8`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:fb78a302d8653e842ab45d60c058aa74ea89549dd319d94f4ca7a4aca05ea741
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
$ docker pull neurodebian@sha256:40c77bc9cd15c45e56f92dd37748f65dccb5c9b25db474e5583299263a9a84da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60197651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91559e8c87c582c15bc416fbe03a5bbc5f4a584a24489ce55920c37298af5235`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:27:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:02991db6507c0026c404c68dc35ba4f9c80895d9d7fc4576cc1507337d1b4eb7`  
		Last Modified: Tue, 19 May 2026 22:36:41 GMT  
		Size: 48.7 MB (48712012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e58d1748e5151dadb72e1f165353c365ea3bfcbfeab0aa145d1b087b5d6f8`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 11.4 MB (11393325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b38bfcc5e625cbecc79aaa8b01e5e2d5059f226d6eb13898b0f437bd891e76`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54e14b8ad488bc00575a9c73515d031181675b31576e3eb72253c6c475a0ed9`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7e3b6d7043fe182d56ec838ca1ec702b85b90778102555a622cd76f574beb`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 89.4 KB (89412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d847daa249197059f5e935dd19b4ea9eedf33149ed7e48cfe007c15f2309cfd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952c080329812ec9363845d75ecc38cb4ac235bee430008cbde7fca8be845388`

```dockerfile
```

-	Layers:
	-	`sha256:66bbb59a3adb62e0ab6fa91117f8718bcc512e41d0ce510cd8df380040bf908c`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 3.6 MB (3553364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f5b45df19088a13691bb334527d8caf74b958c6ff741123494348b8f7f40b50`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:edd8534702838d10c4423132ede211ed67cb3b8aad6e0d66635e99db9a0f1062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59923588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdb84dcbc65ca8290823468d8ddcd2d3907e5ca3a931aaeb8b7de01ed7d468e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:31:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:31:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:31:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:31:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2bc0682b6790aa6b6a3a5a7933e32ea4a35d72d531a3c53509cd76aae83fc88`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48737609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8326e665e37dcddbb4117e65487a3fe42cad6dc654d0685797e71d08a81f41`  
		Last Modified: Tue, 19 May 2026 23:31:17 GMT  
		Size: 11.1 MB (11093058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3eea31e0306f1e7f62ba1545e5336a5b2882bddb05be08647685007419562ab`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8105a082b1fcef71cd46e3265f9493987a9fde8724eb7eef0c0900a25bca33`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1517d5423bb99fa782ff6a0604859e368e373d113f8ed534219ca5a9b438dd57`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 90.0 KB (90020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c7701d7e0a9709d5816ec7ea634a4e09304ea19f8f039720e6abe4353a1076aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d10534cb5a776d3b454d297628278677c6febc6e889117d2a786fa1624ab64`

```dockerfile
```

-	Layers:
	-	`sha256:65821c57772256a43a3e64aa43b60da3762a2de794db20f576d83d048cceea1d`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 3.6 MB (3558069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79dcebfbf845b6b95b62872c6707ec89579e790e83597c63c3dffcf4fd69e0a3`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:80ab709a5003e5bb19b5298fb94704be677eeacae57e1546f3a27c134e408a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61734334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ac3ec238f09fca3619da6c12e8411fbedf0953b46cb91f86aa5f9046836c0a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:26:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:506409f9b5466021b987fde6d84a8bc529520e50798929836cef94e3223d354c`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 50.0 MB (50016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7753854dd3eda9aef2aaa8ce9d1e3f65ad0732a1084526b6ea495204123445`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 11.6 MB (11625732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80680d0e09afe77e520bc718136fe080de719a24960af381889b5325a007ced5`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc9462b033e2edd695c438057a9d245ada5fc84587ca3a58b07feee07ab51`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ad603d2e8d78ab42ac28bace917a076937246df7f6d0c0633126b17f0cadb7`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 89.7 KB (89692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:57343788c201a8c001feffcd753e8cfbb1a6dbad640af928c8b65079937916d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583407654d7c95b5dd7f0c49b8cf2c3dda7a02034c8aecaa2c56a63e3009e10d`

```dockerfile
```

-	Layers:
	-	`sha256:d09a0b84829b224ad027b6f9b437d39c2e73c8cdb44870c4ca0bc993869b1c1e`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 3.6 MB (3551313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcef60f7d04efbb4e57e855b92a9b8620465376f9df755c28290b9aa572be599`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:2624eff6ec3e21c06489236b191eba01b0beab037b9f28fbd3736c7a66bef5fc
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
$ docker pull neurodebian@sha256:b5fe02ba6e80b840d27c9a28023093ea6c23d0c9f89a31872582dae4ae70095b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60197932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8a8113f4d5f843d3701212777122250946f4084ea90c4b210315d8c8552389`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:27:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:02991db6507c0026c404c68dc35ba4f9c80895d9d7fc4576cc1507337d1b4eb7`  
		Last Modified: Tue, 19 May 2026 22:36:41 GMT  
		Size: 48.7 MB (48712012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6e71e03194020c479ea6543a7f33f5099fe2418b16c8172dfe51e95cc37839`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 11.4 MB (11393195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bc269137e2d1ef84e9a7f609fc3cee05da2a89706f759a7fb1d61120dbf448`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f9d3c942e826f99ddc6c49a7e3b652962a818c4f1d9922b0ce1742da0e16d`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a46f5f08e788d4c601b78c2f74ee528b3e922bd597ddc3a26614d7f0b61435e`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 89.4 KB (89401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0712a6b21cf63c1f33a22eb08643b4e391abf913201dbb2729f8ab5e93d38911`  
		Last Modified: Tue, 19 May 2026 23:27:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:07e73ceeba01283e1cfdb5acd37480d6a18e0c497846033f81ddf4428ff6cc53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ea38aae25cdb12c25b7f88c9a1dc8d8fefa9067665af128c4b1e7ecdc13749`

```dockerfile
```

-	Layers:
	-	`sha256:aa9aace3b47fd65d09b268c1a1a0179945bc17f6958197bf895d8106b13fe493`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 3.6 MB (3553400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa2070502a6c70b838ddfe00d5321fddaaf3958e9305ed560c66aab2560d3a97`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fdd6f83569e0862993e48832d03be26ca04c8faf222c5bd056f0869665a221f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59923995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b961227030f6ce3ce85d3b4a28a1bbf746687c9a53ffb5b287e67a7c7838889`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:31:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:31:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:31:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:31:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:31:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c2bc0682b6790aa6b6a3a5a7933e32ea4a35d72d531a3c53509cd76aae83fc88`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48737609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dc44779cb8617743124f685b6bab6ed6aa724234cc4ea684ac0e74eb53ffab`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 11.1 MB (11093028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0b4f7877b91c9ff52ee44f9d75b23d583cc18625559b238ae0ad4ed4ddabb1`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c6c0d651e53ea292ef5612a941931757712de6d1e19de433fbcd7cf87dc2ac`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2e9ab7191a3546247ec4390d48df26cfee47a530af5bca3c34d103849864bc`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 90.0 KB (90034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fae19e42bd61f416eefbbb0e6fbb41a346ae78fa1e9ae01b2d2cff5fc1ec50b`  
		Last Modified: Tue, 19 May 2026 23:31:33 GMT  
		Size: 422.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:edd41d5d71718554898395d73aabbabc52399729a7bccfa89b3a2487b861820f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccf3bae28acb19d66c068d98778afdc4eb4041506e225e424b413673506b68d`

```dockerfile
```

-	Layers:
	-	`sha256:10da892ffed892fcb2aefbf7a1af3177eb97af944f1b959a13f3ac0f0ea0073f`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 3.6 MB (3558105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986de3b52a66825431d3fdd5b0cae2b54b16b8db36ba5742038cf5719470dfc2`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a86f4de25dfa6b6e91e64e0b6f5d40aedaa1ede6fb8e37582ef64613c19b1b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61734790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc88f1a9c7d540c5d0ded18483a54b1c35d38bd566e529c2d509069f6cc8ecb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:27:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:506409f9b5466021b987fde6d84a8bc529520e50798929836cef94e3223d354c`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 50.0 MB (50016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510eda87fd6292dc0e1f9f0e55d72bafc27bf3b6fae3490ebf7da2201fbf34fd`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 11.6 MB (11625786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e78771190378876740c64297e71d7791a44fe070a7d393ec614e250dd891c7b`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a0595dec45a612a498719506c3131b9798d2f5b5909b4127dcb4ff8e4711be`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7047c4ee9b2e983af1985c1c6458f4f8a3b8074315a26585db4bcbef767e38`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 89.7 KB (89678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca8ce972bbd0785587fafbd77eee4417f7e1b6cff9fae89ccec68703c02373e`  
		Last Modified: Tue, 19 May 2026 23:27:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dab455e33202ee0696d74d63c649ac1104d40fe2e90ad3a2e7ecf50d4a94f42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f56c073239f966bc31414fa40751a0c54fb9ed1ed499e8038fb45888fafc6fa`

```dockerfile
```

-	Layers:
	-	`sha256:189d9d6cd49490617375e11667be902783dabc2a73ba55a06af2f6ce1542844e`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 3.6 MB (3551349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:231621bc9581f8c17abcdc788132da2cdd4e950e127faebf5d51ce22cffd68b7`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:eff8b93f637626ebb59c8def717e00670475023d5c1da61cd0ed6f636aa7ca48
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
$ docker pull neurodebian@sha256:9b243bc24265ea356b0c5be55f8a2b411a2ea2290864a7807b60a51ac5c3a613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64975821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22347b7237e8cb430fe55f5b78738e9a3e2398d013e2c3fe0cca9275a438e078`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7236d1089a039f5ffc6e36f0f0c0fa5d2b327158b4baf949b6f4f2efbb115c29`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 11.1 MB (11103419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c366df488968e5fbfefa6fdf8cf3ef33c7cf8c54f81d98f46f231ac0e483c71e`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad28559cefce11e4196ba5ad2f8f0b8c4357774b782c1f2aa86ef2895221736`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a8c66f53355fe68d5301ab9393eee9d2b137ccae00ce12e24369af94e7723a`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 101.4 KB (101393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8776d4efbdeedad14efaac21ef11495cce5a02a1ab472f4a96f18910e7de4875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2b3dde9dd3c4994b35307a367496f1a17e6b0ce9042130e014da2a15bc404b`

```dockerfile
```

-	Layers:
	-	`sha256:27784bee2552828171717d2107483a4211d66523d613a2e66fa9d272833a0a11`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97356413bd0310cd9473f5ad7ddbbdd00b2ce65ccd309a751c863e33581be74b`  
		Last Modified: Tue, 19 May 2026 23:26:40 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:82b0af26743b912b012739ce6e8c20744e6992a30ce5729c13ff5421683205e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63469957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d8df7d8e955f1470b9f5bb291d5a231550cb0422741a69912a7a532d2b61d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:30:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:02 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0cc4562f1c5f7bb18eebecd9ad923d8d4541d490d5454803267f581a0e747c`  
		Last Modified: Tue, 19 May 2026 23:30:12 GMT  
		Size: 11.1 MB (11109955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c766a489b2eb8d722fb99314aab9123c016e02b6356a91d3bbe1037787cfe592`  
		Last Modified: Tue, 19 May 2026 23:30:12 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b887c9d1e4c3b8b180c3e9d16e8f10ba5d0d185f473b3749a2e18cb162451f7`  
		Last Modified: Tue, 19 May 2026 23:30:12 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57b61e40bf16a60d7d5c3a040961119572d6021db6078d4d3d26f2a4a25890e`  
		Last Modified: Tue, 19 May 2026 23:30:12 GMT  
		Size: 101.3 KB (101265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0ec18ac1afedb8703040b4da626bc389fc02969276be301cfee03a1771101f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dae2e6957c59d38736b66da84eb56d10be26eae449f3d9d77dbd2a0b02c85577`

```dockerfile
```

-	Layers:
	-	`sha256:faf74e35773044ccf7896f73ba345067eecc8fb6c573c7d5d0a5e0528a4aa19b`  
		Last Modified: Tue, 19 May 2026 23:30:12 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c332b90e207904b573d2f4aeb7f6e4b7cc662525b6be14551bdf1d563512ab0`  
		Last Modified: Tue, 19 May 2026 23:30:12 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:97ec0a5bc8c4a40c636fd93c1c9fde4a07657b191b94d494d4aba05195fb3fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66315053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf2e159c542858f46e0c17627da7185487e15be8d0598b7d8a797719d782a9a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:25:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:25:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:25:52 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:25:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e09eb609a6245c10b9cb43e597a7ec3d9e4224f925e717a38f2fb36787a4e7c0`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 54.7 MB (54709050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6ef78f35d55a7bdcd4ce51a8250fab7f87447997a985bec19d4f5df93176b7`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 11.5 MB (11502540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381543fb5518886d0decd77840694831287740a98172554d552db0976a629d78`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 1.9 KB (1896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66477593a0b871768cf3a1418cada25d9f4af13c700326cdfd49ab211fcd34ad`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff955a9c4e443cf9f3142612d3ab247200cad20aa22c18cd1409dfd7eca4980`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 101.3 KB (101303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ea456581c23a81a6c38c1653d1c2c94be10f778f8cd85ed42614740430690e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d3e5c7dfc130587ee7865e02dfb567debf1712d918ab299e1430b8ade65e5e`

```dockerfile
```

-	Layers:
	-	`sha256:e307f0838abd851e0cf52756ae65d7aec7e0335039fd55bbcb901812698bafba`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:049f7c47d2e2f1d7d8c5883c6552fb68c7be64c58c35b3dc3549795dd6f1ae98`  
		Last Modified: Tue, 19 May 2026 23:26:03 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:f1f3f65be806cd2e5289859430967fb45d2c86b81d8f9e5647f088472979881a
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
$ docker pull neurodebian@sha256:a31f245a8e23ab333d0cb91a20812909e691960a320848d4ef26b352815a7a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64976262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5f8d51d8fe2e0b29833a6930ee9ed8127229396c7bf674da0550ba14789465`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cb8ccddb7ae905a7c15a308bcc5010fd4a842839e6c4e55aea5037fc2c6f88`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 11.1 MB (11103489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73aec67b21a1a6c0b4dc177a5965f48251ca61285c2843d50601d15bff859db`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f906aead18b295a02b3010f8b914a9b91159b0bda97419216db9f38e2ad3d90b`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60969937977bcc4c5b60c1148c0bc24e73935eb4543bc321604bd0cb403bd1a`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 101.4 KB (101372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dbca80d9daeba4dc863e30e3d1b11e83b590a71f2404c0f81f620de94f8861`  
		Last Modified: Tue, 19 May 2026 23:26:45 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4c7c72ba8aa60242c01595e6c329c6841fdb75347d3a378338e8f79168111c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83b351f919e5d6f50af1abf13db25055742b5206b749deb69a8512c9483a9321`

```dockerfile
```

-	Layers:
	-	`sha256:2f85224be519cfcaeecbec362461b06c554dec6c914ac74dc25ea1b39c2399b1`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0003492d33be36dc5b18d246a9b0ceecfcdc28900cc4527fde33b969d8b65b6`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 16.0 KB (15993 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:44ae51ff793f39946038ce5d95af869b3b70558a685f74437925423722dfc75a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63470348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818e4b617c895bb6f2e851ddf2b7aa3e84a209b97a6f73727ac44d87e804840`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:30:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ec49c2c0e7ae149d1217b1064a04894098733733e47129d491b619501080bc`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 11.1 MB (11109941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3221195c4a3803c742597ae3c20c7938603d4225ba8bc12e2a132e14ec3c1534`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3976723b40480b65484fdac4ff3b9cb3f2c4adfaad97bd5fcc0ce764f71730d`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30ea5cadfabf914d41176cf9b67c2e8c84268162895103d5f5a190a1c91f259`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 101.3 KB (101283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f656a055002be466165c33f521121cc4442274cdf721654db837483142b402e`  
		Last Modified: Tue, 19 May 2026 23:30:31 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a1a1bb1d584fd6181b16c73cdf9c96191c3e2364aa67a79031ed79b692977be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e012ba92c198995a31023ae78735740956364723a16b42738cf90b5bf0d33866`

```dockerfile
```

-	Layers:
	-	`sha256:14bbb92d22c5cfb94345cfb92bdf1472efdbc687a191ad6da80b3deb70706234`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:372972fb25a4fc5ab5ca9c1eb667e639300981bf1c0f0ebfe6758a13599a0111`  
		Last Modified: Tue, 19 May 2026 23:30:30 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:dce71c3d3978a2a855abcf1bc5a83a54b0f1eb84afe9c708d37b9945612e3800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66315350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0801860e74bdd4e1248165adcc97832ff1397a208cb4e9e22f057ff56cc487c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:25:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:25:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:25:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:25:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:25:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e09eb609a6245c10b9cb43e597a7ec3d9e4224f925e717a38f2fb36787a4e7c0`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 54.7 MB (54709050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95b0b4b40e146641da97fbb635272948b4c269cec26aa79cbfb54c37dbe1649`  
		Last Modified: Tue, 19 May 2026 23:26:05 GMT  
		Size: 11.5 MB (11502477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45354a9aa4ef78b02696ceb5c8a0ef10d0988ccf5c880ada568b69ece7d4c16`  
		Last Modified: Tue, 19 May 2026 23:26:04 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987dc208402f1ea8675711285765d6168b97248acb8af9055c80f2d60ce40408`  
		Last Modified: Tue, 19 May 2026 23:26:04 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d6f4d36ca15503abe1f07e2b4c2b1de0779f2c0637b548f8b311632e249513c`  
		Last Modified: Tue, 19 May 2026 23:26:05 GMT  
		Size: 101.3 KB (101276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb5a5de4f9760cf73bff4a94a316eb883b68e28b6e15d06881dcef89e8ea279`  
		Last Modified: Tue, 19 May 2026 23:26:05 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c9a4a7d9ac0a43c6ef88e5f3f498ce786c0ecaea09f7225e425e6ffb3efe7e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b511300d3fa88ec3da28b7d91942be85641b4ee4e5e05658b51c195e548a2da2`

```dockerfile
```

-	Layers:
	-	`sha256:d1b2779cbb92980bf8bab7aece37d6ba04e04f00759c3ad6b8a4de4bec717427`  
		Last Modified: Tue, 19 May 2026 23:26:05 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:715cda405a610752bcc00c2ba1c11215cf139bdc737d545c950bef4d1c5f0117`  
		Last Modified: Tue, 19 May 2026 23:26:04 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:a2f6c6c17cbff7230acda8ba612accec5e349bc96bee30683331819139123c5e
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
$ docker pull neurodebian@sha256:5f1edf985e61cbf97efde486919a11cdd1321784ec5b689c0f663a239d432930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59864512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1cc70e97c70e7365943b885250206fc0d0c006c184e0b4575b525b62313409`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:39 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0b13f85cef1bc2ce7a76cce6ee029b8243a25927e76e49c158f666b198ab34`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 11.3 MB (11273489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce92465114cfa19af1e7d1465a6f07aad31ab6a7f79430a86503f930f75bcd8e`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb5eea44fd635d732ce776ec41e954350fd60febd30f2535ff90a95f02e694f`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65045d6e9755b4521bff489a4cfe874d64afb12913afd6f9409b4db8e75815bb`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 93.4 KB (93418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c9485f81f0ed7a82857ed2e106a72658d92a0a5832d2579c9f4a82793447f3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e762b972906fe4849f770c267338ecc5808183adfbef8b29e5e2a57621bf3a82`

```dockerfile
```

-	Layers:
	-	`sha256:4c8c3519546430d89e9b45731f379793f0aaece5a5b1f8d2226cce0a72c3d9c1`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 4.1 MB (4075897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf2d39b2b10172be44e16176c499bbedcfe866819416458e1e92f0cdf558f0db`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e09ea831c61b1599fee2f299d7b74d41da8949d4716e00c7070574df27d2ec77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59727931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4d565a6c8435852e6e559d6b02681dec3672d38d0a85f01c31ae36fc3d1df8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:30:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afb329fa1729a6052cb601fa1fd906fb64972f64a4d5d5ef8bbbec2a906fe06`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 11.3 MB (11252799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec52cdc62034f3ec44c096f32d8778424dfc37eba422546e223cd08f6eed2d8`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09da1e782941a6a1a9e1201cc009fac57339572ac8dd69850a04fc1a351f594`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f636239c1baebf36cadcf17254c8afd9c5f67cc9c85dbbd502825029a7cafce8`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 93.5 KB (93528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:190c613f459064bb90444e69cf51a087c870c70a443ed2bf9ef5dec9c4725c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd59ed66a025e7638acec0af37cc2fef4495c82bd69e9d16fa6bb0b869682bdb`

```dockerfile
```

-	Layers:
	-	`sha256:d3b2aa904e74e6dcc427cceb1d8b8356233433b22667cb251cee74b1eb2bf7d4`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 4.1 MB (4076139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48223a98ca62724d50b0bd324d3ed7f9901ed2539707511cf2294f84e096fe82`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:06efd2617c2deff0de78668a4b93e2de94a16cd6c1e9cb08d532101a29937c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61271862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48850400bca13d7fdf7526618a52ed599cf2e3bd747447233f88108c81435917`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566da1b3f80bb347d6012fd5fb6da173dfe240808cde5ab901fcade81dcaa9c7`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 11.7 MB (11693150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb3ca3fa9e5e3255de5568039d480a7f42aae72daa70e9876f9d7928795d9ee`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4126cfc6ef24413ff78a87e200613bcccde45c97c74be127627edd576f7af08f`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5d7d17adcbb67f3ad0df7a77b50d4294d8881831996e1cb11f0ef6165ea3f4`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 93.4 KB (93420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c39f6c8b1cdf8815739b276741eaa50ed5c76dfbde1f1835cdc41dea44ad9874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9eaecb3bea7efa86360330985d1ec29e0985e05710bf2a09b60d3ace766fd51`

```dockerfile
```

-	Layers:
	-	`sha256:6587da0d5f807f38b05ab0f76a42070423152338f48345c24225c80a2a938790`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 4.1 MB (4073864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b0fcfbd3941a2122b6c9144f53972601b6d65978393a60dfe8aa09b6228a1a`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:791e12aca1a39722b6d5ae4fba3f0a01bca8d358c1bbc2d4f26ca249dc87b16f
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
$ docker pull neurodebian@sha256:a68c734c00b3698e7b11888eadb04a8991624b39bcf23290d300838be1056578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59864739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b109e02369ad91c522bb9e160852fce154742b03780232bf4cc904c120daf43`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b209413f350467a5ae5c418b73ac48d809463e6e3a290d3c1208cba9f34ab3c4`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 11.3 MB (11273289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958835a82131d9b249019b0445717bd4394054b82052fa141556a6d461bc9f80`  
		Last Modified: Tue, 19 May 2026 23:26:49 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac5731f71ed9fc336e58efcce2de819cd14828671adaff420902f9ea091455`  
		Last Modified: Tue, 19 May 2026 23:26:49 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482b13f29d6faade6a1f514b290c009e4e3359f58d34d63eb1216860ad993e07`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 93.4 KB (93396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129025ba31fda6ce65a428088c21ea0cea14bd38c373c8fd604bfd5a37d1e73a`  
		Last Modified: Tue, 19 May 2026 23:26:50 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4e94433e88f2b411bb7b941a087ce937c99b12e028a35ad7e2ff891096fb5a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93eeca15a1daefa3344c6cee6c1ebd5491b3d9d6cd9da0063c9d72949d646ec`

```dockerfile
```

-	Layers:
	-	`sha256:aac31dcc3ceeda2a52871716697b75acce365af34fa105b8e1b5f4300226f219`  
		Last Modified: Tue, 19 May 2026 23:26:49 GMT  
		Size: 4.1 MB (4075933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ba866a07c775385e7b15a1ddc70d503cab165741c7bdc97dbfe353dc296a8b`  
		Last Modified: Tue, 19 May 2026 23:26:49 GMT  
		Size: 16.0 KB (15991 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:960268a0372f026e30de47583581420aab60507a81b59f30c9ec236c22d8beb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59728479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41ac9c5e150732a2c484624f2b4fa08dd0eea99f7668781be6b9c9dc59d69b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:30:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:28 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ea4a2729c69acfa17c3025a40f85513b1f8639dc8170799e6eec54c9c1bcc3`  
		Last Modified: Tue, 19 May 2026 23:30:36 GMT  
		Size: 11.3 MB (11252891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8e1bb079ba66989f9a8f05c2354e7fd267fc98337b75e080b077d7f9d41a6e`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b8923883494084dd5136c060256ccf663838d09a4d3d46c8111d1cc801baa4`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad721159bb9271b363502e3e9d13a790c54d04a383ed7b61f4c0934f6812e79`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 93.5 KB (93534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb84a30c185b452bf5a889119a5572594d3c7d011797304bfc7ad44dbb80e29`  
		Last Modified: Tue, 19 May 2026 23:30:36 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cef5a64a1236af4f765b8b55512bf00b5960ae98634a89f831af7a3d3cd27f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49220dd3c313a7622e2379927a6d1d0d7d8298ffd7a53206ce6fbb0c4cb994ea`

```dockerfile
```

-	Layers:
	-	`sha256:183066e63f4513b84fc0147089b908d7f81c70d581695c94ac38738674cba9fe`  
		Last Modified: Tue, 19 May 2026 23:30:36 GMT  
		Size: 4.1 MB (4076175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebffd27b4acf3ef30f36b1a2650a111e7419e0033ca66b64ec53a948a253bc21`  
		Last Modified: Tue, 19 May 2026 23:30:35 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:84f110cbc4ed1d46ffeed162a00e9bb00b38814c6ee85c28c21ec82aaa1d40af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61272369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e517f47cfe4822fb2559e4c5816d14cd178edf81821527e0826c845da942de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce19c0c826a9877ab35c71e19668e7fe552ebc4cbf2dfda44942b387c25f88d`  
		Last Modified: Tue, 19 May 2026 23:26:29 GMT  
		Size: 11.7 MB (11693199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622a94d295eafa3598fc7d9046e7abf0c9c4d1d58b75c75db2a9f8f833ce7516`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779d6106bbf28141a507337cd68918f9d28aa64456b30457ccfc33b407f238ab`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f312fbdefaf85dc165c74188b8c6c551e6c3727ba585a5e4bcb19dc72769878a`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 93.4 KB (93426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86a918356a5e7208590f4ebbe73847002c2a322bf305dbd1e31cbeecf50957`  
		Last Modified: Tue, 19 May 2026 23:26:29 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:69518252dc6ce99e801b80526398eeb44fb77b2c07dc53ad098081f7e56e8491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e83b685d9744d857eab93f333917d66051cc16e7151853030a79f3e9da8273`

```dockerfile
```

-	Layers:
	-	`sha256:a0e03d802fcd6e495e1344cb76893109fffb3fa25bc30b5473032e853cc24ef7`  
		Last Modified: Tue, 19 May 2026 23:26:29 GMT  
		Size: 4.1 MB (4073900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0747c02c4b6d7840f1f3c14525dbfdaa1dca392187513d58dfc3381ccb73941`  
		Last Modified: Tue, 19 May 2026 23:26:28 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:018480627781c4f09ea274ec1bc621e0efb67169822f7b105e75a89ab96cabf6
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
$ docker pull neurodebian@sha256:5a9a16c21ab86720341c5aac3fc5e19af871a9930ca090419f6362b69f7e711a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59698019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d7ec001bda49b603142553de0e421284e9a4311d4efa7080638b518e8e8322`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba814ed0b2d9a547c76536523b463e06898aebf2aaa398aa74311d3c1dc1a4e`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 10.3 MB (10294107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2e37411de84cbca2fca1ff8d236df88116d475c59a2c69614af55802a9bbf0`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d341991aaa56f761b5dab25eabf016668a7df99acd80b4a859fea4f6f10f1be8`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471d6791181851b02e8005a6a573347bc3343e727010d156ebff951c01f0831c`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 90.4 KB (90385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ffd1de262fda88d420c478f4e125ce39e37a19e9370de15c8b7bb70f87a37b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bec6da167a19c934ae18b41c68d67abd2c272e0af3c4f82ba0dd5e8a0ec9c2`

```dockerfile
```

-	Layers:
	-	`sha256:1b2cd8a742194e30de120f5799fa47218b060ad8e5813ad5e839bd52cd6a49a5`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 3.6 MB (3614146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba7e66993193c71d173a9a88cb6c1f544da27e64f231bbebc5f2d8865c83015`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1ebb7b15628e7e0ebc948ef63b2191b8379dcce522cebccd39a9a2a685b06513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c791dc53a9166c2866017c86f531369092012575d8755081c0e8524e04cfb0b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1942be77793cf7d7768bf84d6eeb2ba5950a28db24f33091ff5994538cf1a6`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 10.1 MB (10079225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3457a9f11dc4e18f12cc7a4005782198f4b79a88a7eb1d887dacf5a49beac32`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864235a4a0107dda08be1df2d9fb91d16a1bf0cb6425d918f3e7f279b47d9f76`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745f6668de60811fd9ba506dd37cf3433b97f825e2890d3c0ec81b413f3cb511`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 91.0 KB (90998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:169b5ce71453916a845776bdb00f54d254a42a8ac82934fc339558f892a93252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a699a5f993dee3ada544a33120f37cc56d20e87c04aa524725f0f702d7fd45c`

```dockerfile
```

-	Layers:
	-	`sha256:025c64ba23493947f035fcbd203e7fb190c05f790a389eccff9d5f2a626187a7`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 3.6 MB (3615036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f2692cf313664fb8d329acb3431b9dcb225150641afdaaad3d858f6add85ff`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:8de903a96a87d453f0f55e59a481d2ecb136af612e7a8cb1af3ebf7b4c4599b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61391247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc3a9c9e96550ad6abb72f0ed19bcd31f13470b3b8d71a1d44e79bde57cf1ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cc7ed761905fe0f613ac0587c2eee5fc88709addaa08848f0c530ec2dce1e0`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 10.5 MB (10468039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa1ede3b3f88be094ea90befe80e469bf334a24ffc05b7f563662d85c89ca2`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae4073214f3081684e7a0498b92c738fed59cbd0bf33dc5834b8b759736dd6`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff35dae5623186c951a120843fa244868f705164a1489437aa109a8d84704d1`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 90.7 KB (90746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6ecaaff4cf9b54e0b165525fe2690467a6733d849e2a0a48eec9d898da7b371d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244fc09bdd8c8364a7de7fad082cb5c2db5b255f52ff05b1dc5e310aa74ad834`

```dockerfile
```

-	Layers:
	-	`sha256:35f4f12874c2ddbd67f0a31a9593a8d28a9987efb0c2eba8d007bf1b9a0f6e0c`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 3.6 MB (3612094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e3a199c0d4b66452cc112a33ebb31826de992764349f3abee5ec027278b2c8`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:ef3a5c51820c067fa339f4cd86f52de0dade5cbcbfe4570f30c83f1550693147
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
$ docker pull neurodebian@sha256:6a72868c208d4a8be5b7b5f612b35ce62e40f3798cf5fe764ffaaf54bde4f98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59698490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de65a63aaa0d111ac14cc8853ffae5cd4ef9156bc96d4bd3a51d226c42ee89df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb92dddd3e26de8152ea75a9f69a7be5761222e5964f3314a90b2a741df7a67`  
		Last Modified: Tue, 19 May 2026 23:27:10 GMT  
		Size: 10.3 MB (10294134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1c2439c5a41a3f1565849f2bc31ca69db3d67c673bd935365e56e8f32757d8`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd176b7467191c7e24a95efa3ffd50313d148c7ca9ea895d817611de25e2d87`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcf153616e06880716cf7afc320d8ca5b96a6e7592fdf296f7774cee2c61cff`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 90.4 KB (90385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430d60c0f134e218d63b5622fcf67693a4572355671c787fcecc75f6ea05146e`  
		Last Modified: Tue, 19 May 2026 23:27:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6575786d5511d37cb45ea2f2bc9a60a73b23ec4b7a846615187b7d53f4c17b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8c0c8a42b651063403d5abc29b6068a1f0be3c92be2e70cdf69f76f1979e5`

```dockerfile
```

-	Layers:
	-	`sha256:4ad2872e53fafb1cfeb07186d1a983a4d06fb66f95e066efc30f0189d2727f89`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 3.6 MB (3614186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d064af7b145e3a9c6c262ddf2b47d81c9159bb7c8a41e30403adaea836fd0e93`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7aeac7881d0535bae0e2e617f8315a5761b850d71cf58932bd311d4b4d1f16ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48ae2a6c99c13fd0de35eef7b88f31273280054664f82606663688cfb962d60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:48 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aad82dd52a16af0b9a752ae3c6f52083d005b3f021022ac928e217f659b8923`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 10.1 MB (10079251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3457a9f11dc4e18f12cc7a4005782198f4b79a88a7eb1d887dacf5a49beac32`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864235a4a0107dda08be1df2d9fb91d16a1bf0cb6425d918f3e7f279b47d9f76`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129c1fb1c64d94192c382e701d7b14a904efc5fcf1eb658b53cee6dfe4ae533b`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 91.0 KB (91018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7475df3d2a504fa9557ad54214cead31cf01b3c7ca054fe251c62de736745`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4427b4272236147c7e4b07556d22350ca0313cef9b870e82d94aff1f01e3f590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00250ec6efad1de33c7bad769cf3969b6d6530f417f6a779f0ca83ead0468a43`

```dockerfile
```

-	Layers:
	-	`sha256:724a053293413cabf623432bad27c4826b21bfb9630cc4f131df52bf88957783`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 3.6 MB (3615076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b106f5a48dcae253fb77c7274705db08fa073e24eaf2727eb59817d5105d5bed`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2a596ddb9229467c8474294e2e7fa84b37aca64758f2e82a66a7216074aef32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61391860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a3b151ea42db43a346e8d6b49db21ace20626081ed4e9127c0bdaaf47a98cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e6c7527b1ba130a7fd028db4b4f53fe2952922685a72d987e0bb45aba2d459`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 10.5 MB (10468195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac79af1a4117eeb379989c2a6fa268003cbcc7d525c61702842e54d57e9dc65`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37824e2171f8bcb2f390052ce2fa9cb0f979c1030b16c7aab208f7ab72ec972`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750bf144b8fe3a2951d8c7acd97d5afb0704bd216e92fa3a311ab128669845f`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 90.8 KB (90757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822259b6e0e53e9f7d48de30ad4a457448625709e9bdcb8900c1f585458a3b94`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:571389a940bfcc86c5c176393870c94339e1c9c4addba68adca4fc69aeceb89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fe2f14ca78dbec2a02cb0190f6d6fa7ec0db597f47cd9517ec5e4f34f24303`

```dockerfile
```

-	Layers:
	-	`sha256:03d12e0fb081073377307046634158fe58b2600b735ce815ae52909707755842`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 3.6 MB (3612134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18610647bc1842a68384e807f0184ee9984e617990bc40de96da84e376d8d4e`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:124f3cd766fdb6aaa33675b961fe5dc94a3f9e6a957900ed827264af42cdfdfa
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
$ docker pull neurodebian@sha256:f57061aced5b88df44aa3221139686d245a805cd359f62e3a71f8f7c9c3a9109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60181755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7121d0b3446b9c3052cf5091a7bb78220dedb781a0c3d91d34dabde8f374a7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:27:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30b85315dec2d58f35c416abc0e468c9a5fb485e83af8c76ba1b33292e721633`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48697206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c83530a6b51b03de05e55eaeecb58ea7b7ce335817e7289c21cefc0f862cb3`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 11.4 MB (11392191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d02498190a7406351e8a8b106b0cddb3d47e50d1b7880474dcd87e5dadde74`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f543c19bffe03075382a45dfc91388da45cf11bf12ec5be4f33fb84234947212`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5270106ce715802dd9a6ba52b784375677aa57ea1f908f6657055fc3fa3adc36`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 89.5 KB (89451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:49dce879208c36525248f3b7d81cf77a7e45a99563981099c221033c55baf4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84c58a46f234563da19731d3792446c0a348b39255c47d65573ce856c991ce0`

```dockerfile
```

-	Layers:
	-	`sha256:963280b72f123e9ec9bc34ecc09368955c2c72f6338539252f0cced6feee7527`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 3.6 MB (3555633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d28a7d1dee2b324f02d370f9a9386e5558d48e4da78765b27a72b5a8c9d90b`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d2db333e4115682fce4df1e16d76b6fedc97c62b529c682a706bec75f471d3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59906141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e66451b03a9ef7caea93c64d629129a1f9d1211f13d464924e36243cb619050`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:30:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d4360d64f4e71c17817e39372cada00ee239c7d2715cf79f6e6cdc602a7cd46a`  
		Last Modified: Tue, 19 May 2026 22:36:44 GMT  
		Size: 48.7 MB (48720031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4576c4f7d45466740a199d54662cab12c85d21bc75740a97055a71b74822fb25`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 11.1 MB (11093120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9a7a448cc8b0211eb9bef63518a33e6ab21d9096e89b4d32e81161f1b4437b`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e100d1e87b39987108ee142e1e682902047cbc3339a12200c2f6773805ef3056`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41863c941f5466e882167b32083d10a3cff9cb82e7186de9f4097e6bfb1c557`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 90.1 KB (90082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9c3438fe9c4af5de6d4d80b3d33125a7f7cdcf118c2ee3063e8d7a42175ac858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13987104def2f6995f2fe59b900687cbb3d9f7109576c03d65703666cd98da14`

```dockerfile
```

-	Layers:
	-	`sha256:7db5d6425f8abbb85f4075eeffe58aabf77d9534b67e80f7e686f18ac7c6cb83`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 3.6 MB (3560338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a85afa279224730598bd1b8225f47db376acdec114e15fd4c73c07fe25d2a289`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 14.1 KB (14056 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; 386

```console
$ docker pull neurodebian@sha256:5ce574a56b23425bece211570b1ece4c6df414cf625f351a54bf965123f53ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61720477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f2526638ec2933cdadb2da0854e7be0f6f6e3096b2baee6120a885fbe5e431`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:26:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7af1962edabe3d58af5fbd06f3e345528b78b672a4b879b72fcf2e0d92549637`  
		Last Modified: Tue, 19 May 2026 22:36:57 GMT  
		Size: 50.0 MB (50001944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f9c5f81aa30e1e455f4be28ee2b9c7a2f372aa9baad7d1164b050349789042`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 11.6 MB (11625868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289977e8f65a11c099d93af9b5d6100a3be07a1e5230cc672288ad3973b4c79b`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a679fcb6a1b512652aa74206d34f8d5c94d65eb95dba15a6c60df8706b0d7f`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e1363a87009473e2d0e443822d5a07d125247e5297e598a5efe55903304804`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 89.8 KB (89757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4d20751ac6c9509f53f494f8b604eb1c5fb69dcbf005ec453121e82bfac9c4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7eab1ea7fe4a42bf5b8b03524b27b59a22ddcd66cc3c4b3a25af3bcc0ae330`

```dockerfile
```

-	Layers:
	-	`sha256:4058109d32d62eda5118e9f4efd197a8a5e5e43ddd1b17c9b25645a963b9a63f`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 3.6 MB (3553579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ecb7a56e8c9159c1228306bcbd5b31938c520d3edae46de65313aabdab11187`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:fc692782f71ccb077da8611789c9d51663053488c1e1182d5126e93dfda29f1d
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
$ docker pull neurodebian@sha256:dd5bc7f6893df426625b44e21543155e38944c72365cdde75b136cb1114f3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60182055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac711ac0cf19ff39eec3d6b93c2c44ac71263b998019c8ce6d6c3151688edd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:27:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:07 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:30b85315dec2d58f35c416abc0e468c9a5fb485e83af8c76ba1b33292e721633`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48697206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8034887a0bbbfb1d67831fbc844720a3b006206b9e49f7870fb5005bb3c89001`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 11.4 MB (11392061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91ec5878091a1da281fc06f89966a5ce781d30d1cdadb3534b96138fbbca5c`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f543c19bffe03075382a45dfc91388da45cf11bf12ec5be4f33fb84234947212`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399ae341c4077520a588253618e8c4225e95ff6ae9bc4b9e1633da51a6a75100`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 89.4 KB (89436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5bb7d619a42df196180ed8bef0b5f80176bf6f00f546b800c1c31b10d9f9e9`  
		Last Modified: Tue, 19 May 2026 23:27:17 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:044e4a207e873752dda35d4d8cfd81e45c7bbdb7989a0ee0d4311fa09acc29ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e367fda5e18a445afa9fc71877870628f335e4d71a337fc4bdc50de917ca7800`

```dockerfile
```

-	Layers:
	-	`sha256:15a08b05785f1847bd3d3df55e8443c0d80c779856b0862e24ec6c38169d075a`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 3.6 MB (3555669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7dd5aacc2dcb6133d43b785423cf00d00309871d85a776360ceba20e840ce0`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b5343f56c1fb31218429053ffbecc0cdb55062fcd20ecfe9d728041c5c01d50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59906536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c799133513afa7f756207bde3447643a51b965c35cd88008e1a6556f3ffc8999`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:30:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d4360d64f4e71c17817e39372cada00ee239c7d2715cf79f6e6cdc602a7cd46a`  
		Last Modified: Tue, 19 May 2026 22:36:44 GMT  
		Size: 48.7 MB (48720031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec98f49d5e4fa11cebafb79bb6f58fbef7023c8a19fcce5aa94df4a4e7496f9`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 11.1 MB (11093072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9a7a448cc8b0211eb9bef63518a33e6ab21d9096e89b4d32e81161f1b4437b`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e100d1e87b39987108ee142e1e682902047cbc3339a12200c2f6773805ef3056`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c32e23cd1e65b98407dd7e7eb4196697bdb064b3446d752955286f082a89bd2`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 90.1 KB (90077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9bc2b2cf57a5d3f81b2da41573718da95babb252453b4969fc2bfb79f25f89`  
		Last Modified: Tue, 19 May 2026 23:31:02 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8ef9c7076cdb1f64991964c59458038a88cd5185a2cedd92eb15cfe92ddd0946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222b74591ff62cec5f61294bba8e63539d6d288cbfd0767d3ac7f827ed20a158`

```dockerfile
```

-	Layers:
	-	`sha256:5abbd613c8df3b55c925c540eecc65c824e5574b6fb95d4311b7e67d29ef7735`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 3.6 MB (3560374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0379800346bedbe8114baa2a2a59c79880f928a6875b195fcce6d11a9d4d17`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:3b0d1d02630a55a6c377fac8567c347cb626f7b41b37009486d26cc4219a707c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61720915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a46cd04684649a857887b5148ed9863726fbeae7e8cdc8a0c3af9b9e4fb03f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:26:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7af1962edabe3d58af5fbd06f3e345528b78b672a4b879b72fcf2e0d92549637`  
		Last Modified: Tue, 19 May 2026 22:36:57 GMT  
		Size: 50.0 MB (50001944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b022792ab90d17b19c012791d704160e1cb4d9c1094ed5126b1ac93056114f`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 11.6 MB (11625868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80680d0e09afe77e520bc718136fe080de719a24960af381889b5325a007ced5`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a2f99f1f32136fec89aea3b0aaf2aca4477d31c89bde845d0e723a40a5695`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56352ba5cb0918dea97f161038dfd699afb0529bea66b2ba9e35950d31b10132`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 89.7 KB (89747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1ddd8e31b744cbe0b5383cca53cdbaf40687dfc7261d3a1015473b4ff07ac0`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:042aab238d53837875e53c16a3e8ad5d5d5c64f13e80e00a71a6262f9605782e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899c13bc48fc716a0d53b364d858095d8a5fae3ea53f1452ce1e5c91a133f67d`

```dockerfile
```

-	Layers:
	-	`sha256:cbce9fd25812137d4aeb6f43af2ae3016ac0cdc0b3a8a78ff505c25198869c80`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 3.6 MB (3553615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104654a631070bbc809227ff13dd24c16337baf2e2d63f359da294dad41790f9`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:75f904d0c67f4c9858cff6f0103e91027e807518b04fe5f8092efc0c0981aa3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:50424def1a9f9c45659cd9a3c8fd7be20b771d9faf316706d56191817d0a7bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4caa9f0454a8506b06908af40b3180c7ab34e543901a0d141383284031761739`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e965e0cbfb28916191745c6417d4338beea7aec2cb5fd81e10dec40dd2e8366`  
		Last Modified: Fri, 15 May 2026 21:20:18 GMT  
		Size: 3.6 MB (3624588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b460ff363337b53a251fba6ab38f85ae7dbd0d322131f9f7ef3e3e5ec3993841`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c526a5517cd48bc16f89213299da52f9690296195e5ac59667a2bd643e3c5e41`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccf8b1159386b1fd839b78027a3b340ad638ebceb5a5539d309b242933f1831`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 111.2 KB (111232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e412202f26ceb6d4c1bcffdc5575ef0790972dcdd1ad14eaf46f040cac1316cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f887bb03cdd347eeb92f232c6a07d31436a34375b07e390389807dabe87027`

```dockerfile
```

-	Layers:
	-	`sha256:809d99babe923ab2dd062a2f570a5266b242a04c4fafc307c92fed2e3a9b282b`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 2.2 MB (2198324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdea2d028b9d02999d109dc927e7a4f4f2eb569da53527dbaa7364aabe4f58ae`  
		Last Modified: Fri, 15 May 2026 21:20:17 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:97414ed4f59910609b1a9d705b7a3a667c26066208e644efec505f633b47edc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31324763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a849cdc79b65cf626b3b9fcf4493328abde886f8144f0e07b67910f9031ef4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5439fbff57039d8111c79e00db08bd4ce15263bd5b99af9187a4bc0f4e8b3a3f`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 3.6 MB (3604765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4e64fc2883d214a40a57eaf9b537698bd2716c653c6222dcbfe6fe31ae80c9`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16947bc03ead29ec0c191d87407de3718f236783939aab991b0796802259874`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6602ba41307da6865e1f72143c4370a3e8314e6549962b23a911c4258a962097`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 111.2 KB (111196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1b49ffa2049e4591c8f82f011202a785b743c0a435508fa5289cd41580900181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800a7e9d197c9c0dc0a6f3713a812beb76783de250350cd4f1c949813ce36d7b`

```dockerfile
```

-	Layers:
	-	`sha256:6e35d0abb6e3a97793d611df4083460be5d8ca41a0a4a4caad1681ea6c693031`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 2.2 MB (2198584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3059046f1d26c24c93d9cbbebe2a0e41abff976015c5e06bf32a4c00ed72ba5a`  
		Last Modified: Fri, 15 May 2026 21:20:35 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:c15cc5b2609215d38f487ca74d9a0c364fef640456351786ba6ed7ddbdbd9e23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:741e4d235640395bb69af07b20575215e3726c3a51b342d7a6ab63b03f542913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d070a1b4367810c74bf7fd5297d7c2b0bdf28bfb7bf8fb1d2f140a7477eb6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38cc2da34443ee698d2fb5746eeb70d00d8cf9832f5c179c94dd01d32a6c322`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 3.6 MB (3624605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8de9718e2df29fa2d76f88c5bdf5a5d1c67dd9cb2a42ac280a5a11008d6cad`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609c6677ad71bba680f8167c8974b73f8286635b51e89d7e59b83165f5c783e4`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815bfcf7ec7f087a70287169d800d287b5168932caff8ea06f75959b47451481`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 111.2 KB (111242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49aaddb4c43128aebecde25753a0bb923ccbf5ea00aa45045cbaf373d236054`  
		Last Modified: Fri, 15 May 2026 21:20:21 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:81dcf4b3a3c8ea4dc21201c4b401da4547964aa00e40f97394136dfdee1287ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5876d21edff0cea93eac4c36709504c4935003c3b39eff6d3fcb78e2c01670`

```dockerfile
```

-	Layers:
	-	`sha256:fea8fd6c0a0c0ec27d42693017eb03dcb6517cec0badbda611767531ced60f5a`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 2.2 MB (2198360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30444ea650f022aaa5e6707a1d474afb7a85e00f07e9dec8bf133305f85eb69`  
		Last Modified: Fri, 15 May 2026 21:20:20 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ebb7a5aaf051c49d265817b4c21a8f3e1f4340caa4351791250395b45a1daeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f7558d4f7ce8272783cff8b620052a1e42f297365702f22fed127d8fa014ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 15 May 2026 21:20:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 15 May 2026 21:20:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfba9082861e846762690f8c9061bf0b330a06abe65636c2f7b0cdfb25816ca`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 3.6 MB (3604762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41eec572cc90753bca88496df6fd51ebb6a228bd52acfd45bb858c247fe34c87`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6e73b3568c2e79fee913e8fb0a2417d91340fb6ff38a5a55fd03819c0aa86c`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254233f274bb3fe0fd62162e9a7bd9946f215e74774b49e235310bbef9e524f`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 111.2 KB (111186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7e707bf8653b57bc80f5de25934e155b312dfce4cc4e3277a8dec5b82a3aa0`  
		Last Modified: Fri, 15 May 2026 21:20:40 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:02916722ca03dcac193f1f622dfc12e91bf090281b8072122d1ce4e2b71f5c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba93e33625286cae36e90a26e761bf14cb9cc9a67492eb5aee053c0159c1beeb`

```dockerfile
```

-	Layers:
	-	`sha256:81747f061bbcb86cfb76d061f8c57a6146ba8174df02ef5a65b960be9d7224d6`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 2.2 MB (2198620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb84873f4648ef88e059c7ec03f22b542751d2dea12d0f148bd6cd60c7d624d`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 16.3 KB (16301 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:e1f82331fed085ae65759722772d310e652df3d2580df3961a0fb4ed72b242c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:44b94bce3070df694aa69360e5f4d25dd331ac925b63c7b12d722ea917b73199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33404988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f75ce278b18fae6ca6db2466f215ac469aad802640996a9583a48ffd6083f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:19:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:19:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jun 2026 08:19:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 02 Jun 2026 08:19:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575cc642df1608aa3a7dd13a5d11d9c1b0e947da30b140327dcbbb42486acd20`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 3.6 MB (3564688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfdb56313bdee74c9035c64d8f0955f4f96eaf39216dfcc07f1563f915807cb`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 2.6 KB (2640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4058043e8913014bbef8314241b526aff31cc1dafc3fe31d6687bfadd45c15cf`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0f244aa413cafe9503aa54e962810e25eeb5575cf14dabf003e18e01e6b79d`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 104.6 KB (104579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0f9c2a95be017c7cb55d088b520781d84106ced3f5371b3ffcd3c572905a83ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4796c51c23cf5e13016c160f0e99e73711f2d6f598b258ed86fde96380d02044`

```dockerfile
```

-	Layers:
	-	`sha256:d93371c9d6ece2f6cf45976a5c5c15c04a332fa920dda65d6cd64bb5a887d710`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 2.1 MB (2120907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:664b66c569f16540a51491a7c6e5b3ac4abc94ba3e9c470acf20345c740c7dbd`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d68642710aae078b8e89996ac5eafecc634ceb8ae7b59ff56b83785d4973e3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c0d4766cf8a7b23c701e4dba960d86ebe34269987eac6c889ba6f61e561f29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jun 2026 08:20:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 02 Jun 2026 08:20:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7ce85d6a4f7e55f753210ea58a2069bb210b5773b1f90667ae1b96ad6c58f0`  
		Last Modified: Tue, 02 Jun 2026 08:20:20 GMT  
		Size: 3.6 MB (3561778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3586010e44c2321adbb1a013c27b75c2594d069fe8a8b923886da05572f2ca1`  
		Last Modified: Tue, 02 Jun 2026 08:20:19 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9985cfd214b77dd7244a723023eab3d0f045e3a08ae09793263854ad201e1b`  
		Last Modified: Tue, 02 Jun 2026 08:20:19 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c81b86547b2f4045feaa349c342c702bc693662e5f588034446b0903797d34`  
		Last Modified: Tue, 02 Jun 2026 08:20:19 GMT  
		Size: 105.2 KB (105224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8e97b1e00c6b966efd15366c8bd5b64ad7ec88e5f191bf039b92fa49a699b8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699c75ebf1dd1c4225e9322be2587cac789c7c39450ae78578895be5060be76a`

```dockerfile
```

-	Layers:
	-	`sha256:38310a16f1f7da0df5b8da8dd8407e79ff7ca8e4a04591a8f57b7cd2b3ab0c54`  
		Last Modified: Tue, 02 Jun 2026 08:20:20 GMT  
		Size: 2.1 MB (2121952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a6a03093006d13698c10c2e93a860dca32148404ed133224a10bcf8a4231d85`  
		Last Modified: Tue, 02 Jun 2026 08:20:19 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:21e753dec167519b8f9d276a52a750cb73b5f2e3147c47d6c1d55f0433578888
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:88a76ddf418e7f9b5d419705b6395f5711e29911ea12cba732b35dcd2e2fcc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33405309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55e96d43c0bcbff0d82a774298729b80a2a3f51d3e0386209f675f389136c76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:19:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:19:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jun 2026 08:19:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 02 Jun 2026 08:19:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:19:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f6426f8abcddb3f2eabee346a49fc769137e2384ae81e3c68279050edc708e`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 3.6 MB (3564648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea9cf7e7041255ae1b3684f5585696f52812204b705843377099313ec28210b`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e8bf0d61d1b9f9d95ea40be64b7326ee9ec9ce2a7aa14d880de460494cc6c8`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb305bb2db6bd5dc3703cbdea0f3d53108bbdb88f35fe623583bb5039e4db5`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 104.5 KB (104514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7239f41f7275702aa7a967880126b6750296c7483f9c931cad19e9d2cc4c3`  
		Last Modified: Tue, 02 Jun 2026 08:19:43 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4d226a186e171678990cdbe166a540906ad1d0f5223ebfe9d9c6ad0c00583f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6a56bece34cbab88f1e2c4acd587e11dfa72a443aa5b9ea09ed4d1f2956ae5`

```dockerfile
```

-	Layers:
	-	`sha256:45477be9272359e838f7f1964de978824a8109e76c6db2b1005c17cbd0d85d20`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 2.1 MB (2120943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:219e102e2eb76012f5e49b8d6cdb8ee1a93d39b36059b54fa12067f92e9a276a`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3f7be7a944278c419bcf2de6cf7cf420c4fefcfd4ef951b8b34f5fa91fb3538e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4597a0d995072c8f410739cd1ad40ed07f7ea42ecc86fd1a96f2c6ece7fce6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jun 2026 08:20:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 02 Jun 2026 08:20:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5596a2470d94377b1e815cc2ee7c288f546f9f0655926e4d588add3cd4f2e293`  
		Last Modified: Tue, 02 Jun 2026 08:20:25 GMT  
		Size: 3.6 MB (3561810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cafb85dae3875631d851dd53bba7088b2e01691f2169f5dcc5ec223fd7bca8`  
		Last Modified: Tue, 02 Jun 2026 08:20:24 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fbaef9a5c2f2e43f64476a8f78ae6eeac8003a181b7b2d8d7dbe8f0c840c98`  
		Last Modified: Tue, 02 Jun 2026 08:20:24 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f168df6a74f0587779a3e031aaffde9a40b354be7bcd50dc9a4223c12faac0`  
		Last Modified: Tue, 02 Jun 2026 08:20:25 GMT  
		Size: 105.3 KB (105258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711a31b8251ba0a46a3dfc3465a794c66b426a6dabb8804f119adaca8f65ef8`  
		Last Modified: Tue, 02 Jun 2026 08:20:26 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a786fca9404aa81675b92c02536ba3628c08fa98791bd3e4198f38e0152e768d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9781ac8308d43b9c1f45ce9e83a4f530d1cc85a3c701aca51af6fda789451a`

```dockerfile
```

-	Layers:
	-	`sha256:d6c00621d43057baa9f2f60b1e3fc45081a0eb01aa99b8a8c8b84e65436039f7`  
		Last Modified: Tue, 02 Jun 2026 08:20:25 GMT  
		Size: 2.1 MB (2121988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28bc2f43dcbb9bfdd7ed8e6352956dd315b7efd406e226b26e774ff1da94ba06`  
		Last Modified: Tue, 02 Jun 2026 08:20:24 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:e1f82331fed085ae65759722772d310e652df3d2580df3961a0fb4ed72b242c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:44b94bce3070df694aa69360e5f4d25dd331ac925b63c7b12d722ea917b73199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33404988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f75ce278b18fae6ca6db2466f215ac469aad802640996a9583a48ffd6083f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:19:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:19:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jun 2026 08:19:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 02 Jun 2026 08:19:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575cc642df1608aa3a7dd13a5d11d9c1b0e947da30b140327dcbbb42486acd20`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 3.6 MB (3564688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfdb56313bdee74c9035c64d8f0955f4f96eaf39216dfcc07f1563f915807cb`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 2.6 KB (2640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4058043e8913014bbef8314241b526aff31cc1dafc3fe31d6687bfadd45c15cf`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0f244aa413cafe9503aa54e962810e25eeb5575cf14dabf003e18e01e6b79d`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 104.6 KB (104579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0f9c2a95be017c7cb55d088b520781d84106ced3f5371b3ffcd3c572905a83ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4796c51c23cf5e13016c160f0e99e73711f2d6f598b258ed86fde96380d02044`

```dockerfile
```

-	Layers:
	-	`sha256:d93371c9d6ece2f6cf45976a5c5c15c04a332fa920dda65d6cd64bb5a887d710`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 2.1 MB (2120907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:664b66c569f16540a51491a7c6e5b3ac4abc94ba3e9c470acf20345c740c7dbd`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d68642710aae078b8e89996ac5eafecc634ceb8ae7b59ff56b83785d4973e3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c0d4766cf8a7b23c701e4dba960d86ebe34269987eac6c889ba6f61e561f29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jun 2026 08:20:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 02 Jun 2026 08:20:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7ce85d6a4f7e55f753210ea58a2069bb210b5773b1f90667ae1b96ad6c58f0`  
		Last Modified: Tue, 02 Jun 2026 08:20:20 GMT  
		Size: 3.6 MB (3561778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3586010e44c2321adbb1a013c27b75c2594d069fe8a8b923886da05572f2ca1`  
		Last Modified: Tue, 02 Jun 2026 08:20:19 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9985cfd214b77dd7244a723023eab3d0f045e3a08ae09793263854ad201e1b`  
		Last Modified: Tue, 02 Jun 2026 08:20:19 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c81b86547b2f4045feaa349c342c702bc693662e5f588034446b0903797d34`  
		Last Modified: Tue, 02 Jun 2026 08:20:19 GMT  
		Size: 105.2 KB (105224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8e97b1e00c6b966efd15366c8bd5b64ad7ec88e5f191bf039b92fa49a699b8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699c75ebf1dd1c4225e9322be2587cac789c7c39450ae78578895be5060be76a`

```dockerfile
```

-	Layers:
	-	`sha256:38310a16f1f7da0df5b8da8dd8407e79ff7ca8e4a04591a8f57b7cd2b3ab0c54`  
		Last Modified: Tue, 02 Jun 2026 08:20:20 GMT  
		Size: 2.1 MB (2121952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a6a03093006d13698c10c2e93a860dca32148404ed133224a10bcf8a4231d85`  
		Last Modified: Tue, 02 Jun 2026 08:20:19 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:21e753dec167519b8f9d276a52a750cb73b5f2e3147c47d6c1d55f0433578888
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:88a76ddf418e7f9b5d419705b6395f5711e29911ea12cba732b35dcd2e2fcc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33405309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55e96d43c0bcbff0d82a774298729b80a2a3f51d3e0386209f675f389136c76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:19:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:19:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jun 2026 08:19:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 02 Jun 2026 08:19:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:19:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f6426f8abcddb3f2eabee346a49fc769137e2384ae81e3c68279050edc708e`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 3.6 MB (3564648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea9cf7e7041255ae1b3684f5585696f52812204b705843377099313ec28210b`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e8bf0d61d1b9f9d95ea40be64b7326ee9ec9ce2a7aa14d880de460494cc6c8`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23eb305bb2db6bd5dc3703cbdea0f3d53108bbdb88f35fe623583bb5039e4db5`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 104.5 KB (104514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae7239f41f7275702aa7a967880126b6750296c7483f9c931cad19e9d2cc4c3`  
		Last Modified: Tue, 02 Jun 2026 08:19:43 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4d226a186e171678990cdbe166a540906ad1d0f5223ebfe9d9c6ad0c00583f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6a56bece34cbab88f1e2c4acd587e11dfa72a443aa5b9ea09ed4d1f2956ae5`

```dockerfile
```

-	Layers:
	-	`sha256:45477be9272359e838f7f1964de978824a8109e76c6db2b1005c17cbd0d85d20`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 2.1 MB (2120943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:219e102e2eb76012f5e49b8d6cdb8ee1a93d39b36059b54fa12067f92e9a276a`  
		Last Modified: Tue, 02 Jun 2026 08:19:42 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3f7be7a944278c419bcf2de6cf7cf420c4fefcfd4ef951b8b34f5fa91fb3538e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4597a0d995072c8f410739cd1ad40ed07f7ea42ecc86fd1a96f2c6ece7fce6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:20:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jun 2026 08:20:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 02 Jun 2026 08:20:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:20:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5596a2470d94377b1e815cc2ee7c288f546f9f0655926e4d588add3cd4f2e293`  
		Last Modified: Tue, 02 Jun 2026 08:20:25 GMT  
		Size: 3.6 MB (3561810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cafb85dae3875631d851dd53bba7088b2e01691f2169f5dcc5ec223fd7bca8`  
		Last Modified: Tue, 02 Jun 2026 08:20:24 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fbaef9a5c2f2e43f64476a8f78ae6eeac8003a181b7b2d8d7dbe8f0c840c98`  
		Last Modified: Tue, 02 Jun 2026 08:20:24 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f168df6a74f0587779a3e031aaffde9a40b354be7bcd50dc9a4223c12faac0`  
		Last Modified: Tue, 02 Jun 2026 08:20:25 GMT  
		Size: 105.3 KB (105258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711a31b8251ba0a46a3dfc3465a794c66b426a6dabb8804f119adaca8f65ef8`  
		Last Modified: Tue, 02 Jun 2026 08:20:26 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a786fca9404aa81675b92c02536ba3628c08fa98791bd3e4198f38e0152e768d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9781ac8308d43b9c1f45ce9e83a4f530d1cc85a3c701aca51af6fda789451a`

```dockerfile
```

-	Layers:
	-	`sha256:d6c00621d43057baa9f2f60b1e3fc45081a0eb01aa99b8a8c8b84e65436039f7`  
		Last Modified: Tue, 02 Jun 2026 08:20:25 GMT  
		Size: 2.1 MB (2121988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28bc2f43dcbb9bfdd7ed8e6352956dd315b7efd406e226b26e774ff1da94ba06`  
		Last Modified: Tue, 02 Jun 2026 08:20:24 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:ef3a5c51820c067fa339f4cd86f52de0dade5cbcbfe4570f30c83f1550693147
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
$ docker pull neurodebian@sha256:6a72868c208d4a8be5b7b5f612b35ce62e40f3798cf5fe764ffaaf54bde4f98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59698490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de65a63aaa0d111ac14cc8853ffae5cd4ef9156bc96d4bd3a51d226c42ee89df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb92dddd3e26de8152ea75a9f69a7be5761222e5964f3314a90b2a741df7a67`  
		Last Modified: Tue, 19 May 2026 23:27:10 GMT  
		Size: 10.3 MB (10294134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1c2439c5a41a3f1565849f2bc31ca69db3d67c673bd935365e56e8f32757d8`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd176b7467191c7e24a95efa3ffd50313d148c7ca9ea895d817611de25e2d87`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcf153616e06880716cf7afc320d8ca5b96a6e7592fdf296f7774cee2c61cff`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 90.4 KB (90385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430d60c0f134e218d63b5622fcf67693a4572355671c787fcecc75f6ea05146e`  
		Last Modified: Tue, 19 May 2026 23:27:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6575786d5511d37cb45ea2f2bc9a60a73b23ec4b7a846615187b7d53f4c17b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8c0c8a42b651063403d5abc29b6068a1f0be3c92be2e70cdf69f76f1979e5`

```dockerfile
```

-	Layers:
	-	`sha256:4ad2872e53fafb1cfeb07186d1a983a4d06fb66f95e066efc30f0189d2727f89`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 3.6 MB (3614186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d064af7b145e3a9c6c262ddf2b47d81c9159bb7c8a41e30403adaea836fd0e93`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7aeac7881d0535bae0e2e617f8315a5761b850d71cf58932bd311d4b4d1f16ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48ae2a6c99c13fd0de35eef7b88f31273280054664f82606663688cfb962d60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:48 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aad82dd52a16af0b9a752ae3c6f52083d005b3f021022ac928e217f659b8923`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 10.1 MB (10079251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3457a9f11dc4e18f12cc7a4005782198f4b79a88a7eb1d887dacf5a49beac32`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864235a4a0107dda08be1df2d9fb91d16a1bf0cb6425d918f3e7f279b47d9f76`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129c1fb1c64d94192c382e701d7b14a904efc5fcf1eb658b53cee6dfe4ae533b`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 91.0 KB (91018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7475df3d2a504fa9557ad54214cead31cf01b3c7ca054fe251c62de736745`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4427b4272236147c7e4b07556d22350ca0313cef9b870e82d94aff1f01e3f590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00250ec6efad1de33c7bad769cf3969b6d6530f417f6a779f0ca83ead0468a43`

```dockerfile
```

-	Layers:
	-	`sha256:724a053293413cabf623432bad27c4826b21bfb9630cc4f131df52bf88957783`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 3.6 MB (3615076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b106f5a48dcae253fb77c7274705db08fa073e24eaf2727eb59817d5105d5bed`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2a596ddb9229467c8474294e2e7fa84b37aca64758f2e82a66a7216074aef32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61391860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a3b151ea42db43a346e8d6b49db21ace20626081ed4e9127c0bdaaf47a98cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e6c7527b1ba130a7fd028db4b4f53fe2952922685a72d987e0bb45aba2d459`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 10.5 MB (10468195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac79af1a4117eeb379989c2a6fa268003cbcc7d525c61702842e54d57e9dc65`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37824e2171f8bcb2f390052ce2fa9cb0f979c1030b16c7aab208f7ab72ec972`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750bf144b8fe3a2951d8c7acd97d5afb0704bd216e92fa3a311ab128669845f`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 90.8 KB (90757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822259b6e0e53e9f7d48de30ad4a457448625709e9bdcb8900c1f585458a3b94`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:571389a940bfcc86c5c176393870c94339e1c9c4addba68adca4fc69aeceb89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fe2f14ca78dbec2a02cb0190f6d6fa7ec0db597f47cd9517ec5e4f34f24303`

```dockerfile
```

-	Layers:
	-	`sha256:03d12e0fb081073377307046634158fe58b2600b735ce815ae52909707755842`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 3.6 MB (3612134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18610647bc1842a68384e807f0184ee9984e617990bc40de96da84e376d8d4e`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:fb78a302d8653e842ab45d60c058aa74ea89549dd319d94f4ca7a4aca05ea741
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
$ docker pull neurodebian@sha256:40c77bc9cd15c45e56f92dd37748f65dccb5c9b25db474e5583299263a9a84da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60197651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91559e8c87c582c15bc416fbe03a5bbc5f4a584a24489ce55920c37298af5235`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:27:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:02991db6507c0026c404c68dc35ba4f9c80895d9d7fc4576cc1507337d1b4eb7`  
		Last Modified: Tue, 19 May 2026 22:36:41 GMT  
		Size: 48.7 MB (48712012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e58d1748e5151dadb72e1f165353c365ea3bfcbfeab0aa145d1b087b5d6f8`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 11.4 MB (11393325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b38bfcc5e625cbecc79aaa8b01e5e2d5059f226d6eb13898b0f437bd891e76`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54e14b8ad488bc00575a9c73515d031181675b31576e3eb72253c6c475a0ed9`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a7e3b6d7043fe182d56ec838ca1ec702b85b90778102555a622cd76f574beb`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 89.4 KB (89412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d847daa249197059f5e935dd19b4ea9eedf33149ed7e48cfe007c15f2309cfd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952c080329812ec9363845d75ecc38cb4ac235bee430008cbde7fca8be845388`

```dockerfile
```

-	Layers:
	-	`sha256:66bbb59a3adb62e0ab6fa91117f8718bcc512e41d0ce510cd8df380040bf908c`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 3.6 MB (3553364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f5b45df19088a13691bb334527d8caf74b958c6ff741123494348b8f7f40b50`  
		Last Modified: Tue, 19 May 2026 23:27:39 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:edd8534702838d10c4423132ede211ed67cb3b8aad6e0d66635e99db9a0f1062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59923588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdb84dcbc65ca8290823468d8ddcd2d3907e5ca3a931aaeb8b7de01ed7d468e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:31:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:31:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:31:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:31:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2bc0682b6790aa6b6a3a5a7933e32ea4a35d72d531a3c53509cd76aae83fc88`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48737609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8326e665e37dcddbb4117e65487a3fe42cad6dc654d0685797e71d08a81f41`  
		Last Modified: Tue, 19 May 2026 23:31:17 GMT  
		Size: 11.1 MB (11093058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3eea31e0306f1e7f62ba1545e5336a5b2882bddb05be08647685007419562ab`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8105a082b1fcef71cd46e3265f9493987a9fde8724eb7eef0c0900a25bca33`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1517d5423bb99fa782ff6a0604859e368e373d113f8ed534219ca5a9b438dd57`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 90.0 KB (90020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c7701d7e0a9709d5816ec7ea634a4e09304ea19f8f039720e6abe4353a1076aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d10534cb5a776d3b454d297628278677c6febc6e889117d2a786fa1624ab64`

```dockerfile
```

-	Layers:
	-	`sha256:65821c57772256a43a3e64aa43b60da3762a2de794db20f576d83d048cceea1d`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 3.6 MB (3558069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79dcebfbf845b6b95b62872c6707ec89579e790e83597c63c3dffcf4fd69e0a3`  
		Last Modified: Tue, 19 May 2026 23:31:16 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:80ab709a5003e5bb19b5298fb94704be677eeacae57e1546f3a27c134e408a97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61734334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ac3ec238f09fca3619da6c12e8411fbedf0953b46cb91f86aa5f9046836c0a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:26:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:506409f9b5466021b987fde6d84a8bc529520e50798929836cef94e3223d354c`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 50.0 MB (50016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7753854dd3eda9aef2aaa8ce9d1e3f65ad0732a1084526b6ea495204123445`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 11.6 MB (11625732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80680d0e09afe77e520bc718136fe080de719a24960af381889b5325a007ced5`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfcc9462b033e2edd695c438057a9d245ada5fc84587ca3a58b07feee07ab51`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ad603d2e8d78ab42ac28bace917a076937246df7f6d0c0633126b17f0cadb7`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 89.7 KB (89692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:57343788c201a8c001feffcd753e8cfbb1a6dbad640af928c8b65079937916d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583407654d7c95b5dd7f0c49b8cf2c3dda7a02034c8aecaa2c56a63e3009e10d`

```dockerfile
```

-	Layers:
	-	`sha256:d09a0b84829b224ad027b6f9b437d39c2e73c8cdb44870c4ca0bc993869b1c1e`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 3.6 MB (3551313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcef60f7d04efbb4e57e855b92a9b8620465376f9df755c28290b9aa572be599`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:2624eff6ec3e21c06489236b191eba01b0beab037b9f28fbd3736c7a66bef5fc
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
$ docker pull neurodebian@sha256:b5fe02ba6e80b840d27c9a28023093ea6c23d0c9f89a31872582dae4ae70095b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60197932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8a8113f4d5f843d3701212777122250946f4084ea90c4b210315d8c8552389`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:27:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:02991db6507c0026c404c68dc35ba4f9c80895d9d7fc4576cc1507337d1b4eb7`  
		Last Modified: Tue, 19 May 2026 22:36:41 GMT  
		Size: 48.7 MB (48712012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6e71e03194020c479ea6543a7f33f5099fe2418b16c8172dfe51e95cc37839`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 11.4 MB (11393195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bc269137e2d1ef84e9a7f609fc3cee05da2a89706f759a7fb1d61120dbf448`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31f9d3c942e826f99ddc6c49a7e3b652962a818c4f1d9922b0ce1742da0e16d`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a46f5f08e788d4c601b78c2f74ee528b3e922bd597ddc3a26614d7f0b61435e`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 89.4 KB (89401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0712a6b21cf63c1f33a22eb08643b4e391abf913201dbb2729f8ab5e93d38911`  
		Last Modified: Tue, 19 May 2026 23:27:36 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:07e73ceeba01283e1cfdb5acd37480d6a18e0c497846033f81ddf4428ff6cc53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ea38aae25cdb12c25b7f88c9a1dc8d8fefa9067665af128c4b1e7ecdc13749`

```dockerfile
```

-	Layers:
	-	`sha256:aa9aace3b47fd65d09b268c1a1a0179945bc17f6958197bf895d8106b13fe493`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 3.6 MB (3553400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa2070502a6c70b838ddfe00d5321fddaaf3958e9305ed560c66aab2560d3a97`  
		Last Modified: Tue, 19 May 2026 23:27:35 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fdd6f83569e0862993e48832d03be26ca04c8faf222c5bd056f0869665a221f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59923995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b961227030f6ce3ce85d3b4a28a1bbf746687c9a53ffb5b287e67a7c7838889`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:31:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:31:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:31:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:31:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:31:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c2bc0682b6790aa6b6a3a5a7933e32ea4a35d72d531a3c53509cd76aae83fc88`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48737609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dc44779cb8617743124f685b6bab6ed6aa724234cc4ea684ac0e74eb53ffab`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 11.1 MB (11093028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0b4f7877b91c9ff52ee44f9d75b23d583cc18625559b238ae0ad4ed4ddabb1`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c6c0d651e53ea292ef5612a941931757712de6d1e19de433fbcd7cf87dc2ac`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2e9ab7191a3546247ec4390d48df26cfee47a530af5bca3c34d103849864bc`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 90.0 KB (90034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fae19e42bd61f416eefbbb0e6fbb41a346ae78fa1e9ae01b2d2cff5fc1ec50b`  
		Last Modified: Tue, 19 May 2026 23:31:33 GMT  
		Size: 422.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:edd41d5d71718554898395d73aabbabc52399729a7bccfa89b3a2487b861820f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccf3bae28acb19d66c068d98778afdc4eb4041506e225e424b413673506b68d`

```dockerfile
```

-	Layers:
	-	`sha256:10da892ffed892fcb2aefbf7a1af3177eb97af944f1b959a13f3ac0f0ea0073f`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 3.6 MB (3558105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986de3b52a66825431d3fdd5b0cae2b54b16b8db36ba5742038cf5719470dfc2`  
		Last Modified: Tue, 19 May 2026 23:31:32 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a86f4de25dfa6b6e91e64e0b6f5d40aedaa1ede6fb8e37582ef64613c19b1b77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61734790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc88f1a9c7d540c5d0ded18483a54b1c35d38bd566e529c2d509069f6cc8ecb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:27:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:506409f9b5466021b987fde6d84a8bc529520e50798929836cef94e3223d354c`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 50.0 MB (50016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510eda87fd6292dc0e1f9f0e55d72bafc27bf3b6fae3490ebf7da2201fbf34fd`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 11.6 MB (11625786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e78771190378876740c64297e71d7791a44fe070a7d393ec614e250dd891c7b`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a0595dec45a612a498719506c3131b9798d2f5b5909b4127dcb4ff8e4711be`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7047c4ee9b2e983af1985c1c6458f4f8a3b8074315a26585db4bcbef767e38`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 89.7 KB (89678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca8ce972bbd0785587fafbd77eee4417f7e1b6cff9fae89ccec68703c02373e`  
		Last Modified: Tue, 19 May 2026 23:27:23 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dab455e33202ee0696d74d63c649ac1104d40fe2e90ad3a2e7ecf50d4a94f42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f56c073239f966bc31414fa40751a0c54fb9ed1ed499e8038fb45888fafc6fa`

```dockerfile
```

-	Layers:
	-	`sha256:189d9d6cd49490617375e11667be902783dabc2a73ba55a06af2f6ce1542844e`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 3.6 MB (3551349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:231621bc9581f8c17abcdc788132da2cdd4e950e127faebf5d51ce22cffd68b7`  
		Last Modified: Tue, 19 May 2026 23:27:22 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:018480627781c4f09ea274ec1bc621e0efb67169822f7b105e75a89ab96cabf6
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
$ docker pull neurodebian@sha256:5a9a16c21ab86720341c5aac3fc5e19af871a9930ca090419f6362b69f7e711a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59698019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d7ec001bda49b603142553de0e421284e9a4311d4efa7080638b518e8e8322`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba814ed0b2d9a547c76536523b463e06898aebf2aaa398aa74311d3c1dc1a4e`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 10.3 MB (10294107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2e37411de84cbca2fca1ff8d236df88116d475c59a2c69614af55802a9bbf0`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d341991aaa56f761b5dab25eabf016668a7df99acd80b4a859fea4f6f10f1be8`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471d6791181851b02e8005a6a573347bc3343e727010d156ebff951c01f0831c`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 90.4 KB (90385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ffd1de262fda88d420c478f4e125ce39e37a19e9370de15c8b7bb70f87a37b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bec6da167a19c934ae18b41c68d67abd2c272e0af3c4f82ba0dd5e8a0ec9c2`

```dockerfile
```

-	Layers:
	-	`sha256:1b2cd8a742194e30de120f5799fa47218b060ad8e5813ad5e839bd52cd6a49a5`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 3.6 MB (3614146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba7e66993193c71d173a9a88cb6c1f544da27e64f231bbebc5f2d8865c83015`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1ebb7b15628e7e0ebc948ef63b2191b8379dcce522cebccd39a9a2a685b06513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c791dc53a9166c2866017c86f531369092012575d8755081c0e8524e04cfb0b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1942be77793cf7d7768bf84d6eeb2ba5950a28db24f33091ff5994538cf1a6`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 10.1 MB (10079225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3457a9f11dc4e18f12cc7a4005782198f4b79a88a7eb1d887dacf5a49beac32`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864235a4a0107dda08be1df2d9fb91d16a1bf0cb6425d918f3e7f279b47d9f76`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745f6668de60811fd9ba506dd37cf3433b97f825e2890d3c0ec81b413f3cb511`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 91.0 KB (90998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:169b5ce71453916a845776bdb00f54d254a42a8ac82934fc339558f892a93252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a699a5f993dee3ada544a33120f37cc56d20e87c04aa524725f0f702d7fd45c`

```dockerfile
```

-	Layers:
	-	`sha256:025c64ba23493947f035fcbd203e7fb190c05f790a389eccff9d5f2a626187a7`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 3.6 MB (3615036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f2692cf313664fb8d329acb3431b9dcb225150641afdaaad3d858f6add85ff`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:8de903a96a87d453f0f55e59a481d2ecb136af612e7a8cb1af3ebf7b4c4599b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61391247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc3a9c9e96550ad6abb72f0ed19bcd31f13470b3b8d71a1d44e79bde57cf1ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cc7ed761905fe0f613ac0587c2eee5fc88709addaa08848f0c530ec2dce1e0`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 10.5 MB (10468039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faa1ede3b3f88be094ea90befe80e469bf334a24ffc05b7f563662d85c89ca2`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ae4073214f3081684e7a0498b92c738fed59cbd0bf33dc5834b8b759736dd6`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff35dae5623186c951a120843fa244868f705164a1489437aa109a8d84704d1`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 90.7 KB (90746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6ecaaff4cf9b54e0b165525fe2690467a6733d849e2a0a48eec9d898da7b371d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244fc09bdd8c8364a7de7fad082cb5c2db5b255f52ff05b1dc5e310aa74ad834`

```dockerfile
```

-	Layers:
	-	`sha256:35f4f12874c2ddbd67f0a31a9593a8d28a9987efb0c2eba8d007bf1b9a0f6e0c`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 3.6 MB (3612094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e3a199c0d4b66452cc112a33ebb31826de992764349f3abee5ec027278b2c8`  
		Last Modified: Tue, 19 May 2026 23:26:44 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:ef3a5c51820c067fa339f4cd86f52de0dade5cbcbfe4570f30c83f1550693147
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
$ docker pull neurodebian@sha256:6a72868c208d4a8be5b7b5f612b35ce62e40f3798cf5fe764ffaaf54bde4f98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59698490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de65a63aaa0d111ac14cc8853ffae5cd4ef9156bc96d4bd3a51d226c42ee89df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb92dddd3e26de8152ea75a9f69a7be5761222e5964f3314a90b2a741df7a67`  
		Last Modified: Tue, 19 May 2026 23:27:10 GMT  
		Size: 10.3 MB (10294134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1c2439c5a41a3f1565849f2bc31ca69db3d67c673bd935365e56e8f32757d8`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd176b7467191c7e24a95efa3ffd50313d148c7ca9ea895d817611de25e2d87`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcf153616e06880716cf7afc320d8ca5b96a6e7592fdf296f7774cee2c61cff`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 90.4 KB (90385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430d60c0f134e218d63b5622fcf67693a4572355671c787fcecc75f6ea05146e`  
		Last Modified: Tue, 19 May 2026 23:27:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6575786d5511d37cb45ea2f2bc9a60a73b23ec4b7a846615187b7d53f4c17b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8c0c8a42b651063403d5abc29b6068a1f0be3c92be2e70cdf69f76f1979e5`

```dockerfile
```

-	Layers:
	-	`sha256:4ad2872e53fafb1cfeb07186d1a983a4d06fb66f95e066efc30f0189d2727f89`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 3.6 MB (3614186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d064af7b145e3a9c6c262ddf2b47d81c9159bb7c8a41e30403adaea836fd0e93`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7aeac7881d0535bae0e2e617f8315a5761b850d71cf58932bd311d4b4d1f16ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48ae2a6c99c13fd0de35eef7b88f31273280054664f82606663688cfb962d60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:48 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aad82dd52a16af0b9a752ae3c6f52083d005b3f021022ac928e217f659b8923`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 10.1 MB (10079251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3457a9f11dc4e18f12cc7a4005782198f4b79a88a7eb1d887dacf5a49beac32`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864235a4a0107dda08be1df2d9fb91d16a1bf0cb6425d918f3e7f279b47d9f76`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129c1fb1c64d94192c382e701d7b14a904efc5fcf1eb658b53cee6dfe4ae533b`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 91.0 KB (91018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7475df3d2a504fa9557ad54214cead31cf01b3c7ca054fe251c62de736745`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4427b4272236147c7e4b07556d22350ca0313cef9b870e82d94aff1f01e3f590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00250ec6efad1de33c7bad769cf3969b6d6530f417f6a779f0ca83ead0468a43`

```dockerfile
```

-	Layers:
	-	`sha256:724a053293413cabf623432bad27c4826b21bfb9630cc4f131df52bf88957783`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 3.6 MB (3615076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b106f5a48dcae253fb77c7274705db08fa073e24eaf2727eb59817d5105d5bed`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2a596ddb9229467c8474294e2e7fa84b37aca64758f2e82a66a7216074aef32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61391860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a3b151ea42db43a346e8d6b49db21ace20626081ed4e9127c0bdaaf47a98cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e6c7527b1ba130a7fd028db4b4f53fe2952922685a72d987e0bb45aba2d459`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 10.5 MB (10468195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac79af1a4117eeb379989c2a6fa268003cbcc7d525c61702842e54d57e9dc65`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37824e2171f8bcb2f390052ce2fa9cb0f979c1030b16c7aab208f7ab72ec972`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750bf144b8fe3a2951d8c7acd97d5afb0704bd216e92fa3a311ab128669845f`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 90.8 KB (90757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822259b6e0e53e9f7d48de30ad4a457448625709e9bdcb8900c1f585458a3b94`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:571389a940bfcc86c5c176393870c94339e1c9c4addba68adca4fc69aeceb89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fe2f14ca78dbec2a02cb0190f6d6fa7ec0db597f47cd9517ec5e4f34f24303`

```dockerfile
```

-	Layers:
	-	`sha256:03d12e0fb081073377307046634158fe58b2600b735ce815ae52909707755842`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 3.6 MB (3612134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18610647bc1842a68384e807f0184ee9984e617990bc40de96da84e376d8d4e`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
