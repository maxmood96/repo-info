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

**does not exist** (yet?)

## `neurodebian:forky-non-free`

**does not exist** (yet?)

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

### `neurodebian:latest` - linux; amd64

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

### `neurodebian:latest` - unknown; unknown

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

### `neurodebian:latest` - linux; arm64 variant v8

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

### `neurodebian:latest` - unknown; unknown

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

### `neurodebian:latest` - linux; 386

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

### `neurodebian:latest` - unknown; unknown

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
		Last Modified: Fri, 13 Dec 2024 16:15:10 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e623044ed6d226bb08223597c0f380daf46067df42de48e52515dd8b6015bd9`  
		Last Modified: Wed, 01 Jan 2025 05:36:14 GMT  
		Size: 6.3 MB (6309037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df34ef8a3df44564cff9f91477c96045ed1348d5c6bacebb2c30da5ed1d67729`  
		Last Modified: Sun, 15 Dec 2024 06:11:04 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d9ecdc74a71cc7cfaf2b1635937b88fc90e48932874568379bd4948b83d9c0`  
		Last Modified: Sun, 15 Dec 2024 06:11:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4420bbd6a1e5e4067d6048b9cfc560b9b39df72d87d4ed9e93ebb3c7f8be97e6`  
		Last Modified: Sun, 15 Dec 2024 06:11:06 GMT  
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
		Last Modified: Wed, 08 Jan 2025 01:48:52 GMT  
		Size: 3.6 MB (3559094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ddfa355e9e60cc21afc4f6d9b0f6907ad2cd79edba64fdeafb408ff1ebf336c`  
		Last Modified: Tue, 07 Jan 2025 08:49:56 GMT  
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
		Last Modified: Fri, 13 Dec 2024 23:16:00 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Wed, 08 Jan 2025 01:48:55 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 07 Jan 2025 03:47:50 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 07 Jan 2025 00:52:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Wed, 08 Jan 2025 14:49:51 GMT  
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
		Last Modified: Wed, 08 Jan 2025 12:47:55 GMT  
		Size: 3.6 MB (3563973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bcd735f99065db42e22a630fcbdde19cc6d75b63789503857eba2885a0de8be`  
		Last Modified: Tue, 10 Jun 2025 10:05:15 GMT  
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
		Last Modified: Sun, 15 Dec 2024 10:37:49 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c500b7e81fb48a2ca8dfb944bf05a4434b38906509b44c8230cb468350330652`  
		Last Modified: Tue, 07 Jan 2025 06:45:11 GMT  
		Size: 6.6 MB (6636172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cba7baac1bbf19c4eff6cba1e463e4514023f61e5e4f99eabf003c60f53789`  
		Last Modified: Wed, 08 Jan 2025 11:49:52 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bbc8c8ecf4c50fb1afe9f838e8684a9f8283e6edf3aea752fba90ecdfb953c`  
		Last Modified: Mon, 06 Jan 2025 19:56:23 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38faa38e98066ab42e204ada314c609783c4d1432e9755b2bcb597ed43dd599b`  
		Last Modified: Tue, 07 Jan 2025 04:48:56 GMT  
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
		Last Modified: Tue, 07 Jan 2025 00:52:32 GMT  
		Size: 3.6 MB (3556335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a715947ef1aeb942d19d5f3d425c0a032538f9e6b2ee6340f7ab1c249910cdb`  
		Last Modified: Mon, 06 Jan 2025 22:56:02 GMT  
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
		Last Modified: Fri, 13 Dec 2024 16:15:10 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114eb8c7559544e979c7bc06d71d09eaa2cd00debd8cf4f03a56d8104b7699b3`  
		Last Modified: Wed, 01 Jan 2025 05:35:57 GMT  
		Size: 6.3 MB (6308996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff80e11993394c1dc9aaa17af36dfa33cca39fa8e0caabe1b3bf52e80a34369c`  
		Last Modified: Sun, 15 Dec 2024 06:10:39 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4eb1dc4c12753dfe02a45cea97e094916913c37268158aa3b340700e68143f`  
		Last Modified: Sun, 15 Dec 2024 06:10:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12f43e28b0e223dee7e963ea7a4ad3a48f843457e481ee84cfb74772191cd9`  
		Last Modified: Tue, 31 Dec 2024 09:28:35 GMT  
		Size: 91.4 KB (91443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405db61dc15551d8850b73eec4f6ecee2d15504c5d277afd2c8128e17ecf6611`  
		Last Modified: Mon, 06 Jan 2025 17:54:45 GMT  
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
		Last Modified: Mon, 06 Jan 2025 19:56:29 GMT  
		Size: 3.6 MB (3559130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7bb223c6e89608e9722bf8101c7626ae5724ae67e6be3bab333911378929ca4`  
		Last Modified: Wed, 08 Jan 2025 11:49:59 GMT  
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
		Last Modified: Fri, 13 Dec 2024 23:16:00 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Wed, 08 Jan 2025 01:48:55 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 07 Jan 2025 03:47:50 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 07 Jan 2025 00:52:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Wed, 08 Jan 2025 14:49:51 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c880850a32196b5042f578dfb72c4fa93d1ee7ebd60d71fa4d5fbe19814c1ac`  
		Last Modified: Tue, 07 Jan 2025 07:50:09 GMT  
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
		Last Modified: Mon, 06 Jan 2025 22:56:08 GMT  
		Size: 3.6 MB (3564009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c24f5aff628042c5046d45e533873a264167660d2769d5c6aa4aad04528fe9`  
		Last Modified: Wed, 08 Jan 2025 06:46:43 GMT  
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
		Last Modified: Sun, 15 Dec 2024 10:37:49 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998bde38fb7afd531148bc5ada8932ba6909774db1014c810250d2fed9705c28`  
		Last Modified: Mon, 06 Jan 2025 17:54:47 GMT  
		Size: 6.6 MB (6635982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff379f8e9bb8d25d6e0f0189f738f8b022e1073b791de493bf8117cc6d281ae`  
		Last Modified: Tue, 07 Jan 2025 05:49:13 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863c1b51d89e4dd4797ba1c7a7da71a5c460240254b1e7853212c5b2e920c1af`  
		Last Modified: Tue, 07 Jan 2025 23:52:05 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bc6338d9947bdf727b4f355b78ec884ccc098bacc03deb3d7965d5d04398bb`  
		Last Modified: Tue, 07 Jan 2025 02:49:57 GMT  
		Size: 91.6 KB (91629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deb6e8c73557a116710e67686758ffb933b5075a0bed69a3dae3ca0be59627d`  
		Last Modified: Mon, 06 Jan 2025 19:56:32 GMT  
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
		Last Modified: Tue, 07 Jan 2025 00:52:46 GMT  
		Size: 3.6 MB (3556371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d03ff36e1583fd5288b7e43255d4ae49d2af7984f1801d3d5ea02eae17b0cc6`  
		Last Modified: Tue, 07 Jan 2025 20:50:54 GMT  
		Size: 15.6 KB (15623 bytes)  
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
		Last Modified: Fri, 13 Dec 2024 15:34:48 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31fa211153a834040c35ecc855708df74ae143e0f067f5f29d4299bec783171`  
		Last Modified: Fri, 03 Jan 2025 23:08:15 GMT  
		Size: 6.3 MB (6309046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759be46808786c18908d758383834044fed05ddaf818585877931072aaa3bea3`  
		Last Modified: Tue, 07 Jan 2025 02:50:02 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9340f215c3f9e9497b17c7dcc21314a53d5553d70c1a45f9ecd9663aa523c`  
		Last Modified: Mon, 06 Jan 2025 19:56:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809dd25b48752fba0eeac0fcf5c38a88f0e12b0db0b022acf82ae7fafd98800f`  
		Last Modified: Tue, 31 Dec 2024 09:25:24 GMT  
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
		Last Modified: Tue, 07 Jan 2025 00:52:57 GMT  
		Size: 3.6 MB (3564266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291ee8d275476a4f56b64a69bb3c484a527878d207b0f47533dc5df2c24f9458`  
		Last Modified: Tue, 07 Jan 2025 00:52:57 GMT  
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
		Last Modified: Fri, 13 Dec 2024 18:18:26 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8640b31431e2f1a1a2b65b6fed2b7a4bcd6826c4d1cb17e4d8e1e9e2bf2ec5`  
		Last Modified: Tue, 07 Jan 2025 04:49:13 GMT  
		Size: 6.3 MB (6288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f67a6b589fb5f0c9202e6eb9aa7cc5ec0a7c2e67c81df4d2e3f8bc9603c4e9`  
		Last Modified: Tue, 07 Jan 2025 06:45:23 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96d02cd9c1d5c2742decbe351e194414adec825bee6bbd6263521be0a514665`  
		Last Modified: Tue, 07 Jan 2025 03:48:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d38c51092ac20a5bcd1dfc533de43a738889d192e62656482dc22f1505a79`  
		Last Modified: Tue, 07 Jan 2025 03:48:08 GMT  
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
		Last Modified: Tue, 07 Jan 2025 04:49:15 GMT  
		Size: 3.6 MB (3569145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a78c16c7a4e8d937b184fa40339df44fa15f714b5d50ea63d627b3763ab773`  
		Last Modified: Wed, 08 Jan 2025 00:48:58 GMT  
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
		Last Modified: Sun, 15 Dec 2024 23:07:15 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07d21ec843fdae56608290e710928213278f433f216169549f4105b0b7adcde`  
		Last Modified: Tue, 07 Jan 2025 03:48:10 GMT  
		Size: 6.6 MB (6636002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790ba6a36bbd0ddde077446c337522dff4905079f146ba4f81c5f1b1ba01508e`  
		Last Modified: Mon, 06 Jan 2025 22:56:19 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f988e696d1fd940f6f8a41f61db71109214ffa05a741e7ad19280fab3317b7a6`  
		Last Modified: Mon, 06 Jan 2025 19:56:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7105d8b802d7cbbf45432b1a9323e287ee890f7b63ac52b16e684f8aa59aa436`  
		Last Modified: Tue, 07 Jan 2025 03:48:10 GMT  
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
		Last Modified: Mon, 06 Jan 2025 17:55:01 GMT  
		Size: 3.6 MB (3561502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda46b32b1387c0fd07559cd518cb696c94a4a839d171f21cf6124f57cee113a`  
		Last Modified: Tue, 07 Jan 2025 00:53:02 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:34:48 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507e5811b953238ff193b1168d33f51c6e9d529f200a09d5a7cacc81a3cc8c3`  
		Last Modified: Mon, 06 Jan 2025 19:56:45 GMT  
		Size: 6.3 MB (6309097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53110b5d9fe921d17db007a1ddcf5a14b209223be44404d7367639af0432a720`  
		Last Modified: Mon, 06 Jan 2025 19:56:45 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073121ed00d2745775e339f48a955b95fe1cf8f720671dcb447fc1ed84db92f`  
		Last Modified: Tue, 07 Jan 2025 08:50:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a4d13654e7924d6b2b37ec66b136d37c2be5c0336ea4c05ed6c366e2a4fd3f`  
		Last Modified: Tue, 31 Dec 2024 09:25:48 GMT  
		Size: 91.4 KB (91421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8461a91abccfb6a0564642a71b515e4966ed0f07a5adb19dea1de7fda249aaf0`  
		Last Modified: Tue, 31 Dec 2024 09:25:48 GMT  
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
		Last Modified: Tue, 07 Jan 2025 09:46:59 GMT  
		Size: 3.6 MB (3564302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97d1de4b535410fddab63f0e6af15dfaa00cec28ba8c0fde0a15678db848775`  
		Last Modified: Tue, 07 Jan 2025 04:49:25 GMT  
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
		Last Modified: Fri, 13 Dec 2024 18:18:26 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8640b31431e2f1a1a2b65b6fed2b7a4bcd6826c4d1cb17e4d8e1e9e2bf2ec5`  
		Last Modified: Tue, 07 Jan 2025 04:49:13 GMT  
		Size: 6.3 MB (6288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f67a6b589fb5f0c9202e6eb9aa7cc5ec0a7c2e67c81df4d2e3f8bc9603c4e9`  
		Last Modified: Tue, 07 Jan 2025 06:45:23 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96d02cd9c1d5c2742decbe351e194414adec825bee6bbd6263521be0a514665`  
		Last Modified: Tue, 07 Jan 2025 03:48:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d38c51092ac20a5bcd1dfc533de43a738889d192e62656482dc22f1505a79`  
		Last Modified: Tue, 07 Jan 2025 03:48:08 GMT  
		Size: 92.2 KB (92158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da18a25c93d7133b2d4097e549a323142182e4dd20d54315927b6bd6573eb0f1`  
		Last Modified: Tue, 07 Jan 2025 02:50:12 GMT  
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
		Last Modified: Tue, 07 Jan 2025 03:48:15 GMT  
		Size: 3.6 MB (3569181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37b47d54c077c2ac6d602d5b546c068ab8e54b2c34442bb70ec6ca92ca86216`  
		Last Modified: Wed, 08 Jan 2025 12:48:20 GMT  
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
		Last Modified: Sun, 15 Dec 2024 23:07:15 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e886790f9afca68021d7c75698a1217a115b9cc1ad35a2810b2d8b0ad55f3`  
		Last Modified: Wed, 08 Jan 2025 00:49:05 GMT  
		Size: 6.6 MB (6635953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7250eb870a6e7d1ba2c1af2ca41ebfa2fb763a5be83d1710296ff798161459c4`  
		Last Modified: Tue, 07 Jan 2025 02:50:13 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143e50a785fba3cd83cef1e55edff4f0d54e965cede0048ee57f596d5735e0a`  
		Last Modified: Mon, 06 Jan 2025 17:55:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd92cccb8507bf0ea24147acd06ddac399895aa65bc91c02c25f650bd8c41174`  
		Last Modified: Tue, 07 Jan 2025 00:53:11 GMT  
		Size: 91.6 KB (91598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c62cefd1610f7333f6f871c1794e559b2115e00c5863260f9ddedd99769cf8`  
		Last Modified: Wed, 08 Jan 2025 01:49:22 GMT  
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
		Last Modified: Mon, 06 Jan 2025 22:56:28 GMT  
		Size: 3.6 MB (3561538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2606e6a1a87f3ded6407b0d5258d8218f3da05be49ac5201a62941c4296cdb35`  
		Last Modified: Wed, 08 Jan 2025 14:50:26 GMT  
		Size: 15.7 KB (15662 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

**does not exist** (yet?)

## `neurodebian:nd140-non-free`

**does not exist** (yet?)

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
$ docker pull neurodebian@sha256:f95676da88045789e619860caeb6a3ecad7e5735e7fe3cba9bc0245f6499fa2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:d38770387a1f54d95d0d558099909093e51c2a541d725a169a3ab440228ce641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e059b96cc5ab2387c1bb2485d9de3fe3aa2dab08159f4e56de08657ed279f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aae2be978b6887ba33cc355eb60849e9a4b6494da48dbc2025ec215fc048bbd`  
		Last Modified: Fri, 09 May 2025 17:34:34 GMT  
		Size: 3.6 MB (3561550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214a87e3f5642da384965dace0ef6f6fe356aeebd976cea08d1deb25cc5b17cc`  
		Last Modified: Fri, 09 May 2025 13:30:57 GMT  
		Size: 1.9 KB (1907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c2ffabb65505adc1a9bd197602a784b5362d2bf73c24ab87ff05d5de31986b`  
		Last Modified: Fri, 09 May 2025 13:30:57 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418af0f32ee06323cc96c6ebd9014c231ad3deaa60e018b922a41d15df29cd9e`  
		Last Modified: Fri, 09 May 2025 13:30:57 GMT  
		Size: 102.8 KB (102849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d05f6938da9aeb0879b1fe995f7e53f824b9806df54a2cf758869d5a75b9fd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3bb6b2ab29942ba9926b585f6a9f2762e3332b5b0917f6c506a00cb07af85`

```dockerfile
```

-	Layers:
	-	`sha256:db5db1fcebc99c5ee245340feaabb7749eaa8dd62337d6b75728edd76c2e33a1`  
		Last Modified: Wed, 11 Jun 2025 19:44:40 GMT  
		Size: 2.0 MB (1988007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae603c4f8c4fdbb75e2ff13d822ac64719e2cc5269f96c64fbd4e9433d674d53`  
		Last Modified: Wed, 11 Jun 2025 19:46:43 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9ff983cae8fa779ca9d445f0e2e30c9c0c03e867cff63e93ec397123b526af1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9506d7bae42cf7450aa75eaeb8571087a3a9d4066fc59a980c2149e19578d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac21e8e96238695c860d38f337d7bc1fc8004ea7c02420374175bd455adc01`  
		Last Modified: Wed, 11 Jun 2025 19:42:40 GMT  
		Size: 3.6 MB (3560024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc1ea305697372c2857b25e00b899c927cb6bc69155e067e49c0a9bba9402a`  
		Last Modified: Wed, 11 Jun 2025 19:47:27 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b43beb4a469f9bf1d5fbbde21ed17e9307737945bc57d9f78fc561d40e08ea`  
		Last Modified: Wed, 11 Jun 2025 19:47:49 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861dc62479460407739b1ccc0c1b1ed34a4710f546a7bb95fdfa45af3b8efd3c`  
		Last Modified: Wed, 11 Jun 2025 19:46:32 GMT  
		Size: 103.3 KB (103339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:222ce1225e4552dab3c723682de0a2272dd746e75ef288a430f54e46046c4985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de3d7a56bd63248962b3eb96296da8be24233a5f3739114ca94981c5ccecf8a`

```dockerfile
```

-	Layers:
	-	`sha256:691e9a8ce459d8732c2d0bfe0a5462ebd479d481a963330437c6d61ca42d888c`  
		Last Modified: Wed, 11 Jun 2025 19:39:31 GMT  
		Size: 2.0 MB (1989052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c66f9e1f8f25f8e1de91b113698830913584ff5a51823d5484ec6d26a10084`  
		Last Modified: Wed, 11 Jun 2025 19:39:08 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:69ce90ed413297d173afe360aad6f52bb5176e84eca7931478cd30ca79a58961
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:13066bdb3f041d79fea341879cf32fc99e1501130aba61e38b5bb537e26c6d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e766d4c7c665af01ecdf3c7f5ebacdb666da09a8f6a3fc562abc8135cc5e5b1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5d60262949712c1e9b418187e3cc8bd5f8d0cd29eb97c9e363914cedaa63b`  
		Last Modified: Fri, 09 May 2025 17:37:14 GMT  
		Size: 3.6 MB (3561531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d4ccf25a7e89dd343d5f776bf03085f2ba18bbad5a4100ece345624e0a595c`  
		Last Modified: Fri, 09 May 2025 13:51:44 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53011f9a2cfb2befb053a53ab616fbc8cdc2c34c7c16c3d64268caf75936a28d`  
		Last Modified: Fri, 09 May 2025 13:51:44 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d8f4ff9e91fa0098e89a942d5178c56e58307eeddb25322eb98cb14237292c`  
		Last Modified: Fri, 09 May 2025 13:51:44 GMT  
		Size: 102.8 KB (102845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f18bdc3a399429a3003a5facfc548c193056b9f8a3c92159a30cdc1478fdfc`  
		Last Modified: Fri, 09 May 2025 13:51:44 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c63cacdcdeb7eb72ae8539221ee0ebcb57c3925d98bbc09a2a6ec531638dff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c783b424c09b07cd1ef4bfbe1afb9b6a360e746ed91c3589067e70bcefa6ac7a`

```dockerfile
```

-	Layers:
	-	`sha256:0e6a2844b7765ed34907f15e7585e8bdebc12f3faadefd03864a0f5d02a826d0`  
		Last Modified: Wed, 11 Jun 2025 20:49:22 GMT  
		Size: 2.0 MB (1988043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314f1c1506cd318e08789d785bcc4374c81b8056d15a4514197f223b08c7268a`  
		Last Modified: Wed, 11 Jun 2025 20:52:00 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a790631dcdafe28f015c5c0479912489674be9f8f6443c5baa269296a9aac686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6ad30b4f18c93b1b8b0d5ab83d85d1a12a4e4200c5a5b3d74087d39e1af734`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac21e8e96238695c860d38f337d7bc1fc8004ea7c02420374175bd455adc01`  
		Last Modified: Wed, 11 Jun 2025 19:42:40 GMT  
		Size: 3.6 MB (3560024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc1ea305697372c2857b25e00b899c927cb6bc69155e067e49c0a9bba9402a`  
		Last Modified: Wed, 11 Jun 2025 19:47:27 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b43beb4a469f9bf1d5fbbde21ed17e9307737945bc57d9f78fc561d40e08ea`  
		Last Modified: Wed, 11 Jun 2025 19:47:49 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861dc62479460407739b1ccc0c1b1ed34a4710f546a7bb95fdfa45af3b8efd3c`  
		Last Modified: Wed, 11 Jun 2025 19:46:32 GMT  
		Size: 103.3 KB (103339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c89c90922ffd5d5f4ad5e74b112d2030c727ce2904398c5ceef67660d3c259`  
		Last Modified: Wed, 11 Jun 2025 21:01:04 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f372e8ab37fe59a92e06d06cc943b4f987a2b0248f30c3165bfed88b8836e189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc218ebea555829040d03a4a15c0f5df5da7efb29ac615a2891b238c37f82455`

```dockerfile
```

-	Layers:
	-	`sha256:acbad4c4e58f95388548674e8a027f84744a36ba854c40bcfe075c25f9afc1c0`  
		Last Modified: Wed, 11 Jun 2025 20:49:12 GMT  
		Size: 2.0 MB (1989088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d3aee94659ed4646a4d848ec65ba5ffaaf28e5be2b04557c641715a24f788f`  
		Last Modified: Wed, 11 Jun 2025 20:51:33 GMT  
		Size: 16.3 KB (16345 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd25.04`

**does not exist** (yet?)

## `neurodebian:nd25.04-non-free`

**does not exist** (yet?)

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:f95676da88045789e619860caeb6a3ecad7e5735e7fe3cba9bc0245f6499fa2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:d38770387a1f54d95d0d558099909093e51c2a541d725a169a3ab440228ce641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e059b96cc5ab2387c1bb2485d9de3fe3aa2dab08159f4e56de08657ed279f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aae2be978b6887ba33cc355eb60849e9a4b6494da48dbc2025ec215fc048bbd`  
		Last Modified: Fri, 09 May 2025 17:34:34 GMT  
		Size: 3.6 MB (3561550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214a87e3f5642da384965dace0ef6f6fe356aeebd976cea08d1deb25cc5b17cc`  
		Last Modified: Fri, 09 May 2025 13:30:57 GMT  
		Size: 1.9 KB (1907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c2ffabb65505adc1a9bd197602a784b5362d2bf73c24ab87ff05d5de31986b`  
		Last Modified: Fri, 09 May 2025 13:30:57 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418af0f32ee06323cc96c6ebd9014c231ad3deaa60e018b922a41d15df29cd9e`  
		Last Modified: Fri, 09 May 2025 13:30:57 GMT  
		Size: 102.8 KB (102849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d05f6938da9aeb0879b1fe995f7e53f824b9806df54a2cf758869d5a75b9fd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb3bb6b2ab29942ba9926b585f6a9f2762e3332b5b0917f6c506a00cb07af85`

```dockerfile
```

-	Layers:
	-	`sha256:db5db1fcebc99c5ee245340feaabb7749eaa8dd62337d6b75728edd76c2e33a1`  
		Last Modified: Wed, 11 Jun 2025 19:44:40 GMT  
		Size: 2.0 MB (1988007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae603c4f8c4fdbb75e2ff13d822ac64719e2cc5269f96c64fbd4e9433d674d53`  
		Last Modified: Wed, 11 Jun 2025 19:46:43 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9ff983cae8fa779ca9d445f0e2e30c9c0c03e867cff63e93ec397123b526af1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9506d7bae42cf7450aa75eaeb8571087a3a9d4066fc59a980c2149e19578d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac21e8e96238695c860d38f337d7bc1fc8004ea7c02420374175bd455adc01`  
		Last Modified: Wed, 11 Jun 2025 19:42:40 GMT  
		Size: 3.6 MB (3560024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc1ea305697372c2857b25e00b899c927cb6bc69155e067e49c0a9bba9402a`  
		Last Modified: Wed, 11 Jun 2025 19:47:27 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b43beb4a469f9bf1d5fbbde21ed17e9307737945bc57d9f78fc561d40e08ea`  
		Last Modified: Wed, 11 Jun 2025 19:47:49 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861dc62479460407739b1ccc0c1b1ed34a4710f546a7bb95fdfa45af3b8efd3c`  
		Last Modified: Wed, 11 Jun 2025 19:46:32 GMT  
		Size: 103.3 KB (103339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:222ce1225e4552dab3c723682de0a2272dd746e75ef288a430f54e46046c4985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de3d7a56bd63248962b3eb96296da8be24233a5f3739114ca94981c5ccecf8a`

```dockerfile
```

-	Layers:
	-	`sha256:691e9a8ce459d8732c2d0bfe0a5462ebd479d481a963330437c6d61ca42d888c`  
		Last Modified: Wed, 11 Jun 2025 19:39:31 GMT  
		Size: 2.0 MB (1989052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c66f9e1f8f25f8e1de91b113698830913584ff5a51823d5484ec6d26a10084`  
		Last Modified: Wed, 11 Jun 2025 19:39:08 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:69ce90ed413297d173afe360aad6f52bb5176e84eca7931478cd30ca79a58961
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:13066bdb3f041d79fea341879cf32fc99e1501130aba61e38b5bb537e26c6d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e766d4c7c665af01ecdf3c7f5ebacdb666da09a8f6a3fc562abc8135cc5e5b1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c5d60262949712c1e9b418187e3cc8bd5f8d0cd29eb97c9e363914cedaa63b`  
		Last Modified: Fri, 09 May 2025 17:37:14 GMT  
		Size: 3.6 MB (3561531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4d4ccf25a7e89dd343d5f776bf03085f2ba18bbad5a4100ece345624e0a595c`  
		Last Modified: Fri, 09 May 2025 13:51:44 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53011f9a2cfb2befb053a53ab616fbc8cdc2c34c7c16c3d64268caf75936a28d`  
		Last Modified: Fri, 09 May 2025 13:51:44 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d8f4ff9e91fa0098e89a942d5178c56e58307eeddb25322eb98cb14237292c`  
		Last Modified: Fri, 09 May 2025 13:51:44 GMT  
		Size: 102.8 KB (102845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f18bdc3a399429a3003a5facfc548c193056b9f8a3c92159a30cdc1478fdfc`  
		Last Modified: Fri, 09 May 2025 13:51:44 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c63cacdcdeb7eb72ae8539221ee0ebcb57c3925d98bbc09a2a6ec531638dff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c783b424c09b07cd1ef4bfbe1afb9b6a360e746ed91c3589067e70bcefa6ac7a`

```dockerfile
```

-	Layers:
	-	`sha256:0e6a2844b7765ed34907f15e7585e8bdebc12f3faadefd03864a0f5d02a826d0`  
		Last Modified: Wed, 11 Jun 2025 20:49:22 GMT  
		Size: 2.0 MB (1988043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314f1c1506cd318e08789d785bcc4374c81b8056d15a4514197f223b08c7268a`  
		Last Modified: Wed, 11 Jun 2025 20:52:00 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a790631dcdafe28f015c5c0479912489674be9f8f6443c5baa269296a9aac686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6ad30b4f18c93b1b8b0d5ab83d85d1a12a4e4200c5a5b3d74087d39e1af734`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbac21e8e96238695c860d38f337d7bc1fc8004ea7c02420374175bd455adc01`  
		Last Modified: Wed, 11 Jun 2025 19:42:40 GMT  
		Size: 3.6 MB (3560024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfc1ea305697372c2857b25e00b899c927cb6bc69155e067e49c0a9bba9402a`  
		Last Modified: Wed, 11 Jun 2025 19:47:27 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b43beb4a469f9bf1d5fbbde21ed17e9307737945bc57d9f78fc561d40e08ea`  
		Last Modified: Wed, 11 Jun 2025 19:47:49 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861dc62479460407739b1ccc0c1b1ed34a4710f546a7bb95fdfa45af3b8efd3c`  
		Last Modified: Wed, 11 Jun 2025 19:46:32 GMT  
		Size: 103.3 KB (103339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c89c90922ffd5d5f4ad5e74b112d2030c727ce2904398c5ceef67660d3c259`  
		Last Modified: Wed, 11 Jun 2025 21:01:04 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f372e8ab37fe59a92e06d06cc943b4f987a2b0248f30c3165bfed88b8836e189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc218ebea555829040d03a4a15c0f5df5da7efb29ac615a2891b238c37f82455`

```dockerfile
```

-	Layers:
	-	`sha256:acbad4c4e58f95388548674e8a027f84744a36ba854c40bcfe075c25f9afc1c0`  
		Last Modified: Wed, 11 Jun 2025 20:49:12 GMT  
		Size: 2.0 MB (1989088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d3aee94659ed4646a4d848ec65ba5ffaaf28e5be2b04557c641715a24f788f`  
		Last Modified: Wed, 11 Jun 2025 20:51:33 GMT  
		Size: 16.3 KB (16345 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

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

### `neurodebian:non-free` - linux; amd64

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

### `neurodebian:non-free` - unknown; unknown

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

### `neurodebian:non-free` - linux; arm64 variant v8

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

### `neurodebian:non-free` - unknown; unknown

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

### `neurodebian:non-free` - linux; 386

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

### `neurodebian:non-free` - unknown; unknown

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

## `neurodebian:plucky`

**does not exist** (yet?)

## `neurodebian:plucky-non-free`

**does not exist** (yet?)

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
		Last Modified: Fri, 13 Dec 2024 16:15:10 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e623044ed6d226bb08223597c0f380daf46067df42de48e52515dd8b6015bd9`  
		Last Modified: Wed, 01 Jan 2025 05:36:14 GMT  
		Size: 6.3 MB (6309037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df34ef8a3df44564cff9f91477c96045ed1348d5c6bacebb2c30da5ed1d67729`  
		Last Modified: Sun, 15 Dec 2024 06:11:04 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d9ecdc74a71cc7cfaf2b1635937b88fc90e48932874568379bd4948b83d9c0`  
		Last Modified: Sun, 15 Dec 2024 06:11:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4420bbd6a1e5e4067d6048b9cfc560b9b39df72d87d4ed9e93ebb3c7f8be97e6`  
		Last Modified: Sun, 15 Dec 2024 06:11:06 GMT  
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
		Last Modified: Wed, 08 Jan 2025 01:48:52 GMT  
		Size: 3.6 MB (3559094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ddfa355e9e60cc21afc4f6d9b0f6907ad2cd79edba64fdeafb408ff1ebf336c`  
		Last Modified: Tue, 07 Jan 2025 08:49:56 GMT  
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
		Last Modified: Fri, 13 Dec 2024 23:16:00 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Wed, 08 Jan 2025 01:48:55 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 07 Jan 2025 03:47:50 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 07 Jan 2025 00:52:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Wed, 08 Jan 2025 14:49:51 GMT  
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
		Last Modified: Wed, 08 Jan 2025 12:47:55 GMT  
		Size: 3.6 MB (3563973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bcd735f99065db42e22a630fcbdde19cc6d75b63789503857eba2885a0de8be`  
		Last Modified: Tue, 10 Jun 2025 10:05:15 GMT  
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
		Last Modified: Sun, 15 Dec 2024 10:37:49 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c500b7e81fb48a2ca8dfb944bf05a4434b38906509b44c8230cb468350330652`  
		Last Modified: Tue, 07 Jan 2025 06:45:11 GMT  
		Size: 6.6 MB (6636172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cba7baac1bbf19c4eff6cba1e463e4514023f61e5e4f99eabf003c60f53789`  
		Last Modified: Wed, 08 Jan 2025 11:49:52 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bbc8c8ecf4c50fb1afe9f838e8684a9f8283e6edf3aea752fba90ecdfb953c`  
		Last Modified: Mon, 06 Jan 2025 19:56:23 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38faa38e98066ab42e204ada314c609783c4d1432e9755b2bcb597ed43dd599b`  
		Last Modified: Tue, 07 Jan 2025 04:48:56 GMT  
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
		Last Modified: Tue, 07 Jan 2025 00:52:32 GMT  
		Size: 3.6 MB (3556335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a715947ef1aeb942d19d5f3d425c0a032538f9e6b2ee6340f7ab1c249910cdb`  
		Last Modified: Mon, 06 Jan 2025 22:56:02 GMT  
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
		Last Modified: Fri, 13 Dec 2024 16:15:10 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114eb8c7559544e979c7bc06d71d09eaa2cd00debd8cf4f03a56d8104b7699b3`  
		Last Modified: Wed, 01 Jan 2025 05:35:57 GMT  
		Size: 6.3 MB (6308996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff80e11993394c1dc9aaa17af36dfa33cca39fa8e0caabe1b3bf52e80a34369c`  
		Last Modified: Sun, 15 Dec 2024 06:10:39 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4eb1dc4c12753dfe02a45cea97e094916913c37268158aa3b340700e68143f`  
		Last Modified: Sun, 15 Dec 2024 06:10:37 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12f43e28b0e223dee7e963ea7a4ad3a48f843457e481ee84cfb74772191cd9`  
		Last Modified: Tue, 31 Dec 2024 09:28:35 GMT  
		Size: 91.4 KB (91443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405db61dc15551d8850b73eec4f6ecee2d15504c5d277afd2c8128e17ecf6611`  
		Last Modified: Mon, 06 Jan 2025 17:54:45 GMT  
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
		Last Modified: Mon, 06 Jan 2025 19:56:29 GMT  
		Size: 3.6 MB (3559130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7bb223c6e89608e9722bf8101c7626ae5724ae67e6be3bab333911378929ca4`  
		Last Modified: Wed, 08 Jan 2025 11:49:59 GMT  
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
		Last Modified: Fri, 13 Dec 2024 23:16:00 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c1944b6bf321c80bca628a1f2806106275b5823b1d9a2194d80db72c1240d0`  
		Last Modified: Wed, 08 Jan 2025 01:48:55 GMT  
		Size: 6.3 MB (6288605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f848cf5ceeefd58f0b25aad8a4ae18f3778a65f33fc9460661f7b5f4b7e340e`  
		Last Modified: Tue, 07 Jan 2025 03:47:50 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f54f177bb5980856b76068107daf64a196986c4cab67e6faf6eaf3ed6dda566`  
		Last Modified: Tue, 07 Jan 2025 00:52:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410851795a0d0599053b940c07c6a163f0727fc402dd559169c25bd9de9ec7eb`  
		Last Modified: Wed, 08 Jan 2025 14:49:51 GMT  
		Size: 92.2 KB (92218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c880850a32196b5042f578dfb72c4fa93d1ee7ebd60d71fa4d5fbe19814c1ac`  
		Last Modified: Tue, 07 Jan 2025 07:50:09 GMT  
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
		Last Modified: Mon, 06 Jan 2025 22:56:08 GMT  
		Size: 3.6 MB (3564009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c24f5aff628042c5046d45e533873a264167660d2769d5c6aa4aad04528fe9`  
		Last Modified: Wed, 08 Jan 2025 06:46:43 GMT  
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
		Last Modified: Sun, 15 Dec 2024 10:37:49 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998bde38fb7afd531148bc5ada8932ba6909774db1014c810250d2fed9705c28`  
		Last Modified: Mon, 06 Jan 2025 17:54:47 GMT  
		Size: 6.6 MB (6635982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff379f8e9bb8d25d6e0f0189f738f8b022e1073b791de493bf8117cc6d281ae`  
		Last Modified: Tue, 07 Jan 2025 05:49:13 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863c1b51d89e4dd4797ba1c7a7da71a5c460240254b1e7853212c5b2e920c1af`  
		Last Modified: Tue, 07 Jan 2025 23:52:05 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bc6338d9947bdf727b4f355b78ec884ccc098bacc03deb3d7965d5d04398bb`  
		Last Modified: Tue, 07 Jan 2025 02:49:57 GMT  
		Size: 91.6 KB (91629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5deb6e8c73557a116710e67686758ffb933b5075a0bed69a3dae3ca0be59627d`  
		Last Modified: Mon, 06 Jan 2025 19:56:32 GMT  
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
		Last Modified: Tue, 07 Jan 2025 00:52:46 GMT  
		Size: 3.6 MB (3556371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d03ff36e1583fd5288b7e43255d4ae49d2af7984f1801d3d5ea02eae17b0cc6`  
		Last Modified: Tue, 07 Jan 2025 20:50:54 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:34:48 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31fa211153a834040c35ecc855708df74ae143e0f067f5f29d4299bec783171`  
		Last Modified: Fri, 03 Jan 2025 23:08:15 GMT  
		Size: 6.3 MB (6309046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759be46808786c18908d758383834044fed05ddaf818585877931072aaa3bea3`  
		Last Modified: Tue, 07 Jan 2025 02:50:02 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b9340f215c3f9e9497b17c7dcc21314a53d5553d70c1a45f9ecd9663aa523c`  
		Last Modified: Mon, 06 Jan 2025 19:56:38 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809dd25b48752fba0eeac0fcf5c38a88f0e12b0db0b022acf82ae7fafd98800f`  
		Last Modified: Tue, 31 Dec 2024 09:25:24 GMT  
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
		Last Modified: Tue, 07 Jan 2025 00:52:57 GMT  
		Size: 3.6 MB (3564266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291ee8d275476a4f56b64a69bb3c484a527878d207b0f47533dc5df2c24f9458`  
		Last Modified: Tue, 07 Jan 2025 00:52:57 GMT  
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
		Last Modified: Fri, 13 Dec 2024 18:18:26 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8640b31431e2f1a1a2b65b6fed2b7a4bcd6826c4d1cb17e4d8e1e9e2bf2ec5`  
		Last Modified: Tue, 07 Jan 2025 04:49:13 GMT  
		Size: 6.3 MB (6288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f67a6b589fb5f0c9202e6eb9aa7cc5ec0a7c2e67c81df4d2e3f8bc9603c4e9`  
		Last Modified: Tue, 07 Jan 2025 06:45:23 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96d02cd9c1d5c2742decbe351e194414adec825bee6bbd6263521be0a514665`  
		Last Modified: Tue, 07 Jan 2025 03:48:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d38c51092ac20a5bcd1dfc533de43a738889d192e62656482dc22f1505a79`  
		Last Modified: Tue, 07 Jan 2025 03:48:08 GMT  
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
		Last Modified: Tue, 07 Jan 2025 04:49:15 GMT  
		Size: 3.6 MB (3569145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a78c16c7a4e8d937b184fa40339df44fa15f714b5d50ea63d627b3763ab773`  
		Last Modified: Wed, 08 Jan 2025 00:48:58 GMT  
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
		Last Modified: Sun, 15 Dec 2024 23:07:15 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07d21ec843fdae56608290e710928213278f433f216169549f4105b0b7adcde`  
		Last Modified: Tue, 07 Jan 2025 03:48:10 GMT  
		Size: 6.6 MB (6636002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790ba6a36bbd0ddde077446c337522dff4905079f146ba4f81c5f1b1ba01508e`  
		Last Modified: Mon, 06 Jan 2025 22:56:19 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f988e696d1fd940f6f8a41f61db71109214ffa05a741e7ad19280fab3317b7a6`  
		Last Modified: Mon, 06 Jan 2025 19:56:41 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7105d8b802d7cbbf45432b1a9323e287ee890f7b63ac52b16e684f8aa59aa436`  
		Last Modified: Tue, 07 Jan 2025 03:48:10 GMT  
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
		Last Modified: Mon, 06 Jan 2025 17:55:01 GMT  
		Size: 3.6 MB (3561502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda46b32b1387c0fd07559cd518cb696c94a4a839d171f21cf6124f57cee113a`  
		Last Modified: Tue, 07 Jan 2025 00:53:02 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:34:48 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4507e5811b953238ff193b1168d33f51c6e9d529f200a09d5a7cacc81a3cc8c3`  
		Last Modified: Mon, 06 Jan 2025 19:56:45 GMT  
		Size: 6.3 MB (6309097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53110b5d9fe921d17db007a1ddcf5a14b209223be44404d7367639af0432a720`  
		Last Modified: Mon, 06 Jan 2025 19:56:45 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073121ed00d2745775e339f48a955b95fe1cf8f720671dcb447fc1ed84db92f`  
		Last Modified: Tue, 07 Jan 2025 08:50:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a4d13654e7924d6b2b37ec66b136d37c2be5c0336ea4c05ed6c366e2a4fd3f`  
		Last Modified: Tue, 31 Dec 2024 09:25:48 GMT  
		Size: 91.4 KB (91421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8461a91abccfb6a0564642a71b515e4966ed0f07a5adb19dea1de7fda249aaf0`  
		Last Modified: Tue, 31 Dec 2024 09:25:48 GMT  
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
		Last Modified: Tue, 07 Jan 2025 09:46:59 GMT  
		Size: 3.6 MB (3564302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c97d1de4b535410fddab63f0e6af15dfaa00cec28ba8c0fde0a15678db848775`  
		Last Modified: Tue, 07 Jan 2025 04:49:25 GMT  
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
		Last Modified: Fri, 13 Dec 2024 18:18:26 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8640b31431e2f1a1a2b65b6fed2b7a4bcd6826c4d1cb17e4d8e1e9e2bf2ec5`  
		Last Modified: Tue, 07 Jan 2025 04:49:13 GMT  
		Size: 6.3 MB (6288606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f67a6b589fb5f0c9202e6eb9aa7cc5ec0a7c2e67c81df4d2e3f8bc9603c4e9`  
		Last Modified: Tue, 07 Jan 2025 06:45:23 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96d02cd9c1d5c2742decbe351e194414adec825bee6bbd6263521be0a514665`  
		Last Modified: Tue, 07 Jan 2025 03:48:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1d38c51092ac20a5bcd1dfc533de43a738889d192e62656482dc22f1505a79`  
		Last Modified: Tue, 07 Jan 2025 03:48:08 GMT  
		Size: 92.2 KB (92158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da18a25c93d7133b2d4097e549a323142182e4dd20d54315927b6bd6573eb0f1`  
		Last Modified: Tue, 07 Jan 2025 02:50:12 GMT  
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
		Last Modified: Tue, 07 Jan 2025 03:48:15 GMT  
		Size: 3.6 MB (3569181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37b47d54c077c2ac6d602d5b546c068ab8e54b2c34442bb70ec6ca92ca86216`  
		Last Modified: Wed, 08 Jan 2025 12:48:20 GMT  
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
		Last Modified: Sun, 15 Dec 2024 23:07:15 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e886790f9afca68021d7c75698a1217a115b9cc1ad35a2810b2d8b0ad55f3`  
		Last Modified: Wed, 08 Jan 2025 00:49:05 GMT  
		Size: 6.6 MB (6635953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7250eb870a6e7d1ba2c1af2ca41ebfa2fb763a5be83d1710296ff798161459c4`  
		Last Modified: Tue, 07 Jan 2025 02:50:13 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2143e50a785fba3cd83cef1e55edff4f0d54e965cede0048ee57f596d5735e0a`  
		Last Modified: Mon, 06 Jan 2025 17:55:10 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd92cccb8507bf0ea24147acd06ddac399895aa65bc91c02c25f650bd8c41174`  
		Last Modified: Tue, 07 Jan 2025 00:53:11 GMT  
		Size: 91.6 KB (91598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c62cefd1610f7333f6f871c1794e559b2115e00c5863260f9ddedd99769cf8`  
		Last Modified: Wed, 08 Jan 2025 01:49:22 GMT  
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
		Last Modified: Mon, 06 Jan 2025 22:56:28 GMT  
		Size: 3.6 MB (3561538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2606e6a1a87f3ded6407b0d5258d8218f3da05be49ac5201a62941c4296cdb35`  
		Last Modified: Wed, 08 Jan 2025 14:50:26 GMT  
		Size: 15.7 KB (15662 bytes)  
		MIME: application/vnd.in-toto+json
