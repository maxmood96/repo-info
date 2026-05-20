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
$ docker pull neurodebian@sha256:356231256775a4b0d3316fe01e22251f9309722d6efc0706ccac533eaaae79ba
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
$ docker pull neurodebian@sha256:4db04057176b65f60447ea0de14d71e589435efc93f5f9e0942650cbc343e201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d0d6bea08068fbb0f25ca7e55202dd93371d5e2f960b095b57d73b56802257`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb9739c6b4f68bc7ceda360ba82976ffea2a2b0f910162f3baaddf10c30baaf`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 11.7 MB (11693065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d4aa3bbcd7f103db531b544aa469fc669490bf0f63070fb63340476b4b2ff6`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f5291b6f5da64f52099bfd741111dd36b90a2fef3af20ec6d5cc367da8d4bb`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaea8274562ed42a6906cd9cd33a459780630e229f388af5b5627ab5ae06b749`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 93.4 KB (93437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e167ffe5ba168b8cc58cf782364dda325b14826d22b80241ce109a8f1f87cfd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c80c7632358c017feeb7106b43d3f8a70130d34fb57220e3a95f07cf348c3e8`

```dockerfile
```

-	Layers:
	-	`sha256:f6175cf9e3596d080ca37a17bf2e4e4756b45b06df58d192cd2d34c654ec1021`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e857221844e8f6652439e116a12b9371a11d1e340573ecc8b292cf063c8552`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 13.9 KB (13935 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:3829cdccee4364db4c1959cfb67208062e1e9895a0f70d970201e3bf3f914b8c
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
$ docker pull neurodebian@sha256:7bc7df072b8d4192da532d04d6fead4b1e24bc92dc244d3039bd8a47c37f53fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3f5e69332c4e42d45a5f556b5626d9a922ed8e3e5702c07d3e8270f7a02cd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fd686c2be4701aa5e99504e0a0a231438cebab31803f9703d4f2817fcfaf3c`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 11.7 MB (11693032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c275dff193370be94cf6b05afcd2f50b992d61b429151ede147e0d16bd143`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed34c26dacdd7f022ad39094d3a0e7234c0e1adaf272d36639f4a548d0bb34a`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed24d41000306ac52cbf2623e08455d064489dded03b85fd01bce6bd72a7c0`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 93.4 KB (93421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c476f9525210c69f52698c6764a1dd93f0e3c72cb3941432ffad0b4dfe7ee5f`  
		Last Modified: Fri, 08 May 2026 19:44:53 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8707a48f987ea14bd078ac3746d28881d4119f0480d7627964a7d15c52545760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db7f5ae92125a30eea36bb373c2d4ef882b6f6936fbc0adf910cfc3e2feec4c`

```dockerfile
```

-	Layers:
	-	`sha256:f5e53c43561d0cbbbb39a871b900ba903431c52a26c9b7b5d743b6635d3bfdc9`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f6d2384fe0ae77451cec1bc567fb85d31e77c7b721f8bf337871e4e30ebdf90`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:a10175f8577ebd2900474594b994ed98951c30adad108f30a1372408d8401189
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
$ docker pull neurodebian@sha256:8008767bb706f4c4cb709ab5f06a757d417059201885cf55e86abcb4cb6dcef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66311198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2c192eae3260d4134a76b7bfbe15ddfec137154687d3fa42db1128cb0fe0a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e381fa04b31e7bcb9cbbc40e4bf2902f0c275db7edc7b0462ee8936db48315`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 11.5 MB (11502397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ab2eed64c3b37a86ab0b509b8f661cecbf7b66e171eaec9e5c546fa3036762`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134a997cd26a4c569d5d64a9da26466d3c5c487619a3e32f1c97969f13fa616a`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3596ad0c31ef351fa9a9305382ce6d40415c6c0b91c7298614f295de6c8582`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 101.3 KB (101301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:42f660d3785330ad3907a27b2a3014a5478c77cb6a2ae7174a586851e2a97d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f329d1467811d726f323694ba1065308a4220276c10e46100ba962ecb9c53f90`

```dockerfile
```

-	Layers:
	-	`sha256:a6c78a26c8ba94bd4d662a5f8aa1daccf0739185d688ddd88ead6c3050508785`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad96a7377786062bdd01bea8d0bb1ed027db71956b280c297a74b774fa1ab0db`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:a62913443fbbad4e4a78ff2a26bafca2715a51d6cf73e121a760add480a6be6f
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
$ docker pull neurodebian@sha256:ded0c9f44bfebe4345080e2a4390c3b4fed39780d1353b24e811e6661fba9ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66311558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a59c5ac3b1631f24b5bc8d5baae5bb53973e1d0f372a2f088c0314105f17e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9627add8f31e74417d79a305014794f3cbdfc718e75672d32ef679cae4d543`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 11.5 MB (11502376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fbbd060166db850453937acb417b1629ded3d89e8f175047d313eb4d4ea249`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bda2e809eea5007777365a49ca07551a25dead0adc7cab0981a605143ef59a`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f25d850d54a1638e683ef541be2effa3bca6c0b42442affc13c0b580347563f`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fad3e9fd8287dfd51f1b9399e6918557a0ab780529cfb43d95f377c5871ffc`  
		Last Modified: Fri, 08 May 2026 19:44:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:84d520f83be769fc2d681e70788d29039c5cde27701f289c18e4bab929ce8d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24962661fd033444e442b5d8f8a4cce6aa12e5693c6953d7f1bff736b34e166d`

```dockerfile
```

-	Layers:
	-	`sha256:423513329c10f41f709cff6f55c81130aebb09ea250c3f3d837102c1163b7fbc`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4f37060f92539dd9a20f74d6de85a1f15bebe90d992329da9927373d4af4e8`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:d5f6096a6a003f533e7c844997c6efa784cd8ab50e379117584c0895316a05a6
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
$ docker pull neurodebian@sha256:229b368a6b98d7ce660433a55e8b2363a19a2f808ab9c873f24b05b1a8a7be84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61605870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075291128ef3150dc12f76a862c4d327c51305f9d2d92705a276cef92e88d3be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:45:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37fd7fd52239cf41c1513003560316f753d3b29bffb106c1c8cbf260e58621e`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 11.6 MB (11589003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b51446d80054a5f43c4ce780e4dc27dd69be5690c5515991223b5af7a9fdb9`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39c1cdcded0b2bce400d9caac28b0b5ddc7273cc5e5c057393fdcebbb9055d5`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3edebb8be1094d35833e792183bac8d8b69a4cce9b1de1627b384fde68c22b`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 89.7 KB (89744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7585901b3fcd61be98cc07c0fce812830eeccbd9bbbc4c73075927b5a94c6ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b2de58ad6d4212e7b4a3044a392c77b1cb7b570cafeb9b7a95c08097b9b83`

```dockerfile
```

-	Layers:
	-	`sha256:a5e656a37608c6c496bbc4e3f21f2e6ebdd0ca00774a6b5e42196d97aca1ff25`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 3.6 MB (3554190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac42095d0498fb668d35a1880cc1400381b34697805a03ea4a3cef3243668e26`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:0dc2f773daa7d22adba6aa7de74836388e88697d6fe3a215830b29a8913137bc
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
$ docker pull neurodebian@sha256:03a1a328bfee5ff0a2bcd6a694bf094d95381b9b663a843aa2e3ae99924b758c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61606220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c3c7ade491f697623eaf25c70f50f5a71cfb7bb1d3153121edb8caadc6b964`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:45:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a99493d96d6f92ea6d88890fe995d3918a05c9baec0b84c6e9d10b95007a82`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 11.6 MB (11588918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a0c33e147fa59d9124cbf1b02679d5996d94f20e43a0b0dcc7bac0c76d9bae`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d6a895ebfb8de9b1aba761e3f5032daf08032da3fa41c4770fb7be187e4cf0`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d22eba06c949e34b02517b4968779ffafdb8e6ce52c51cf497c682389b154`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 89.7 KB (89726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2616c3f976bfa74ec623fc4792a7910f4ad8177ed3b117a8e270087f0510a539`  
		Last Modified: Fri, 08 May 2026 19:45:21 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c75c21cbb9fff8f22041a53794d1631c30d371e24e4a25d431e1c649eb7fa77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7075d85a25976a8e3bcacbf0a99c3a51ddb29e013c5b42c7da1a973f852c1ea0`

```dockerfile
```

-	Layers:
	-	`sha256:7ca33354efa5a678e18c52598a002e0f989c7bb096e45147472c2b5788c43e45`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 3.6 MB (3554226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53d2a0a43649d8f679119161461ce4dc60d130a0faefe0533fc5173dbdb17353`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
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
$ docker pull neurodebian@sha256:3602890299b829a6c3d93bd6aedf212cd74262599093b249c2287b5c6bb5cca0
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
$ docker pull neurodebian@sha256:674b7f113ab98f457c90a5407cf9fce5d326c1ada9d335c3bb736dac15df1d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd893df613b6c8c15a740d7cf4906096d1c477af22aea43f2c1a7965c5c10b95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918b15ce42e2f43331d7ca8a6909c2f318788178997f3be2a6c20d15686eae08`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 10.5 MB (10467078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d8c3e17a2f821d9a1e4a647dd71fd281974066ed12286ff5344c3c70918add`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745c310d83150426f135a032fe18cc82a8e5631e02d97a07354f8c9341131d6`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d13836b8f7a1419799c27ce5e5586655df8273d6004aaa0c492b5a99f6622d`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 90.7 KB (90733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e4dfc7f492836cce5f36a3a8e3941b8d6619c004fb9fb3e8a3df42c8c567950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1911b218b44e62288fb317f239ec58d54680252b6ad5b7b84abdeee0eff2adaf`

```dockerfile
```

-	Layers:
	-	`sha256:b35285063f63c97ca1e2f1b58a75539e178f06a4277ff94135e31ab43d844d97`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be65c44927642dbaf0443b5d950bdb2eba7e045ec2186605bd5528701cc1ccdc`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:d7ba43baf5310e8c3f0c94b93be9d680773a3b10f016e7ecdfc6bfd16e9b5e7c
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
$ docker pull neurodebian@sha256:73ba3061222d6c325c0a346e63bc504de41f9532e07a59209fa44e4519dcdabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61725184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5af2eace4327f02703f432d25d547b430da3ef4030f8154d0d4dd1322459e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f0c0878f24a22f4bae1cce2bb33ade2528e750968c7f19e4683f865ecf624f`  
		Last Modified: Fri, 08 May 2026 19:45:28 GMT  
		Size: 11.6 MB (11625846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83aff980bc85ff5b2ce155faf54e6e3fbf0412fad6b9b461726d7a94f49ec8b`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1690741b56c00af9a9e027b2f45da2d3c964439f6016d2a01ae49e540c9a138`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403996057114e2cd0d36ee941960ee517faaab068e8e0cbc9de09e96c9223a56`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 89.7 KB (89717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ab1c10a7c00e20030be43916af676fbd69ea524a13a3d1f1100bc9cad07f30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df6d819178bee19b394bd34bd99b9a33ff2d758ed51a85705d80ba78362451f`

```dockerfile
```

-	Layers:
	-	`sha256:2890089b6f33dd50ea7d84ff7f43fd03e40b52a12e2925bb4cd5456bc7dd9b0a`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 3.6 MB (3554180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27aea920f78950a42d40670e7327c30443ef99b9d23d92570dbbee1e83f95701`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:244ceb264bcf03306877999321ceb7e02989a73bf95ae57d5ee85e72e1028e30
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
$ docker pull neurodebian@sha256:fdfa585524dbca77dc88c79d28594b439056998a1873b0734100d0fbfcc4983a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61725576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e746d8a97559c27eb06570b8eb5bf7fd0656d5f75194b377aaefd9ce7fea3f94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60950ea8f81eeb40f4ffd4c9eb5344310a3d3b4a3ba10d8636c3e11c143743a`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 11.6 MB (11625857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e999e91d392ae0fef15aeed6175ba39d08817b5593d30f26ef16d1565d28f379`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b208859bef58c08283e7c0113598e89b5851cffe3ad75ec5cbe4f8826bba0007`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec1337df25fa89a088252f15b64bba7bf8f37501ac5944f7352dd621c52673`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 89.7 KB (89684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354222966e2e2c36cd8e4d1a765f5ce435c85024a44468f4c76ad662da8dbe34`  
		Last Modified: Fri, 08 May 2026 19:45:42 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:efdcb503bdb440864d0bfd5fcf11ce13a5bcd3ca870806e08019df74f241815d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77f0b27c9a0833de49273eb014ec6b6900a97b4265c8339e9c8422a12a57f18`

```dockerfile
```

-	Layers:
	-	`sha256:d3ca879e53a051396232cc6749a325b48a90a77b314898d6642ff4a75b84707d`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 3.6 MB (3554216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99bf0aae2c3093143415998f808232246df063b6a5a9ac0bd9e4a9bd97ff539e`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:a10175f8577ebd2900474594b994ed98951c30adad108f30a1372408d8401189
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
$ docker pull neurodebian@sha256:8008767bb706f4c4cb709ab5f06a757d417059201885cf55e86abcb4cb6dcef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66311198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2c192eae3260d4134a76b7bfbe15ddfec137154687d3fa42db1128cb0fe0a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e381fa04b31e7bcb9cbbc40e4bf2902f0c275db7edc7b0462ee8936db48315`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 11.5 MB (11502397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ab2eed64c3b37a86ab0b509b8f661cecbf7b66e171eaec9e5c546fa3036762`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134a997cd26a4c569d5d64a9da26466d3c5c487619a3e32f1c97969f13fa616a`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3596ad0c31ef351fa9a9305382ce6d40415c6c0b91c7298614f295de6c8582`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 101.3 KB (101301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:42f660d3785330ad3907a27b2a3014a5478c77cb6a2ae7174a586851e2a97d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f329d1467811d726f323694ba1065308a4220276c10e46100ba962ecb9c53f90`

```dockerfile
```

-	Layers:
	-	`sha256:a6c78a26c8ba94bd4d662a5f8aa1daccf0739185d688ddd88ead6c3050508785`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad96a7377786062bdd01bea8d0bb1ed027db71956b280c297a74b774fa1ab0db`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:a62913443fbbad4e4a78ff2a26bafca2715a51d6cf73e121a760add480a6be6f
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
$ docker pull neurodebian@sha256:ded0c9f44bfebe4345080e2a4390c3b4fed39780d1353b24e811e6661fba9ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66311558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a59c5ac3b1631f24b5bc8d5baae5bb53973e1d0f372a2f088c0314105f17e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9627add8f31e74417d79a305014794f3cbdfc718e75672d32ef679cae4d543`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 11.5 MB (11502376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fbbd060166db850453937acb417b1629ded3d89e8f175047d313eb4d4ea249`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bda2e809eea5007777365a49ca07551a25dead0adc7cab0981a605143ef59a`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f25d850d54a1638e683ef541be2effa3bca6c0b42442affc13c0b580347563f`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fad3e9fd8287dfd51f1b9399e6918557a0ab780529cfb43d95f377c5871ffc`  
		Last Modified: Fri, 08 May 2026 19:44:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:84d520f83be769fc2d681e70788d29039c5cde27701f289c18e4bab929ce8d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24962661fd033444e442b5d8f8a4cce6aa12e5693c6953d7f1bff736b34e166d`

```dockerfile
```

-	Layers:
	-	`sha256:423513329c10f41f709cff6f55c81130aebb09ea250c3f3d837102c1163b7fbc`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4f37060f92539dd9a20f74d6de85a1f15bebe90d992329da9927373d4af4e8`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:356231256775a4b0d3316fe01e22251f9309722d6efc0706ccac533eaaae79ba
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
$ docker pull neurodebian@sha256:4db04057176b65f60447ea0de14d71e589435efc93f5f9e0942650cbc343e201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d0d6bea08068fbb0f25ca7e55202dd93371d5e2f960b095b57d73b56802257`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb9739c6b4f68bc7ceda360ba82976ffea2a2b0f910162f3baaddf10c30baaf`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 11.7 MB (11693065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d4aa3bbcd7f103db531b544aa469fc669490bf0f63070fb63340476b4b2ff6`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f5291b6f5da64f52099bfd741111dd36b90a2fef3af20ec6d5cc367da8d4bb`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaea8274562ed42a6906cd9cd33a459780630e229f388af5b5627ab5ae06b749`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 93.4 KB (93437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e167ffe5ba168b8cc58cf782364dda325b14826d22b80241ce109a8f1f87cfd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c80c7632358c017feeb7106b43d3f8a70130d34fb57220e3a95f07cf348c3e8`

```dockerfile
```

-	Layers:
	-	`sha256:f6175cf9e3596d080ca37a17bf2e4e4756b45b06df58d192cd2d34c654ec1021`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e857221844e8f6652439e116a12b9371a11d1e340573ecc8b292cf063c8552`  
		Last Modified: Fri, 08 May 2026 19:44:44 GMT  
		Size: 13.9 KB (13935 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:3829cdccee4364db4c1959cfb67208062e1e9895a0f70d970201e3bf3f914b8c
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
$ docker pull neurodebian@sha256:7bc7df072b8d4192da532d04d6fead4b1e24bc92dc244d3039bd8a47c37f53fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3f5e69332c4e42d45a5f556b5626d9a922ed8e3e5702c07d3e8270f7a02cd7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fd686c2be4701aa5e99504e0a0a231438cebab31803f9703d4f2817fcfaf3c`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 11.7 MB (11693032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c275dff193370be94cf6b05afcd2f50b992d61b429151ede147e0d16bd143`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed34c26dacdd7f022ad39094d3a0e7234c0e1adaf272d36639f4a548d0bb34a`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eed24d41000306ac52cbf2623e08455d064489dded03b85fd01bce6bd72a7c0`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 93.4 KB (93421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c476f9525210c69f52698c6764a1dd93f0e3c72cb3941432ffad0b4dfe7ee5f`  
		Last Modified: Fri, 08 May 2026 19:44:53 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8707a48f987ea14bd078ac3746d28881d4119f0480d7627964a7d15c52545760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db7f5ae92125a30eea36bb373c2d4ef882b6f6936fbc0adf910cfc3e2feec4c`

```dockerfile
```

-	Layers:
	-	`sha256:f5e53c43561d0cbbbb39a871b900ba903431c52a26c9b7b5d743b6635d3bfdc9`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f6d2384fe0ae77451cec1bc567fb85d31e77c7b721f8bf337871e4e30ebdf90`  
		Last Modified: Fri, 08 May 2026 19:44:52 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:3602890299b829a6c3d93bd6aedf212cd74262599093b249c2287b5c6bb5cca0
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
$ docker pull neurodebian@sha256:674b7f113ab98f457c90a5407cf9fce5d326c1ada9d335c3bb736dac15df1d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd893df613b6c8c15a740d7cf4906096d1c477af22aea43f2c1a7965c5c10b95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918b15ce42e2f43331d7ca8a6909c2f318788178997f3be2a6c20d15686eae08`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 10.5 MB (10467078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d8c3e17a2f821d9a1e4a647dd71fd281974066ed12286ff5344c3c70918add`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745c310d83150426f135a032fe18cc82a8e5631e02d97a07354f8c9341131d6`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d13836b8f7a1419799c27ce5e5586655df8273d6004aaa0c492b5a99f6622d`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 90.7 KB (90733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e4dfc7f492836cce5f36a3a8e3941b8d6619c004fb9fb3e8a3df42c8c567950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1911b218b44e62288fb317f239ec58d54680252b6ad5b7b84abdeee0eff2adaf`

```dockerfile
```

-	Layers:
	-	`sha256:b35285063f63c97ca1e2f1b58a75539e178f06a4277ff94135e31ab43d844d97`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be65c44927642dbaf0443b5d950bdb2eba7e045ec2186605bd5528701cc1ccdc`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:08712eeb02ae3887d1f25109551263d3b401486dc0a77287955a6447b4becc0d
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
$ docker pull neurodebian@sha256:b75946ef52c181c76c2e00440d05d0622edfe6da94570e49ddae38ea079dd3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b263265c43778c4c1b4e8f75212dc86f2c4bef41fbb14feea9119600cafa0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4a335a9da7e3093e947b7d57025190b5739906b8bd558a221a15ddf6aa9ee1`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 10.5 MB (10467127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b54ccf8ac71030c118f8ef845986b5523b82fed115f87119415e7d8cc6a7e8`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfaab1b9dbef7720bd0084cf9e3eb661688ece913432774491e5c8964364e34`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a31952666a61c2db472bc221ef5ccc404ecc5d08cea8a1059c7cc6d24e1f2e`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 90.7 KB (90749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a9d9d9e1e36df62b6a57b49fb8a76a463da0ead6d8b53ad51fe669976c35f`  
		Last Modified: Fri, 08 May 2026 19:45:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2acad64ea16cc709a06d2a5aee32e9877e05ebb94c5c760a32e21c3e45deac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a59f41855cbbd51dc2e3c593cbaa8adf474717a361518cb3ebb5186e2b4760`

```dockerfile
```

-	Layers:
	-	`sha256:0d1f3edb3bc163776717dfd578079bce618888a806181425e93980efaaffe421`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cb1f47cd785673497359532ec8428f026e1c4021584f5b6423cb001e8a911c`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:d5f6096a6a003f533e7c844997c6efa784cd8ab50e379117584c0895316a05a6
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
$ docker pull neurodebian@sha256:229b368a6b98d7ce660433a55e8b2363a19a2f808ab9c873f24b05b1a8a7be84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61605870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075291128ef3150dc12f76a862c4d327c51305f9d2d92705a276cef92e88d3be`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:45:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37fd7fd52239cf41c1513003560316f753d3b29bffb106c1c8cbf260e58621e`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 11.6 MB (11589003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b51446d80054a5f43c4ce780e4dc27dd69be5690c5515991223b5af7a9fdb9`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39c1cdcded0b2bce400d9caac28b0b5ddc7273cc5e5c057393fdcebbb9055d5`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3edebb8be1094d35833e792183bac8d8b69a4cce9b1de1627b384fde68c22b`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 89.7 KB (89744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7585901b3fcd61be98cc07c0fce812830eeccbd9bbbc4c73075927b5a94c6ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b2de58ad6d4212e7b4a3044a392c77b1cb7b570cafeb9b7a95c08097b9b83`

```dockerfile
```

-	Layers:
	-	`sha256:a5e656a37608c6c496bbc4e3f21f2e6ebdd0ca00774a6b5e42196d97aca1ff25`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 3.6 MB (3554190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac42095d0498fb668d35a1880cc1400381b34697805a03ea4a3cef3243668e26`  
		Last Modified: Fri, 08 May 2026 19:45:13 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:0dc2f773daa7d22adba6aa7de74836388e88697d6fe3a215830b29a8913137bc
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
$ docker pull neurodebian@sha256:03a1a328bfee5ff0a2bcd6a694bf094d95381b9b663a843aa2e3ae99924b758c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61606220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c3c7ade491f697623eaf25c70f50f5a71cfb7bb1d3153121edb8caadc6b964`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:45:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a99493d96d6f92ea6d88890fe995d3918a05c9baec0b84c6e9d10b95007a82`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 11.6 MB (11588918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a0c33e147fa59d9124cbf1b02679d5996d94f20e43a0b0dcc7bac0c76d9bae`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d6a895ebfb8de9b1aba761e3f5032daf08032da3fa41c4770fb7be187e4cf0`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d22eba06c949e34b02517b4968779ffafdb8e6ce52c51cf497c682389b154`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 89.7 KB (89726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2616c3f976bfa74ec623fc4792a7910f4ad8177ed3b117a8e270087f0510a539`  
		Last Modified: Fri, 08 May 2026 19:45:21 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c75c21cbb9fff8f22041a53794d1631c30d371e24e4a25d431e1c649eb7fa77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7075d85a25976a8e3bcacbf0a99c3a51ddb29e013c5b42c7da1a973f852c1ea0`

```dockerfile
```

-	Layers:
	-	`sha256:7ca33354efa5a678e18c52598a002e0f989c7bb096e45147472c2b5788c43e45`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 3.6 MB (3554226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53d2a0a43649d8f679119161461ce4dc60d130a0faefe0533fc5173dbdb17353`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
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
$ docker pull neurodebian@sha256:c9591f4172a58016cea53f10633f28c9a67eb0c4fbab204e98458063173e7e36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:1518613179d554ee395421eeb519425512ab078a24ce559713b4606e857cba74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33404826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc43d80b9e552ae205bf50ff50f0113b430ede2c359ed52f3a0d2327df2f493d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91080953c2acbc96d10fe4828cad1bc2ab4c82db5ad02792fb933f2f13d70499`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 3.6 MB (3564544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1da89c7f3acd4423e93a16abf1489589f3fbdfcdfab0b54df625457971fef8b`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650122efd7cf995263806f1fe9121463a523a5bbf31f21d00c0ba81d6d9fa7f8`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ce33ae3d4d5119b02d4348559779a6077a6bb3619b38275c043e5ca34fb175`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 104.4 KB (104395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c64c241bf3bcb286d2669479231d7b5953479c2b33e5e0317e711e845b82beea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43acc54ca15fdaab04e44258b4027e15d888095aaf22666a598513e7f21a7aad`

```dockerfile
```

-	Layers:
	-	`sha256:aef0071be2d264eb5d2f4b705a5ea4f2c3c964edb559665e113daee604652134`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 2.1 MB (2120889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e55928452738f82644f08e8558fc8b565f25553a9a422a68775fd846c39d6fb`  
		Last Modified: Wed, 15 Apr 2026 20:46:20 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0dbeaa0754ba2cdcb516d4e39a6416bdf4b7da10525f24b49a61a5feff148dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32545705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7e10aaa4b0b64ac0c39126ae227a9bdbec863342e509b369c6be2f8b82be23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f12429cade407731c202b448c703c798c9843ba5b9efa8f1a25a05dc3e8431`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 3.6 MB (3561756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0b0c76a6f242383cf184fe0f4b6508ddb63d2551c1887ac7ea459225396d5e`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6ec1313b41e7c409808c452fe2ec0303a6c067f2aa660e1ae358e5c1a81a75`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9641397dcb223d6c745a891cfd688294dd62dd50c7d4cbe7a43ff6cf2263a9c4`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 105.3 KB (105254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7b321a66d15717b3b34d38d2409b7da87889dddead7ab790a2e96cbc6bb4ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c3f02ab98fb8ba900768139bc6cce9d405d08fd7c739b9500102dee1c52ed6`

```dockerfile
```

-	Layers:
	-	`sha256:1a33387cf012fc9bb15766ae8a05b79ea4d5bfad8dde9f4fa45bf81a7fe88da2`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 2.1 MB (2121934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:697097c5075451332b4cba4f90f0e91bdbd2283eaf06a606e58e535bbcacbdba`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:bda267ffb25655b138791cdc439402237cdd57fc240dbd1ba48fa2175c635fa3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:753f04dda59b30f6d474a02368db6d4f6a878af353dd81f4e2d07514311453f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33405189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a23d22a82f9e7a0e1b7fca068649af2b195d7bc4a3444159e8f9ee151c4ffc7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a614a601681e659d79f5c69f0390c48a36c84a64b92bb8e53e4358eeb0bb3eeb`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 3.6 MB (3564486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa5d8582b88e334628969d6d48b2099e0a7a8bb3d62fc00fdabf16f034233a5`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d2ac74681d70d35cdcf2431d8762c164f671eec996d2a3dafa98689ac83823`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f39a48763b024b1a23e5214e867803863840d93086632a2fb92ac045daaf4dd`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 104.4 KB (104383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa07982c3e5c85c7afbd286cd46af0d532c819440627f7583bbf701ca623087`  
		Last Modified: Wed, 15 Apr 2026 20:46:29 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:72aaef1b785221a079ce03cca78c0bd381d9afb9199b21a165a243f2d21eef9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee8d96813bdf0095b63b0700d9b6a14bb56b946b99f400d0dd3d55a92d9cb06`

```dockerfile
```

-	Layers:
	-	`sha256:d47849cd84c0097cb2a3418c558e81a77037bd392916aa7c14f7fe2ca4574547`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 2.1 MB (2120925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:511bee88869cc2d89ef9c1b421317dc586f9dca84881109cfa34b8979f0fb982`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:291bc47a26a7b51a80ea7ed02233b7699565c12c6d20a912a40e8d58045ded22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0877cf08816abcc870642ed5dc27b24bef2d18dbeb76c5ac2c324300f72d89aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:45 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20e0ca3ac0fbfe1bdd4cec3f984ada36b78041af894097406a8b6c45a300d6`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 3.6 MB (3561763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75275b141d7d2666df1d5d74b6716f343b5860db710efdef969380b54e00e2dd`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e077fd96e28046b9bc25a82b6c9cdb92cc2748fa320d3329753b6ea1c8322d3`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6172f876e47872566aea14fe5035b707fa576624cc97fec495aee863f822843d`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 105.3 KB (105269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30abc1f01381670ec2eed5998a62313532731d3c41ca4dd6f1b1549c601e9804`  
		Last Modified: Wed, 15 Apr 2026 20:46:53 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4ff95d846cfe672fc8b83392edc13971714f0f54564c81d9c64760f31e9bf250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26251360511a41e7a9968f92c92dbf251012bede7d3744b70d46ad83d4e98f7c`

```dockerfile
```

-	Layers:
	-	`sha256:0f315ba6b52f9fc12490c58464febe57a58d57d017ce508d206b02e88fff432a`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 2.1 MB (2121970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5b7e6de6c91d5088ba7363653354f5f14eb64acabd62b1ba1eda4cf8c9fae44`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:c9591f4172a58016cea53f10633f28c9a67eb0c4fbab204e98458063173e7e36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:1518613179d554ee395421eeb519425512ab078a24ce559713b4606e857cba74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33404826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc43d80b9e552ae205bf50ff50f0113b430ede2c359ed52f3a0d2327df2f493d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91080953c2acbc96d10fe4828cad1bc2ab4c82db5ad02792fb933f2f13d70499`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 3.6 MB (3564544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1da89c7f3acd4423e93a16abf1489589f3fbdfcdfab0b54df625457971fef8b`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650122efd7cf995263806f1fe9121463a523a5bbf31f21d00c0ba81d6d9fa7f8`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ce33ae3d4d5119b02d4348559779a6077a6bb3619b38275c043e5ca34fb175`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 104.4 KB (104395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c64c241bf3bcb286d2669479231d7b5953479c2b33e5e0317e711e845b82beea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43acc54ca15fdaab04e44258b4027e15d888095aaf22666a598513e7f21a7aad`

```dockerfile
```

-	Layers:
	-	`sha256:aef0071be2d264eb5d2f4b705a5ea4f2c3c964edb559665e113daee604652134`  
		Last Modified: Wed, 15 Apr 2026 20:46:21 GMT  
		Size: 2.1 MB (2120889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e55928452738f82644f08e8558fc8b565f25553a9a422a68775fd846c39d6fb`  
		Last Modified: Wed, 15 Apr 2026 20:46:20 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0dbeaa0754ba2cdcb516d4e39a6416bdf4b7da10525f24b49a61a5feff148dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32545705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7e10aaa4b0b64ac0c39126ae227a9bdbec863342e509b369c6be2f8b82be23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f12429cade407731c202b448c703c798c9843ba5b9efa8f1a25a05dc3e8431`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 3.6 MB (3561756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0b0c76a6f242383cf184fe0f4b6508ddb63d2551c1887ac7ea459225396d5e`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6ec1313b41e7c409808c452fe2ec0303a6c067f2aa660e1ae358e5c1a81a75`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9641397dcb223d6c745a891cfd688294dd62dd50c7d4cbe7a43ff6cf2263a9c4`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 105.3 KB (105254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7b321a66d15717b3b34d38d2409b7da87889dddead7ab790a2e96cbc6bb4ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c3f02ab98fb8ba900768139bc6cce9d405d08fd7c739b9500102dee1c52ed6`

```dockerfile
```

-	Layers:
	-	`sha256:1a33387cf012fc9bb15766ae8a05b79ea4d5bfad8dde9f4fa45bf81a7fe88da2`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 2.1 MB (2121934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:697097c5075451332b4cba4f90f0e91bdbd2283eaf06a606e58e535bbcacbdba`  
		Last Modified: Wed, 15 Apr 2026 20:46:35 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:bda267ffb25655b138791cdc439402237cdd57fc240dbd1ba48fa2175c635fa3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:753f04dda59b30f6d474a02368db6d4f6a878af353dd81f4e2d07514311453f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33405189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a23d22a82f9e7a0e1b7fca068649af2b195d7bc4a3444159e8f9ee151c4ffc7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a614a601681e659d79f5c69f0390c48a36c84a64b92bb8e53e4358eeb0bb3eeb`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 3.6 MB (3564486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa5d8582b88e334628969d6d48b2099e0a7a8bb3d62fc00fdabf16f034233a5`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d2ac74681d70d35cdcf2431d8762c164f671eec996d2a3dafa98689ac83823`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f39a48763b024b1a23e5214e867803863840d93086632a2fb92ac045daaf4dd`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 104.4 KB (104383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa07982c3e5c85c7afbd286cd46af0d532c819440627f7583bbf701ca623087`  
		Last Modified: Wed, 15 Apr 2026 20:46:29 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:72aaef1b785221a079ce03cca78c0bd381d9afb9199b21a165a243f2d21eef9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee8d96813bdf0095b63b0700d9b6a14bb56b946b99f400d0dd3d55a92d9cb06`

```dockerfile
```

-	Layers:
	-	`sha256:d47849cd84c0097cb2a3418c558e81a77037bd392916aa7c14f7fe2ca4574547`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 2.1 MB (2120925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:511bee88869cc2d89ef9c1b421317dc586f9dca84881109cfa34b8979f0fb982`  
		Last Modified: Wed, 15 Apr 2026 20:46:28 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:291bc47a26a7b51a80ea7ed02233b7699565c12c6d20a912a40e8d58045ded22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0877cf08816abcc870642ed5dc27b24bef2d18dbeb76c5ac2c324300f72d89aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:36 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:45 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20e0ca3ac0fbfe1bdd4cec3f984ada36b78041af894097406a8b6c45a300d6`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 3.6 MB (3561763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75275b141d7d2666df1d5d74b6716f343b5860db710efdef969380b54e00e2dd`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e077fd96e28046b9bc25a82b6c9cdb92cc2748fa320d3329753b6ea1c8322d3`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6172f876e47872566aea14fe5035b707fa576624cc97fec495aee863f822843d`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 105.3 KB (105269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30abc1f01381670ec2eed5998a62313532731d3c41ca4dd6f1b1549c601e9804`  
		Last Modified: Wed, 15 Apr 2026 20:46:53 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4ff95d846cfe672fc8b83392edc13971714f0f54564c81d9c64760f31e9bf250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26251360511a41e7a9968f92c92dbf251012bede7d3744b70d46ad83d4e98f7c`

```dockerfile
```

-	Layers:
	-	`sha256:0f315ba6b52f9fc12490c58464febe57a58d57d017ce508d206b02e88fff432a`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 2.1 MB (2121970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5b7e6de6c91d5088ba7363653354f5f14eb64acabd62b1ba1eda4cf8c9fae44`  
		Last Modified: Wed, 15 Apr 2026 20:46:52 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:08712eeb02ae3887d1f25109551263d3b401486dc0a77287955a6447b4becc0d
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
$ docker pull neurodebian@sha256:b75946ef52c181c76c2e00440d05d0622edfe6da94570e49ddae38ea079dd3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b263265c43778c4c1b4e8f75212dc86f2c4bef41fbb14feea9119600cafa0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4a335a9da7e3093e947b7d57025190b5739906b8bd558a221a15ddf6aa9ee1`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 10.5 MB (10467127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b54ccf8ac71030c118f8ef845986b5523b82fed115f87119415e7d8cc6a7e8`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfaab1b9dbef7720bd0084cf9e3eb661688ece913432774491e5c8964364e34`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a31952666a61c2db472bc221ef5ccc404ecc5d08cea8a1059c7cc6d24e1f2e`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 90.7 KB (90749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a9d9d9e1e36df62b6a57b49fb8a76a463da0ead6d8b53ad51fe669976c35f`  
		Last Modified: Fri, 08 May 2026 19:45:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2acad64ea16cc709a06d2a5aee32e9877e05ebb94c5c760a32e21c3e45deac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a59f41855cbbd51dc2e3c593cbaa8adf474717a361518cb3ebb5186e2b4760`

```dockerfile
```

-	Layers:
	-	`sha256:0d1f3edb3bc163776717dfd578079bce618888a806181425e93980efaaffe421`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cb1f47cd785673497359532ec8428f026e1c4021584f5b6423cb001e8a911c`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:d7ba43baf5310e8c3f0c94b93be9d680773a3b10f016e7ecdfc6bfd16e9b5e7c
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
$ docker pull neurodebian@sha256:73ba3061222d6c325c0a346e63bc504de41f9532e07a59209fa44e4519dcdabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61725184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5af2eace4327f02703f432d25d547b430da3ef4030f8154d0d4dd1322459e3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:15 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f0c0878f24a22f4bae1cce2bb33ade2528e750968c7f19e4683f865ecf624f`  
		Last Modified: Fri, 08 May 2026 19:45:28 GMT  
		Size: 11.6 MB (11625846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83aff980bc85ff5b2ce155faf54e6e3fbf0412fad6b9b461726d7a94f49ec8b`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1690741b56c00af9a9e027b2f45da2d3c964439f6016d2a01ae49e540c9a138`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403996057114e2cd0d36ee941960ee517faaab068e8e0cbc9de09e96c9223a56`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 89.7 KB (89717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ab1c10a7c00e20030be43916af676fbd69ea524a13a3d1f1100bc9cad07f30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df6d819178bee19b394bd34bd99b9a33ff2d758ed51a85705d80ba78362451f`

```dockerfile
```

-	Layers:
	-	`sha256:2890089b6f33dd50ea7d84ff7f43fd03e40b52a12e2925bb4cd5456bc7dd9b0a`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 3.6 MB (3554180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27aea920f78950a42d40670e7327c30443ef99b9d23d92570dbbee1e83f95701`  
		Last Modified: Fri, 08 May 2026 19:45:27 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:244ceb264bcf03306877999321ceb7e02989a73bf95ae57d5ee85e72e1028e30
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
$ docker pull neurodebian@sha256:fdfa585524dbca77dc88c79d28594b439056998a1873b0734100d0fbfcc4983a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61725576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e746d8a97559c27eb06570b8eb5bf7fd0656d5f75194b377aaefd9ce7fea3f94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60950ea8f81eeb40f4ffd4c9eb5344310a3d3b4a3ba10d8636c3e11c143743a`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 11.6 MB (11625857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e999e91d392ae0fef15aeed6175ba39d08817b5593d30f26ef16d1565d28f379`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b208859bef58c08283e7c0113598e89b5851cffe3ad75ec5cbe4f8826bba0007`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec1337df25fa89a088252f15b64bba7bf8f37501ac5944f7352dd621c52673`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 89.7 KB (89684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354222966e2e2c36cd8e4d1a765f5ce435c85024a44468f4c76ad662da8dbe34`  
		Last Modified: Fri, 08 May 2026 19:45:42 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:efdcb503bdb440864d0bfd5fcf11ce13a5bcd3ca870806e08019df74f241815d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77f0b27c9a0833de49273eb014ec6b6900a97b4265c8339e9c8422a12a57f18`

```dockerfile
```

-	Layers:
	-	`sha256:d3ca879e53a051396232cc6749a325b48a90a77b314898d6642ff4a75b84707d`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 3.6 MB (3554216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99bf0aae2c3093143415998f808232246df063b6a5a9ac0bd9e4a9bd97ff539e`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:3602890299b829a6c3d93bd6aedf212cd74262599093b249c2287b5c6bb5cca0
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
$ docker pull neurodebian@sha256:674b7f113ab98f457c90a5407cf9fce5d326c1ada9d335c3bb736dac15df1d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd893df613b6c8c15a740d7cf4906096d1c477af22aea43f2c1a7965c5c10b95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:49 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918b15ce42e2f43331d7ca8a6909c2f318788178997f3be2a6c20d15686eae08`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 10.5 MB (10467078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d8c3e17a2f821d9a1e4a647dd71fd281974066ed12286ff5344c3c70918add`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745c310d83150426f135a032fe18cc82a8e5631e02d97a07354f8c9341131d6`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d13836b8f7a1419799c27ce5e5586655df8273d6004aaa0c492b5a99f6622d`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 90.7 KB (90733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e4dfc7f492836cce5f36a3a8e3941b8d6619c004fb9fb3e8a3df42c8c567950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1911b218b44e62288fb317f239ec58d54680252b6ad5b7b84abdeee0eff2adaf`

```dockerfile
```

-	Layers:
	-	`sha256:b35285063f63c97ca1e2f1b58a75539e178f06a4277ff94135e31ab43d844d97`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be65c44927642dbaf0443b5d950bdb2eba7e045ec2186605bd5528701cc1ccdc`  
		Last Modified: Fri, 08 May 2026 19:45:00 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:08712eeb02ae3887d1f25109551263d3b401486dc0a77287955a6447b4becc0d
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
$ docker pull neurodebian@sha256:b75946ef52c181c76c2e00440d05d0622edfe6da94570e49ddae38ea079dd3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b263265c43778c4c1b4e8f75212dc86f2c4bef41fbb14feea9119600cafa0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4a335a9da7e3093e947b7d57025190b5739906b8bd558a221a15ddf6aa9ee1`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 10.5 MB (10467127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b54ccf8ac71030c118f8ef845986b5523b82fed115f87119415e7d8cc6a7e8`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfaab1b9dbef7720bd0084cf9e3eb661688ece913432774491e5c8964364e34`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a31952666a61c2db472bc221ef5ccc404ecc5d08cea8a1059c7cc6d24e1f2e`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 90.7 KB (90749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a9d9d9e1e36df62b6a57b49fb8a76a463da0ead6d8b53ad51fe669976c35f`  
		Last Modified: Fri, 08 May 2026 19:45:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2acad64ea16cc709a06d2a5aee32e9877e05ebb94c5c760a32e21c3e45deac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a59f41855cbbd51dc2e3c593cbaa8adf474717a361518cb3ebb5186e2b4760`

```dockerfile
```

-	Layers:
	-	`sha256:0d1f3edb3bc163776717dfd578079bce618888a806181425e93980efaaffe421`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cb1f47cd785673497359532ec8428f026e1c4021584f5b6423cb001e8a911c`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
