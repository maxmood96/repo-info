<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:jammy`](#neurodebianjammy)
-	[`neurodebian:jammy-non-free`](#neurodebianjammy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)

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
