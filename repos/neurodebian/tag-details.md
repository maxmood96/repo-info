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
$ docker pull neurodebian@sha256:efedb862d721302994e92fe0a819b0ac89dbd22ec9a629156ab2c19a50c9a19b
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
$ docker pull neurodebian@sha256:5a6560e98de0074d4f556e3a3d723a82ddaf0ae65f34cda741c0584e755c69fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80daaf772d06e04317a105c593b722bf4830f53083a1c3041236aa8f303df83d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc68ad6246d17dbfc153a24bae65f1a5f73ff584955429a8236e563aa3d001f`  
		Last Modified: Mon, 08 Sep 2025 22:48:31 GMT  
		Size: 11.3 MB (11269479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a1c1b4568c9392569145efa49e13b53064de29748b4330157f35fe17d3c28d`  
		Last Modified: Mon, 08 Sep 2025 21:42:51 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa576ad08b5522d438407cf741520c4be3638d6c6f66e9080164d0e470978c8e`  
		Last Modified: Mon, 08 Sep 2025 21:42:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3c1b0722585c6a8c19c079e8987ed2951983f7aed063647f1b7f7fa3133937`  
		Last Modified: Mon, 08 Sep 2025 21:42:59 GMT  
		Size: 93.3 KB (93346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:814f7556d4158f8a1e283388b3c402e0654227d8a269ee0ab181e6b21f434b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2579c266cae1e084172b034d8c94e5fcdf1519765bb54f306e76f79b625b0dea`

```dockerfile
```

-	Layers:
	-	`sha256:4eb751fc0f69002c0dfaadfa36ab65ef9b01d64364167eb630243f00f1019f08`  
		Last Modified: Mon, 08 Sep 2025 22:07:34 GMT  
		Size: 4.1 MB (4075544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1205fd63d05f019c473c467d0b5d0792d62a875286ab84731f3f8b99040391`  
		Last Modified: Mon, 08 Sep 2025 22:07:35 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:12a913f897befb556c7ceb2558fb8738adbf563ca7ff1157d4e6e11d488df2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2602e1dfb24784e0f598940a8ac2f312dc62011a39e9dc8319db551898e92b2d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d75efbe6214a9b809e0d59c23f7a209f1aa2e67a86e2e01a58b89cda3f55a1`  
		Last Modified: Tue, 09 Sep 2025 05:52:28 GMT  
		Size: 11.3 MB (11253369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d25897438383aab600d85c585491adcb45151c81c148474dddebefd2ba68c7d`  
		Last Modified: Mon, 08 Sep 2025 21:47:08 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2b740c0c23e3e3623ab3e866ec075ea7f234e756897d3331b6c4fca4f953f1`  
		Last Modified: Mon, 08 Sep 2025 21:47:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a0cf5951e988c99b15b73f59a045bac72bd5418654228ea9976b612cdf7bd`  
		Last Modified: Mon, 08 Sep 2025 21:47:15 GMT  
		Size: 93.5 KB (93483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f15610b49b8b74ba8b43e1d9748fc173946dbe38a914bbe037fe4d22b924d7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b73ae38a458f069357c6b7ed3f9700bc00f0cbcf6a69c6a334d22717cf4002`

```dockerfile
```

-	Layers:
	-	`sha256:611956d89297f28c59fc723ca0a839c4f9bc091723e81b976d5734b770fd645f`  
		Last Modified: Mon, 08 Sep 2025 22:07:40 GMT  
		Size: 4.1 MB (4075798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829bd69ec3af1019bf9ffcaca8a14d93efb865e96208722280160398adb38b64`  
		Last Modified: Mon, 08 Sep 2025 22:07:41 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:5107aba3d0890867538a1eb3f0a85eb79bd2358d74107fca2636a7c6e319deac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5499da1fa80624060b6dd313bcdec442965968b0ab251f319ad8d5ef629b34cd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5538e96bb7df1a7ef01bd7fcbf51f4cbc041246109c06cf661f7058c203851af`  
		Last Modified: Mon, 08 Sep 2025 21:12:26 GMT  
		Size: 49.5 MB (49466684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50daaf33853e9bc9be195d0d0d91eb860c20339e0307587f495f92ab4ee3eb09`  
		Last Modified: Mon, 08 Sep 2025 22:06:15 GMT  
		Size: 11.7 MB (11690113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaa2d687517972c9cfc2d08bbc8e9a2d086b3407ee8a0ca60a56ece41aa3cfb`  
		Last Modified: Mon, 08 Sep 2025 22:06:09 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194eae81f05840e1d9e73f4cc66018ae05b766dec142b1d85e9b180dafeeb2ac`  
		Last Modified: Mon, 08 Sep 2025 22:06:10 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ba20391efc1b63213570c7a46041007aef9876ef79f229b994bb3a9d040c97`  
		Last Modified: Mon, 08 Sep 2025 22:06:09 GMT  
		Size: 93.4 KB (93386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:01ea02c921f10ac49caad05945c95f548e78efd8ff5440275c344c15bb235a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80efd81b0e74c1c05e45f223537a7bd9092af273e347a4fd178455d8a9222e15`

```dockerfile
```

-	Layers:
	-	`sha256:73118df0fe0697ee892246dc709ee5f8e8a0c72cd79a3f16640e638aa9e7a3ce`  
		Last Modified: Mon, 08 Sep 2025 22:07:45 GMT  
		Size: 4.1 MB (4073507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb129146de30c7f7b4c3307bb7cac0e930a1af225a47572b94ccee9b08ffffd`  
		Last Modified: Mon, 08 Sep 2025 22:07:46 GMT  
		Size: 14.3 KB (14282 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:1d227f401b183c72194a9f4236ed8d04d43de44d1cc46f66ec8aa5b2fd4d231d
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
$ docker pull neurodebian@sha256:6f43ef7eb07bc7c20266846a1c98b55a22011567a05f2ac5eff2909071eae0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c172ba0b81dd8f89238b22511a3d5be1d5180c0258e9e889a6ecb01624a3a2cb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb3e3b92bc6482e0df10b8b95bf25efd483c108ad208a60664cf5f1d1e77be1`  
		Last Modified: Tue, 09 Sep 2025 17:33:49 GMT  
		Size: 11.3 MB (11269552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e96c4ca1ae8d9db1d4c02f9c3d0652e417622ed05ff6eb736432722662ccdb`  
		Last Modified: Mon, 08 Sep 2025 22:09:05 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4541b568aaf9f21e14e1425e4fc093a5dd0496df3829b6404b3ad6c41efbbbe3`  
		Last Modified: Mon, 08 Sep 2025 22:09:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c1b15bdadbbe93287ac427ea3a8620f5b0157a4e6b13f7635f592e3bcc2708`  
		Last Modified: Mon, 08 Sep 2025 22:09:05 GMT  
		Size: 93.4 KB (93361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c38cbf257c18774f93a43d3e807c5ccb87233a46bd639fbf19fd1391531342`  
		Last Modified: Mon, 08 Sep 2025 22:09:05 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a2a94de25facf95724b2d16ca71a72d99a2e112b2d316cd949056412564d4d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206e4e0e5813d979635e9c61374bdbc88d22a2f82bc265b156b17600d6bdbdb3`

```dockerfile
```

-	Layers:
	-	`sha256:6d1673c322c9fbb37ea05028f45c19a0ce42f508639ca61a70c7c7f98a8aa319`  
		Last Modified: Mon, 08 Sep 2025 22:07:46 GMT  
		Size: 4.1 MB (4075584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae33da5884a0a82ad883b93e19d26853d993626f9c39065efe0d9f5aafc836be`  
		Last Modified: Mon, 08 Sep 2025 22:07:47 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c332ce47e958183cb410e1d6ec20b2be14015b101bbb5817ec4d0a9aa6b0cb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9a8e8b41d0f732b856635dfc148c9421fbca0429e8f76b5fa0bd31453ab413`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb34e261136388af42fa0af1335a030eea1a9f401d4dff98142f1da415eabd5`  
		Last Modified: Tue, 09 Sep 2025 06:31:19 GMT  
		Size: 11.3 MB (11253403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea36eb6d50e0170603953736681c374dc844fe3f7850016340a1d2f4918c0b5`  
		Last Modified: Mon, 08 Sep 2025 22:08:07 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29da554fa0fcd3032487aee0478d47e8a805146cb3bddd18fbad5d609038870e`  
		Last Modified: Mon, 08 Sep 2025 22:08:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2b09e8e858e4635fa19d6758bdf39314fa0cde577075e129e7e80e186328d`  
		Last Modified: Mon, 08 Sep 2025 22:08:14 GMT  
		Size: 93.5 KB (93529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99a489584be5c159eac218a7e93493c1813b822a296ce44cf81cb4637f9423c`  
		Last Modified: Mon, 08 Sep 2025 22:08:18 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cc7b844224cfc087081bd611b411d90140d4bae81280676b5dc0b13af788416a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f86f083a734b088c99b09c277fea3d8963dec528e9b2417e7bbdc58af53a0bb`

```dockerfile
```

-	Layers:
	-	`sha256:9a0d14da4341d08026ac22ce25ef56efe152434f1ed4d94d8ea0c1a31e4cc6b2`  
		Last Modified: Mon, 08 Sep 2025 22:07:53 GMT  
		Size: 4.1 MB (4075838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c09eae5cd42ea87228f8f7591823ff5cbe807f16966c782f8da6a3af8966e35`  
		Last Modified: Mon, 08 Sep 2025 22:07:54 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:180c2a286506c8d607df812e0989c88b708940bfb3792411db5953ff7a4f7a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4db251014580c0601148a94559714d6947766d1bfd4fd6fc7aaf84bd623b71`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5538e96bb7df1a7ef01bd7fcbf51f4cbc041246109c06cf661f7058c203851af`  
		Last Modified: Mon, 08 Sep 2025 21:12:26 GMT  
		Size: 49.5 MB (49466684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f1e0563153cc066df6491c74f133efcb40edc5eb0f61d987c52753414e037`  
		Last Modified: Tue, 09 Sep 2025 19:09:28 GMT  
		Size: 11.7 MB (11690127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7814d96039aa8fd6261aaf7b5cfceb3feba133e8bca1568a0cdde34995dee5`  
		Last Modified: Mon, 08 Sep 2025 22:10:19 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276fb743fd607e676358632f33e7d22590ee66cc30f7fd6cd688310b84d3a657`  
		Last Modified: Mon, 08 Sep 2025 22:10:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2275f662700e5881813db764845fb48bbf160416ae633242276ca625541288`  
		Last Modified: Mon, 08 Sep 2025 22:10:19 GMT  
		Size: 93.4 KB (93394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2763fded54c1182ff5b5f837e771c5a48137168e2870ab52ec1e17e95ba7c662`  
		Last Modified: Mon, 08 Sep 2025 22:10:19 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:db9f952b4b9884f6b15810229bc63b5376c07e0f3900c2afcc6677bc0bc1a1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d749b7a567dd87cfbc285161259edf132f25ec3dfb417384dc5dc5256253192`

```dockerfile
```

-	Layers:
	-	`sha256:1fffdd5ba041000de4d566ef98f57e8c336b242b4c13f370edd28d7d6a4abddf`  
		Last Modified: Mon, 08 Sep 2025 22:07:59 GMT  
		Size: 4.1 MB (4073547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9c49b10626993226be76089c1be657c79ca21feae895f3e4f09aeb6fc9d642b`  
		Last Modified: Mon, 08 Sep 2025 22:08:00 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:b54416add4022775bf919d0e0abfb8cbda491554ef578c39bf9888f1a020b432
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
$ docker pull neurodebian@sha256:c4ac10aca9d701399e8059fed0f3683fcc43a249e2de8dc5b703589379443d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f003052791c76388eb09d6b5230b2f0713bd5bf456e39fe782dfac5890f29a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c231b933ca832a0c36d4cba46f9eeaedb9913c09636c25ce6d261352667fd48`  
		Last Modified: Mon, 08 Sep 2025 22:08:41 GMT  
		Size: 11.1 MB (11105076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8126255966cf6421eb2f642922f88113072953d06a53c6a95a9554ad1e284a`  
		Last Modified: Mon, 08 Sep 2025 22:08:42 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b85a016ecb81303bf1897e6ad0cfeda630f5a1af5354503c89578631b3fa03`  
		Last Modified: Mon, 08 Sep 2025 22:08:45 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1241a27a0bef5b0024728b30531d8b53e115880620d30ce42d2f76d852c3131e`  
		Last Modified: Mon, 08 Sep 2025 22:08:43 GMT  
		Size: 101.2 KB (101191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c46afae86d287eebbb68e23b2c5ce3cf58dfed02b6684aa3dc2cafda66652203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60570ff774619c687eceaed5c2022dc61e11da936755ef3242c8976dfb4d0598`

```dockerfile
```

-	Layers:
	-	`sha256:5f12dcd54e3818839f5d4c3be83df30851bfc702e132dc1ae84c16cb0395686f`  
		Last Modified: Mon, 08 Sep 2025 22:07:57 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2449d04b028dbb27f28513e77cbe4bcabcf71e4df475a5698495f060244ad66a`  
		Last Modified: Mon, 08 Sep 2025 22:07:58 GMT  
		Size: 14.0 KB (14006 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:29bb6396a7006b87e56c5c87f5c04c857a5e54ec6e6961011ec053f5df297ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b43ffe30921f68be3120756251010affc5f55767fefa9a8da63cfb85de4400`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506a68e63d709b0336fb706c51de8c1e603b1df16e9106a832f21bc878fe6666`  
		Last Modified: Mon, 08 Sep 2025 22:31:46 GMT  
		Size: 11.1 MB (11106043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bed627daba504393f2bb65c69175080a0c1dc9f7406c509115b6322337161eb`  
		Last Modified: Mon, 08 Sep 2025 22:08:07 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c0025ed7021539172e67d0899d2fe7529cbe38e34d0f99b798b6ec1b481706`  
		Last Modified: Mon, 08 Sep 2025 22:08:12 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0987ec09011a460f5f4488ca2ca3556e0cdb012eb86af2a758c3d47575da2fd`  
		Last Modified: Mon, 08 Sep 2025 22:08:15 GMT  
		Size: 101.1 KB (101101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b1e65441c0eac75a1b3596f2acaf7f0938ce53da5b1bae30e13896f69bbe6737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5680c5113abf81f92497dcaafda941b87ebc91c5f2264289fd919f29be57b1`

```dockerfile
```

-	Layers:
	-	`sha256:1d4579dd6e46c7813118ac3d11b1ef7178c61a088a7281d87a5230bcbbdfa95f`  
		Last Modified: Mon, 08 Sep 2025 22:08:03 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43412f615be664f10c40a384d470f7c04a83cc84bc424ad92406d633d4ded76c`  
		Last Modified: Mon, 08 Sep 2025 22:08:04 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:78a75ac5c4abdaeddcc9badb935de5862bfeafe843761b6f43988b87c82cacfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66294140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbc2a7cf791eb151d220b70de637a2e1610c4a6ab3a9c4e841541db18f954e6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:21d761bd0e7544a956d2e6eb27c7a89e081fa93136574d1836ddae535c60eb08`  
		Last Modified: Mon, 08 Sep 2025 21:20:56 GMT  
		Size: 54.7 MB (54690513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bcf50ddb3bde9d26919d87c81b6c7c12eded5ccb729a876c587bff0eaae516`  
		Last Modified: Tue, 09 Sep 2025 19:09:30 GMT  
		Size: 11.5 MB (11500383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56087a829ba6035b7de8d716cce53bfeebcc087746bd8e66060624def844438f`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118f626190454cc7685791c8d92c61557d8fb3d2b346c7a029a46e59b4d3ceac`  
		Last Modified: Mon, 08 Sep 2025 21:42:45 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4ff78c5caba7d0b2956fc7b6fb24551cfd791cb4f72d1c24bdf1258e6dac7`  
		Last Modified: Mon, 08 Sep 2025 21:42:47 GMT  
		Size: 101.1 KB (101087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:642ba7c39761def52a2e42768d532bb203767a9c204457b70e1803c2a4dce50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00439b7b9b6d4129aeb9972240100291b69a336767320c0588fa8219227221ed`

```dockerfile
```

-	Layers:
	-	`sha256:9e3589203787d71e9205971750cdb77c5b6368f063b256a4eae0e07126e7919b`  
		Last Modified: Mon, 08 Sep 2025 22:08:09 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7df867cc8e9752de7141cff1b59624b2f6de89c16029a506650faa9d695a1e86`  
		Last Modified: Mon, 08 Sep 2025 22:08:10 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:1dbbf9289b2ad193183e1e71bda8b77bb520aaab950ca383f3aec43405230d30
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
$ docker pull neurodebian@sha256:cf2b0107b521b07c09cd8f0d6f2232804897ec219dae5b415ac6080bfc9f7bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64964208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8423ca4834782bbb52ba1b463635c0fb090f38cbc0abd2393490bfec676c2e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe7be945ca1d4ff00608253b3f95e1a361b3e1658a6d35ba756d1a822f4009e`  
		Last Modified: Tue, 09 Sep 2025 15:08:33 GMT  
		Size: 11.1 MB (11105059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4afaf61dcf2c3a3e97b00e38a7b282d6da0cc72ef7cc2b0c069c9edb48b2f4c`  
		Last Modified: Mon, 08 Sep 2025 22:18:07 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ef242a43dfaf618601ec16b63ead04fade1097d4a1400e3a0819709f23ac6e`  
		Last Modified: Mon, 08 Sep 2025 22:18:08 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017275926e0a64df9e263e6cad1313319f543330a7a3b875e3bdca01981d9c39`  
		Last Modified: Mon, 08 Sep 2025 22:18:08 GMT  
		Size: 101.2 KB (101207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3097308c522a15a9692c7e94637a73743af81f9691179dd6728fb95941d246e7`  
		Last Modified: Mon, 08 Sep 2025 22:18:08 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:31ac23e41c549e335f6b401aacf3d49586f19dbbef7ef0f3a9f26b3c0bfb26a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ece6ad3106008a1f58c0370d6affce1ce2ba875991135228a66b0e7cd3b5257`

```dockerfile
```

-	Layers:
	-	`sha256:2cef72b1b98411c7050f892cf873d0a8704e474fdc42750499dcc6a297716f9f`  
		Last Modified: Mon, 08 Sep 2025 22:08:10 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e707d602322999e0d45acb7e825baf6c17156cfe2e17ac13d3af7e1a5f0e70b9`  
		Last Modified: Mon, 08 Sep 2025 22:08:11 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:49cdd86d6094082e5c0b91aed3d41708edd31b2f433d55c9c6dcc85b20f4fb0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63458023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479a5df7e493af38146eda3102fb71be7d6f336ee13b7a15319bd570ad7d152d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c495a26a9e4cd1f21f84bf5b3c134dc31e3169cdbb2ae21932a376b84c9af`  
		Last Modified: Tue, 09 Sep 2025 06:33:37 GMT  
		Size: 11.1 MB (11106011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdd0b9d570ec2b080e33923af86d5f54c70cda76ed17161bd32a317ed00cd83`  
		Last Modified: Mon, 08 Sep 2025 21:47:08 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b48960bf6dc0d4e10f5e03f55c3a95296532ac622dd51e994e008d06ad396`  
		Last Modified: Mon, 08 Sep 2025 21:47:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4857e517b1c8570a0d32ff53cff06abe67744f65132d9a630d0987ba3304287`  
		Last Modified: Mon, 08 Sep 2025 21:47:14 GMT  
		Size: 101.1 KB (101096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa383623dc759a311dd6aba320a62daa8abb69707532e9c8b8e2a7e5662d218b`  
		Last Modified: Mon, 08 Sep 2025 21:47:18 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef64147d2a71637e0a769c0c5583af824cba73f5b6feeee0e9a80923f21b4773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8f10e5af3373299468ebbaec3cf5b3518e41b9837db3de6f26ff00a11ef918`

```dockerfile
```

-	Layers:
	-	`sha256:585ea56eeb16979083d627ff907af00959a6ed709cf48ed9de0abfc20e515c78`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2584dc1bbcd66f1c97c5f0904ab94a886650d24d982a46ae6812c2e864a74946`  
		Last Modified: Mon, 08 Sep 2025 22:08:17 GMT  
		Size: 16.2 KB (16176 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ddb755225316d7a69b8bc3acb2fedaecd3861d4825ac4d6c4862457b09d669db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66294566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb563c59380e9008e2f93777c0233483f18f305f619485af36185763ce0dbaf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:21d761bd0e7544a956d2e6eb27c7a89e081fa93136574d1836ddae535c60eb08`  
		Last Modified: Mon, 08 Sep 2025 21:20:56 GMT  
		Size: 54.7 MB (54690513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab465fb146f682b3fd2334e192eb2fc7aad496a892f0eb0dd9481bb125638c0`  
		Last Modified: Mon, 08 Sep 2025 21:24:42 GMT  
		Size: 11.5 MB (11500427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927362fdf6d12722a8bb46023cbc12a3e6f987226957520bba9358d757c2af88`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8bb597efc90f77d80af6e59807e850d33a80c2667cfeb714e4deb0b350b5d5`  
		Last Modified: Mon, 08 Sep 2025 21:42:46 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e274b6acee8e6b2078e44f11e044cef5f066de579c5a7c8a325e21f280ef129`  
		Last Modified: Mon, 08 Sep 2025 21:42:49 GMT  
		Size: 101.1 KB (101078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ace93800c079b0b29023ad72a5006fe9153207cc1ba4d195860c874018a5de5`  
		Last Modified: Mon, 08 Sep 2025 21:42:53 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8b131d00cfba46164d8d8c5c746045d9b01dda92efd52a4075480978e50bb7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bdf7196b07be183008280c04c2818b8346639949e2dfedd1f58e43ff245d77`

```dockerfile
```

-	Layers:
	-	`sha256:32b559285a58b98dc726e037b9352c0e4c87c94562807550c704e5b9e5309dfe`  
		Last Modified: Mon, 08 Sep 2025 22:08:21 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3056fb0e0c32ea9229dad62508be7a1ca2bbe228416168c990ba1b9f07277c`  
		Last Modified: Mon, 08 Sep 2025 22:08:22 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:c21c580fa14771b6568790b6552843482311747d0eea0fc8320281aeba3f110a
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
$ docker pull neurodebian@sha256:3db03e36a763b7633f46e2ca0db8208918182df6a443e43a1fd7485adfafff44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60031509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6125f2a10160e058dad34118c4a742d0f66d22e9f7bfa33305f86416e2c1206c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1757289600'
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
	-	`sha256:92b4a1a651b0c3628297f7472014e3ecb5580ebbd73dd0616ae4e5d399ff0831`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 49.6 MB (49575035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3ecd164755360c7d3158ba626da720ba20606a84b73d2f5d44fdf6b1b0f314`  
		Last Modified: Tue, 23 Sep 2025 22:27:34 GMT  
		Size: 10.4 MB (10363661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2d676e3c4010bd6870c6ec83b61c40d6b9faaf8dac899dd2accebd96277744`  
		Last Modified: Tue, 23 Sep 2025 19:54:33 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e971c120691ee658f1cb90fcf0e69860b04616f58ff566c5483bbd822dc67a6`  
		Last Modified: Tue, 23 Sep 2025 19:54:39 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185b113cf0c7998249027d6906c29c817b3ddd1525f6c8ae4eb527d9c24ee4b7`  
		Last Modified: Tue, 23 Sep 2025 19:54:43 GMT  
		Size: 89.9 KB (89904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9a98acc34d53a37806d9189e385cc79d30c660ba7d5a31c681e98fcc9587c096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c01b97ef76ef859b6c54734c9d9a79cd3580f25fc4111f12d5bde3009bc8bf`

```dockerfile
```

-	Layers:
	-	`sha256:2bd7237e5bccc6d38ede79c6b4174adcdf44f31782e946a4327a8880e7d817ba`  
		Last Modified: Tue, 23 Sep 2025 22:07:24 GMT  
		Size: 3.6 MB (3609656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f351a44b3e6bb28c5af16732567a0fc31ae502d27a6a44fc7e8e5e211d4270b0`  
		Last Modified: Tue, 23 Sep 2025 22:07:24 GMT  
		Size: 14.0 KB (13975 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1884f414d7f4d42d9194552cca4f2f561cb5c831930c25069ca8dc52b51d7600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2bf448f9d640a57c8d25e475b948218b398464dae0079c10f902a6bc5e682b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1757289600'
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
	-	`sha256:43c9f83b4c0cbba0c49dce5bbb999963ed78f9198001feb88e7464916cedc070`  
		Last Modified: Mon, 08 Sep 2025 21:14:38 GMT  
		Size: 49.9 MB (49863496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b389e1eb5e3644c29fe20800e97ad88d4130d8f91f2afd0935089cb492e67d`  
		Last Modified: Tue, 23 Sep 2025 17:39:30 GMT  
		Size: 10.1 MB (10143305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcde2bbb2b8e25a5f487a9ec062838dbb061b545dc78378db54ab4fe327e022`  
		Last Modified: Tue, 23 Sep 2025 17:39:30 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedaf43c0ade1074e3f4761d8a0db8d3cc800c99518e23a233f454ba8272e3e8`  
		Last Modified: Tue, 23 Sep 2025 17:39:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322389dfacf69a954619302405610c10bf093a760bc966f8abaa9a575fc47919`  
		Last Modified: Tue, 23 Sep 2025 17:39:30 GMT  
		Size: 90.5 KB (90538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4ae4111f9fb4f8661c3112d2c2094f3af49e04a1628e6b9d5807514493edf440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183abe123d0c6b4848582b78924a88e96c0a8b2551abc83c0ed2a029c8677f86`

```dockerfile
```

-	Layers:
	-	`sha256:1c0cab0102cdf0749d41ec86eacf9634fdd3b97d0ef197c01d483a01c4ccc770`  
		Last Modified: Tue, 23 Sep 2025 19:07:24 GMT  
		Size: 3.6 MB (3611171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1aa1f7c47c6525788e4cb300f8b8deda3a356c92a5e3b51068340adbbbd84a`  
		Last Modified: Tue, 23 Sep 2025 19:07:25 GMT  
		Size: 14.1 KB (14098 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:11058c58d04f9cee09e7772e9af12753ec9cc535796c2aeb6751267eefe68aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61660217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84fcd8cf2ae8736e66857a83ef432820c3d8cc164f30bc89dce3e4196b755ea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1757289600'
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
	-	`sha256:e46ba83d4247b0505c7b4e05b89ae8056e10eb07f4e445e17e2dc44b8c60b063`  
		Last Modified: Mon, 08 Sep 2025 21:12:21 GMT  
		Size: 51.0 MB (51049810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd9f653dffb60029283947ae432468f0744bc5c41ac2cd7864462e7b6d346cd`  
		Last Modified: Tue, 23 Sep 2025 17:35:01 GMT  
		Size: 10.5 MB (10517206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032540512c217e4bf41f9f21bca693e5aabe57f0c14470ff5098b3d3612cb1c`  
		Last Modified: Tue, 23 Sep 2025 17:34:56 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08556b76c8fe9f856b650913ccc3ff442c89533583c2941baabc7b50ee94542a`  
		Last Modified: Tue, 23 Sep 2025 17:34:56 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0308513bea14133c14dc940e28140185ffcd143c9922260858228366073ae7ed`  
		Last Modified: Tue, 23 Sep 2025 17:34:56 GMT  
		Size: 90.3 KB (90291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93d806e3bbaa5ebec0e64643b1858947433f7614dfbcdfda7f015305f34fa27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76949e8a60eac27296a23b51b51583e48630e90252fb1923122ed413b37fca83`

```dockerfile
```

-	Layers:
	-	`sha256:17e4e13f8695ea16be8eb97fd0af10b9701dbe3c21ce93de22f0599eb721cc2a`  
		Last Modified: Tue, 23 Sep 2025 19:07:29 GMT  
		Size: 3.6 MB (3607616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a3465cb6ec2bb111fabb3a3472c418c2f00acfb5c99ebd3f5d89dbbd1a578c`  
		Last Modified: Tue, 23 Sep 2025 19:07:30 GMT  
		Size: 13.9 KB (13946 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:e0fbe001d3a08d53127effde6310c1ea79e1de80e6770a493f18d1c7dc6e7c86
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
$ docker pull neurodebian@sha256:5366af3f90a45684e74903e70210e4bb68b49d59276eb6931adce082b981b45e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60032010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d6887d14c2e11779df6cb0d4e30520f6e8fa717b31b551c6ce8b010c1f8540`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1757289600'
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
	-	`sha256:92b4a1a651b0c3628297f7472014e3ecb5580ebbd73dd0616ae4e5d399ff0831`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 49.6 MB (49575035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7db97dff5175af40ec6025214bb079c09ac897f5789989aff24bb46c90af7f`  
		Last Modified: Tue, 23 Sep 2025 19:50:58 GMT  
		Size: 10.4 MB (10363736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7cd68ebbe1b4bb5790baf1d4f8c57c2b1c6566d79b9243fe8d96506c3abf64`  
		Last Modified: Tue, 23 Sep 2025 19:50:54 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f5aaf1deba36ade8b00c1b1aed3ce3cba5b662b288e95fcd9767641770fda9`  
		Last Modified: Tue, 23 Sep 2025 19:50:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8d3b32d3a43489dbf76579ccbcc3d6d10c549d0d0dd14e7f8967a18fd0289e`  
		Last Modified: Tue, 23 Sep 2025 19:50:54 GMT  
		Size: 89.9 KB (89885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610f51ac5bbee14ce886acdea59761c66321ae40ad41ec1fd151a64c6cce3c6`  
		Last Modified: Tue, 23 Sep 2025 19:50:53 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3fce87b257cf771d7bc40c767e0e6d6c28b3794633c996aae20121189cb1ded3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807259444ad74f4c97676e376b584b585fab817dc8c497e10dec98d27acf9d3d`

```dockerfile
```

-	Layers:
	-	`sha256:592b60b52129e3462b375f44c2cdbdd5fd57a1374a2d7c3e79d1d2e07d19450a`  
		Last Modified: Tue, 23 Sep 2025 22:07:30 GMT  
		Size: 3.6 MB (3609692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53903836a6b295d6e68e9f43596675d6bc665dbaae112077cc8afcf758cfb22a`  
		Last Modified: Tue, 23 Sep 2025 22:07:31 GMT  
		Size: 16.0 KB (16002 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:92b039616dcf059809b62e835c2ce1fb356f4cd490c14c863ddbb4f81570d2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5695ee1268cbe16821e636a6a6de9143f516e858fba50a8746679ac8c8e02f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1757289600'
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
	-	`sha256:43c9f83b4c0cbba0c49dce5bbb999963ed78f9198001feb88e7464916cedc070`  
		Last Modified: Mon, 08 Sep 2025 21:14:38 GMT  
		Size: 49.9 MB (49863496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad7660c35dc9245a3651760544eb6d528a0717570b22435a069d38bebcd4357`  
		Last Modified: Tue, 23 Sep 2025 17:39:16 GMT  
		Size: 10.1 MB (10143297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dd4856fbbd8812c3c3b07b916f604327d04013c0b756c50d815b3737d5a3a3`  
		Last Modified: Tue, 23 Sep 2025 18:26:23 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b49b1700cbeb581584f2de01718799af245efd3c1972207bb7a4cb2cd586b`  
		Last Modified: Tue, 23 Sep 2025 18:26:24 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c05e31d8c611a15105712c9f93a7d834b93de603459f204925647c9e891abb`  
		Last Modified: Tue, 23 Sep 2025 18:26:23 GMT  
		Size: 90.5 KB (90542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b573a07e48b33f323dac37694b9a4a2ac7a9be42a1d64ffe538334c6725ecb`  
		Last Modified: Tue, 23 Sep 2025 18:26:22 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dc967d49f585f0360b55969f2a013216fab797309dfe973f1d413f39b39e2119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd6eb2694ece8d67925bc06c1ac0aa05f71d39d9a1852f52a881473f433cf61`

```dockerfile
```

-	Layers:
	-	`sha256:7f44ac7080f4f07f4a92b14c9203b3500126b0a1a15a00e395e3678201cdac02`  
		Last Modified: Tue, 23 Sep 2025 19:07:31 GMT  
		Size: 3.6 MB (3611207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b186d8b4531db4698e1f2b80fe05e77d72e2ae2c9b558c2e1e3b38bd5777443`  
		Last Modified: Tue, 23 Sep 2025 19:07:32 GMT  
		Size: 16.1 KB (16142 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:715ecfa0220f7fd01738785f9c42ee3d2ac9b835a64a08b806a94b5fb6a82afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61660669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49c25b5eb4f3ce42160d048e69202a5b427df77adbe42bf1c90db6ae05bcddb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1757289600'
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
	-	`sha256:e46ba83d4247b0505c7b4e05b89ae8056e10eb07f4e445e17e2dc44b8c60b063`  
		Last Modified: Mon, 08 Sep 2025 21:12:21 GMT  
		Size: 51.0 MB (51049810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361bd0e810695bdbe9086ecda5df8904416a487bc5a0ab43e7495d3598650bcf`  
		Last Modified: Wed, 24 Sep 2025 02:15:15 GMT  
		Size: 10.5 MB (10517223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f39ed7022b30182eeeb2b6e84799ec704eb6ed39b6b25a8ae84f4484d7e0680`  
		Last Modified: Tue, 23 Sep 2025 18:22:25 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317b5fe370cd1003cd49347234721b59a8595b0d60b476ff8e76e2a2f020a38`  
		Last Modified: Tue, 23 Sep 2025 18:22:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea9c5768445e1715d5adb3c925a6337fe3629fbba9d4736c7300a995c493bd4`  
		Last Modified: Tue, 23 Sep 2025 18:22:24 GMT  
		Size: 90.3 KB (90276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45b3fdb11b8dbbc68f00e2fc25d31ea20aca0b0cbd042c8e6812b59b3619f72`  
		Last Modified: Tue, 23 Sep 2025 18:22:24 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7855e2a2d3a399325fa66efac0702ee6144d1103a4aab879ba2ef8db9a1324e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25f019bc15a42d275adef0a10d965245e5a53d609818d34d0f8947e18168294`

```dockerfile
```

-	Layers:
	-	`sha256:273801161af411b9ca75df5f2ce6622db20fa373538ba54a0c24f2c4bf746b18`  
		Last Modified: Tue, 23 Sep 2025 19:07:39 GMT  
		Size: 3.6 MB (3607652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6349aefa2276bd907a81a03bfa347913a3a681b8efd053e0e8aca34bc5e0112c`  
		Last Modified: Tue, 23 Sep 2025 19:07:40 GMT  
		Size: 16.0 KB (15972 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:975465318c2961a62e84945b66e3eb674c0cc276f3f1c79e9d775380ed7e2978
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
$ docker pull neurodebian@sha256:3d755067362f393c7585144595d3f2754010a5c721f206cd73de9f771bc93aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31072458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef546e0120c2e4950f832e3f1f63ea76331b4eddda9a60829a347bccc6d11f0`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187b0329cf2a4a15a9bf4b14570d09ca06b3b9b031182d9d673722455466dea4`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 3.6 MB (3598206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b2c6c73f48a5205154bbeefdc3a62200f2912abd347eab19218d25884b59c6`  
		Last Modified: Tue, 02 Sep 2025 02:31:43 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c6dd113705bb44b0596d44cfd3ff0395aac0b756dc8da44d1563df648bedfe`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02baa23e0d6f84b6310f25f56d9459f98c61c4ae69864e811e3f6d95714f90`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 110.6 KB (110605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:50ea19520af7ff7bb17b1c87749b89c3d943ef0cd19a831bb8d497304d58d9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322e60f23e6672fb7149c0f864f30ec442e1b554da2264f5133d991f7e647c51`

```dockerfile
```

-	Layers:
	-	`sha256:5c2043d6adc338e426d3f82ccf4134905c4a04e1d8a86411801d898cb43d5ce9`  
		Last Modified: Tue, 02 Sep 2025 04:07:27 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d1c964ae4683d90f63a5cbd6b78ef63792fd7523b7173d484e631d31afa51ba`  
		Last Modified: Tue, 02 Sep 2025 04:07:27 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:5a0fd02a955581821f5e1e61b232651e9eb3e9d8f5d112dd221a5079ab5a4655
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
$ docker pull neurodebian@sha256:16c1487ee25e15abee9aa27c20c3bc91b9fa4c99bab65e7a742963d60666def6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31072747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6792b8f84d3304ef6e28de08173b87ae23cf5b542ae198b8bd962bf5b29b4a40`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187b0329cf2a4a15a9bf4b14570d09ca06b3b9b031182d9d673722455466dea4`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 3.6 MB (3598206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b2c6c73f48a5205154bbeefdc3a62200f2912abd347eab19218d25884b59c6`  
		Last Modified: Tue, 02 Sep 2025 02:31:43 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c6dd113705bb44b0596d44cfd3ff0395aac0b756dc8da44d1563df648bedfe`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02baa23e0d6f84b6310f25f56d9459f98c61c4ae69864e811e3f6d95714f90`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 110.6 KB (110605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b579638f5ad784db8571cf092a6ef4ab30b240756a48f6c38c0e8dc718d7610d`  
		Last Modified: Tue, 02 Sep 2025 02:31:46 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cf925a26094fa612cb22d55b1e64484fb6c1683525aa871d37fd1df276896a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c790b7b9e0fe69d544874fceaebe8f92b6265deaed73d3e8ed48cec56061cf7`

```dockerfile
```

-	Layers:
	-	`sha256:b956c6cf699422639abaacca5984085ebbe4ef744fc698f2bc3ef106bba50906`  
		Last Modified: Tue, 02 Sep 2025 04:07:28 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42e7b9a80bb3eb37d02c02dc8ae979642d01e3d3644d30077268d4519deff36`  
		Last Modified: Tue, 02 Sep 2025 04:07:29 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:8e5fd833ef1fdbd0634a429ce619af13a0b3bc394a4316528e395989a2b7e559
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
$ docker pull neurodebian@sha256:b8554b98c7b61391bb22bd4a7220df7f7c62650527e0d5418399a94917423fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59662220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a057003cd756d9f5325107c7c4251c56e1861281d12bbfbe20b5a12828bd9cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed7aad3c42d8c3bcd905875cd29230e367d1c38916321ad3ab12c4fdb0d7214`  
		Last Modified: Tue, 23 Sep 2025 19:50:15 GMT  
		Size: 10.3 MB (10289604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b5a09c0af2cd1b2f3b536c610a8484aae29784608be965bc9a76f6adbaa4a2`  
		Last Modified: Tue, 23 Sep 2025 19:50:13 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f6f38bb43cac782ca903da5f508ccc0c581e9a68a8a8e69f171bdfa0c61e70`  
		Last Modified: Tue, 23 Sep 2025 19:50:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff7d4510024de4cd17cd7f0cd21f3979b98414430b20d3562fa40e36bbeec0e`  
		Last Modified: Tue, 23 Sep 2025 19:50:14 GMT  
		Size: 90.2 KB (90176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ac143161be3e17b7c8eafcd0a3d2cb85ddbbbc215ecf917aa9d531c2e6c28c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b72ef0681bd3bb94d50bac07af0c81640b7f02c0ea6f106e3115f463f5b5f6`

```dockerfile
```

-	Layers:
	-	`sha256:aa3f4c83d483d36764c0891f01c50ea9f2c8d0622d9d1b9889ab1cf350e68d9d`  
		Last Modified: Tue, 23 Sep 2025 22:07:36 GMT  
		Size: 3.6 MB (3612981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55df46487d54f44f5754ee59a2a3ad256b28ccf84ecd6f797b4af6e104aeb382`  
		Last Modified: Tue, 23 Sep 2025 22:07:37 GMT  
		Size: 14.3 KB (14293 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c21dbd0a1b16c4fb222391d8e8e637e2922cdaa24fe9ed526552317f113eec9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59810755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008b6ced829a9d58058b2cbab03447436e078b2409fe75b5b1378777ba39b2ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d54f0a8b8cdeb016765b4421672e7132d34ac6b326223b731d5282d5c3ae095`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 10.1 MB (10073260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ca08b2ff60dcd56cef5ab73acd2c160b4e06751f62df7e0e95d1bcfd11d8d6`  
		Last Modified: Tue, 23 Sep 2025 17:39:18 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e35bc05e600c15f0db597abe53e56f5133f1a07cef5ceef2dde74108818d40b`  
		Last Modified: Tue, 23 Sep 2025 17:39:18 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87503a3dead3a4605bff54bd22c67f01d31f31f6b7c17460c90ae59af2d30d76`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 90.8 KB (90839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:20da5439101ef73faac42cf32c8dacca771cdd9cdce9a342d0499874e2dfdc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000c048359af5327f48f359238ffbbbf20737b7e60535c97db620c1ebe6f0cab`

```dockerfile
```

-	Layers:
	-	`sha256:c8c473610319b2e88f677aca463db980bd056b2466974dfa73007cbbb5f01c33`  
		Last Modified: Tue, 23 Sep 2025 19:07:45 GMT  
		Size: 3.6 MB (3614508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb37a93695cd94314c8d98c7d617488ec6ee93baa6906bb6aa6804b7f9e796f`  
		Last Modified: Tue, 23 Sep 2025 19:07:46 GMT  
		Size: 14.4 KB (14431 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:557a466129fe8cd12edbf882dc0ebf898652e8b101e0138a9fce8af68ef67f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61351348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e7b84e0788bd3a7eeacb70c4ab0929b84ccf10892c9650e34e5bec7ca21199`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768b3fdcc0892aba7d97f3db5214e7a8724b3691fbe410f5aec7c9f7729c19e4`  
		Last Modified: Tue, 23 Sep 2025 17:34:19 GMT  
		Size: 10.5 MB (10462915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13e953626a5863b8c7828fd4ed69028cf735723c389479008359be4d9edd990`  
		Last Modified: Tue, 23 Sep 2025 17:34:18 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980b88e4c67b14fb8d1d73a427f8fcdf3eb95789988d2d91ec6970cc6c22bd58`  
		Last Modified: Tue, 23 Sep 2025 17:34:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3482123fd30bdde26844e46aa5360dc605124e27e13b22a8e44866fbc344d156`  
		Last Modified: Tue, 23 Sep 2025 17:34:19 GMT  
		Size: 90.6 KB (90579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3b4d14f31a3774572ceef81ad84383cb0c1ae39ebd131510cfcda15a3630d172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f3fa91eb5042a491e37386d2d34c7c933cc12376225de8f5eac7702a61a2f`

```dockerfile
```

-	Layers:
	-	`sha256:93eaec6d2f1f521fc263252d9ca16cb3a360a3af7531bb55ec9c8264df60460c`  
		Last Modified: Tue, 23 Sep 2025 19:07:51 GMT  
		Size: 3.6 MB (3610930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5f4614670f64ec9fb8c7b72d96283e5b91deb0d9f10815b2ac4881be86ae82`  
		Last Modified: Tue, 23 Sep 2025 19:07:53 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:28ed00c3b99a93843498bcdf4dbb2e106a98bd6f09cb16cb0f429c7287b5b92d
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
$ docker pull neurodebian@sha256:3a7c2310d559960aaf251bc55abe9a2ab7db5737be3afbf4fe917255a3297e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60150107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237a847b33b05b4e89235d3b6749d4840276b001e4738669e669a1a496565414`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1757289600'
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
	-	`sha256:8d64c6c7c21822ac171c4c396d70161707401d6d50d133075d661956f08dc756`  
		Last Modified: Mon, 08 Sep 2025 21:13:08 GMT  
		Size: 49.7 MB (49657990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d854924ae9b4b1288c9dfda064ea896d3981b318987c9c6ffe8efb82e63325d9`  
		Last Modified: Tue, 23 Sep 2025 19:50:14 GMT  
		Size: 10.4 MB (10399375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e96eca8e251a3599c0646fff211e1ad902995d9c8f4cdcb9aea901bbe51fc8`  
		Last Modified: Tue, 23 Sep 2025 19:50:09 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b127e8318640efb0fdf4c7d5c155014b89218f931be0840c2468e892e0fe82`  
		Last Modified: Tue, 23 Sep 2025 19:50:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f94e92357646159f3de34f7a59b35af379809eb95e8ca6cdebfc80f6bf415b5`  
		Last Modified: Tue, 23 Sep 2025 19:50:11 GMT  
		Size: 89.8 KB (89839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:db93141dbaaab047d2c5961e0f3a40a490a3bc4c02858e362684aac66d8f11cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ec5dfabfdd39f0aaf814e90273b851f03175e48b64cc6bdc82acd7e035dd64`

```dockerfile
```

-	Layers:
	-	`sha256:b3b0384cfc3d61d143a214949d2e595f859d287f885e4e4d78e634cc601b3ca2`  
		Last Modified: Tue, 23 Sep 2025 22:07:41 GMT  
		Size: 3.6 MB (3609940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15b8bd663afd20bb3f9e9dd8d1902aa8ea08259a6ff7149fc262d1757f040bfb`  
		Last Modified: Tue, 23 Sep 2025 22:07:42 GMT  
		Size: 13.9 KB (13947 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3473d74285345688dad026ef0917211d20aaac7a63891d8b253c51ac76c7f36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60205188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3780f0e6abc99ad711f80a483189a852bc2a1d2bd2d9ce913bc7f0a749388490`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1757289600'
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
	-	`sha256:00e024daab2d43f36749bffb01f2b299b405cff0659a8e4f4f00bb468dd24c27`  
		Last Modified: Mon, 08 Sep 2025 21:14:58 GMT  
		Size: 49.9 MB (49934721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67162de59cae8432f37018bdfca1926d8d40b34084a6e6ca535064ebafd11af7`  
		Last Modified: Tue, 23 Sep 2025 17:39:57 GMT  
		Size: 10.2 MB (10177061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bb81dbbd87423aed66a55483c3b6d0acb4129dabd3c0147e74c76b0addb550`  
		Last Modified: Tue, 23 Sep 2025 17:39:56 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba3ff27e7afe1dc3962ba33f3faa4fbaba125ab630cb86d1125223c943c68d6`  
		Last Modified: Tue, 23 Sep 2025 17:39:56 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03b9f2f2b5433c7d521cd2962c537a2863678d15ff9ec8e3d1f7d6a4677c1ca`  
		Last Modified: Tue, 23 Sep 2025 17:39:56 GMT  
		Size: 90.5 KB (90502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5f6b3b64165dd6cf8115298360e079d70eadbd2cb05021d0f0e61c82e695744f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631b4c7bfa49457dfcdf6c8869cf60c5f244c01f22f3bab8aca7e9c5ff4d4d68`

```dockerfile
```

-	Layers:
	-	`sha256:7d39ac1ae9919d67a330944d83252b6fba745ae3f16dce0326e07afcfb619d25`  
		Last Modified: Tue, 23 Sep 2025 19:07:54 GMT  
		Size: 3.6 MB (3611455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b646a4ca03999ebf0a0e86482bbb39a1c31c084ad7112cd593dc386c8241932f`  
		Last Modified: Tue, 23 Sep 2025 19:07:55 GMT  
		Size: 14.1 KB (14072 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:087bfe5c7fe5a858c0dad888bdae06c7aa709dd89a70dfd28b9efb1eecb2a247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61758851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9911b404ee218bf7821aafaf7618a81634351f6f5577a865753205cecbce39`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1757289600'
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
	-	`sha256:eb039ce3bcf3fbed73729096e510ae45e98c7db73d412a09aa57aaad6f2f6267`  
		Last Modified: Mon, 08 Sep 2025 21:12:53 GMT  
		Size: 51.1 MB (51113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc41e7d47140b0d1fc4152bc7af8595e60e5b75abcc8d92b17c1e4bccdc2777`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 10.6 MB (10552105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeabcf2a16d8446d9f601b7a5f0e0dcc7eec713032a5af69f0e62133b4d0a5e`  
		Last Modified: Tue, 23 Sep 2025 17:35:57 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a81e3c095adac2afeafbb59a941a25173e7979c43c100a882514bea7877cf2`  
		Last Modified: Tue, 23 Sep 2025 17:36:00 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a5f5e7ce5e4c5bd3868fbeb258a1b9acc9bf9658887f081960ec7b90b4c574`  
		Last Modified: Tue, 23 Sep 2025 17:35:57 GMT  
		Size: 90.2 KB (90230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2b4e860b4c2cf391bdc9ff71e490d986221996da51ec3a24f0cfd46a85c4480c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62dabffd47060461fc93e44830dedddbd7576c04f5afea31f63b493c1da5551`

```dockerfile
```

-	Layers:
	-	`sha256:9896fe7c4d9ef11f9576f83857d7f2ba9fdadb7b07a9a04d20d5e2e494dd447f`  
		Last Modified: Tue, 23 Sep 2025 19:08:00 GMT  
		Size: 3.6 MB (3607901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09cc604acd1809bed7d56e0d91d55d2eec5d7d859506811fc30bc2c91a6f86fc`  
		Last Modified: Tue, 23 Sep 2025 19:08:01 GMT  
		Size: 13.9 KB (13919 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:3fe7c675223c4e0405d4207e24eb1e4c3bf19ee11a9646cf0e7619d6e62779e6
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
$ docker pull neurodebian@sha256:a35aa8b45c44873f50d11bb966c016c4668451a55520ef298bfa46fa311873a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60150471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6104e8936f061faa342c4c523fdfacfac26378d45d9486da91ddae637f479695`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1757289600'
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
	-	`sha256:8d64c6c7c21822ac171c4c396d70161707401d6d50d133075d661956f08dc756`  
		Last Modified: Mon, 08 Sep 2025 21:13:08 GMT  
		Size: 49.7 MB (49657990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144fde7d694dd5ef88504ba55ce29576ef669fa6f3df0c8853397b6a3268cbbe`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 10.4 MB (10399314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbf6772f1e0545288e07cf0ceaa3f94da2fc29c74d7eb03d4bf094e99392ae5`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fba2595e2127b79c17e4ae5386fc3f5c426141156e917da1355fbb85ccf90d`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f417ad3fc8c42aac0bc4283557ce36de1dc98cdfdd91eabb26c4a7b7d3de070e`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 89.8 KB (89844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f06a1a1687a3f978541c38dcb673e5ff3361f7b879268038c9e2420127745c0`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2be98938edcce0a407fcfe2b626638987bd84491450fe88ebaec0cc09dcd1ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e0efac7157da5dd4116b8db93ba1fa1296880d93eff0a00171cf0cecee7910`

```dockerfile
```

-	Layers:
	-	`sha256:af1ba855b844937cc2f5a8faba90ea901d7c9070e32458e6762b67c378313e49`  
		Last Modified: Tue, 23 Sep 2025 22:07:46 GMT  
		Size: 3.6 MB (3609976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d04311730d3fcedc87b7d493ad4f221c9022f4283ba58e82cdcb99f34672705c`  
		Last Modified: Tue, 23 Sep 2025 22:07:47 GMT  
		Size: 16.0 KB (15974 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9191edad731c3777239ab7a6df02e8c3cca27fd39f070d3a9f2130a27b286529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60205498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed9d6ab91c97c1ce364b776c074b575641047e24efa1851b32dceb9d3e43f91`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1757289600'
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
	-	`sha256:00e024daab2d43f36749bffb01f2b299b405cff0659a8e4f4f00bb468dd24c27`  
		Last Modified: Mon, 08 Sep 2025 21:14:58 GMT  
		Size: 49.9 MB (49934721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81efd0f0dcca0cb336b828640e6827714cf6b6db92f89cd82e323f6982d7f4d`  
		Last Modified: Tue, 23 Sep 2025 17:39:59 GMT  
		Size: 10.2 MB (10176977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603959d5699befce3d731668bbda6ef5af594a431dacdcd4f999328e185fbf82`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e002eb0aadc14a90478115b718f1549b2e972b9c8b9828cfcf24af8768e48b6f`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbcb7eb4cc610f644f057f5935ee9846750de3ed5aa29b6b4626721d2881bc3`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 90.5 KB (90473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f379b3fb391ace6e8169e270dfe80ba47aa454ebabc6a261938b427e9ba848f`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:84290dc5531ab703d1ea0a46c4080e9bb469fb5ffa14f513534e950f69ab9aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b99802cb1d850e1aa7fdd8c934d54b5c43752f6d208c43ddb6954d3353ab6b5`

```dockerfile
```

-	Layers:
	-	`sha256:3e46be236b4284404936a8f6998febda1ad729b8427e99900db52dfd85f23c32`  
		Last Modified: Tue, 23 Sep 2025 19:08:01 GMT  
		Size: 3.6 MB (3611491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a6e5fd5021e1f648ebc119ba8cab091880a2c17c44168587834ec61baf52878`  
		Last Modified: Tue, 23 Sep 2025 19:08:02 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:acab89f48ba43732b4aa66549b33e99073d08cb0d8b4dda8f2068b22a2150a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61759091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed2e9dfd34d78d1208dab49205386f5cb5dac7477cf3eeffd318a45bfd13e2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1757289600'
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
	-	`sha256:eb039ce3bcf3fbed73729096e510ae45e98c7db73d412a09aa57aaad6f2f6267`  
		Last Modified: Mon, 08 Sep 2025 21:12:53 GMT  
		Size: 51.1 MB (51113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef9e924b51d56631ff7e60d9ffc923651a932453cc070c44c790dda109655cb`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 10.6 MB (10551936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a5c4260c5226a4139c1dcf60e7a5115ab5f76a7b0d9d8ab9dfba9e32017937`  
		Last Modified: Tue, 23 Sep 2025 17:35:57 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98aee0679f611ea7162c52e6ab4785f27f80c5589830cb5157d23e657c207730`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fd04207b73d5d0c0f97e7396b06c06e07035f1819525455162e75489f45e32`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 90.2 KB (90220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119bae56cac036245f6d4048fe985553edfdc542188b8fb42f75eb63b6c081c`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:72c4c16e05b5307900604596e5f718afa79b1171da6da0bbd2e78516f68dee81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4dd3ed7a3d34c1598c331733008530b70861d2d4880f6fde569b86843d3972`

```dockerfile
```

-	Layers:
	-	`sha256:74c2a34baf1ea8506bb8987565d0762224ddd979d8096a23060702450fd2d660`  
		Last Modified: Tue, 23 Sep 2025 19:08:07 GMT  
		Size: 3.6 MB (3607937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad7f63ff5b26fd7dede37a98e92c1e59e3fcab2829d49ab90c1fc8f1296a48ec`  
		Last Modified: Tue, 23 Sep 2025 19:08:07 GMT  
		Size: 15.9 KB (15944 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:b54416add4022775bf919d0e0abfb8cbda491554ef578c39bf9888f1a020b432
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
$ docker pull neurodebian@sha256:c4ac10aca9d701399e8059fed0f3683fcc43a249e2de8dc5b703589379443d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f003052791c76388eb09d6b5230b2f0713bd5bf456e39fe782dfac5890f29a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c231b933ca832a0c36d4cba46f9eeaedb9913c09636c25ce6d261352667fd48`  
		Last Modified: Mon, 08 Sep 2025 22:08:41 GMT  
		Size: 11.1 MB (11105076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8126255966cf6421eb2f642922f88113072953d06a53c6a95a9554ad1e284a`  
		Last Modified: Mon, 08 Sep 2025 22:08:42 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b85a016ecb81303bf1897e6ad0cfeda630f5a1af5354503c89578631b3fa03`  
		Last Modified: Mon, 08 Sep 2025 22:08:45 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1241a27a0bef5b0024728b30531d8b53e115880620d30ce42d2f76d852c3131e`  
		Last Modified: Mon, 08 Sep 2025 22:08:43 GMT  
		Size: 101.2 KB (101191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c46afae86d287eebbb68e23b2c5ce3cf58dfed02b6684aa3dc2cafda66652203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60570ff774619c687eceaed5c2022dc61e11da936755ef3242c8976dfb4d0598`

```dockerfile
```

-	Layers:
	-	`sha256:5f12dcd54e3818839f5d4c3be83df30851bfc702e132dc1ae84c16cb0395686f`  
		Last Modified: Mon, 08 Sep 2025 22:07:57 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2449d04b028dbb27f28513e77cbe4bcabcf71e4df475a5698495f060244ad66a`  
		Last Modified: Mon, 08 Sep 2025 22:07:58 GMT  
		Size: 14.0 KB (14006 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:29bb6396a7006b87e56c5c87f5c04c857a5e54ec6e6961011ec053f5df297ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b43ffe30921f68be3120756251010affc5f55767fefa9a8da63cfb85de4400`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506a68e63d709b0336fb706c51de8c1e603b1df16e9106a832f21bc878fe6666`  
		Last Modified: Mon, 08 Sep 2025 22:31:46 GMT  
		Size: 11.1 MB (11106043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bed627daba504393f2bb65c69175080a0c1dc9f7406c509115b6322337161eb`  
		Last Modified: Mon, 08 Sep 2025 22:08:07 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c0025ed7021539172e67d0899d2fe7529cbe38e34d0f99b798b6ec1b481706`  
		Last Modified: Mon, 08 Sep 2025 22:08:12 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0987ec09011a460f5f4488ca2ca3556e0cdb012eb86af2a758c3d47575da2fd`  
		Last Modified: Mon, 08 Sep 2025 22:08:15 GMT  
		Size: 101.1 KB (101101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b1e65441c0eac75a1b3596f2acaf7f0938ce53da5b1bae30e13896f69bbe6737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5680c5113abf81f92497dcaafda941b87ebc91c5f2264289fd919f29be57b1`

```dockerfile
```

-	Layers:
	-	`sha256:1d4579dd6e46c7813118ac3d11b1ef7178c61a088a7281d87a5230bcbbdfa95f`  
		Last Modified: Mon, 08 Sep 2025 22:08:03 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43412f615be664f10c40a384d470f7c04a83cc84bc424ad92406d633d4ded76c`  
		Last Modified: Mon, 08 Sep 2025 22:08:04 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:78a75ac5c4abdaeddcc9badb935de5862bfeafe843761b6f43988b87c82cacfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66294140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fbc2a7cf791eb151d220b70de637a2e1610c4a6ab3a9c4e841541db18f954e6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:21d761bd0e7544a956d2e6eb27c7a89e081fa93136574d1836ddae535c60eb08`  
		Last Modified: Mon, 08 Sep 2025 21:20:56 GMT  
		Size: 54.7 MB (54690513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bcf50ddb3bde9d26919d87c81b6c7c12eded5ccb729a876c587bff0eaae516`  
		Last Modified: Tue, 09 Sep 2025 19:09:30 GMT  
		Size: 11.5 MB (11500383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56087a829ba6035b7de8d716cce53bfeebcc087746bd8e66060624def844438f`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118f626190454cc7685791c8d92c61557d8fb3d2b346c7a029a46e59b4d3ceac`  
		Last Modified: Mon, 08 Sep 2025 21:42:45 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4ff78c5caba7d0b2956fc7b6fb24551cfd791cb4f72d1c24bdf1258e6dac7`  
		Last Modified: Mon, 08 Sep 2025 21:42:47 GMT  
		Size: 101.1 KB (101087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:642ba7c39761def52a2e42768d532bb203767a9c204457b70e1803c2a4dce50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00439b7b9b6d4129aeb9972240100291b69a336767320c0588fa8219227221ed`

```dockerfile
```

-	Layers:
	-	`sha256:9e3589203787d71e9205971750cdb77c5b6368f063b256a4eae0e07126e7919b`  
		Last Modified: Mon, 08 Sep 2025 22:08:09 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7df867cc8e9752de7141cff1b59624b2f6de89c16029a506650faa9d695a1e86`  
		Last Modified: Mon, 08 Sep 2025 22:08:10 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:1dbbf9289b2ad193183e1e71bda8b77bb520aaab950ca383f3aec43405230d30
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
$ docker pull neurodebian@sha256:cf2b0107b521b07c09cd8f0d6f2232804897ec219dae5b415ac6080bfc9f7bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64964208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8423ca4834782bbb52ba1b463635c0fb090f38cbc0abd2393490bfec676c2e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe7be945ca1d4ff00608253b3f95e1a361b3e1658a6d35ba756d1a822f4009e`  
		Last Modified: Tue, 09 Sep 2025 15:08:33 GMT  
		Size: 11.1 MB (11105059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4afaf61dcf2c3a3e97b00e38a7b282d6da0cc72ef7cc2b0c069c9edb48b2f4c`  
		Last Modified: Mon, 08 Sep 2025 22:18:07 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ef242a43dfaf618601ec16b63ead04fade1097d4a1400e3a0819709f23ac6e`  
		Last Modified: Mon, 08 Sep 2025 22:18:08 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017275926e0a64df9e263e6cad1313319f543330a7a3b875e3bdca01981d9c39`  
		Last Modified: Mon, 08 Sep 2025 22:18:08 GMT  
		Size: 101.2 KB (101207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3097308c522a15a9692c7e94637a73743af81f9691179dd6728fb95941d246e7`  
		Last Modified: Mon, 08 Sep 2025 22:18:08 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:31ac23e41c549e335f6b401aacf3d49586f19dbbef7ef0f3a9f26b3c0bfb26a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ece6ad3106008a1f58c0370d6affce1ce2ba875991135228a66b0e7cd3b5257`

```dockerfile
```

-	Layers:
	-	`sha256:2cef72b1b98411c7050f892cf873d0a8704e474fdc42750499dcc6a297716f9f`  
		Last Modified: Mon, 08 Sep 2025 22:08:10 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e707d602322999e0d45acb7e825baf6c17156cfe2e17ac13d3af7e1a5f0e70b9`  
		Last Modified: Mon, 08 Sep 2025 22:08:11 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:49cdd86d6094082e5c0b91aed3d41708edd31b2f433d55c9c6dcc85b20f4fb0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63458023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479a5df7e493af38146eda3102fb71be7d6f336ee13b7a15319bd570ad7d152d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c495a26a9e4cd1f21f84bf5b3c134dc31e3169cdbb2ae21932a376b84c9af`  
		Last Modified: Tue, 09 Sep 2025 06:33:37 GMT  
		Size: 11.1 MB (11106011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdd0b9d570ec2b080e33923af86d5f54c70cda76ed17161bd32a317ed00cd83`  
		Last Modified: Mon, 08 Sep 2025 21:47:08 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71b48960bf6dc0d4e10f5e03f55c3a95296532ac622dd51e994e008d06ad396`  
		Last Modified: Mon, 08 Sep 2025 21:47:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4857e517b1c8570a0d32ff53cff06abe67744f65132d9a630d0987ba3304287`  
		Last Modified: Mon, 08 Sep 2025 21:47:14 GMT  
		Size: 101.1 KB (101096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa383623dc759a311dd6aba320a62daa8abb69707532e9c8b8e2a7e5662d218b`  
		Last Modified: Mon, 08 Sep 2025 21:47:18 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef64147d2a71637e0a769c0c5583af824cba73f5b6feeee0e9a80923f21b4773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8f10e5af3373299468ebbaec3cf5b3518e41b9837db3de6f26ff00a11ef918`

```dockerfile
```

-	Layers:
	-	`sha256:585ea56eeb16979083d627ff907af00959a6ed709cf48ed9de0abfc20e515c78`  
		Last Modified: Mon, 08 Sep 2025 22:08:16 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2584dc1bbcd66f1c97c5f0904ab94a886650d24d982a46ae6812c2e864a74946`  
		Last Modified: Mon, 08 Sep 2025 22:08:17 GMT  
		Size: 16.2 KB (16176 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ddb755225316d7a69b8bc3acb2fedaecd3861d4825ac4d6c4862457b09d669db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66294566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb563c59380e9008e2f93777c0233483f18f305f619485af36185763ce0dbaf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:21d761bd0e7544a956d2e6eb27c7a89e081fa93136574d1836ddae535c60eb08`  
		Last Modified: Mon, 08 Sep 2025 21:20:56 GMT  
		Size: 54.7 MB (54690513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab465fb146f682b3fd2334e192eb2fc7aad496a892f0eb0dd9481bb125638c0`  
		Last Modified: Mon, 08 Sep 2025 21:24:42 GMT  
		Size: 11.5 MB (11500427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927362fdf6d12722a8bb46023cbc12a3e6f987226957520bba9358d757c2af88`  
		Last Modified: Mon, 08 Sep 2025 21:42:42 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8bb597efc90f77d80af6e59807e850d33a80c2667cfeb714e4deb0b350b5d5`  
		Last Modified: Mon, 08 Sep 2025 21:42:46 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e274b6acee8e6b2078e44f11e044cef5f066de579c5a7c8a325e21f280ef129`  
		Last Modified: Mon, 08 Sep 2025 21:42:49 GMT  
		Size: 101.1 KB (101078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ace93800c079b0b29023ad72a5006fe9153207cc1ba4d195860c874018a5de5`  
		Last Modified: Mon, 08 Sep 2025 21:42:53 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8b131d00cfba46164d8d8c5c746045d9b01dda92efd52a4075480978e50bb7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2bdf7196b07be183008280c04c2818b8346639949e2dfedd1f58e43ff245d77`

```dockerfile
```

-	Layers:
	-	`sha256:32b559285a58b98dc726e037b9352c0e4c87c94562807550c704e5b9e5309dfe`  
		Last Modified: Mon, 08 Sep 2025 22:08:21 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3056fb0e0c32ea9229dad62508be7a1ca2bbe228416168c990ba1b9f07277c`  
		Last Modified: Mon, 08 Sep 2025 22:08:22 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:efedb862d721302994e92fe0a819b0ac89dbd22ec9a629156ab2c19a50c9a19b
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
$ docker pull neurodebian@sha256:5a6560e98de0074d4f556e3a3d723a82ddaf0ae65f34cda741c0584e755c69fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80daaf772d06e04317a105c593b722bf4830f53083a1c3041236aa8f303df83d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc68ad6246d17dbfc153a24bae65f1a5f73ff584955429a8236e563aa3d001f`  
		Last Modified: Mon, 08 Sep 2025 22:48:31 GMT  
		Size: 11.3 MB (11269479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a1c1b4568c9392569145efa49e13b53064de29748b4330157f35fe17d3c28d`  
		Last Modified: Mon, 08 Sep 2025 21:42:51 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa576ad08b5522d438407cf741520c4be3638d6c6f66e9080164d0e470978c8e`  
		Last Modified: Mon, 08 Sep 2025 21:42:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3c1b0722585c6a8c19c079e8987ed2951983f7aed063647f1b7f7fa3133937`  
		Last Modified: Mon, 08 Sep 2025 21:42:59 GMT  
		Size: 93.3 KB (93346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:814f7556d4158f8a1e283388b3c402e0654227d8a269ee0ab181e6b21f434b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2579c266cae1e084172b034d8c94e5fcdf1519765bb54f306e76f79b625b0dea`

```dockerfile
```

-	Layers:
	-	`sha256:4eb751fc0f69002c0dfaadfa36ab65ef9b01d64364167eb630243f00f1019f08`  
		Last Modified: Mon, 08 Sep 2025 22:07:34 GMT  
		Size: 4.1 MB (4075544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea1205fd63d05f019c473c467d0b5d0792d62a875286ab84731f3f8b99040391`  
		Last Modified: Mon, 08 Sep 2025 22:07:35 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:12a913f897befb556c7ceb2558fb8738adbf563ca7ff1157d4e6e11d488df2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2602e1dfb24784e0f598940a8ac2f312dc62011a39e9dc8319db551898e92b2d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d75efbe6214a9b809e0d59c23f7a209f1aa2e67a86e2e01a58b89cda3f55a1`  
		Last Modified: Tue, 09 Sep 2025 05:52:28 GMT  
		Size: 11.3 MB (11253369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d25897438383aab600d85c585491adcb45151c81c148474dddebefd2ba68c7d`  
		Last Modified: Mon, 08 Sep 2025 21:47:08 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2b740c0c23e3e3623ab3e866ec075ea7f234e756897d3331b6c4fca4f953f1`  
		Last Modified: Mon, 08 Sep 2025 21:47:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24a0cf5951e988c99b15b73f59a045bac72bd5418654228ea9976b612cdf7bd`  
		Last Modified: Mon, 08 Sep 2025 21:47:15 GMT  
		Size: 93.5 KB (93483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f15610b49b8b74ba8b43e1d9748fc173946dbe38a914bbe037fe4d22b924d7f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b73ae38a458f069357c6b7ed3f9700bc00f0cbcf6a69c6a334d22717cf4002`

```dockerfile
```

-	Layers:
	-	`sha256:611956d89297f28c59fc723ca0a839c4f9bc091723e81b976d5734b770fd645f`  
		Last Modified: Mon, 08 Sep 2025 22:07:40 GMT  
		Size: 4.1 MB (4075798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829bd69ec3af1019bf9ffcaca8a14d93efb865e96208722280160398adb38b64`  
		Last Modified: Mon, 08 Sep 2025 22:07:41 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:5107aba3d0890867538a1eb3f0a85eb79bd2358d74107fca2636a7c6e319deac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5499da1fa80624060b6dd313bcdec442965968b0ab251f319ad8d5ef629b34cd`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5538e96bb7df1a7ef01bd7fcbf51f4cbc041246109c06cf661f7058c203851af`  
		Last Modified: Mon, 08 Sep 2025 21:12:26 GMT  
		Size: 49.5 MB (49466684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50daaf33853e9bc9be195d0d0d91eb860c20339e0307587f495f92ab4ee3eb09`  
		Last Modified: Mon, 08 Sep 2025 22:06:15 GMT  
		Size: 11.7 MB (11690113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaa2d687517972c9cfc2d08bbc8e9a2d086b3407ee8a0ca60a56ece41aa3cfb`  
		Last Modified: Mon, 08 Sep 2025 22:06:09 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194eae81f05840e1d9e73f4cc66018ae05b766dec142b1d85e9b180dafeeb2ac`  
		Last Modified: Mon, 08 Sep 2025 22:06:10 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ba20391efc1b63213570c7a46041007aef9876ef79f229b994bb3a9d040c97`  
		Last Modified: Mon, 08 Sep 2025 22:06:09 GMT  
		Size: 93.4 KB (93386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:01ea02c921f10ac49caad05945c95f548e78efd8ff5440275c344c15bb235a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80efd81b0e74c1c05e45f223537a7bd9092af273e347a4fd178455d8a9222e15`

```dockerfile
```

-	Layers:
	-	`sha256:73118df0fe0697ee892246dc709ee5f8e8a0c72cd79a3f16640e638aa9e7a3ce`  
		Last Modified: Mon, 08 Sep 2025 22:07:45 GMT  
		Size: 4.1 MB (4073507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb129146de30c7f7b4c3307bb7cac0e930a1af225a47572b94ccee9b08ffffd`  
		Last Modified: Mon, 08 Sep 2025 22:07:46 GMT  
		Size: 14.3 KB (14282 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:1d227f401b183c72194a9f4236ed8d04d43de44d1cc46f66ec8aa5b2fd4d231d
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
$ docker pull neurodebian@sha256:6f43ef7eb07bc7c20266846a1c98b55a22011567a05f2ac5eff2909071eae0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c172ba0b81dd8f89238b22511a3d5be1d5180c0258e9e889a6ecb01624a3a2cb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb3e3b92bc6482e0df10b8b95bf25efd483c108ad208a60664cf5f1d1e77be1`  
		Last Modified: Tue, 09 Sep 2025 17:33:49 GMT  
		Size: 11.3 MB (11269552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e96c4ca1ae8d9db1d4c02f9c3d0652e417622ed05ff6eb736432722662ccdb`  
		Last Modified: Mon, 08 Sep 2025 22:09:05 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4541b568aaf9f21e14e1425e4fc093a5dd0496df3829b6404b3ad6c41efbbbe3`  
		Last Modified: Mon, 08 Sep 2025 22:09:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c1b15bdadbbe93287ac427ea3a8620f5b0157a4e6b13f7635f592e3bcc2708`  
		Last Modified: Mon, 08 Sep 2025 22:09:05 GMT  
		Size: 93.4 KB (93361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c38cbf257c18774f93a43d3e807c5ccb87233a46bd639fbf19fd1391531342`  
		Last Modified: Mon, 08 Sep 2025 22:09:05 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a2a94de25facf95724b2d16ca71a72d99a2e112b2d316cd949056412564d4d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206e4e0e5813d979635e9c61374bdbc88d22a2f82bc265b156b17600d6bdbdb3`

```dockerfile
```

-	Layers:
	-	`sha256:6d1673c322c9fbb37ea05028f45c19a0ce42f508639ca61a70c7c7f98a8aa319`  
		Last Modified: Mon, 08 Sep 2025 22:07:46 GMT  
		Size: 4.1 MB (4075584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae33da5884a0a82ad883b93e19d26853d993626f9c39065efe0d9f5aafc836be`  
		Last Modified: Mon, 08 Sep 2025 22:07:47 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c332ce47e958183cb410e1d6ec20b2be14015b101bbb5817ec4d0a9aa6b0cb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9a8e8b41d0f732b856635dfc148c9421fbca0429e8f76b5fa0bd31453ab413`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb34e261136388af42fa0af1335a030eea1a9f401d4dff98142f1da415eabd5`  
		Last Modified: Tue, 09 Sep 2025 06:31:19 GMT  
		Size: 11.3 MB (11253403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea36eb6d50e0170603953736681c374dc844fe3f7850016340a1d2f4918c0b5`  
		Last Modified: Mon, 08 Sep 2025 22:08:07 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29da554fa0fcd3032487aee0478d47e8a805146cb3bddd18fbad5d609038870e`  
		Last Modified: Mon, 08 Sep 2025 22:08:11 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc2b09e8e858e4635fa19d6758bdf39314fa0cde577075e129e7e80e186328d`  
		Last Modified: Mon, 08 Sep 2025 22:08:14 GMT  
		Size: 93.5 KB (93529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99a489584be5c159eac218a7e93493c1813b822a296ce44cf81cb4637f9423c`  
		Last Modified: Mon, 08 Sep 2025 22:08:18 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cc7b844224cfc087081bd611b411d90140d4bae81280676b5dc0b13af788416a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f86f083a734b088c99b09c277fea3d8963dec528e9b2417e7bbdc58af53a0bb`

```dockerfile
```

-	Layers:
	-	`sha256:9a0d14da4341d08026ac22ce25ef56efe152434f1ed4d94d8ea0c1a31e4cc6b2`  
		Last Modified: Mon, 08 Sep 2025 22:07:53 GMT  
		Size: 4.1 MB (4075838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c09eae5cd42ea87228f8f7591823ff5cbe807f16966c782f8da6a3af8966e35`  
		Last Modified: Mon, 08 Sep 2025 22:07:54 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:180c2a286506c8d607df812e0989c88b708940bfb3792411db5953ff7a4f7a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4db251014580c0601148a94559714d6947766d1bfd4fd6fc7aaf84bd623b71`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5538e96bb7df1a7ef01bd7fcbf51f4cbc041246109c06cf661f7058c203851af`  
		Last Modified: Mon, 08 Sep 2025 21:12:26 GMT  
		Size: 49.5 MB (49466684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9f1e0563153cc066df6491c74f133efcb40edc5eb0f61d987c52753414e037`  
		Last Modified: Tue, 09 Sep 2025 19:09:28 GMT  
		Size: 11.7 MB (11690127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7814d96039aa8fd6261aaf7b5cfceb3feba133e8bca1568a0cdde34995dee5`  
		Last Modified: Mon, 08 Sep 2025 22:10:19 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276fb743fd607e676358632f33e7d22590ee66cc30f7fd6cd688310b84d3a657`  
		Last Modified: Mon, 08 Sep 2025 22:10:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2275f662700e5881813db764845fb48bbf160416ae633242276ca625541288`  
		Last Modified: Mon, 08 Sep 2025 22:10:19 GMT  
		Size: 93.4 KB (93394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2763fded54c1182ff5b5f837e771c5a48137168e2870ab52ec1e17e95ba7c662`  
		Last Modified: Mon, 08 Sep 2025 22:10:19 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:db9f952b4b9884f6b15810229bc63b5376c07e0f3900c2afcc6677bc0bc1a1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d749b7a567dd87cfbc285161259edf132f25ec3dfb417384dc5dc5256253192`

```dockerfile
```

-	Layers:
	-	`sha256:1fffdd5ba041000de4d566ef98f57e8c336b242b4c13f370edd28d7d6a4abddf`  
		Last Modified: Mon, 08 Sep 2025 22:07:59 GMT  
		Size: 4.1 MB (4073547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9c49b10626993226be76089c1be657c79ca21feae895f3e4f09aeb6fc9d642b`  
		Last Modified: Mon, 08 Sep 2025 22:08:00 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:8e5fd833ef1fdbd0634a429ce619af13a0b3bc394a4316528e395989a2b7e559
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
$ docker pull neurodebian@sha256:b8554b98c7b61391bb22bd4a7220df7f7c62650527e0d5418399a94917423fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59662220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a057003cd756d9f5325107c7c4251c56e1861281d12bbfbe20b5a12828bd9cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed7aad3c42d8c3bcd905875cd29230e367d1c38916321ad3ab12c4fdb0d7214`  
		Last Modified: Tue, 23 Sep 2025 19:50:15 GMT  
		Size: 10.3 MB (10289604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b5a09c0af2cd1b2f3b536c610a8484aae29784608be965bc9a76f6adbaa4a2`  
		Last Modified: Tue, 23 Sep 2025 19:50:13 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f6f38bb43cac782ca903da5f508ccc0c581e9a68a8a8e69f171bdfa0c61e70`  
		Last Modified: Tue, 23 Sep 2025 19:50:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff7d4510024de4cd17cd7f0cd21f3979b98414430b20d3562fa40e36bbeec0e`  
		Last Modified: Tue, 23 Sep 2025 19:50:14 GMT  
		Size: 90.2 KB (90176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ac143161be3e17b7c8eafcd0a3d2cb85ddbbbc215ecf917aa9d531c2e6c28c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b72ef0681bd3bb94d50bac07af0c81640b7f02c0ea6f106e3115f463f5b5f6`

```dockerfile
```

-	Layers:
	-	`sha256:aa3f4c83d483d36764c0891f01c50ea9f2c8d0622d9d1b9889ab1cf350e68d9d`  
		Last Modified: Tue, 23 Sep 2025 22:07:36 GMT  
		Size: 3.6 MB (3612981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55df46487d54f44f5754ee59a2a3ad256b28ccf84ecd6f797b4af6e104aeb382`  
		Last Modified: Tue, 23 Sep 2025 22:07:37 GMT  
		Size: 14.3 KB (14293 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c21dbd0a1b16c4fb222391d8e8e637e2922cdaa24fe9ed526552317f113eec9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59810755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008b6ced829a9d58058b2cbab03447436e078b2409fe75b5b1378777ba39b2ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d54f0a8b8cdeb016765b4421672e7132d34ac6b326223b731d5282d5c3ae095`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 10.1 MB (10073260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ca08b2ff60dcd56cef5ab73acd2c160b4e06751f62df7e0e95d1bcfd11d8d6`  
		Last Modified: Tue, 23 Sep 2025 17:39:18 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e35bc05e600c15f0db597abe53e56f5133f1a07cef5ceef2dde74108818d40b`  
		Last Modified: Tue, 23 Sep 2025 17:39:18 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87503a3dead3a4605bff54bd22c67f01d31f31f6b7c17460c90ae59af2d30d76`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 90.8 KB (90839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:20da5439101ef73faac42cf32c8dacca771cdd9cdce9a342d0499874e2dfdc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000c048359af5327f48f359238ffbbbf20737b7e60535c97db620c1ebe6f0cab`

```dockerfile
```

-	Layers:
	-	`sha256:c8c473610319b2e88f677aca463db980bd056b2466974dfa73007cbbb5f01c33`  
		Last Modified: Tue, 23 Sep 2025 19:07:45 GMT  
		Size: 3.6 MB (3614508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb37a93695cd94314c8d98c7d617488ec6ee93baa6906bb6aa6804b7f9e796f`  
		Last Modified: Tue, 23 Sep 2025 19:07:46 GMT  
		Size: 14.4 KB (14431 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:557a466129fe8cd12edbf882dc0ebf898652e8b101e0138a9fce8af68ef67f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61351348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e7b84e0788bd3a7eeacb70c4ab0929b84ccf10892c9650e34e5bec7ca21199`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768b3fdcc0892aba7d97f3db5214e7a8724b3691fbe410f5aec7c9f7729c19e4`  
		Last Modified: Tue, 23 Sep 2025 17:34:19 GMT  
		Size: 10.5 MB (10462915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13e953626a5863b8c7828fd4ed69028cf735723c389479008359be4d9edd990`  
		Last Modified: Tue, 23 Sep 2025 17:34:18 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980b88e4c67b14fb8d1d73a427f8fcdf3eb95789988d2d91ec6970cc6c22bd58`  
		Last Modified: Tue, 23 Sep 2025 17:34:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3482123fd30bdde26844e46aa5360dc605124e27e13b22a8e44866fbc344d156`  
		Last Modified: Tue, 23 Sep 2025 17:34:19 GMT  
		Size: 90.6 KB (90579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3b4d14f31a3774572ceef81ad84383cb0c1ae39ebd131510cfcda15a3630d172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f3fa91eb5042a491e37386d2d34c7c933cc12376225de8f5eac7702a61a2f`

```dockerfile
```

-	Layers:
	-	`sha256:93eaec6d2f1f521fc263252d9ca16cb3a360a3af7531bb55ec9c8264df60460c`  
		Last Modified: Tue, 23 Sep 2025 19:07:51 GMT  
		Size: 3.6 MB (3610930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5f4614670f64ec9fb8c7b72d96283e5b91deb0d9f10815b2ac4881be86ae82`  
		Last Modified: Tue, 23 Sep 2025 19:07:53 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:f7201d496a19f6c2d8a1f89f2bb7f27f8b320ece50e6d8ffd150fd501dda635b
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
$ docker pull neurodebian@sha256:d74480c4fb0d1aea0a60cb68b4dfef8091023d322dc86b7c19769106365595b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59662773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721e07dac792da5b2ac44a59dfbd4f50647f9183fa34f4784bfb2a36cc969191`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304286e8d41b300322bd5ef5086cfa8d719a3b329d244e9982a79d086c44b1d8`  
		Last Modified: Tue, 23 Sep 2025 22:53:16 GMT  
		Size: 10.3 MB (10289746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa9f2a028d94e3c22db46a837a81396392ea689aaa4118be25c47bb5b375324`  
		Last Modified: Tue, 23 Sep 2025 20:16:40 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c4dfe087dbd4ea8bbfbd31d0d0eda058a05d76b97835953dcaa5c142a64645`  
		Last Modified: Tue, 23 Sep 2025 20:16:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d46510a601b4b4189265f8638e995c426e8f19d6f67de49916b018f6f7cde8`  
		Last Modified: Tue, 23 Sep 2025 20:16:49 GMT  
		Size: 90.1 KB (90143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa8b4b7362210cbd9b130d371c891566f8cc83046ee4ee42ad0d114b48f4aac`  
		Last Modified: Tue, 23 Sep 2025 20:16:52 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d4093664e2464d099b57fc22c993c6fb81a386b3722a625e2724cf6058a22b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bae71ae6a23d6a834292bb10943454e6dd6648a554dd098e8416b5395bf02e9`

```dockerfile
```

-	Layers:
	-	`sha256:967ec45e0f9fbe3c02a83631debb6dcbfb0f9a21f09ac17521e9c0695bad6396`  
		Last Modified: Tue, 23 Sep 2025 22:07:56 GMT  
		Size: 3.6 MB (3613021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ab5d9cd4119039f7280b04fcfe7173b52cc842979ed5780914ac981f275e023`  
		Last Modified: Tue, 23 Sep 2025 22:07:57 GMT  
		Size: 16.3 KB (16325 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1eda3906e3d74753dc6108406609474e17922bc4473c0650138d2a71e0bb0a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59811107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1c0ab49c63ddb928d1ea6152bce13a56e8924cf87b59b98426b5735b06a017`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8928402f9240101fa8045309f2d1f99869f404958b90ade93c18a6fdd5103b`  
		Last Modified: Tue, 23 Sep 2025 17:39:21 GMT  
		Size: 10.1 MB (10073166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc260bea759081fbc813dc13e45189e07a89ad889eb04898b83095ebe8e46f6`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7be6fa450a008c0111b995191dcbebe968fec4b2291cb9f77b640b8d90186b`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c083f97f9134022f86c20007997675be9039bd0cd5b261235fc0333b295336`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 90.8 KB (90839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c02e6d484f97370f3d3a31c333d86ab85c56434cf062ec9db96eafa89afbb58`  
		Last Modified: Tue, 23 Sep 2025 17:39:21 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:67f19ba1c382f706a6c0546d668de36db5eb279435eb55be0b971d0d1d6e0d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41fa20712a0c042f42ad63fb2ad11b46db8ea8e4742bcf4d3e9369a094bd33f`

```dockerfile
```

-	Layers:
	-	`sha256:072889b65b38c27822eae4197991fe09aab464f059df703c0ad31613b64ffe68`  
		Last Modified: Tue, 23 Sep 2025 19:08:17 GMT  
		Size: 3.6 MB (3614548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfa28fcb3ba4cc4a53499f985d3803766945bb3f97081ac0415fd7b7b58a8a4`  
		Last Modified: Tue, 23 Sep 2025 19:08:18 GMT  
		Size: 16.5 KB (16477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2685dd7fe3afbe2157a72c212a66ffebfa1465d998490f39ad7fcda33a6079de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61351708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcff7d47fc0d643368953858e2e160918fd389ce7a8454f06445f8f694148b92`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb41c38efac3c3a4e479715bbfbc2b0cf2daac281761c6f91ffab849e5c8190`  
		Last Modified: Tue, 23 Sep 2025 17:35:05 GMT  
		Size: 10.5 MB (10462867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500ab29cbf1ed8b8d382ae37afa2d978700800d7f839dbf340f2b3573a7e131d`  
		Last Modified: Tue, 23 Sep 2025 17:35:04 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351373291dcdae77241331e750e91a9d52b1632c6ef73f989f1801a1126abcbc`  
		Last Modified: Tue, 23 Sep 2025 17:35:04 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa920d26fee157ad165e0eeea4da5aa8faab9500938265f152c6cd6b98ec089`  
		Last Modified: Tue, 23 Sep 2025 17:35:05 GMT  
		Size: 90.5 KB (90535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31df9627b83b4bc4a24ead4a19c413ddfa015c8dd02d315d050d11654445897a`  
		Last Modified: Tue, 23 Sep 2025 17:35:04 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b8294a8060dfa8487b4aabb007bdb278688245077d6acb64e69b97a41e98e2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb7094164a2f8304232900ae7771326641faafedada4ae34e3f96b23f4b435e`

```dockerfile
```

-	Layers:
	-	`sha256:464f2f4ee7c536a30f535caa5b810a4fe3b192a5ac0e163b2bbc250ebe2f6f77`  
		Last Modified: Tue, 23 Sep 2025 19:08:22 GMT  
		Size: 3.6 MB (3610970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f90069b14333bca50c5c0537e5a3deaf9cb3036ecb495ff5dd8610331168857`  
		Last Modified: Tue, 23 Sep 2025 19:08:23 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:c21c580fa14771b6568790b6552843482311747d0eea0fc8320281aeba3f110a
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
$ docker pull neurodebian@sha256:3db03e36a763b7633f46e2ca0db8208918182df6a443e43a1fd7485adfafff44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60031509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6125f2a10160e058dad34118c4a742d0f66d22e9f7bfa33305f86416e2c1206c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1757289600'
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
	-	`sha256:92b4a1a651b0c3628297f7472014e3ecb5580ebbd73dd0616ae4e5d399ff0831`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 49.6 MB (49575035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3ecd164755360c7d3158ba626da720ba20606a84b73d2f5d44fdf6b1b0f314`  
		Last Modified: Tue, 23 Sep 2025 22:27:34 GMT  
		Size: 10.4 MB (10363661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2d676e3c4010bd6870c6ec83b61c40d6b9faaf8dac899dd2accebd96277744`  
		Last Modified: Tue, 23 Sep 2025 19:54:33 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e971c120691ee658f1cb90fcf0e69860b04616f58ff566c5483bbd822dc67a6`  
		Last Modified: Tue, 23 Sep 2025 19:54:39 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185b113cf0c7998249027d6906c29c817b3ddd1525f6c8ae4eb527d9c24ee4b7`  
		Last Modified: Tue, 23 Sep 2025 19:54:43 GMT  
		Size: 89.9 KB (89904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9a98acc34d53a37806d9189e385cc79d30c660ba7d5a31c681e98fcc9587c096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c01b97ef76ef859b6c54734c9d9a79cd3580f25fc4111f12d5bde3009bc8bf`

```dockerfile
```

-	Layers:
	-	`sha256:2bd7237e5bccc6d38ede79c6b4174adcdf44f31782e946a4327a8880e7d817ba`  
		Last Modified: Tue, 23 Sep 2025 22:07:24 GMT  
		Size: 3.6 MB (3609656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f351a44b3e6bb28c5af16732567a0fc31ae502d27a6a44fc7e8e5e211d4270b0`  
		Last Modified: Tue, 23 Sep 2025 22:07:24 GMT  
		Size: 14.0 KB (13975 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1884f414d7f4d42d9194552cca4f2f561cb5c831930c25069ca8dc52b51d7600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2bf448f9d640a57c8d25e475b948218b398464dae0079c10f902a6bc5e682b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1757289600'
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
	-	`sha256:43c9f83b4c0cbba0c49dce5bbb999963ed78f9198001feb88e7464916cedc070`  
		Last Modified: Mon, 08 Sep 2025 21:14:38 GMT  
		Size: 49.9 MB (49863496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b389e1eb5e3644c29fe20800e97ad88d4130d8f91f2afd0935089cb492e67d`  
		Last Modified: Tue, 23 Sep 2025 17:39:30 GMT  
		Size: 10.1 MB (10143305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcde2bbb2b8e25a5f487a9ec062838dbb061b545dc78378db54ab4fe327e022`  
		Last Modified: Tue, 23 Sep 2025 17:39:30 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedaf43c0ade1074e3f4761d8a0db8d3cc800c99518e23a233f454ba8272e3e8`  
		Last Modified: Tue, 23 Sep 2025 17:39:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322389dfacf69a954619302405610c10bf093a760bc966f8abaa9a575fc47919`  
		Last Modified: Tue, 23 Sep 2025 17:39:30 GMT  
		Size: 90.5 KB (90538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4ae4111f9fb4f8661c3112d2c2094f3af49e04a1628e6b9d5807514493edf440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183abe123d0c6b4848582b78924a88e96c0a8b2551abc83c0ed2a029c8677f86`

```dockerfile
```

-	Layers:
	-	`sha256:1c0cab0102cdf0749d41ec86eacf9634fdd3b97d0ef197c01d483a01c4ccc770`  
		Last Modified: Tue, 23 Sep 2025 19:07:24 GMT  
		Size: 3.6 MB (3611171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1aa1f7c47c6525788e4cb300f8b8deda3a356c92a5e3b51068340adbbbd84a`  
		Last Modified: Tue, 23 Sep 2025 19:07:25 GMT  
		Size: 14.1 KB (14098 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; 386

```console
$ docker pull neurodebian@sha256:11058c58d04f9cee09e7772e9af12753ec9cc535796c2aeb6751267eefe68aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61660217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84fcd8cf2ae8736e66857a83ef432820c3d8cc164f30bc89dce3e4196b755ea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1757289600'
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
	-	`sha256:e46ba83d4247b0505c7b4e05b89ae8056e10eb07f4e445e17e2dc44b8c60b063`  
		Last Modified: Mon, 08 Sep 2025 21:12:21 GMT  
		Size: 51.0 MB (51049810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd9f653dffb60029283947ae432468f0744bc5c41ac2cd7864462e7b6d346cd`  
		Last Modified: Tue, 23 Sep 2025 17:35:01 GMT  
		Size: 10.5 MB (10517206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032540512c217e4bf41f9f21bca693e5aabe57f0c14470ff5098b3d3612cb1c`  
		Last Modified: Tue, 23 Sep 2025 17:34:56 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08556b76c8fe9f856b650913ccc3ff442c89533583c2941baabc7b50ee94542a`  
		Last Modified: Tue, 23 Sep 2025 17:34:56 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0308513bea14133c14dc940e28140185ffcd143c9922260858228366073ae7ed`  
		Last Modified: Tue, 23 Sep 2025 17:34:56 GMT  
		Size: 90.3 KB (90291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93d806e3bbaa5ebec0e64643b1858947433f7614dfbcdfda7f015305f34fa27c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76949e8a60eac27296a23b51b51583e48630e90252fb1923122ed413b37fca83`

```dockerfile
```

-	Layers:
	-	`sha256:17e4e13f8695ea16be8eb97fd0af10b9701dbe3c21ce93de22f0599eb721cc2a`  
		Last Modified: Tue, 23 Sep 2025 19:07:29 GMT  
		Size: 3.6 MB (3607616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a3465cb6ec2bb111fabb3a3472c418c2f00acfb5c99ebd3f5d89dbbd1a578c`  
		Last Modified: Tue, 23 Sep 2025 19:07:30 GMT  
		Size: 13.9 KB (13946 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:e0fbe001d3a08d53127effde6310c1ea79e1de80e6770a493f18d1c7dc6e7c86
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
$ docker pull neurodebian@sha256:5366af3f90a45684e74903e70210e4bb68b49d59276eb6931adce082b981b45e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60032010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d6887d14c2e11779df6cb0d4e30520f6e8fa717b31b551c6ce8b010c1f8540`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1757289600'
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
	-	`sha256:92b4a1a651b0c3628297f7472014e3ecb5580ebbd73dd0616ae4e5d399ff0831`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 49.6 MB (49575035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7db97dff5175af40ec6025214bb079c09ac897f5789989aff24bb46c90af7f`  
		Last Modified: Tue, 23 Sep 2025 19:50:58 GMT  
		Size: 10.4 MB (10363736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7cd68ebbe1b4bb5790baf1d4f8c57c2b1c6566d79b9243fe8d96506c3abf64`  
		Last Modified: Tue, 23 Sep 2025 19:50:54 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f5aaf1deba36ade8b00c1b1aed3ce3cba5b662b288e95fcd9767641770fda9`  
		Last Modified: Tue, 23 Sep 2025 19:50:54 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8d3b32d3a43489dbf76579ccbcc3d6d10c549d0d0dd14e7f8967a18fd0289e`  
		Last Modified: Tue, 23 Sep 2025 19:50:54 GMT  
		Size: 89.9 KB (89885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610f51ac5bbee14ce886acdea59761c66321ae40ad41ec1fd151a64c6cce3c6`  
		Last Modified: Tue, 23 Sep 2025 19:50:53 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3fce87b257cf771d7bc40c767e0e6d6c28b3794633c996aae20121189cb1ded3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:807259444ad74f4c97676e376b584b585fab817dc8c497e10dec98d27acf9d3d`

```dockerfile
```

-	Layers:
	-	`sha256:592b60b52129e3462b375f44c2cdbdd5fd57a1374a2d7c3e79d1d2e07d19450a`  
		Last Modified: Tue, 23 Sep 2025 22:07:30 GMT  
		Size: 3.6 MB (3609692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53903836a6b295d6e68e9f43596675d6bc665dbaae112077cc8afcf758cfb22a`  
		Last Modified: Tue, 23 Sep 2025 22:07:31 GMT  
		Size: 16.0 KB (16002 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:92b039616dcf059809b62e835c2ce1fb356f4cd490c14c863ddbb4f81570d2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5695ee1268cbe16821e636a6a6de9143f516e858fba50a8746679ac8c8e02f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1757289600'
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
	-	`sha256:43c9f83b4c0cbba0c49dce5bbb999963ed78f9198001feb88e7464916cedc070`  
		Last Modified: Mon, 08 Sep 2025 21:14:38 GMT  
		Size: 49.9 MB (49863496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad7660c35dc9245a3651760544eb6d528a0717570b22435a069d38bebcd4357`  
		Last Modified: Tue, 23 Sep 2025 17:39:16 GMT  
		Size: 10.1 MB (10143297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dd4856fbbd8812c3c3b07b916f604327d04013c0b756c50d815b3737d5a3a3`  
		Last Modified: Tue, 23 Sep 2025 18:26:23 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b49b1700cbeb581584f2de01718799af245efd3c1972207bb7a4cb2cd586b`  
		Last Modified: Tue, 23 Sep 2025 18:26:24 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c05e31d8c611a15105712c9f93a7d834b93de603459f204925647c9e891abb`  
		Last Modified: Tue, 23 Sep 2025 18:26:23 GMT  
		Size: 90.5 KB (90542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b573a07e48b33f323dac37694b9a4a2ac7a9be42a1d64ffe538334c6725ecb`  
		Last Modified: Tue, 23 Sep 2025 18:26:22 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dc967d49f585f0360b55969f2a013216fab797309dfe973f1d413f39b39e2119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd6eb2694ece8d67925bc06c1ac0aa05f71d39d9a1852f52a881473f433cf61`

```dockerfile
```

-	Layers:
	-	`sha256:7f44ac7080f4f07f4a92b14c9203b3500126b0a1a15a00e395e3678201cdac02`  
		Last Modified: Tue, 23 Sep 2025 19:07:31 GMT  
		Size: 3.6 MB (3611207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b186d8b4531db4698e1f2b80fe05e77d72e2ae2c9b558c2e1e3b38bd5777443`  
		Last Modified: Tue, 23 Sep 2025 19:07:32 GMT  
		Size: 16.1 KB (16142 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:715ecfa0220f7fd01738785f9c42ee3d2ac9b835a64a08b806a94b5fb6a82afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61660669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49c25b5eb4f3ce42160d048e69202a5b427df77adbe42bf1c90db6ae05bcddb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1757289600'
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
	-	`sha256:e46ba83d4247b0505c7b4e05b89ae8056e10eb07f4e445e17e2dc44b8c60b063`  
		Last Modified: Mon, 08 Sep 2025 21:12:21 GMT  
		Size: 51.0 MB (51049810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361bd0e810695bdbe9086ecda5df8904416a487bc5a0ab43e7495d3598650bcf`  
		Last Modified: Wed, 24 Sep 2025 02:15:15 GMT  
		Size: 10.5 MB (10517223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f39ed7022b30182eeeb2b6e84799ec704eb6ed39b6b25a8ae84f4484d7e0680`  
		Last Modified: Tue, 23 Sep 2025 18:22:25 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c317b5fe370cd1003cd49347234721b59a8595b0d60b476ff8e76e2a2f020a38`  
		Last Modified: Tue, 23 Sep 2025 18:22:24 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea9c5768445e1715d5adb3c925a6337fe3629fbba9d4736c7300a995c493bd4`  
		Last Modified: Tue, 23 Sep 2025 18:22:24 GMT  
		Size: 90.3 KB (90276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45b3fdb11b8dbbc68f00e2fc25d31ea20aca0b0cbd042c8e6812b59b3619f72`  
		Last Modified: Tue, 23 Sep 2025 18:22:24 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7855e2a2d3a399325fa66efac0702ee6144d1103a4aab879ba2ef8db9a1324e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25f019bc15a42d275adef0a10d965245e5a53d609818d34d0f8947e18168294`

```dockerfile
```

-	Layers:
	-	`sha256:273801161af411b9ca75df5f2ce6622db20fa373538ba54a0c24f2c4bf746b18`  
		Last Modified: Tue, 23 Sep 2025 19:07:39 GMT  
		Size: 3.6 MB (3607652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6349aefa2276bd907a81a03bfa347913a3a681b8efd053e0e8aca34bc5e0112c`  
		Last Modified: Tue, 23 Sep 2025 19:07:40 GMT  
		Size: 16.0 KB (15972 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:975465318c2961a62e84945b66e3eb674c0cc276f3f1c79e9d775380ed7e2978
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
$ docker pull neurodebian@sha256:3d755067362f393c7585144595d3f2754010a5c721f206cd73de9f771bc93aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31072458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef546e0120c2e4950f832e3f1f63ea76331b4eddda9a60829a347bccc6d11f0`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187b0329cf2a4a15a9bf4b14570d09ca06b3b9b031182d9d673722455466dea4`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 3.6 MB (3598206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b2c6c73f48a5205154bbeefdc3a62200f2912abd347eab19218d25884b59c6`  
		Last Modified: Tue, 02 Sep 2025 02:31:43 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c6dd113705bb44b0596d44cfd3ff0395aac0b756dc8da44d1563df648bedfe`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02baa23e0d6f84b6310f25f56d9459f98c61c4ae69864e811e3f6d95714f90`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 110.6 KB (110605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:50ea19520af7ff7bb17b1c87749b89c3d943ef0cd19a831bb8d497304d58d9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322e60f23e6672fb7149c0f864f30ec442e1b554da2264f5133d991f7e647c51`

```dockerfile
```

-	Layers:
	-	`sha256:5c2043d6adc338e426d3f82ccf4134905c4a04e1d8a86411801d898cb43d5ce9`  
		Last Modified: Tue, 02 Sep 2025 04:07:27 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d1c964ae4683d90f63a5cbd6b78ef63792fd7523b7173d484e631d31afa51ba`  
		Last Modified: Tue, 02 Sep 2025 04:07:27 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:5a0fd02a955581821f5e1e61b232651e9eb3e9d8f5d112dd221a5079ab5a4655
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
$ docker pull neurodebian@sha256:16c1487ee25e15abee9aa27c20c3bc91b9fa4c99bab65e7a742963d60666def6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31072747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6792b8f84d3304ef6e28de08173b87ae23cf5b542ae198b8bd962bf5b29b4a40`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187b0329cf2a4a15a9bf4b14570d09ca06b3b9b031182d9d673722455466dea4`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 3.6 MB (3598206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b2c6c73f48a5205154bbeefdc3a62200f2912abd347eab19218d25884b59c6`  
		Last Modified: Tue, 02 Sep 2025 02:31:43 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c6dd113705bb44b0596d44cfd3ff0395aac0b756dc8da44d1563df648bedfe`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02baa23e0d6f84b6310f25f56d9459f98c61c4ae69864e811e3f6d95714f90`  
		Last Modified: Tue, 02 Sep 2025 02:31:44 GMT  
		Size: 110.6 KB (110605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b579638f5ad784db8571cf092a6ef4ab30b240756a48f6c38c0e8dc718d7610d`  
		Last Modified: Tue, 02 Sep 2025 02:31:46 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cf925a26094fa612cb22d55b1e64484fb6c1683525aa871d37fd1df276896a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c790b7b9e0fe69d544874fceaebe8f92b6265deaed73d3e8ed48cec56061cf7`

```dockerfile
```

-	Layers:
	-	`sha256:b956c6cf699422639abaacca5984085ebbe4ef744fc698f2bc3ef106bba50906`  
		Last Modified: Tue, 02 Sep 2025 04:07:28 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42e7b9a80bb3eb37d02c02dc8ae979642d01e3d3644d30077268d4519deff36`  
		Last Modified: Tue, 02 Sep 2025 04:07:29 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:6e02989b47df7db2a08e054a1081f44c5535bb6edd9802f11d44e195a4fe069a
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
$ docker pull neurodebian@sha256:73a6378e6e4bd851f1da2345032967fa99534080bf5b055548d62c0456e215e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32529991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5d31949edec4e28e7c400a605a8b46f2df3673eaf8a1329e52de63c2136e83`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650e56fe94b24f589aeae16b5dfa6d26517aca0aeddc85a06af498630734f661`  
		Last Modified: Tue, 23 Sep 2025 17:39:05 GMT  
		Size: 3.6 MB (3561120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a041334afb20314801562a56931694e78663063d71879b331753366890f7eb8`  
		Last Modified: Tue, 23 Sep 2025 17:39:05 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cf07850519cc1df9ced969c933d2884855713964a671bd55762ca1a5c0868f`  
		Last Modified: Tue, 23 Sep 2025 17:39:05 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ff886cee52db9a32053371b1366c3d345d09a731394fe5970c4de2fb283551`  
		Last Modified: Tue, 23 Sep 2025 17:39:05 GMT  
		Size: 104.6 KB (104648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cdbd066ba9fad9e6111deb019fcd64648e1bb4bfd4df5a65bf2666b4c3a8840a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a72f68b1a693f32926d5b6bb47fcf874185240b8eb084f2e8b75734c6e08f9`

```dockerfile
```

-	Layers:
	-	`sha256:672d3ab998ebc12efdefa49238eaa1f87a8f317ce05209af628f31cd31bd0f49`  
		Last Modified: Tue, 23 Sep 2025 19:08:25 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3411f31a278f28da2cdce861cc58d20bbdc30ce6d25c3d68335d2478041ab27d`  
		Last Modified: Tue, 23 Sep 2025 19:08:27 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:6941fff017f6f39f25f9d63101390d8394722f3e605f92d7dcfe6ddce7da8c5b
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
$ docker pull neurodebian@sha256:31bfdfc2278dd076f92b861b4929da08e4f4c244b94ddd532096063701ff0b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1ab0a34a219558af9cc4a064ddc7533ea27f36016970f505d775e1860c9f2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cbce970f4fcde4087f471439241feb6f78d46533e1a5654ab48235434b9af6`  
		Last Modified: Tue, 23 Sep 2025 17:39:10 GMT  
		Size: 3.6 MB (3561055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff13a18c517670117fdf68b05cfaae331ab04efd8a13f15f51051c360252c247`  
		Last Modified: Tue, 23 Sep 2025 17:39:10 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbff6157ab4036660d2ba48d811c5f9528fcc4c4f03904177d8c6bab1d6d5b0d`  
		Last Modified: Tue, 23 Sep 2025 17:39:10 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d935ff6965fd4b3182d28f4504a550e5e6217b25e97ecfcab337ec68e0d0401`  
		Last Modified: Tue, 23 Sep 2025 17:39:10 GMT  
		Size: 104.6 KB (104633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a254668991176799838bb3b40462d8ba805a4d8c86c14cb865bb1cbe2d9b379`  
		Last Modified: Tue, 23 Sep 2025 17:39:10 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5c3b09855a580c2dcb881441d1ed05483b6305043b31d968b50525166a2fbf11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7a6fb7f63a63ca2d1ac39393ce95aea63177211c4d58b2479d1dd29fb5a356`

```dockerfile
```

-	Layers:
	-	`sha256:838fb0e926eb0b4c3cd6592958c8d1cc36b74efbb510a44ebcbe22124a491405`  
		Last Modified: Tue, 23 Sep 2025 19:08:30 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1129bb605f28a3d814c54f9c8718030096fc619327ab6ddca3f14708092de5a2`  
		Last Modified: Tue, 23 Sep 2025 19:08:31 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd25.04`

```console
$ docker pull neurodebian@sha256:98208b852dc713c99937e8ca58961d9db9e0dd727c690c79bda5280d3065b178
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
$ docker pull neurodebian@sha256:55a68eac248a8d42afae7771815316c6597bc23414f2bcb24610df9e6dc7e75b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34804798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94188be5c2812cd4d434a3510f2ab091126185cc132c235484f5d8a9ac13d08f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:07:41 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:07:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:07:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:07:41 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 10 Sep 2025 05:07:44 GMT
ADD file:1d0db44377aa33c495de438dd435408b4391cf11e887ef1a542a8ab49275c67c in / 
# Wed, 10 Sep 2025 05:07:44 GMT
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
	-	`sha256:47429ff9cdd3006afbf0a7a02f144b5a7444e546614a97a12fd567f7a4e3afdb`  
		Last Modified: Wed, 10 Sep 2025 15:57:53 GMT  
		Size: 28.3 MB (28305856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d950a571b00bde276c30d63f2ee2a5b9567f2fb831c12cd1eb737519ed1480`  
		Last Modified: Tue, 23 Sep 2025 17:39:24 GMT  
		Size: 6.4 MB (6392123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebe2c7b5214a82ea313c8e78ea11f5ae93f4d1db70d09a1b7265327764c87f9`  
		Last Modified: Tue, 23 Sep 2025 17:39:22 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242a2790fa0f37041a04be6d0aa7128f9deada84df5b813f1d252e0b7b2b5951`  
		Last Modified: Tue, 23 Sep 2025 17:39:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b8e683f9c29882925b49af66393f164647dfa8910c654219c5c3e3e4299abd`  
		Last Modified: Tue, 23 Sep 2025 17:39:22 GMT  
		Size: 103.9 KB (103907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:81aabe3836e3743663a639189c3c1d1c9c2ff9d04fe9729d8bdd06b7c73aea9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e7dbd796cad8555b51207ba5b6dacc473494b04b36b052b5e21733c861d667`

```dockerfile
```

-	Layers:
	-	`sha256:975dba4328ee4fefd23c6e963d51ed262a6282c5a3c6e80007f4d1aeaba86d5a`  
		Last Modified: Tue, 23 Sep 2025 19:08:33 GMT  
		Size: 2.1 MB (2129591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38214ac78604bf6125c273adcbdfaa727fd4c183ec0ae0ae4d88b3389834d212`  
		Last Modified: Tue, 23 Sep 2025 19:08:33 GMT  
		Size: 14.1 KB (14112 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd25.04-non-free`

```console
$ docker pull neurodebian@sha256:cdb8099e6c5dc2b8895a4ae7b65016fa7eda2cbf2426d4c7bd8f8d19c3c2513a
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
$ docker pull neurodebian@sha256:e7e12a8494e56c96b8e743d68b661259bd850d79cda5e240f678665dea664e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34805176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8a964bf53bf298b9fda4da6ee1cf2dfb78d231037035040a8e9e15837b3368`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:07:41 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:07:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:07:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:07:41 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 10 Sep 2025 05:07:44 GMT
ADD file:1d0db44377aa33c495de438dd435408b4391cf11e887ef1a542a8ab49275c67c in / 
# Wed, 10 Sep 2025 05:07:44 GMT
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
	-	`sha256:47429ff9cdd3006afbf0a7a02f144b5a7444e546614a97a12fd567f7a4e3afdb`  
		Last Modified: Wed, 10 Sep 2025 15:57:53 GMT  
		Size: 28.3 MB (28305856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7422c772e4bebb82915c942d5d65cee5cb73f3fa9d071314036f12211bfbd35`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 6.4 MB (6392080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab86a9a06680b71282957a516de592ec540d4a3a3085dd99770143b53ec4f8`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad68505bcdededd57953f74dd00caa2c6585aae6568b7b50b821a33e1750a89`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578f665a5e0bc3591b4eceef30540c01829e4e5e22367f95b3d347ad70de0d96`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 103.9 KB (103902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cea750d95d3d4c2c0c60e9495f5ca6be923d353c078878135a374eeb6fd688c`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:777bfcf11ec281aab0a7a0452dc2ff515160a15fa2deb6b1350b7d86ad703933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba055ad51cb0966bc47f359d61b9e7366de88d63000a6a4d0ba557ebd5ff739e`

```dockerfile
```

-	Layers:
	-	`sha256:c5eed7530f2fa3ee9c35819415fd3c037dd5b1b351f7bb24d980eefdf4ec16b1`  
		Last Modified: Tue, 23 Sep 2025 19:08:37 GMT  
		Size: 2.1 MB (2129627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab62724697affbc8b975acf6239ccea91b8af0a438a9131fc842c9c82e1703a`  
		Last Modified: Tue, 23 Sep 2025 19:08:37 GMT  
		Size: 16.4 KB (16356 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:6e02989b47df7db2a08e054a1081f44c5535bb6edd9802f11d44e195a4fe069a
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
$ docker pull neurodebian@sha256:73a6378e6e4bd851f1da2345032967fa99534080bf5b055548d62c0456e215e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32529991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5d31949edec4e28e7c400a605a8b46f2df3673eaf8a1329e52de63c2136e83`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650e56fe94b24f589aeae16b5dfa6d26517aca0aeddc85a06af498630734f661`  
		Last Modified: Tue, 23 Sep 2025 17:39:05 GMT  
		Size: 3.6 MB (3561120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a041334afb20314801562a56931694e78663063d71879b331753366890f7eb8`  
		Last Modified: Tue, 23 Sep 2025 17:39:05 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cf07850519cc1df9ced969c933d2884855713964a671bd55762ca1a5c0868f`  
		Last Modified: Tue, 23 Sep 2025 17:39:05 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ff886cee52db9a32053371b1366c3d345d09a731394fe5970c4de2fb283551`  
		Last Modified: Tue, 23 Sep 2025 17:39:05 GMT  
		Size: 104.6 KB (104648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cdbd066ba9fad9e6111deb019fcd64648e1bb4bfd4df5a65bf2666b4c3a8840a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a72f68b1a693f32926d5b6bb47fcf874185240b8eb084f2e8b75734c6e08f9`

```dockerfile
```

-	Layers:
	-	`sha256:672d3ab998ebc12efdefa49238eaa1f87a8f317ce05209af628f31cd31bd0f49`  
		Last Modified: Tue, 23 Sep 2025 19:08:25 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3411f31a278f28da2cdce861cc58d20bbdc30ce6d25c3d68335d2478041ab27d`  
		Last Modified: Tue, 23 Sep 2025 19:08:27 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:6941fff017f6f39f25f9d63101390d8394722f3e605f92d7dcfe6ddce7da8c5b
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
$ docker pull neurodebian@sha256:31bfdfc2278dd076f92b861b4929da08e4f4c244b94ddd532096063701ff0b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1ab0a34a219558af9cc4a064ddc7533ea27f36016970f505d775e1860c9f2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:45:34 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:45:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:45:34 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:45:38 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Wed, 10 Sep 2025 05:45:39 GMT
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cbce970f4fcde4087f471439241feb6f78d46533e1a5654ab48235434b9af6`  
		Last Modified: Tue, 23 Sep 2025 17:39:10 GMT  
		Size: 3.6 MB (3561055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff13a18c517670117fdf68b05cfaae331ab04efd8a13f15f51051c360252c247`  
		Last Modified: Tue, 23 Sep 2025 17:39:10 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbff6157ab4036660d2ba48d811c5f9528fcc4c4f03904177d8c6bab1d6d5b0d`  
		Last Modified: Tue, 23 Sep 2025 17:39:10 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d935ff6965fd4b3182d28f4504a550e5e6217b25e97ecfcab337ec68e0d0401`  
		Last Modified: Tue, 23 Sep 2025 17:39:10 GMT  
		Size: 104.6 KB (104633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a254668991176799838bb3b40462d8ba805a4d8c86c14cb865bb1cbe2d9b379`  
		Last Modified: Tue, 23 Sep 2025 17:39:10 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5c3b09855a580c2dcb881441d1ed05483b6305043b31d968b50525166a2fbf11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7a6fb7f63a63ca2d1ac39393ce95aea63177211c4d58b2479d1dd29fb5a356`

```dockerfile
```

-	Layers:
	-	`sha256:838fb0e926eb0b4c3cd6592958c8d1cc36b74efbb510a44ebcbe22124a491405`  
		Last Modified: Tue, 23 Sep 2025 19:08:30 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1129bb605f28a3d814c54f9c8718030096fc619327ab6ddca3f14708092de5a2`  
		Last Modified: Tue, 23 Sep 2025 19:08:31 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:f7201d496a19f6c2d8a1f89f2bb7f27f8b320ece50e6d8ffd150fd501dda635b
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
$ docker pull neurodebian@sha256:d74480c4fb0d1aea0a60cb68b4dfef8091023d322dc86b7c19769106365595b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59662773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721e07dac792da5b2ac44a59dfbd4f50647f9183fa34f4784bfb2a36cc969191`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304286e8d41b300322bd5ef5086cfa8d719a3b329d244e9982a79d086c44b1d8`  
		Last Modified: Tue, 23 Sep 2025 22:53:16 GMT  
		Size: 10.3 MB (10289746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa9f2a028d94e3c22db46a837a81396392ea689aaa4118be25c47bb5b375324`  
		Last Modified: Tue, 23 Sep 2025 20:16:40 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c4dfe087dbd4ea8bbfbd31d0d0eda058a05d76b97835953dcaa5c142a64645`  
		Last Modified: Tue, 23 Sep 2025 20:16:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d46510a601b4b4189265f8638e995c426e8f19d6f67de49916b018f6f7cde8`  
		Last Modified: Tue, 23 Sep 2025 20:16:49 GMT  
		Size: 90.1 KB (90143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa8b4b7362210cbd9b130d371c891566f8cc83046ee4ee42ad0d114b48f4aac`  
		Last Modified: Tue, 23 Sep 2025 20:16:52 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d4093664e2464d099b57fc22c993c6fb81a386b3722a625e2724cf6058a22b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bae71ae6a23d6a834292bb10943454e6dd6648a554dd098e8416b5395bf02e9`

```dockerfile
```

-	Layers:
	-	`sha256:967ec45e0f9fbe3c02a83631debb6dcbfb0f9a21f09ac17521e9c0695bad6396`  
		Last Modified: Tue, 23 Sep 2025 22:07:56 GMT  
		Size: 3.6 MB (3613021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ab5d9cd4119039f7280b04fcfe7173b52cc842979ed5780914ac981f275e023`  
		Last Modified: Tue, 23 Sep 2025 22:07:57 GMT  
		Size: 16.3 KB (16325 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1eda3906e3d74753dc6108406609474e17922bc4473c0650138d2a71e0bb0a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59811107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1c0ab49c63ddb928d1ea6152bce13a56e8924cf87b59b98426b5735b06a017`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8928402f9240101fa8045309f2d1f99869f404958b90ade93c18a6fdd5103b`  
		Last Modified: Tue, 23 Sep 2025 17:39:21 GMT  
		Size: 10.1 MB (10073166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc260bea759081fbc813dc13e45189e07a89ad889eb04898b83095ebe8e46f6`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7be6fa450a008c0111b995191dcbebe968fec4b2291cb9f77b640b8d90186b`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c083f97f9134022f86c20007997675be9039bd0cd5b261235fc0333b295336`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 90.8 KB (90839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c02e6d484f97370f3d3a31c333d86ab85c56434cf062ec9db96eafa89afbb58`  
		Last Modified: Tue, 23 Sep 2025 17:39:21 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:67f19ba1c382f706a6c0546d668de36db5eb279435eb55be0b971d0d1d6e0d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41fa20712a0c042f42ad63fb2ad11b46db8ea8e4742bcf4d3e9369a094bd33f`

```dockerfile
```

-	Layers:
	-	`sha256:072889b65b38c27822eae4197991fe09aab464f059df703c0ad31613b64ffe68`  
		Last Modified: Tue, 23 Sep 2025 19:08:17 GMT  
		Size: 3.6 MB (3614548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfa28fcb3ba4cc4a53499f985d3803766945bb3f97081ac0415fd7b7b58a8a4`  
		Last Modified: Tue, 23 Sep 2025 19:08:18 GMT  
		Size: 16.5 KB (16477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2685dd7fe3afbe2157a72c212a66ffebfa1465d998490f39ad7fcda33a6079de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61351708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcff7d47fc0d643368953858e2e160918fd389ce7a8454f06445f8f694148b92`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb41c38efac3c3a4e479715bbfbc2b0cf2daac281761c6f91ffab849e5c8190`  
		Last Modified: Tue, 23 Sep 2025 17:35:05 GMT  
		Size: 10.5 MB (10462867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500ab29cbf1ed8b8d382ae37afa2d978700800d7f839dbf340f2b3573a7e131d`  
		Last Modified: Tue, 23 Sep 2025 17:35:04 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351373291dcdae77241331e750e91a9d52b1632c6ef73f989f1801a1126abcbc`  
		Last Modified: Tue, 23 Sep 2025 17:35:04 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa920d26fee157ad165e0eeea4da5aa8faab9500938265f152c6cd6b98ec089`  
		Last Modified: Tue, 23 Sep 2025 17:35:05 GMT  
		Size: 90.5 KB (90535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31df9627b83b4bc4a24ead4a19c413ddfa015c8dd02d315d050d11654445897a`  
		Last Modified: Tue, 23 Sep 2025 17:35:04 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b8294a8060dfa8487b4aabb007bdb278688245077d6acb64e69b97a41e98e2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb7094164a2f8304232900ae7771326641faafedada4ae34e3f96b23f4b435e`

```dockerfile
```

-	Layers:
	-	`sha256:464f2f4ee7c536a30f535caa5b810a4fe3b192a5ac0e163b2bbc250ebe2f6f77`  
		Last Modified: Tue, 23 Sep 2025 19:08:22 GMT  
		Size: 3.6 MB (3610970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f90069b14333bca50c5c0537e5a3deaf9cb3036ecb495ff5dd8610331168857`  
		Last Modified: Tue, 23 Sep 2025 19:08:23 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:plucky`

```console
$ docker pull neurodebian@sha256:98208b852dc713c99937e8ca58961d9db9e0dd727c690c79bda5280d3065b178
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
$ docker pull neurodebian@sha256:55a68eac248a8d42afae7771815316c6597bc23414f2bcb24610df9e6dc7e75b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34804798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94188be5c2812cd4d434a3510f2ab091126185cc132c235484f5d8a9ac13d08f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:07:41 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:07:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:07:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:07:41 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 10 Sep 2025 05:07:44 GMT
ADD file:1d0db44377aa33c495de438dd435408b4391cf11e887ef1a542a8ab49275c67c in / 
# Wed, 10 Sep 2025 05:07:44 GMT
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
	-	`sha256:47429ff9cdd3006afbf0a7a02f144b5a7444e546614a97a12fd567f7a4e3afdb`  
		Last Modified: Wed, 10 Sep 2025 15:57:53 GMT  
		Size: 28.3 MB (28305856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d950a571b00bde276c30d63f2ee2a5b9567f2fb831c12cd1eb737519ed1480`  
		Last Modified: Tue, 23 Sep 2025 17:39:24 GMT  
		Size: 6.4 MB (6392123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebe2c7b5214a82ea313c8e78ea11f5ae93f4d1db70d09a1b7265327764c87f9`  
		Last Modified: Tue, 23 Sep 2025 17:39:22 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242a2790fa0f37041a04be6d0aa7128f9deada84df5b813f1d252e0b7b2b5951`  
		Last Modified: Tue, 23 Sep 2025 17:39:22 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b8e683f9c29882925b49af66393f164647dfa8910c654219c5c3e3e4299abd`  
		Last Modified: Tue, 23 Sep 2025 17:39:22 GMT  
		Size: 103.9 KB (103907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:81aabe3836e3743663a639189c3c1d1c9c2ff9d04fe9729d8bdd06b7c73aea9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e7dbd796cad8555b51207ba5b6dacc473494b04b36b052b5e21733c861d667`

```dockerfile
```

-	Layers:
	-	`sha256:975dba4328ee4fefd23c6e963d51ed262a6282c5a3c6e80007f4d1aeaba86d5a`  
		Last Modified: Tue, 23 Sep 2025 19:08:33 GMT  
		Size: 2.1 MB (2129591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38214ac78604bf6125c273adcbdfaa727fd4c183ec0ae0ae4d88b3389834d212`  
		Last Modified: Tue, 23 Sep 2025 19:08:33 GMT  
		Size: 14.1 KB (14112 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:plucky-non-free`

```console
$ docker pull neurodebian@sha256:cdb8099e6c5dc2b8895a4ae7b65016fa7eda2cbf2426d4c7bd8f8d19c3c2513a
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
$ docker pull neurodebian@sha256:e7e12a8494e56c96b8e743d68b661259bd850d79cda5e240f678665dea664e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34805176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8a964bf53bf298b9fda4da6ee1cf2dfb78d231037035040a8e9e15837b3368`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:07:41 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:07:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:07:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:07:41 GMT
LABEL org.opencontainers.image.version=25.04
# Wed, 10 Sep 2025 05:07:44 GMT
ADD file:1d0db44377aa33c495de438dd435408b4391cf11e887ef1a542a8ab49275c67c in / 
# Wed, 10 Sep 2025 05:07:44 GMT
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
	-	`sha256:47429ff9cdd3006afbf0a7a02f144b5a7444e546614a97a12fd567f7a4e3afdb`  
		Last Modified: Wed, 10 Sep 2025 15:57:53 GMT  
		Size: 28.3 MB (28305856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7422c772e4bebb82915c942d5d65cee5cb73f3fa9d071314036f12211bfbd35`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 6.4 MB (6392080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab86a9a06680b71282957a516de592ec540d4a3a3085dd99770143b53ec4f8`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad68505bcdededd57953f74dd00caa2c6585aae6568b7b50b821a33e1750a89`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578f665a5e0bc3591b4eceef30540c01829e4e5e22367f95b3d347ad70de0d96`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 103.9 KB (103902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cea750d95d3d4c2c0c60e9495f5ca6be923d353c078878135a374eeb6fd688c`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:777bfcf11ec281aab0a7a0452dc2ff515160a15fa2deb6b1350b7d86ad703933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba055ad51cb0966bc47f359d61b9e7366de88d63000a6a4d0ba557ebd5ff739e`

```dockerfile
```

-	Layers:
	-	`sha256:c5eed7530f2fa3ee9c35819415fd3c037dd5b1b351f7bb24d980eefdf4ec16b1`  
		Last Modified: Tue, 23 Sep 2025 19:08:37 GMT  
		Size: 2.1 MB (2129627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aab62724697affbc8b975acf6239ccea91b8af0a438a9131fc842c9c82e1703a`  
		Last Modified: Tue, 23 Sep 2025 19:08:37 GMT  
		Size: 16.4 KB (16356 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:28ed00c3b99a93843498bcdf4dbb2e106a98bd6f09cb16cb0f429c7287b5b92d
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
$ docker pull neurodebian@sha256:3a7c2310d559960aaf251bc55abe9a2ab7db5737be3afbf4fe917255a3297e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60150107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237a847b33b05b4e89235d3b6749d4840276b001e4738669e669a1a496565414`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1757289600'
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
	-	`sha256:8d64c6c7c21822ac171c4c396d70161707401d6d50d133075d661956f08dc756`  
		Last Modified: Mon, 08 Sep 2025 21:13:08 GMT  
		Size: 49.7 MB (49657990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d854924ae9b4b1288c9dfda064ea896d3981b318987c9c6ffe8efb82e63325d9`  
		Last Modified: Tue, 23 Sep 2025 19:50:14 GMT  
		Size: 10.4 MB (10399375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e96eca8e251a3599c0646fff211e1ad902995d9c8f4cdcb9aea901bbe51fc8`  
		Last Modified: Tue, 23 Sep 2025 19:50:09 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b127e8318640efb0fdf4c7d5c155014b89218f931be0840c2468e892e0fe82`  
		Last Modified: Tue, 23 Sep 2025 19:50:11 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f94e92357646159f3de34f7a59b35af379809eb95e8ca6cdebfc80f6bf415b5`  
		Last Modified: Tue, 23 Sep 2025 19:50:11 GMT  
		Size: 89.8 KB (89839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:db93141dbaaab047d2c5961e0f3a40a490a3bc4c02858e362684aac66d8f11cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ec5dfabfdd39f0aaf814e90273b851f03175e48b64cc6bdc82acd7e035dd64`

```dockerfile
```

-	Layers:
	-	`sha256:b3b0384cfc3d61d143a214949d2e595f859d287f885e4e4d78e634cc601b3ca2`  
		Last Modified: Tue, 23 Sep 2025 22:07:41 GMT  
		Size: 3.6 MB (3609940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15b8bd663afd20bb3f9e9dd8d1902aa8ea08259a6ff7149fc262d1757f040bfb`  
		Last Modified: Tue, 23 Sep 2025 22:07:42 GMT  
		Size: 13.9 KB (13947 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3473d74285345688dad026ef0917211d20aaac7a63891d8b253c51ac76c7f36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60205188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3780f0e6abc99ad711f80a483189a852bc2a1d2bd2d9ce913bc7f0a749388490`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1757289600'
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
	-	`sha256:00e024daab2d43f36749bffb01f2b299b405cff0659a8e4f4f00bb468dd24c27`  
		Last Modified: Mon, 08 Sep 2025 21:14:58 GMT  
		Size: 49.9 MB (49934721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67162de59cae8432f37018bdfca1926d8d40b34084a6e6ca535064ebafd11af7`  
		Last Modified: Tue, 23 Sep 2025 17:39:57 GMT  
		Size: 10.2 MB (10177061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bb81dbbd87423aed66a55483c3b6d0acb4129dabd3c0147e74c76b0addb550`  
		Last Modified: Tue, 23 Sep 2025 17:39:56 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba3ff27e7afe1dc3962ba33f3faa4fbaba125ab630cb86d1125223c943c68d6`  
		Last Modified: Tue, 23 Sep 2025 17:39:56 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03b9f2f2b5433c7d521cd2962c537a2863678d15ff9ec8e3d1f7d6a4677c1ca`  
		Last Modified: Tue, 23 Sep 2025 17:39:56 GMT  
		Size: 90.5 KB (90502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5f6b3b64165dd6cf8115298360e079d70eadbd2cb05021d0f0e61c82e695744f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631b4c7bfa49457dfcdf6c8869cf60c5f244c01f22f3bab8aca7e9c5ff4d4d68`

```dockerfile
```

-	Layers:
	-	`sha256:7d39ac1ae9919d67a330944d83252b6fba745ae3f16dce0326e07afcfb619d25`  
		Last Modified: Tue, 23 Sep 2025 19:07:54 GMT  
		Size: 3.6 MB (3611455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b646a4ca03999ebf0a0e86482bbb39a1c31c084ad7112cd593dc386c8241932f`  
		Last Modified: Tue, 23 Sep 2025 19:07:55 GMT  
		Size: 14.1 KB (14072 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:087bfe5c7fe5a858c0dad888bdae06c7aa709dd89a70dfd28b9efb1eecb2a247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61758851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9911b404ee218bf7821aafaf7618a81634351f6f5577a865753205cecbce39`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1757289600'
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
	-	`sha256:eb039ce3bcf3fbed73729096e510ae45e98c7db73d412a09aa57aaad6f2f6267`  
		Last Modified: Mon, 08 Sep 2025 21:12:53 GMT  
		Size: 51.1 MB (51113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc41e7d47140b0d1fc4152bc7af8595e60e5b75abcc8d92b17c1e4bccdc2777`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 10.6 MB (10552105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edeabcf2a16d8446d9f601b7a5f0e0dcc7eec713032a5af69f0e62133b4d0a5e`  
		Last Modified: Tue, 23 Sep 2025 17:35:57 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a81e3c095adac2afeafbb59a941a25173e7979c43c100a882514bea7877cf2`  
		Last Modified: Tue, 23 Sep 2025 17:36:00 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a5f5e7ce5e4c5bd3868fbeb258a1b9acc9bf9658887f081960ec7b90b4c574`  
		Last Modified: Tue, 23 Sep 2025 17:35:57 GMT  
		Size: 90.2 KB (90230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2b4e860b4c2cf391bdc9ff71e490d986221996da51ec3a24f0cfd46a85c4480c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62dabffd47060461fc93e44830dedddbd7576c04f5afea31f63b493c1da5551`

```dockerfile
```

-	Layers:
	-	`sha256:9896fe7c4d9ef11f9576f83857d7f2ba9fdadb7b07a9a04d20d5e2e494dd447f`  
		Last Modified: Tue, 23 Sep 2025 19:08:00 GMT  
		Size: 3.6 MB (3607901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09cc604acd1809bed7d56e0d91d55d2eec5d7d859506811fc30bc2c91a6f86fc`  
		Last Modified: Tue, 23 Sep 2025 19:08:01 GMT  
		Size: 13.9 KB (13919 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:3fe7c675223c4e0405d4207e24eb1e4c3bf19ee11a9646cf0e7619d6e62779e6
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
$ docker pull neurodebian@sha256:a35aa8b45c44873f50d11bb966c016c4668451a55520ef298bfa46fa311873a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60150471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6104e8936f061faa342c4c523fdfacfac26378d45d9486da91ddae637f479695`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1757289600'
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
	-	`sha256:8d64c6c7c21822ac171c4c396d70161707401d6d50d133075d661956f08dc756`  
		Last Modified: Mon, 08 Sep 2025 21:13:08 GMT  
		Size: 49.7 MB (49657990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144fde7d694dd5ef88504ba55ce29576ef669fa6f3df0c8853397b6a3268cbbe`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 10.4 MB (10399314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbf6772f1e0545288e07cf0ceaa3f94da2fc29c74d7eb03d4bf094e99392ae5`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fba2595e2127b79c17e4ae5386fc3f5c426141156e917da1355fbb85ccf90d`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f417ad3fc8c42aac0bc4283557ce36de1dc98cdfdd91eabb26c4a7b7d3de070e`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 89.8 KB (89844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f06a1a1687a3f978541c38dcb673e5ff3361f7b879268038c9e2420127745c0`  
		Last Modified: Tue, 23 Sep 2025 19:50:57 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2be98938edcce0a407fcfe2b626638987bd84491450fe88ebaec0cc09dcd1ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e0efac7157da5dd4116b8db93ba1fa1296880d93eff0a00171cf0cecee7910`

```dockerfile
```

-	Layers:
	-	`sha256:af1ba855b844937cc2f5a8faba90ea901d7c9070e32458e6762b67c378313e49`  
		Last Modified: Tue, 23 Sep 2025 22:07:46 GMT  
		Size: 3.6 MB (3609976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d04311730d3fcedc87b7d493ad4f221c9022f4283ba58e82cdcb99f34672705c`  
		Last Modified: Tue, 23 Sep 2025 22:07:47 GMT  
		Size: 16.0 KB (15974 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9191edad731c3777239ab7a6df02e8c3cca27fd39f070d3a9f2130a27b286529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60205498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed9d6ab91c97c1ce364b776c074b575641047e24efa1851b32dceb9d3e43f91`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1757289600'
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
	-	`sha256:00e024daab2d43f36749bffb01f2b299b405cff0659a8e4f4f00bb468dd24c27`  
		Last Modified: Mon, 08 Sep 2025 21:14:58 GMT  
		Size: 49.9 MB (49934721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81efd0f0dcca0cb336b828640e6827714cf6b6db92f89cd82e323f6982d7f4d`  
		Last Modified: Tue, 23 Sep 2025 17:39:59 GMT  
		Size: 10.2 MB (10176977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603959d5699befce3d731668bbda6ef5af594a431dacdcd4f999328e185fbf82`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e002eb0aadc14a90478115b718f1549b2e972b9c8b9828cfcf24af8768e48b6f`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbcb7eb4cc610f644f057f5935ee9846750de3ed5aa29b6b4626721d2881bc3`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 90.5 KB (90473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f379b3fb391ace6e8169e270dfe80ba47aa454ebabc6a261938b427e9ba848f`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:84290dc5531ab703d1ea0a46c4080e9bb469fb5ffa14f513534e950f69ab9aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b99802cb1d850e1aa7fdd8c934d54b5c43752f6d208c43ddb6954d3353ab6b5`

```dockerfile
```

-	Layers:
	-	`sha256:3e46be236b4284404936a8f6998febda1ad729b8427e99900db52dfd85f23c32`  
		Last Modified: Tue, 23 Sep 2025 19:08:01 GMT  
		Size: 3.6 MB (3611491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a6e5fd5021e1f648ebc119ba8cab091880a2c17c44168587834ec61baf52878`  
		Last Modified: Tue, 23 Sep 2025 19:08:02 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:acab89f48ba43732b4aa66549b33e99073d08cb0d8b4dda8f2068b22a2150a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61759091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed2e9dfd34d78d1208dab49205386f5cb5dac7477cf3eeffd318a45bfd13e2b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1757289600'
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
	-	`sha256:eb039ce3bcf3fbed73729096e510ae45e98c7db73d412a09aa57aaad6f2f6267`  
		Last Modified: Mon, 08 Sep 2025 21:12:53 GMT  
		Size: 51.1 MB (51113613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef9e924b51d56631ff7e60d9ffc923651a932453cc070c44c790dda109655cb`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 10.6 MB (10551936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a5c4260c5226a4139c1dcf60e7a5115ab5f76a7b0d9d8ab9dfba9e32017937`  
		Last Modified: Tue, 23 Sep 2025 17:35:57 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98aee0679f611ea7162c52e6ab4785f27f80c5589830cb5157d23e657c207730`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fd04207b73d5d0c0f97e7396b06c06e07035f1819525455162e75489f45e32`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 90.2 KB (90220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119bae56cac036245f6d4048fe985553edfdc542188b8fb42f75eb63b6c081c`  
		Last Modified: Tue, 23 Sep 2025 17:35:59 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:72c4c16e05b5307900604596e5f718afa79b1171da6da0bbd2e78516f68dee81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4dd3ed7a3d34c1598c331733008530b70861d2d4880f6fde569b86843d3972`

```dockerfile
```

-	Layers:
	-	`sha256:74c2a34baf1ea8506bb8987565d0762224ddd979d8096a23060702450fd2d660`  
		Last Modified: Tue, 23 Sep 2025 19:08:07 GMT  
		Size: 3.6 MB (3607937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad7f63ff5b26fd7dede37a98e92c1e59e3fcab2829d49ab90c1fc8f1296a48ec`  
		Last Modified: Tue, 23 Sep 2025 19:08:07 GMT  
		Size: 15.9 KB (15944 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:8e5fd833ef1fdbd0634a429ce619af13a0b3bc394a4316528e395989a2b7e559
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
$ docker pull neurodebian@sha256:b8554b98c7b61391bb22bd4a7220df7f7c62650527e0d5418399a94917423fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59662220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a057003cd756d9f5325107c7c4251c56e1861281d12bbfbe20b5a12828bd9cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed7aad3c42d8c3bcd905875cd29230e367d1c38916321ad3ab12c4fdb0d7214`  
		Last Modified: Tue, 23 Sep 2025 19:50:15 GMT  
		Size: 10.3 MB (10289604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b5a09c0af2cd1b2f3b536c610a8484aae29784608be965bc9a76f6adbaa4a2`  
		Last Modified: Tue, 23 Sep 2025 19:50:13 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f6f38bb43cac782ca903da5f508ccc0c581e9a68a8a8e69f171bdfa0c61e70`  
		Last Modified: Tue, 23 Sep 2025 19:50:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff7d4510024de4cd17cd7f0cd21f3979b98414430b20d3562fa40e36bbeec0e`  
		Last Modified: Tue, 23 Sep 2025 19:50:14 GMT  
		Size: 90.2 KB (90176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ac143161be3e17b7c8eafcd0a3d2cb85ddbbbc215ecf917aa9d531c2e6c28c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b72ef0681bd3bb94d50bac07af0c81640b7f02c0ea6f106e3115f463f5b5f6`

```dockerfile
```

-	Layers:
	-	`sha256:aa3f4c83d483d36764c0891f01c50ea9f2c8d0622d9d1b9889ab1cf350e68d9d`  
		Last Modified: Tue, 23 Sep 2025 22:07:36 GMT  
		Size: 3.6 MB (3612981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55df46487d54f44f5754ee59a2a3ad256b28ccf84ecd6f797b4af6e104aeb382`  
		Last Modified: Tue, 23 Sep 2025 22:07:37 GMT  
		Size: 14.3 KB (14293 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c21dbd0a1b16c4fb222391d8e8e637e2922cdaa24fe9ed526552317f113eec9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59810755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008b6ced829a9d58058b2cbab03447436e078b2409fe75b5b1378777ba39b2ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d54f0a8b8cdeb016765b4421672e7132d34ac6b326223b731d5282d5c3ae095`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 10.1 MB (10073260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ca08b2ff60dcd56cef5ab73acd2c160b4e06751f62df7e0e95d1bcfd11d8d6`  
		Last Modified: Tue, 23 Sep 2025 17:39:18 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e35bc05e600c15f0db597abe53e56f5133f1a07cef5ceef2dde74108818d40b`  
		Last Modified: Tue, 23 Sep 2025 17:39:18 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87503a3dead3a4605bff54bd22c67f01d31f31f6b7c17460c90ae59af2d30d76`  
		Last Modified: Tue, 23 Sep 2025 17:39:19 GMT  
		Size: 90.8 KB (90839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:20da5439101ef73faac42cf32c8dacca771cdd9cdce9a342d0499874e2dfdc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000c048359af5327f48f359238ffbbbf20737b7e60535c97db620c1ebe6f0cab`

```dockerfile
```

-	Layers:
	-	`sha256:c8c473610319b2e88f677aca463db980bd056b2466974dfa73007cbbb5f01c33`  
		Last Modified: Tue, 23 Sep 2025 19:07:45 GMT  
		Size: 3.6 MB (3614508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb37a93695cd94314c8d98c7d617488ec6ee93baa6906bb6aa6804b7f9e796f`  
		Last Modified: Tue, 23 Sep 2025 19:07:46 GMT  
		Size: 14.4 KB (14431 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:557a466129fe8cd12edbf882dc0ebf898652e8b101e0138a9fce8af68ef67f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61351348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e7b84e0788bd3a7eeacb70c4ab0929b84ccf10892c9650e34e5bec7ca21199`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768b3fdcc0892aba7d97f3db5214e7a8724b3691fbe410f5aec7c9f7729c19e4`  
		Last Modified: Tue, 23 Sep 2025 17:34:19 GMT  
		Size: 10.5 MB (10462915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13e953626a5863b8c7828fd4ed69028cf735723c389479008359be4d9edd990`  
		Last Modified: Tue, 23 Sep 2025 17:34:18 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980b88e4c67b14fb8d1d73a427f8fcdf3eb95789988d2d91ec6970cc6c22bd58`  
		Last Modified: Tue, 23 Sep 2025 17:34:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3482123fd30bdde26844e46aa5360dc605124e27e13b22a8e44866fbc344d156`  
		Last Modified: Tue, 23 Sep 2025 17:34:19 GMT  
		Size: 90.6 KB (90579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3b4d14f31a3774572ceef81ad84383cb0c1ae39ebd131510cfcda15a3630d172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f3fa91eb5042a491e37386d2d34c7c933cc12376225de8f5eac7702a61a2f`

```dockerfile
```

-	Layers:
	-	`sha256:93eaec6d2f1f521fc263252d9ca16cb3a360a3af7531bb55ec9c8264df60460c`  
		Last Modified: Tue, 23 Sep 2025 19:07:51 GMT  
		Size: 3.6 MB (3610930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5f4614670f64ec9fb8c7b72d96283e5b91deb0d9f10815b2ac4881be86ae82`  
		Last Modified: Tue, 23 Sep 2025 19:07:53 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:f7201d496a19f6c2d8a1f89f2bb7f27f8b320ece50e6d8ffd150fd501dda635b
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
$ docker pull neurodebian@sha256:d74480c4fb0d1aea0a60cb68b4dfef8091023d322dc86b7c19769106365595b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59662773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:721e07dac792da5b2ac44a59dfbd4f50647f9183fa34f4784bfb2a36cc969191`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304286e8d41b300322bd5ef5086cfa8d719a3b329d244e9982a79d086c44b1d8`  
		Last Modified: Tue, 23 Sep 2025 22:53:16 GMT  
		Size: 10.3 MB (10289746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa9f2a028d94e3c22db46a837a81396392ea689aaa4118be25c47bb5b375324`  
		Last Modified: Tue, 23 Sep 2025 20:16:40 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c4dfe087dbd4ea8bbfbd31d0d0eda058a05d76b97835953dcaa5c142a64645`  
		Last Modified: Tue, 23 Sep 2025 20:16:44 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d46510a601b4b4189265f8638e995c426e8f19d6f67de49916b018f6f7cde8`  
		Last Modified: Tue, 23 Sep 2025 20:16:49 GMT  
		Size: 90.1 KB (90143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa8b4b7362210cbd9b130d371c891566f8cc83046ee4ee42ad0d114b48f4aac`  
		Last Modified: Tue, 23 Sep 2025 20:16:52 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d4093664e2464d099b57fc22c993c6fb81a386b3722a625e2724cf6058a22b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bae71ae6a23d6a834292bb10943454e6dd6648a554dd098e8416b5395bf02e9`

```dockerfile
```

-	Layers:
	-	`sha256:967ec45e0f9fbe3c02a83631debb6dcbfb0f9a21f09ac17521e9c0695bad6396`  
		Last Modified: Tue, 23 Sep 2025 22:07:56 GMT  
		Size: 3.6 MB (3613021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ab5d9cd4119039f7280b04fcfe7173b52cc842979ed5780914ac981f275e023`  
		Last Modified: Tue, 23 Sep 2025 22:07:57 GMT  
		Size: 16.3 KB (16325 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1eda3906e3d74753dc6108406609474e17922bc4473c0650138d2a71e0bb0a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59811107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1c0ab49c63ddb928d1ea6152bce13a56e8924cf87b59b98426b5735b06a017`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8928402f9240101fa8045309f2d1f99869f404958b90ade93c18a6fdd5103b`  
		Last Modified: Tue, 23 Sep 2025 17:39:21 GMT  
		Size: 10.1 MB (10073166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc260bea759081fbc813dc13e45189e07a89ad889eb04898b83095ebe8e46f6`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7be6fa450a008c0111b995191dcbebe968fec4b2291cb9f77b640b8d90186b`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c083f97f9134022f86c20007997675be9039bd0cd5b261235fc0333b295336`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 90.8 KB (90839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c02e6d484f97370f3d3a31c333d86ab85c56434cf062ec9db96eafa89afbb58`  
		Last Modified: Tue, 23 Sep 2025 17:39:21 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:67f19ba1c382f706a6c0546d668de36db5eb279435eb55be0b971d0d1d6e0d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41fa20712a0c042f42ad63fb2ad11b46db8ea8e4742bcf4d3e9369a094bd33f`

```dockerfile
```

-	Layers:
	-	`sha256:072889b65b38c27822eae4197991fe09aab464f059df703c0ad31613b64ffe68`  
		Last Modified: Tue, 23 Sep 2025 19:08:17 GMT  
		Size: 3.6 MB (3614548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfa28fcb3ba4cc4a53499f985d3803766945bb3f97081ac0415fd7b7b58a8a4`  
		Last Modified: Tue, 23 Sep 2025 19:08:18 GMT  
		Size: 16.5 KB (16477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2685dd7fe3afbe2157a72c212a66ffebfa1465d998490f39ad7fcda33a6079de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61351708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcff7d47fc0d643368953858e2e160918fd389ce7a8454f06445f8f694148b92`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb41c38efac3c3a4e479715bbfbc2b0cf2daac281761c6f91ffab849e5c8190`  
		Last Modified: Tue, 23 Sep 2025 17:35:05 GMT  
		Size: 10.5 MB (10462867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500ab29cbf1ed8b8d382ae37afa2d978700800d7f839dbf340f2b3573a7e131d`  
		Last Modified: Tue, 23 Sep 2025 17:35:04 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351373291dcdae77241331e750e91a9d52b1632c6ef73f989f1801a1126abcbc`  
		Last Modified: Tue, 23 Sep 2025 17:35:04 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa920d26fee157ad165e0eeea4da5aa8faab9500938265f152c6cd6b98ec089`  
		Last Modified: Tue, 23 Sep 2025 17:35:05 GMT  
		Size: 90.5 KB (90535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31df9627b83b4bc4a24ead4a19c413ddfa015c8dd02d315d050d11654445897a`  
		Last Modified: Tue, 23 Sep 2025 17:35:04 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b8294a8060dfa8487b4aabb007bdb278688245077d6acb64e69b97a41e98e2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb7094164a2f8304232900ae7771326641faafedada4ae34e3f96b23f4b435e`

```dockerfile
```

-	Layers:
	-	`sha256:464f2f4ee7c536a30f535caa5b810a4fe3b192a5ac0e163b2bbc250ebe2f6f77`  
		Last Modified: Tue, 23 Sep 2025 19:08:22 GMT  
		Size: 3.6 MB (3610970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f90069b14333bca50c5c0537e5a3deaf9cb3036ecb495ff5dd8610331168857`  
		Last Modified: Tue, 23 Sep 2025 19:08:23 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json
