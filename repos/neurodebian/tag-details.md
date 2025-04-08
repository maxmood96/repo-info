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
$ docker pull neurodebian@sha256:e7653463330c9126ea1eec402d23989d49b28dea5be93237f2efcded4bc2ee75
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
$ docker pull neurodebian@sha256:a0dcbdd5d33f6b4ded90721e79214b48eb07fdfb81a611bf00f38b84d6732433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59852653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56702c61529f652e18e461b9d975da1b918fb642b0bcda7dc99adf61b3ca13c8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de7fc88f83bcd2ca272e9807479a820de15d4593a3dc968f48b4d1a264a15d`  
		Last Modified: Tue, 08 Apr 2025 01:26:18 GMT  
		Size: 11.3 MB (11266816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c97f36fd4e9a7f0a6099eee5422210349bcceb3ada17c5b6e372b193e1c53e`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9bb8e081d93848263d5c8ff20270983c16677528d3cb8280bff02ad12ab3c0`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738450aea5f8426606d81f919575dd5d096b41723b21d3907e88864249d8944b`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 93.1 KB (93122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3f958aa19a0cc84caf4443c0a5262b383f914a113a69501f1067faebeb388fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b65e7f8c4f9fe56144b3b34843001eef2fc8ab312552bdecda43286b373e72`

```dockerfile
```

-	Layers:
	-	`sha256:c9dcc5dde5954616e94ca09bc8d97aa97919cf2de5e71636e27304a17d7859f1`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 3.9 MB (3934172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b0e321829f52c1752633cdb98a97311dfcf9f59962d259c9bd20835c9e0310`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:316e85d6b21524cdbc0ad15080e717847fd5073eb7bb75d67349765ad063d86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e8af420ec5da3048814d4cbb202aff23e79ea370511fbaf0b7b066ac993921`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce08a29378b322d580a290ac850ee07138f732ffb563fd5c9ced94337ecfadf`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 11.2 MB (11232654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c994ce850f986eb5546d5276357b320b7bde68728c6257f9f77b9539290f72`  
		Last Modified: Tue, 08 Apr 2025 06:36:08 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c982b1954d94fe6ee8540f3d265491f3cf0dd395d3534a72e93c4fad36fbd9`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1367d165818a29284a9956a4df5e0769d1e2307631fc56bb05d36b69ca141`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 93.4 KB (93402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:29cce2b5a259f9c9f056e1510d143b2bafda8f596db6f9057a1b5f855d7450bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2d09196cebed934f4fefcd0203e85074211214122b021911166b08d731ee49`

```dockerfile
```

-	Layers:
	-	`sha256:f3e113528761941f55aee8901be4568a28106af0dad374fa90926309dce2b06f`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 3.9 MB (3934426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7c22551460781337ed41c7327a05b21f15a1c30f17258e6ec4776b3c7f7379`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:b89bfeab4f715e94bc3700d8663421acdfe91d53470cbebc93731b319e997d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f166a586e8ba988278b8e797306d03e139439505e284834af0e9ae2d0a87b4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1793e288819ca8e5da81164fd3b0b1d24868aafe1d8a9d34f091a2f21c58d474`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 11.7 MB (11688962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8157d1e1ccb587dd93d76e563527e79db61a20ea5a68a6c403990dfac4c4afe2`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311b058d618e974504bbd6d59732c7adb9d6ae51b0e044e6d23722d4d75dd51e`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cc6e969d13f9c2cf36335348948dd286883e74afa777719fca45c5b7494b71`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 93.2 KB (93220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1a3a2e7151462913ce91f40d07426091dd56d0538e73a5912341dcb207dbc1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539f5b686c724a08c2290236cbb9eb0a22a1720be1314f8cd5295968526f47aa`

```dockerfile
```

-	Layers:
	-	`sha256:4fafb8b7f5dbe92132a656924115da59d568b9a2d25df7c119e69607f36496f0`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 3.9 MB (3932089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c3da41f1e996b0bea791a288b31615f5e252addac9255378820496817694b2`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:fe69c78b7324bb178dee86ba6feee10b12ce31ff043b238f974f8a6563650d1c
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
$ docker pull neurodebian@sha256:7e398bdf282bf7b2de959d4e7871a00efdba7a3b94315f38909d9ad9eaec37c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59853092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0b605439b5903c5bd63e29c9fb820b6abb0892ce58d30d207c979223b9ec1d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8384fb657fddabb65893303e0a8f3c12bff01fafe00408cb06cb59da23a5b77b`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 11.3 MB (11266799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af38886ee03781ededd4d9c12fae87ab80880ef72a9c2e172c8d5f219d9824f`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88ac60b75849f44596a182fc0d9c00455a3ec54a32e5b38069df6b450a74def`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbc24edec90455b4172e2932b5777bc5f1382faef1259e1e04ecc6bae4cbf98`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 93.1 KB (93129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29795a5744ab07889ef89525b2147edf8c116dcfe94fa2db1132658a2dd9ad0`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b87313acde5fcf89bf43bf7b3b5871cd545f8a3285587ed68bfb4b5b57e61579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53c6b4dc71ea8685a6a40ed80932879e4014a40561bdd1a447d5f358545ec1c`

```dockerfile
```

-	Layers:
	-	`sha256:6c9ecc685f67450b07394a41de82db9fbf4ad8d9e1893feceb4134ce6a4d0ac7`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 3.9 MB (3934212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b606bc0549f263243d00b7f86422fb054bfcddf31523519a277b3ef0a891815f`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:45ad749f9bcd8e51602bd81dbd4201d29678379baa897125f9bb7f77d20f8465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59656149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddecea2fbc72473b511ca2e1fd47d21929e18fb548c9d544c0ac01712e3f9ac`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce08a29378b322d580a290ac850ee07138f732ffb563fd5c9ced94337ecfadf`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 11.2 MB (11232654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c994ce850f986eb5546d5276357b320b7bde68728c6257f9f77b9539290f72`  
		Last Modified: Tue, 08 Apr 2025 06:36:08 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c982b1954d94fe6ee8540f3d265491f3cf0dd395d3534a72e93c4fad36fbd9`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1367d165818a29284a9956a4df5e0769d1e2307631fc56bb05d36b69ca141`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 93.4 KB (93402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4af8e57251ac91dbbc525315d0377b42e6a750861089644e6f83134df5f4cf7`  
		Last Modified: Tue, 08 Apr 2025 06:36:22 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:889d830f6f8c37bb97f6c577d74b44ac7134ecc7067b9e1659c0329b7051917b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0c4c6354a373d3e63afd8b8b68da58b7b301db319e4432a32787cf11bc2a36`

```dockerfile
```

-	Layers:
	-	`sha256:f1b36a946b7421c5d1db125ead18ecf82bd46dc1d400123d4f5a8799b10fec5d`  
		Last Modified: Tue, 08 Apr 2025 06:36:22 GMT  
		Size: 3.9 MB (3934466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10e4b44ba7973ffe780662ff642440c6f6ceb6d4d6578bbfded6f9aaf6ee4c5`  
		Last Modified: Tue, 08 Apr 2025 06:36:22 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:77c4a11b877bd3695148289f8a619cd0a20b104bf12de5acf55b239b72c0dc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fb6ad261db4fd2e52ce4f0d6ccf15f1d0a4db69e6b7dd032dcea490167ed52`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c608ceda0b7454a97d884128aeeaa0bbda21fdbdf8119d7d88369c9ad0b91dd`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 11.7 MB (11688951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76c42422411b6fa3e8310cda6b4848d0ce9e210ed01e9825da2fbda0d3aa64c`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6869c5c8538c781cc3026ff93a7d2bc201709cba9d62d71943d18c2656e5a614`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883527fb04daca1643441eac1d252402727d310a2f385e3bad00cc08e0a95ea4`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 93.2 KB (93216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0e418c69eea3da98ff7405c3faa74ae00a63913463d0cb139fea3d28916a4`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f231e6f1d97565b2e28c8e6e28278ae3ded47c6088092bba32ad9deafe1677d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48e2b84fd898e55805a1a87c6dc5ae8c4ed71d306e06cd096b5ffd8b0a9b40a`

```dockerfile
```

-	Layers:
	-	`sha256:50be1ac0d7eaa72054bc23932238bcb1c9ab939bad36afe36ddd2c47b82a387e`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 3.9 MB (3932129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e81fcc4d5a20ce3e7c427e156d5ebd3b43b59d07e310b47b711be387be00e8a`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:f4eb45faa73785bf4e2f02daefde3ce03f1e1c9256a03a8d3095ee83879393cc
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
$ docker pull neurodebian@sha256:74fc96b02460550048711777d4aee359b9d01a9910c726876274e6bfd350d661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64956989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97b32b68c755a266a123b80f24780368f8dea2b3a1f6ac6188a3dec4df671d7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9d7693a3bd08decf0ee034f8039bc16bc9fd521dd5db19ed701e183d704389`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 11.1 MB (11105084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d069ea1fb1f3ff59787f0ebb7111b602580aa38a86620c44a0cf24b8da6fe2`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0449a295cdbde22577c56e960271a6b9c63d85cf48c5b36b936aea44657e2f5b`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a264dd350eaddb6c5d16f8f69e14b10ecb8c43398066153a4defa90943598202`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 101.2 KB (101216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:65521b7fac9e6793348f912e391f08944fff56db0c77d013c8e99aa3a0a87912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3184399104e7be94e5ebee6d2a88fdb28157e96bf1c1c0dbbf9d628b9de0f7`

```dockerfile
```

-	Layers:
	-	`sha256:8de8a61e2205b3e02d472f6563591743ad6b9c7b2966a5bfe2defdbee23493f9`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 4.2 MB (4234710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f47e7282dafc9f31a669196e043aa1e4c6bb8826b64d8144215bf7ee37d736`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:19c4313b113a7eda5828898c8df8f3908051d6000606180f8391c19f02ca0b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63463624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a0ec5531fc0954741dd521a579e93954d353b3edf38cfa90511b319f8e49b5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87946706aa736ef80d52aa62b6591f2914c573640b3b36ab0581897ab67232c1`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 11.1 MB (11106119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328bb261a19ee93d5235ad1623cb40c9fb7dc36a4ea866d51e418dd5bb75524`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5723df042ddc1277c89c7a1509daa7b17d8f5f8e95463f86467bdd6689acc65`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4164f8be20cd1c5fff9c06e619bb825756f4005a3439bbedca991306a75b0462`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 101.1 KB (101124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:958381046cdd411cca4125de0da9c7615ca1d2c628213f956ca663515873cde9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab51ece13395ab50445fc65a49b85960830481cd7301220802b84e11d5c8972`

```dockerfile
```

-	Layers:
	-	`sha256:a3e414d1ff92c63874277e06ab4a1fffb797aaf9fa7dccd8c32852db115618fd`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 4.2 MB (4234317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb2251c4c84b1487c91a885a838b0be95903dbe790a260490705dcf399088f75`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:e7d98c86b376667da8554880ac322c30aa9cfa26b35052c10354aa90ac8b17c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e5552518c011902b1720cb8123841b125e7eba4b7da20beda8a2266b1d1463`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
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
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b5ae7d85bf65d375a5f6dc6a0b0877fb963ae7bf8f8f4d27cf5b08eceff6f9`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 11.5 MB (11500465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daa007e54c239fbfbe5087cb47ca43af4a7d1df694c5e8a8020174726c19a42`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97eac2879e0c6b2ac36eace93767cf632bd46666df09233d59b0a518e37b7db9`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd62ce6834bda03604f319f34b2e62bba14e067be7c7ddb22397f7ea2e79fa12`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 101.1 KB (101100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:59c273c7a6c7e3b8553acd2497cdf98e3326e7e781c78906f5307b20777714b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2aebc2a7ceb47599386a1c4acdac11b4bcb10218d9198e6d60bf8fcc08caa2`

```dockerfile
```

-	Layers:
	-	`sha256:0d3e045b8fd612a40cd1c751b642873c3f741adfa5c7e7401fcc6f79f04bd152`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 4.2 MB (4231172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:105b1585b3731f8a7f5fe4b7d5575ba9daff42547c16e7c4c8d5b850660363ef`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 14.0 KB (13980 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:f4eaca29f9f94121e8d5b1cb2392425b163b2d8e32c5197658255d175db7e106
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
$ docker pull neurodebian@sha256:e9b08a4628cc0df81488abe3ce1e1eddc5c70f22369e2dbe723ff78225403472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64957378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d2a0a9ddbd93a0767eaaf18f1b3bcdc38c24b62533a24cf6f0c562985a80d3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2fc2274cc6634839d68f5e460a9544a5782d133f59626508b045414e2f27f8`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 11.1 MB (11105076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6b68ea8572b2570c073b9243b0db0755bdcd466de7c937673f018d1ddb6fe3`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f32b16d100896c8cb96acbf370519854f68fabf5252e129da5c49a635ce976`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80428172f8989bf82b58af2babdc46d7bea35f281d105c8a5a60c677b82602d9`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 101.2 KB (101229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db677a40776f6422a0f689f31e3f965d6bc24f44f6cc8811e567145883e7890`  
		Last Modified: Tue, 08 Apr 2025 01:37:12 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:31fdb5293eff980bf6e24668e5abdf9a455e640a6fa6d070df5d8cae2f4eb9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539bf5eb871955fe1c2af15745cd78183121c312b908e0dbf51e6b26ddacc6f6`

```dockerfile
```

-	Layers:
	-	`sha256:6fd14a45678113abdbeef00560f1034d94a141a5e8bfe3538ef072c6a51be24e`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 4.2 MB (4234746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84f902c5e5c6f814c43bd0abbc9897e15729cc1b9de0762b781673d50fce2539`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:575f0d6c76078c6a8d9806ddf6953b7641c7150bfe99933bec3d0fcb54829971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63464012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe075bbb7ee45dac5202adb64e4d47fa89d41eabb902a3e97d8c8c7019d04fa`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87946706aa736ef80d52aa62b6591f2914c573640b3b36ab0581897ab67232c1`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 11.1 MB (11106119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328bb261a19ee93d5235ad1623cb40c9fb7dc36a4ea866d51e418dd5bb75524`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5723df042ddc1277c89c7a1509daa7b17d8f5f8e95463f86467bdd6689acc65`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4164f8be20cd1c5fff9c06e619bb825756f4005a3439bbedca991306a75b0462`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 101.1 KB (101124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43195c5207b2a2869775a305cafeb460ca03ff3938082591b9f3cd39f945926`  
		Last Modified: Tue, 08 Apr 2025 06:35:45 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:65415b1eba54a3fd24e5f47ad4b182b20145806d337227346d50ead8df24713a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b058dde6e782950b11772c5671f138d1c54c896d987103349f03dad57e06c`

```dockerfile
```

-	Layers:
	-	`sha256:bc9f7f017e0174059f0f1032f4beb8a56ff0df243b9aa3cbe18d7824f511a5ca`  
		Last Modified: Tue, 08 Apr 2025 06:35:45 GMT  
		Size: 4.2 MB (4234353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de14165df62a3c79cbf714192baeac35bae2b68c96d2dccf0d7cb723b0af08cb`  
		Last Modified: Tue, 08 Apr 2025 06:35:45 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a8ee53203df6e5dde510596d39428632c1e95f5c91d757bbb5d7f1275e77aaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66288560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008756991a14b89fd8de3242193f66450ca230da9df385fc3430ef12aebf2f22`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
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
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14a195df3e575bc81f4bf5db264dd69b9119e972d82f56708aaa3fef07fb796`  
		Last Modified: Tue, 08 Apr 2025 01:24:40 GMT  
		Size: 11.5 MB (11500460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daa007e54c239fbfbe5087cb47ca43af4a7d1df694c5e8a8020174726c19a42`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97eac2879e0c6b2ac36eace93767cf632bd46666df09233d59b0a518e37b7db9`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205f71647024d7da981756d414aad5c1b87ec5904332bbb27f834d260e8b0621`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 101.1 KB (101093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f1021c8f19beb5ca34caf396e54ede187b5ddd0d6a17667da83c0ece55b0fd`  
		Last Modified: Tue, 08 Apr 2025 01:24:40 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3f139afc6eea84db213d78138d5ff18dcda1d6b9105af3f17743f10c704af381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3157179441aaf0491abf19187475be087c6b41bde68ab8899132b16d601bd858`

```dockerfile
```

-	Layers:
	-	`sha256:00f891168d9d1b5d2facdaee9854c54ceb9bcdb7609c5e9112af4c72938cc7f7`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 4.2 MB (4231208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccf36a89e0212365ddf58f880ecedf46791ad68d8789f7d0319055de5de2dfbf`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:4e81d6cb8e4af912f338848eda9951e8147f712ccfafc3e682bbf4d34cf920c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:1c97453dec70c7efc9007259430f068cb477df58a16f4d0f1000d4a6f74cefd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce51ce7faa01aaa50eb79111f2207c49cd8cf77c052f3ed2e6a1e70d911c3f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c384eeec84a7d9d62536825196bd2d97ffa42a5fbfce466ea3a431bcd69c5d54`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 5.4 MB (5360321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7e9ed62dd19182e793c8720084b02d813e8443bb86383956646999743c750d`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fa33ae715deafc7d46726a0d58d1a3e65407d81ba7146eb5f62176530494ac`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1ee38920cb19459e2dfcd2af486ce4bde5220f4b2877e5c22d7005164ab5e7`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 105.4 KB (105352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:feb41a5e703ebfd4274f0d775dd7e68c7259d6f3ef23bcbebb1020bad637eed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a1c6cac6704d7e91c07341aaed9bc57e27110ca7e33920c6638f2fc32aa473`

```dockerfile
```

-	Layers:
	-	`sha256:ed12c0b2d66cfbe2ac53317061a5719adb5732eab19971aafdffd9d8ff887f02`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 2.0 MB (2017767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f782b087bc3c99a0b39527dc790f475ba74c3acbeb826db207490309dd6ef33`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7ec68ffd4ce8b557d7733c44da2dd9db37a8c6e708cce9c26d0135f27ca64ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ae7a295cd2085775954ea846d58735c2a3057c2dfa6e35bb89e58df630802e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050735cec161cd8b6805e37dbf6aa92594ddffe88bfeb882c73207404df64f5b`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 5.3 MB (5340554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a24ffd648ad141a6c5f8d0a6bc9e4d061aabfc66f7ac709961fce88b9f48e6`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd527b60b667b0ed5a04bc8072f39d40c36fbf670cb1b84168920c7e61d839`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c37dedc3365ebdd4053270bd242fa8036af553bea745d2c3dfd61f13f37bb4b`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 105.4 KB (105371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:987268df32ff3b51e2b347c001877f974ac1882341fc0edd71564ad452850039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a57ddd25e6a9969d9a4fcd17f9545019ab29817f41c38313d21901602c83467`

```dockerfile
```

-	Layers:
	-	`sha256:b685d760802ecab2a600f9bba4f037b08fe8fe4cdf5c8a83c33074d14c5172e8`  
		Last Modified: Tue, 04 Mar 2025 00:47:41 GMT  
		Size: 2.0 MB (2017996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdd65cf18ae5378746c3c972db14702272c7a9e1b3d6f34ee01f2eb60b52237f`  
		Last Modified: Tue, 04 Mar 2025 00:47:40 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:9c4394a3645aa0cfd6feb047c1859d32889ca477df6cada0d1c34ea38a3e215c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bc41ec19d89c52fb33f61598be74521101cfccf0cabaaca406457d28e7a69fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12f329554086fa94340403bb193b76575103c2b554209a8410eff81d66231ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00567a6856fe1fc6b0b938ac9a89b3af7a249c77fa567fcff8c6aef78b32d38`  
		Last Modified: Tue, 04 Mar 2025 00:29:21 GMT  
		Size: 5.4 MB (5360306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a5f2d87aaf56e4b8a8d5644bcd7a85be4d504ba4def1615cf59e33fd53118`  
		Last Modified: Tue, 04 Mar 2025 00:29:21 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f616f3ad56f604c7fffc817b6c606d3161052e91810a831bd029280d6ef1a4d`  
		Last Modified: Tue, 04 Mar 2025 00:29:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5329a3fa7960ce7c66b46351ea95faf1a747f58d0b203f91ea650fc029fea15`  
		Last Modified: Tue, 04 Mar 2025 00:29:21 GMT  
		Size: 105.4 KB (105392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469abebe0269c4e7c08dfb9a28708bfd3d03ed5b7f21c19a1973de67782ed265`  
		Last Modified: Tue, 04 Mar 2025 00:29:22 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:06f64e1174358c52e1f7144007caa53e73b848415583c462935aa503a3da7f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7008651005bf66a3b76db15e875e1bbd234391df1a2835afd6b8b6065d10fa`

```dockerfile
```

-	Layers:
	-	`sha256:7db2af5d9137ccd23c9c5c6402da37d8ce79e469af978ed22050933878db7fa7`  
		Last Modified: Tue, 04 Mar 2025 00:29:21 GMT  
		Size: 2.0 MB (2017803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af422f1d83ae93c58d0742f028ccd34024444aa21372760518b8040f1f1b2449`  
		Last Modified: Tue, 04 Mar 2025 00:29:21 GMT  
		Size: 16.2 KB (16204 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f1af2ecb9a21feb330cd347ed15068db050f289105e2bdf3ec7c73f721a67af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d1dc7b4acf605a88141b16452a82bed6ded61f584d1707889d5ce9f825742d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050735cec161cd8b6805e37dbf6aa92594ddffe88bfeb882c73207404df64f5b`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 5.3 MB (5340554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a24ffd648ad141a6c5f8d0a6bc9e4d061aabfc66f7ac709961fce88b9f48e6`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd527b60b667b0ed5a04bc8072f39d40c36fbf670cb1b84168920c7e61d839`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c37dedc3365ebdd4053270bd242fa8036af553bea745d2c3dfd61f13f37bb4b`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 105.4 KB (105371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae865708d0b42dee9438a375c5a94efff641f15bc2df26488f326dda1626bf73`  
		Last Modified: Tue, 04 Mar 2025 00:47:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5594276a7d675b1211afa73a5e4657d666801fd628a86b3e04ca8a52ebd10688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94d6272d376b63c6522aab8d8e26167f6837ec440e8e0baeb30b5b9dfbd486c`

```dockerfile
```

-	Layers:
	-	`sha256:8eb4f3c5431a7fdd04e4a39d527cc69eaeb72da6950844801223bd43c47882c9`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 2.0 MB (2018032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a6eee93eb123d95d55402c9840f3c21fe2a23eda49d445843b210eb6c751b8c`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:259d4d6a9a9d24b1aa3cda6019a5f1a0e7f0c276ccea94aa8becc509d9023e31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:d3b045145a039095c921991d0ccdf892513e0759cdfdcf939d6f555e50824010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33271913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a8816ca18232a97cc980ff54f39cba4ac69ca46591ac329ae8127b626b838c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8c0acd572d3dd0137b69c5c82ec5e9fcb4c9fb8a6b6e2e2ec3a079afd3f40f`  
		Last Modified: Tue, 04 Mar 2025 00:29:35 GMT  
		Size: 3.6 MB (3623300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88bec03f6ef0567f62c851a9fdf69fbb9ed089d6523e006396dc0dd43fdffe`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9952844280c0e8e44be01d0bdd116c42f6ce15b6f2cdcd370f60a2dc1b239b9`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bdcf0d54e7cd8653653ce1247ca1bdb9b8879e450361dda90aab325adcddc1`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 110.5 KB (110493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:063eec82bc542ed413cbe925201769a48040ce8ec65f760455817e4af36a82e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af44b320bb60ee05c69f7d3b418de7cb89bb068ff486f4db11177fcbc7ae451`

```dockerfile
```

-	Layers:
	-	`sha256:99fb86291040d259ff73667ae41c8b055a6c74261dd979c674b3bf7b4e070101`  
		Last Modified: Tue, 04 Mar 2025 00:29:35 GMT  
		Size: 2.1 MB (2055319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:053470ebbef1fcf0e76ac69012793fbd3b6d86f57ea9db4ca181e3ab203a1337`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 14.0 KB (13975 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d57e784783ad1a705d4b8c4157a0f4bb0943d7f6016e40df665238a15ef8860d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31065206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f0a8666d5bafd58418834fdf6e839ca15e281b96ae50c41a3016f4ec798784`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd0af78ec9a7234b4b8066acae901b517ec725b4b29eb3d3bf430dc385c1eb1`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 3.6 MB (3594513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7400c8425778acd83b44cf2785e337c859d1c977da3b9a2795e0154477224f`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d27e1717deca9852671128d6b31175f596e5f09cf5fc4effd28c82c483b011d`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e582d3dc1a65d0aea3250617d371ab13284b64fd6fe5ab3f0dbf3bc4101a90`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 110.3 KB (110332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3871acf98e1d412c0bbf92e87b5cc8eee10057151f1ebdbc773b3315f73abad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560ca57ae12d8ff4513dbc043f3dba4d1a425136e422e34da7abd376b6f9f8c6`

```dockerfile
```

-	Layers:
	-	`sha256:0167c0288ba0ba488a3192109de14b31b713fdc3d7c7cee5348e4242b703f59b`  
		Last Modified: Tue, 04 Mar 2025 00:44:51 GMT  
		Size: 2.1 MB (2055579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0275d81429a3961d8b305a66c00331fc6fe78199be62152875deba7ac984078`  
		Last Modified: Tue, 04 Mar 2025 00:44:51 GMT  
		Size: 14.1 KB (14099 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:91a41ef8cadf2e4d524d4fa934d9f704a288026dae973a9beb1f4b38f333ba4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:95b1ef9f8d31888329d96601f18cf64504fad1683e3d4fb2ed5f332488ac5813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33272144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4767ff37c1f171be15037a996db015f5aca002c86622d3211787a7270a8c506`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c18277838fb626074044daef2d6391c2c0616bca636635c11230870cdbcecec`  
		Last Modified: Tue, 04 Mar 2025 00:29:35 GMT  
		Size: 3.6 MB (3623243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a837609f07f6ff52f016dedbcdaa8f12beced342f88dcc0b9e97fa1c672d677`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffa499ac965f5ed0d47c274d866262913a94d008947a24d6df3d15508de286e`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16411ea5d2a7aad041f59a454409172d40aeb3943548303c3f78e9533391c71c`  
		Last Modified: Tue, 04 Mar 2025 00:29:35 GMT  
		Size: 110.5 KB (110496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71302ab02528ec0e96c4622cbc04b7a6eaa50ba19ec3a4dbdcab480a8b6565f`  
		Last Modified: Tue, 04 Mar 2025 00:29:35 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cf8c9f7bce0fb8db6c4a1b57a4fd44e55d2cb7b3d078175e7bcef51ef71cb39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d726d8566fcfe02fb0815624425c525a1803e040a961c7b3e4814eb60c9ea`

```dockerfile
```

-	Layers:
	-	`sha256:537239a2d53c6f5ef8b7168e58624d4ce5b89581c831389c36a98eef3d3f85f6`  
		Last Modified: Tue, 04 Mar 2025 00:29:35 GMT  
		Size: 2.1 MB (2055355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21a23028a0e6e6b65591d8bfb47d271f3821b0110e0b0eefb10374c7e1bd214`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f6ddfbf955e665ad40fb1dfa079547a850b413fbe8b982bd8eb549be6065990a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31065491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd950fe3e7f592acb6cf98582eaf270067c43213d155d1d67c2393599dbf117`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd0af78ec9a7234b4b8066acae901b517ec725b4b29eb3d3bf430dc385c1eb1`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 3.6 MB (3594513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7400c8425778acd83b44cf2785e337c859d1c977da3b9a2795e0154477224f`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d27e1717deca9852671128d6b31175f596e5f09cf5fc4effd28c82c483b011d`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e582d3dc1a65d0aea3250617d371ab13284b64fd6fe5ab3f0dbf3bc4101a90`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 110.3 KB (110332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeb11c7f284a500f2100a21c4b5744a74759985b38be0ed392f622c2c757a7f`  
		Last Modified: Tue, 04 Mar 2025 00:42:45 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:23b90fbd4e6fead00e5a1f468c3395f0f56b3b67f746a78fda933eac29359282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dd9d986af870ecb59bf7187c1ac7b3b628075e5155c98b020177664bda5d4`

```dockerfile
```

-	Layers:
	-	`sha256:1fa940c620bbbdfc1ff3d595658a132e12ccd3c40c351e2f1050b1e671a07b14`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 2.1 MB (2055615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:568466c12db8fc80aeffbba52149b2df24f96405b18e5842cc789d68cd7d3d7e`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:e7653463330c9126ea1eec402d23989d49b28dea5be93237f2efcded4bc2ee75
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
$ docker pull neurodebian@sha256:a0dcbdd5d33f6b4ded90721e79214b48eb07fdfb81a611bf00f38b84d6732433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59852653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56702c61529f652e18e461b9d975da1b918fb642b0bcda7dc99adf61b3ca13c8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de7fc88f83bcd2ca272e9807479a820de15d4593a3dc968f48b4d1a264a15d`  
		Last Modified: Tue, 08 Apr 2025 01:26:18 GMT  
		Size: 11.3 MB (11266816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c97f36fd4e9a7f0a6099eee5422210349bcceb3ada17c5b6e372b193e1c53e`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9bb8e081d93848263d5c8ff20270983c16677528d3cb8280bff02ad12ab3c0`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738450aea5f8426606d81f919575dd5d096b41723b21d3907e88864249d8944b`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 93.1 KB (93122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3f958aa19a0cc84caf4443c0a5262b383f914a113a69501f1067faebeb388fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b65e7f8c4f9fe56144b3b34843001eef2fc8ab312552bdecda43286b373e72`

```dockerfile
```

-	Layers:
	-	`sha256:c9dcc5dde5954616e94ca09bc8d97aa97919cf2de5e71636e27304a17d7859f1`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 3.9 MB (3934172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b0e321829f52c1752633cdb98a97311dfcf9f59962d259c9bd20835c9e0310`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:316e85d6b21524cdbc0ad15080e717847fd5073eb7bb75d67349765ad063d86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e8af420ec5da3048814d4cbb202aff23e79ea370511fbaf0b7b066ac993921`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce08a29378b322d580a290ac850ee07138f732ffb563fd5c9ced94337ecfadf`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 11.2 MB (11232654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c994ce850f986eb5546d5276357b320b7bde68728c6257f9f77b9539290f72`  
		Last Modified: Tue, 08 Apr 2025 06:36:08 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c982b1954d94fe6ee8540f3d265491f3cf0dd395d3534a72e93c4fad36fbd9`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1367d165818a29284a9956a4df5e0769d1e2307631fc56bb05d36b69ca141`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 93.4 KB (93402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:29cce2b5a259f9c9f056e1510d143b2bafda8f596db6f9057a1b5f855d7450bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2d09196cebed934f4fefcd0203e85074211214122b021911166b08d731ee49`

```dockerfile
```

-	Layers:
	-	`sha256:f3e113528761941f55aee8901be4568a28106af0dad374fa90926309dce2b06f`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 3.9 MB (3934426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7c22551460781337ed41c7327a05b21f15a1c30f17258e6ec4776b3c7f7379`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:b89bfeab4f715e94bc3700d8663421acdfe91d53470cbebc93731b319e997d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f166a586e8ba988278b8e797306d03e139439505e284834af0e9ae2d0a87b4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1793e288819ca8e5da81164fd3b0b1d24868aafe1d8a9d34f091a2f21c58d474`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 11.7 MB (11688962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8157d1e1ccb587dd93d76e563527e79db61a20ea5a68a6c403990dfac4c4afe2`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311b058d618e974504bbd6d59732c7adb9d6ae51b0e044e6d23722d4d75dd51e`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cc6e969d13f9c2cf36335348948dd286883e74afa777719fca45c5b7494b71`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 93.2 KB (93220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1a3a2e7151462913ce91f40d07426091dd56d0538e73a5912341dcb207dbc1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539f5b686c724a08c2290236cbb9eb0a22a1720be1314f8cd5295968526f47aa`

```dockerfile
```

-	Layers:
	-	`sha256:4fafb8b7f5dbe92132a656924115da59d568b9a2d25df7c119e69607f36496f0`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 3.9 MB (3932089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c3da41f1e996b0bea791a288b31615f5e252addac9255378820496817694b2`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:f4eb45faa73785bf4e2f02daefde3ce03f1e1c9256a03a8d3095ee83879393cc
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
$ docker pull neurodebian@sha256:74fc96b02460550048711777d4aee359b9d01a9910c726876274e6bfd350d661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64956989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97b32b68c755a266a123b80f24780368f8dea2b3a1f6ac6188a3dec4df671d7`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9d7693a3bd08decf0ee034f8039bc16bc9fd521dd5db19ed701e183d704389`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 11.1 MB (11105084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d069ea1fb1f3ff59787f0ebb7111b602580aa38a86620c44a0cf24b8da6fe2`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0449a295cdbde22577c56e960271a6b9c63d85cf48c5b36b936aea44657e2f5b`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a264dd350eaddb6c5d16f8f69e14b10ecb8c43398066153a4defa90943598202`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 101.2 KB (101216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:65521b7fac9e6793348f912e391f08944fff56db0c77d013c8e99aa3a0a87912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3184399104e7be94e5ebee6d2a88fdb28157e96bf1c1c0dbbf9d628b9de0f7`

```dockerfile
```

-	Layers:
	-	`sha256:8de8a61e2205b3e02d472f6563591743ad6b9c7b2966a5bfe2defdbee23493f9`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 4.2 MB (4234710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0f47e7282dafc9f31a669196e043aa1e4c6bb8826b64d8144215bf7ee37d736`  
		Last Modified: Tue, 08 Apr 2025 01:26:05 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:19c4313b113a7eda5828898c8df8f3908051d6000606180f8391c19f02ca0b7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63463624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a0ec5531fc0954741dd521a579e93954d353b3edf38cfa90511b319f8e49b5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87946706aa736ef80d52aa62b6591f2914c573640b3b36ab0581897ab67232c1`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 11.1 MB (11106119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328bb261a19ee93d5235ad1623cb40c9fb7dc36a4ea866d51e418dd5bb75524`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5723df042ddc1277c89c7a1509daa7b17d8f5f8e95463f86467bdd6689acc65`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4164f8be20cd1c5fff9c06e619bb825756f4005a3439bbedca991306a75b0462`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 101.1 KB (101124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:958381046cdd411cca4125de0da9c7615ca1d2c628213f956ca663515873cde9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab51ece13395ab50445fc65a49b85960830481cd7301220802b84e11d5c8972`

```dockerfile
```

-	Layers:
	-	`sha256:a3e414d1ff92c63874277e06ab4a1fffb797aaf9fa7dccd8c32852db115618fd`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 4.2 MB (4234317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb2251c4c84b1487c91a885a838b0be95903dbe790a260490705dcf399088f75`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:e7d98c86b376667da8554880ac322c30aa9cfa26b35052c10354aa90ac8b17c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66288186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e5552518c011902b1720cb8123841b125e7eba4b7da20beda8a2266b1d1463`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
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
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b5ae7d85bf65d375a5f6dc6a0b0877fb963ae7bf8f8f4d27cf5b08eceff6f9`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 11.5 MB (11500465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daa007e54c239fbfbe5087cb47ca43af4a7d1df694c5e8a8020174726c19a42`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97eac2879e0c6b2ac36eace93767cf632bd46666df09233d59b0a518e37b7db9`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd62ce6834bda03604f319f34b2e62bba14e067be7c7ddb22397f7ea2e79fa12`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 101.1 KB (101100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:59c273c7a6c7e3b8553acd2497cdf98e3326e7e781c78906f5307b20777714b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f2aebc2a7ceb47599386a1c4acdac11b4bcb10218d9198e6d60bf8fcc08caa2`

```dockerfile
```

-	Layers:
	-	`sha256:0d3e045b8fd612a40cd1c751b642873c3f741adfa5c7e7401fcc6f79f04bd152`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 4.2 MB (4231172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:105b1585b3731f8a7f5fe4b7d5575ba9daff42547c16e7c4c8d5b850660363ef`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 14.0 KB (13980 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:f4eaca29f9f94121e8d5b1cb2392425b163b2d8e32c5197658255d175db7e106
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
$ docker pull neurodebian@sha256:e9b08a4628cc0df81488abe3ce1e1eddc5c70f22369e2dbe723ff78225403472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64957378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d2a0a9ddbd93a0767eaaf18f1b3bcdc38c24b62533a24cf6f0c562985a80d3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f2fc2274cc6634839d68f5e460a9544a5782d133f59626508b045414e2f27f8`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 11.1 MB (11105076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6b68ea8572b2570c073b9243b0db0755bdcd466de7c937673f018d1ddb6fe3`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f32b16d100896c8cb96acbf370519854f68fabf5252e129da5c49a635ce976`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80428172f8989bf82b58af2babdc46d7bea35f281d105c8a5a60c677b82602d9`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 101.2 KB (101229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db677a40776f6422a0f689f31e3f965d6bc24f44f6cc8811e567145883e7890`  
		Last Modified: Tue, 08 Apr 2025 01:37:12 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:31fdb5293eff980bf6e24668e5abdf9a455e640a6fa6d070df5d8cae2f4eb9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539bf5eb871955fe1c2af15745cd78183121c312b908e0dbf51e6b26ddacc6f6`

```dockerfile
```

-	Layers:
	-	`sha256:6fd14a45678113abdbeef00560f1034d94a141a5e8bfe3538ef072c6a51be24e`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 4.2 MB (4234746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84f902c5e5c6f814c43bd0abbc9897e15729cc1b9de0762b781673d50fce2539`  
		Last Modified: Tue, 08 Apr 2025 01:37:11 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:575f0d6c76078c6a8d9806ddf6953b7641c7150bfe99933bec3d0fcb54829971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63464012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe075bbb7ee45dac5202adb64e4d47fa89d41eabb902a3e97d8c8c7019d04fa`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87946706aa736ef80d52aa62b6591f2914c573640b3b36ab0581897ab67232c1`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 11.1 MB (11106119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3328bb261a19ee93d5235ad1623cb40c9fb7dc36a4ea866d51e418dd5bb75524`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5723df042ddc1277c89c7a1509daa7b17d8f5f8e95463f86467bdd6689acc65`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4164f8be20cd1c5fff9c06e619bb825756f4005a3439bbedca991306a75b0462`  
		Last Modified: Tue, 08 Apr 2025 06:35:32 GMT  
		Size: 101.1 KB (101124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43195c5207b2a2869775a305cafeb460ca03ff3938082591b9f3cd39f945926`  
		Last Modified: Tue, 08 Apr 2025 06:35:45 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:65415b1eba54a3fd24e5f47ad4b182b20145806d337227346d50ead8df24713a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093b058dde6e782950b11772c5671f138d1c54c896d987103349f03dad57e06c`

```dockerfile
```

-	Layers:
	-	`sha256:bc9f7f017e0174059f0f1032f4beb8a56ff0df243b9aa3cbe18d7824f511a5ca`  
		Last Modified: Tue, 08 Apr 2025 06:35:45 GMT  
		Size: 4.2 MB (4234353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de14165df62a3c79cbf714192baeac35bae2b68c96d2dccf0d7cb723b0af08cb`  
		Last Modified: Tue, 08 Apr 2025 06:35:45 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a8ee53203df6e5dde510596d39428632c1e95f5c91d757bbb5d7f1275e77aaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66288560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008756991a14b89fd8de3242193f66450ca230da9df385fc3430ef12aebf2f22`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
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
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14a195df3e575bc81f4bf5db264dd69b9119e972d82f56708aaa3fef07fb796`  
		Last Modified: Tue, 08 Apr 2025 01:24:40 GMT  
		Size: 11.5 MB (11500460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daa007e54c239fbfbe5087cb47ca43af4a7d1df694c5e8a8020174726c19a42`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97eac2879e0c6b2ac36eace93767cf632bd46666df09233d59b0a518e37b7db9`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205f71647024d7da981756d414aad5c1b87ec5904332bbb27f834d260e8b0621`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 101.1 KB (101093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f1021c8f19beb5ca34caf396e54ede187b5ddd0d6a17667da83c0ece55b0fd`  
		Last Modified: Tue, 08 Apr 2025 01:24:40 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3f139afc6eea84db213d78138d5ff18dcda1d6b9105af3f17743f10c704af381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3157179441aaf0491abf19187475be087c6b41bde68ab8899132b16d601bd858`

```dockerfile
```

-	Layers:
	-	`sha256:00f891168d9d1b5d2facdaee9854c54ceb9bcdb7609c5e9112af4c72938cc7f7`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 4.2 MB (4231208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccf36a89e0212365ddf58f880ecedf46791ad68d8789f7d0319055de5de2dfbf`  
		Last Modified: Tue, 08 Apr 2025 01:24:39 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:e7653463330c9126ea1eec402d23989d49b28dea5be93237f2efcded4bc2ee75
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
$ docker pull neurodebian@sha256:a0dcbdd5d33f6b4ded90721e79214b48eb07fdfb81a611bf00f38b84d6732433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59852653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56702c61529f652e18e461b9d975da1b918fb642b0bcda7dc99adf61b3ca13c8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de7fc88f83bcd2ca272e9807479a820de15d4593a3dc968f48b4d1a264a15d`  
		Last Modified: Tue, 08 Apr 2025 01:26:18 GMT  
		Size: 11.3 MB (11266816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c97f36fd4e9a7f0a6099eee5422210349bcceb3ada17c5b6e372b193e1c53e`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9bb8e081d93848263d5c8ff20270983c16677528d3cb8280bff02ad12ab3c0`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738450aea5f8426606d81f919575dd5d096b41723b21d3907e88864249d8944b`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 93.1 KB (93122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3f958aa19a0cc84caf4443c0a5262b383f914a113a69501f1067faebeb388fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b65e7f8c4f9fe56144b3b34843001eef2fc8ab312552bdecda43286b373e72`

```dockerfile
```

-	Layers:
	-	`sha256:c9dcc5dde5954616e94ca09bc8d97aa97919cf2de5e71636e27304a17d7859f1`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 3.9 MB (3934172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b0e321829f52c1752633cdb98a97311dfcf9f59962d259c9bd20835c9e0310`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:316e85d6b21524cdbc0ad15080e717847fd5073eb7bb75d67349765ad063d86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e8af420ec5da3048814d4cbb202aff23e79ea370511fbaf0b7b066ac993921`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce08a29378b322d580a290ac850ee07138f732ffb563fd5c9ced94337ecfadf`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 11.2 MB (11232654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c994ce850f986eb5546d5276357b320b7bde68728c6257f9f77b9539290f72`  
		Last Modified: Tue, 08 Apr 2025 06:36:08 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c982b1954d94fe6ee8540f3d265491f3cf0dd395d3534a72e93c4fad36fbd9`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1367d165818a29284a9956a4df5e0769d1e2307631fc56bb05d36b69ca141`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 93.4 KB (93402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:29cce2b5a259f9c9f056e1510d143b2bafda8f596db6f9057a1b5f855d7450bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2d09196cebed934f4fefcd0203e85074211214122b021911166b08d731ee49`

```dockerfile
```

-	Layers:
	-	`sha256:f3e113528761941f55aee8901be4568a28106af0dad374fa90926309dce2b06f`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 3.9 MB (3934426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7c22551460781337ed41c7327a05b21f15a1c30f17258e6ec4776b3c7f7379`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:b89bfeab4f715e94bc3700d8663421acdfe91d53470cbebc93731b319e997d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f166a586e8ba988278b8e797306d03e139439505e284834af0e9ae2d0a87b4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1793e288819ca8e5da81164fd3b0b1d24868aafe1d8a9d34f091a2f21c58d474`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 11.7 MB (11688962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8157d1e1ccb587dd93d76e563527e79db61a20ea5a68a6c403990dfac4c4afe2`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311b058d618e974504bbd6d59732c7adb9d6ae51b0e044e6d23722d4d75dd51e`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cc6e969d13f9c2cf36335348948dd286883e74afa777719fca45c5b7494b71`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 93.2 KB (93220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1a3a2e7151462913ce91f40d07426091dd56d0538e73a5912341dcb207dbc1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539f5b686c724a08c2290236cbb9eb0a22a1720be1314f8cd5295968526f47aa`

```dockerfile
```

-	Layers:
	-	`sha256:4fafb8b7f5dbe92132a656924115da59d568b9a2d25df7c119e69607f36496f0`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 3.9 MB (3932089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c3da41f1e996b0bea791a288b31615f5e252addac9255378820496817694b2`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:fe69c78b7324bb178dee86ba6feee10b12ce31ff043b238f974f8a6563650d1c
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
$ docker pull neurodebian@sha256:7e398bdf282bf7b2de959d4e7871a00efdba7a3b94315f38909d9ad9eaec37c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59853092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0b605439b5903c5bd63e29c9fb820b6abb0892ce58d30d207c979223b9ec1d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8384fb657fddabb65893303e0a8f3c12bff01fafe00408cb06cb59da23a5b77b`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 11.3 MB (11266799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af38886ee03781ededd4d9c12fae87ab80880ef72a9c2e172c8d5f219d9824f`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88ac60b75849f44596a182fc0d9c00455a3ec54a32e5b38069df6b450a74def`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbc24edec90455b4172e2932b5777bc5f1382faef1259e1e04ecc6bae4cbf98`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 93.1 KB (93129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29795a5744ab07889ef89525b2147edf8c116dcfe94fa2db1132658a2dd9ad0`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b87313acde5fcf89bf43bf7b3b5871cd545f8a3285587ed68bfb4b5b57e61579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53c6b4dc71ea8685a6a40ed80932879e4014a40561bdd1a447d5f358545ec1c`

```dockerfile
```

-	Layers:
	-	`sha256:6c9ecc685f67450b07394a41de82db9fbf4ad8d9e1893feceb4134ce6a4d0ac7`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 3.9 MB (3934212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b606bc0549f263243d00b7f86422fb054bfcddf31523519a277b3ef0a891815f`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:45ad749f9bcd8e51602bd81dbd4201d29678379baa897125f9bb7f77d20f8465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59656149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddecea2fbc72473b511ca2e1fd47d21929e18fb548c9d544c0ac01712e3f9ac`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce08a29378b322d580a290ac850ee07138f732ffb563fd5c9ced94337ecfadf`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 11.2 MB (11232654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c994ce850f986eb5546d5276357b320b7bde68728c6257f9f77b9539290f72`  
		Last Modified: Tue, 08 Apr 2025 06:36:08 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c982b1954d94fe6ee8540f3d265491f3cf0dd395d3534a72e93c4fad36fbd9`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1367d165818a29284a9956a4df5e0769d1e2307631fc56bb05d36b69ca141`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 93.4 KB (93402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4af8e57251ac91dbbc525315d0377b42e6a750861089644e6f83134df5f4cf7`  
		Last Modified: Tue, 08 Apr 2025 06:36:22 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:889d830f6f8c37bb97f6c577d74b44ac7134ecc7067b9e1659c0329b7051917b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0c4c6354a373d3e63afd8b8b68da58b7b301db319e4432a32787cf11bc2a36`

```dockerfile
```

-	Layers:
	-	`sha256:f1b36a946b7421c5d1db125ead18ecf82bd46dc1d400123d4f5a8799b10fec5d`  
		Last Modified: Tue, 08 Apr 2025 06:36:22 GMT  
		Size: 3.9 MB (3934466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10e4b44ba7973ffe780662ff642440c6f6ceb6d4d6578bbfded6f9aaf6ee4c5`  
		Last Modified: Tue, 08 Apr 2025 06:36:22 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:77c4a11b877bd3695148289f8a619cd0a20b104bf12de5acf55b239b72c0dc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fb6ad261db4fd2e52ce4f0d6ccf15f1d0a4db69e6b7dd032dcea490167ed52`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c608ceda0b7454a97d884128aeeaa0bbda21fdbdf8119d7d88369c9ad0b91dd`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 11.7 MB (11688951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76c42422411b6fa3e8310cda6b4848d0ce9e210ed01e9825da2fbda0d3aa64c`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6869c5c8538c781cc3026ff93a7d2bc201709cba9d62d71943d18c2656e5a614`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883527fb04daca1643441eac1d252402727d310a2f385e3bad00cc08e0a95ea4`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 93.2 KB (93216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0e418c69eea3da98ff7405c3faa74ae00a63913463d0cb139fea3d28916a4`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f231e6f1d97565b2e28c8e6e28278ae3ded47c6088092bba32ad9deafe1677d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48e2b84fd898e55805a1a87c6dc5ae8c4ed71d306e06cd096b5ffd8b0a9b40a`

```dockerfile
```

-	Layers:
	-	`sha256:50be1ac0d7eaa72054bc23932238bcb1c9ab939bad36afe36ddd2c47b82a387e`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 3.9 MB (3932129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e81fcc4d5a20ce3e7c427e156d5ebd3b43b59d07e310b47b711be387be00e8a`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:4e81d6cb8e4af912f338848eda9951e8147f712ccfafc3e682bbf4d34cf920c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:1c97453dec70c7efc9007259430f068cb477df58a16f4d0f1000d4a6f74cefd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce51ce7faa01aaa50eb79111f2207c49cd8cf77c052f3ed2e6a1e70d911c3f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c384eeec84a7d9d62536825196bd2d97ffa42a5fbfce466ea3a431bcd69c5d54`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 5.4 MB (5360321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7e9ed62dd19182e793c8720084b02d813e8443bb86383956646999743c750d`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fa33ae715deafc7d46726a0d58d1a3e65407d81ba7146eb5f62176530494ac`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1ee38920cb19459e2dfcd2af486ce4bde5220f4b2877e5c22d7005164ab5e7`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 105.4 KB (105352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:feb41a5e703ebfd4274f0d775dd7e68c7259d6f3ef23bcbebb1020bad637eed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a1c6cac6704d7e91c07341aaed9bc57e27110ca7e33920c6638f2fc32aa473`

```dockerfile
```

-	Layers:
	-	`sha256:ed12c0b2d66cfbe2ac53317061a5719adb5732eab19971aafdffd9d8ff887f02`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 2.0 MB (2017767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f782b087bc3c99a0b39527dc790f475ba74c3acbeb826db207490309dd6ef33`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7ec68ffd4ce8b557d7733c44da2dd9db37a8c6e708cce9c26d0135f27ca64ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ae7a295cd2085775954ea846d58735c2a3057c2dfa6e35bb89e58df630802e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050735cec161cd8b6805e37dbf6aa92594ddffe88bfeb882c73207404df64f5b`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 5.3 MB (5340554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a24ffd648ad141a6c5f8d0a6bc9e4d061aabfc66f7ac709961fce88b9f48e6`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd527b60b667b0ed5a04bc8072f39d40c36fbf670cb1b84168920c7e61d839`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c37dedc3365ebdd4053270bd242fa8036af553bea745d2c3dfd61f13f37bb4b`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 105.4 KB (105371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:987268df32ff3b51e2b347c001877f974ac1882341fc0edd71564ad452850039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a57ddd25e6a9969d9a4fcd17f9545019ab29817f41c38313d21901602c83467`

```dockerfile
```

-	Layers:
	-	`sha256:b685d760802ecab2a600f9bba4f037b08fe8fe4cdf5c8a83c33074d14c5172e8`  
		Last Modified: Tue, 04 Mar 2025 00:47:41 GMT  
		Size: 2.0 MB (2017996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdd65cf18ae5378746c3c972db14702272c7a9e1b3d6f34ee01f2eb60b52237f`  
		Last Modified: Tue, 04 Mar 2025 00:47:40 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:9c4394a3645aa0cfd6feb047c1859d32889ca477df6cada0d1c34ea38a3e215c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:bc41ec19d89c52fb33f61598be74521101cfccf0cabaaca406457d28e7a69fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12f329554086fa94340403bb193b76575103c2b554209a8410eff81d66231ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00567a6856fe1fc6b0b938ac9a89b3af7a249c77fa567fcff8c6aef78b32d38`  
		Last Modified: Tue, 04 Mar 2025 00:29:21 GMT  
		Size: 5.4 MB (5360306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976a5f2d87aaf56e4b8a8d5644bcd7a85be4d504ba4def1615cf59e33fd53118`  
		Last Modified: Tue, 04 Mar 2025 00:29:21 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f616f3ad56f604c7fffc817b6c606d3161052e91810a831bd029280d6ef1a4d`  
		Last Modified: Tue, 04 Mar 2025 00:29:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5329a3fa7960ce7c66b46351ea95faf1a747f58d0b203f91ea650fc029fea15`  
		Last Modified: Tue, 04 Mar 2025 00:29:21 GMT  
		Size: 105.4 KB (105392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469abebe0269c4e7c08dfb9a28708bfd3d03ed5b7f21c19a1973de67782ed265`  
		Last Modified: Tue, 04 Mar 2025 00:29:22 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:06f64e1174358c52e1f7144007caa53e73b848415583c462935aa503a3da7f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7008651005bf66a3b76db15e875e1bbd234391df1a2835afd6b8b6065d10fa`

```dockerfile
```

-	Layers:
	-	`sha256:7db2af5d9137ccd23c9c5c6402da37d8ce79e469af978ed22050933878db7fa7`  
		Last Modified: Tue, 04 Mar 2025 00:29:21 GMT  
		Size: 2.0 MB (2017803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af422f1d83ae93c58d0742f028ccd34024444aa21372760518b8040f1f1b2449`  
		Last Modified: Tue, 04 Mar 2025 00:29:21 GMT  
		Size: 16.2 KB (16204 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f1af2ecb9a21feb330cd347ed15068db050f289105e2bdf3ec7c73f721a67af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d1dc7b4acf605a88141b16452a82bed6ded61f584d1707889d5ce9f825742d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian focal main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050735cec161cd8b6805e37dbf6aa92594ddffe88bfeb882c73207404df64f5b`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 5.3 MB (5340554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a24ffd648ad141a6c5f8d0a6bc9e4d061aabfc66f7ac709961fce88b9f48e6`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bd527b60b667b0ed5a04bc8072f39d40c36fbf670cb1b84168920c7e61d839`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c37dedc3365ebdd4053270bd242fa8036af553bea745d2c3dfd61f13f37bb4b`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 105.4 KB (105371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae865708d0b42dee9438a375c5a94efff641f15bc2df26488f326dda1626bf73`  
		Last Modified: Tue, 04 Mar 2025 00:47:29 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5594276a7d675b1211afa73a5e4657d666801fd628a86b3e04ca8a52ebd10688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94d6272d376b63c6522aab8d8e26167f6837ec440e8e0baeb30b5b9dfbd486c`

```dockerfile
```

-	Layers:
	-	`sha256:8eb4f3c5431a7fdd04e4a39d527cc69eaeb72da6950844801223bd43c47882c9`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 2.0 MB (2018032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a6eee93eb123d95d55402c9840f3c21fe2a23eda49d445843b210eb6c751b8c`  
		Last Modified: Tue, 04 Mar 2025 00:47:28 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:259d4d6a9a9d24b1aa3cda6019a5f1a0e7f0c276ccea94aa8becc509d9023e31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:d3b045145a039095c921991d0ccdf892513e0759cdfdcf939d6f555e50824010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33271913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24a8816ca18232a97cc980ff54f39cba4ac69ca46591ac329ae8127b626b838c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8c0acd572d3dd0137b69c5c82ec5e9fcb4c9fb8a6b6e2e2ec3a079afd3f40f`  
		Last Modified: Tue, 04 Mar 2025 00:29:35 GMT  
		Size: 3.6 MB (3623300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88bec03f6ef0567f62c851a9fdf69fbb9ed089d6523e006396dc0dd43fdffe`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9952844280c0e8e44be01d0bdd116c42f6ce15b6f2cdcd370f60a2dc1b239b9`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bdcf0d54e7cd8653653ce1247ca1bdb9b8879e450361dda90aab325adcddc1`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 110.5 KB (110493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:063eec82bc542ed413cbe925201769a48040ce8ec65f760455817e4af36a82e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af44b320bb60ee05c69f7d3b418de7cb89bb068ff486f4db11177fcbc7ae451`

```dockerfile
```

-	Layers:
	-	`sha256:99fb86291040d259ff73667ae41c8b055a6c74261dd979c674b3bf7b4e070101`  
		Last Modified: Tue, 04 Mar 2025 00:29:35 GMT  
		Size: 2.1 MB (2055319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:053470ebbef1fcf0e76ac69012793fbd3b6d86f57ea9db4ca181e3ab203a1337`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 14.0 KB (13975 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d57e784783ad1a705d4b8c4157a0f4bb0943d7f6016e40df665238a15ef8860d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31065206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f0a8666d5bafd58418834fdf6e839ca15e281b96ae50c41a3016f4ec798784`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd0af78ec9a7234b4b8066acae901b517ec725b4b29eb3d3bf430dc385c1eb1`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 3.6 MB (3594513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7400c8425778acd83b44cf2785e337c859d1c977da3b9a2795e0154477224f`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d27e1717deca9852671128d6b31175f596e5f09cf5fc4effd28c82c483b011d`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e582d3dc1a65d0aea3250617d371ab13284b64fd6fe5ab3f0dbf3bc4101a90`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 110.3 KB (110332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3871acf98e1d412c0bbf92e87b5cc8eee10057151f1ebdbc773b3315f73abad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560ca57ae12d8ff4513dbc043f3dba4d1a425136e422e34da7abd376b6f9f8c6`

```dockerfile
```

-	Layers:
	-	`sha256:0167c0288ba0ba488a3192109de14b31b713fdc3d7c7cee5348e4242b703f59b`  
		Last Modified: Tue, 04 Mar 2025 00:44:51 GMT  
		Size: 2.1 MB (2055579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0275d81429a3961d8b305a66c00331fc6fe78199be62152875deba7ac984078`  
		Last Modified: Tue, 04 Mar 2025 00:44:51 GMT  
		Size: 14.1 KB (14099 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:91a41ef8cadf2e4d524d4fa934d9f704a288026dae973a9beb1f4b38f333ba4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:95b1ef9f8d31888329d96601f18cf64504fad1683e3d4fb2ed5f332488ac5813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33272144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4767ff37c1f171be15037a996db015f5aca002c86622d3211787a7270a8c506`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c18277838fb626074044daef2d6391c2c0616bca636635c11230870cdbcecec`  
		Last Modified: Tue, 04 Mar 2025 00:29:35 GMT  
		Size: 3.6 MB (3623243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a837609f07f6ff52f016dedbcdaa8f12beced342f88dcc0b9e97fa1c672d677`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffa499ac965f5ed0d47c274d866262913a94d008947a24d6df3d15508de286e`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16411ea5d2a7aad041f59a454409172d40aeb3943548303c3f78e9533391c71c`  
		Last Modified: Tue, 04 Mar 2025 00:29:35 GMT  
		Size: 110.5 KB (110496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71302ab02528ec0e96c4622cbc04b7a6eaa50ba19ec3a4dbdcab480a8b6565f`  
		Last Modified: Tue, 04 Mar 2025 00:29:35 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cf8c9f7bce0fb8db6c4a1b57a4fd44e55d2cb7b3d078175e7bcef51ef71cb39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d726d8566fcfe02fb0815624425c525a1803e040a961c7b3e4814eb60c9ea`

```dockerfile
```

-	Layers:
	-	`sha256:537239a2d53c6f5ef8b7168e58624d4ce5b89581c831389c36a98eef3d3f85f6`  
		Last Modified: Tue, 04 Mar 2025 00:29:35 GMT  
		Size: 2.1 MB (2055355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e21a23028a0e6e6b65591d8bfb47d271f3821b0110e0b0eefb10374c7e1bd214`  
		Last Modified: Tue, 04 Mar 2025 00:29:34 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f6ddfbf955e665ad40fb1dfa079547a850b413fbe8b982bd8eb549be6065990a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31065491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd950fe3e7f592acb6cf98582eaf270067c43213d155d1d67c2393599dbf117`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd0af78ec9a7234b4b8066acae901b517ec725b4b29eb3d3bf430dc385c1eb1`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 3.6 MB (3594513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7400c8425778acd83b44cf2785e337c859d1c977da3b9a2795e0154477224f`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d27e1717deca9852671128d6b31175f596e5f09cf5fc4effd28c82c483b011d`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e582d3dc1a65d0aea3250617d371ab13284b64fd6fe5ab3f0dbf3bc4101a90`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 110.3 KB (110332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffeb11c7f284a500f2100a21c4b5744a74759985b38be0ed392f622c2c757a7f`  
		Last Modified: Tue, 04 Mar 2025 00:42:45 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:23b90fbd4e6fead00e5a1f468c3395f0f56b3b67f746a78fda933eac29359282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613dd9d986af870ecb59bf7187c1ac7b3b628075e5155c98b020177664bda5d4`

```dockerfile
```

-	Layers:
	-	`sha256:1fa940c620bbbdfc1ff3d595658a132e12ccd3c40c351e2f1050b1e671a07b14`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 2.1 MB (2055615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:568466c12db8fc80aeffbba52149b2df24f96405b18e5842cc789d68cd7d3d7e`  
		Last Modified: Tue, 04 Mar 2025 00:42:44 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:f0d5f843205a2ae098e0844da2e1ecf56eeddd53db657248179286d7cc1f5287
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:9645f02dde06917a5a74caf5b114d078bf91fecefa3c07bad650e3931da83637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33417906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f9c18bc0d93844d2148aeb3b4355b3b11a8e353b7f52c2581a66dc0b51bc09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e886d53fd71e34f156677e5f3c920065aec39bde653bed233a70cdbfd293103`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 3.6 MB (3559510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3068eeee698392a01193a71b63ede1a5e518fc8079770e4b696a35f572bb97c`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c093511c5a764eeaded55731d227fe276f447b8fbe71cae8002c4a7fbed03f`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd37acaa1173e3184a5824af4926fbc9ce4c47cbd2cdf3196b03dda72e9927e`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 101.9 KB (101927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e187254640288032d41b6e8ba1e8ef9ffe4c421ec2968fd584b3e51f61cdf795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b0494fd11cb3bfcf0c023f1effdefbbebbbd223243b99fac2c71aa9593e7d0`

```dockerfile
```

-	Layers:
	-	`sha256:dfc81f831f5be335aaf17d0db9d47853a277e0edebdb9364c87854ef69a22cf1`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 2.0 MB (1990198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5f55ce97e47412e004a856f83c528789c22b6cc4a16dc12b3d979932e81855`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3dd1e435c740c24734c65d3bb973d75ba2ebce140a2fa3fef81924275d21faf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e330be390a61c6e4d85e1739a1b9807f4ba679d390c021debfb11d724ef231`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fc8223c5bfd2974f1e05403e6b16eef355b4b3272a34640a41ea3ce63e574b`  
		Last Modified: Tue, 04 Mar 2025 00:36:52 GMT  
		Size: 3.6 MB (3558575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a930a686c00255d94fa75b714398830e2cc19fec0bb994159c2df89ea4c62`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13588764d7bbbcc04cc8341becaa22e0fc7076b43e2a4129198b5742c5fa025c`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86653a920a655d981fab36b40898b654a80b7d964bc158906a301770d57723f`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 102.5 KB (102510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9a2b04d41c3799986593fdde6d7402f81328c74bb2efa4cd5f55b445bd72b4ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b4329610f8523b4d9dfcf233339355d5d9c499f959d36ae077d52f2fcae060`

```dockerfile
```

-	Layers:
	-	`sha256:7b73af928b2f5bb1686242e809464fe28a2677b599065a5f5195fcb9538de4f1`  
		Last Modified: Tue, 04 Mar 2025 00:39:42 GMT  
		Size: 2.0 MB (1991243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac61bb4a356e60e66f18048c86c8b321aa9f94d110f63954799b4296bd56453d`  
		Last Modified: Tue, 04 Mar 2025 00:39:42 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:5ed76d74703cfeade7526b64778498405a6b0f35cc69c856a05b2f632c4ecf69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b095e6c6319bf7c1cce7eb76d75e483210bacbb48b04e7322b86b20176b077a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33418310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5757f2249498d019d8c0d49567275c0b8c9c91a9e8ab6b7366f61310a6aacb6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c07e101f716ecaaf863f5ef5bdcdb836204c8ee500d83ceabc00569f0f765bb`  
		Last Modified: Tue, 04 Mar 2025 00:29:32 GMT  
		Size: 3.6 MB (3559488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b18b9881cb934a9f3170d4b841686ce025ae9509b2ff39dc763902c3f55125`  
		Last Modified: Tue, 04 Mar 2025 00:29:32 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c402d3346208a0b69a9ec6c95d744c829061948e3b245d53ec63ac224ebfed9d`  
		Last Modified: Tue, 04 Mar 2025 00:29:31 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e26fc8ef633226d0fd33ca8f838b407ebe7590c02ac5a1b416d09605c1dfb96`  
		Last Modified: Tue, 04 Mar 2025 00:29:32 GMT  
		Size: 101.9 KB (101925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba3654517b09ca7324d64819b14995cb8828fd7c24e1de0f714171523bd1cd6`  
		Last Modified: Tue, 04 Mar 2025 00:29:32 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9de324e0aa16cdcf385bee6793ec98597b70aaf61290a583ee66d9b05b9f7acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2006439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e442844c8c9cc73a6ad32dc829ddfaa39d3981db3c7523a612cd2bf2f6778a`

```dockerfile
```

-	Layers:
	-	`sha256:e362b54ff5a30c78e24dfd266cb8e8f030ff546925d25e724486de6a4b503299`  
		Last Modified: Tue, 04 Mar 2025 00:29:32 GMT  
		Size: 2.0 MB (1990234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e5a516710b6cff860b2d98174d33225c28853466753ac68b6fa9ba032f120ce`  
		Last Modified: Tue, 04 Mar 2025 00:29:31 GMT  
		Size: 16.2 KB (16205 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e291829efc768081b9d7bac4c01d2dff15fb8be1ae1a9ef49679889b9ace1e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32557291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251a51bac4252c9aeb6f74f5d2f33f11a9e480a7004a7bf5aaffe64765375519`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fc8223c5bfd2974f1e05403e6b16eef355b4b3272a34640a41ea3ce63e574b`  
		Last Modified: Tue, 04 Mar 2025 00:36:52 GMT  
		Size: 3.6 MB (3558575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a930a686c00255d94fa75b714398830e2cc19fec0bb994159c2df89ea4c62`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13588764d7bbbcc04cc8341becaa22e0fc7076b43e2a4129198b5742c5fa025c`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86653a920a655d981fab36b40898b654a80b7d964bc158906a301770d57723f`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 102.5 KB (102510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b78c87c174f56887ff96d9b2ecdc24d27439258fc7cb4cc419556ed40d6fe92`  
		Last Modified: Tue, 04 Mar 2025 00:36:52 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6051271174c4d7ec656656806822b1b6b03cb04d0c0827d19a7dc94fda82a2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2007625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b9f88d616247e159dcafdb4e2e5c7dbaef05cac58c645928ada49cb667c82c`

```dockerfile
```

-	Layers:
	-	`sha256:930ce98a6f76f340688d7713fb219b0ca92b57d6dbf5c409b462f8361555c604`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 2.0 MB (1991279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece64be789c0181e0bf58fe02db6f0eb052643d0f0fda5ddf9fd41a8c402d345`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:f0d5f843205a2ae098e0844da2e1ecf56eeddd53db657248179286d7cc1f5287
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:9645f02dde06917a5a74caf5b114d078bf91fecefa3c07bad650e3931da83637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33417906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f9c18bc0d93844d2148aeb3b4355b3b11a8e353b7f52c2581a66dc0b51bc09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e886d53fd71e34f156677e5f3c920065aec39bde653bed233a70cdbfd293103`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 3.6 MB (3559510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3068eeee698392a01193a71b63ede1a5e518fc8079770e4b696a35f572bb97c`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c093511c5a764eeaded55731d227fe276f447b8fbe71cae8002c4a7fbed03f`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd37acaa1173e3184a5824af4926fbc9ce4c47cbd2cdf3196b03dda72e9927e`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 101.9 KB (101927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e187254640288032d41b6e8ba1e8ef9ffe4c421ec2968fd584b3e51f61cdf795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58b0494fd11cb3bfcf0c023f1effdefbbebbbd223243b99fac2c71aa9593e7d0`

```dockerfile
```

-	Layers:
	-	`sha256:dfc81f831f5be335aaf17d0db9d47853a277e0edebdb9364c87854ef69a22cf1`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 2.0 MB (1990198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5f55ce97e47412e004a856f83c528789c22b6cc4a16dc12b3d979932e81855`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3dd1e435c740c24734c65d3bb973d75ba2ebce140a2fa3fef81924275d21faf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32556861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e330be390a61c6e4d85e1739a1b9807f4ba679d390c021debfb11d724ef231`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fc8223c5bfd2974f1e05403e6b16eef355b4b3272a34640a41ea3ce63e574b`  
		Last Modified: Tue, 04 Mar 2025 00:36:52 GMT  
		Size: 3.6 MB (3558575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a930a686c00255d94fa75b714398830e2cc19fec0bb994159c2df89ea4c62`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13588764d7bbbcc04cc8341becaa22e0fc7076b43e2a4129198b5742c5fa025c`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86653a920a655d981fab36b40898b654a80b7d964bc158906a301770d57723f`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 102.5 KB (102510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9a2b04d41c3799986593fdde6d7402f81328c74bb2efa4cd5f55b445bd72b4ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b4329610f8523b4d9dfcf233339355d5d9c499f959d36ae077d52f2fcae060`

```dockerfile
```

-	Layers:
	-	`sha256:7b73af928b2f5bb1686242e809464fe28a2677b599065a5f5195fcb9538de4f1`  
		Last Modified: Tue, 04 Mar 2025 00:39:42 GMT  
		Size: 2.0 MB (1991243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac61bb4a356e60e66f18048c86c8b321aa9f94d110f63954799b4296bd56453d`  
		Last Modified: Tue, 04 Mar 2025 00:39:42 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:5ed76d74703cfeade7526b64778498405a6b0f35cc69c856a05b2f632c4ecf69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b095e6c6319bf7c1cce7eb76d75e483210bacbb48b04e7322b86b20176b077a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33418310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5757f2249498d019d8c0d49567275c0b8c9c91a9e8ab6b7366f61310a6aacb6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c07e101f716ecaaf863f5ef5bdcdb836204c8ee500d83ceabc00569f0f765bb`  
		Last Modified: Tue, 04 Mar 2025 00:29:32 GMT  
		Size: 3.6 MB (3559488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b18b9881cb934a9f3170d4b841686ce025ae9509b2ff39dc763902c3f55125`  
		Last Modified: Tue, 04 Mar 2025 00:29:32 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c402d3346208a0b69a9ec6c95d744c829061948e3b245d53ec63ac224ebfed9d`  
		Last Modified: Tue, 04 Mar 2025 00:29:31 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e26fc8ef633226d0fd33ca8f838b407ebe7590c02ac5a1b416d09605c1dfb96`  
		Last Modified: Tue, 04 Mar 2025 00:29:32 GMT  
		Size: 101.9 KB (101925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba3654517b09ca7324d64819b14995cb8828fd7c24e1de0f714171523bd1cd6`  
		Last Modified: Tue, 04 Mar 2025 00:29:32 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9de324e0aa16cdcf385bee6793ec98597b70aaf61290a583ee66d9b05b9f7acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2006439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e442844c8c9cc73a6ad32dc829ddfaa39d3981db3c7523a612cd2bf2f6778a`

```dockerfile
```

-	Layers:
	-	`sha256:e362b54ff5a30c78e24dfd266cb8e8f030ff546925d25e724486de6a4b503299`  
		Last Modified: Tue, 04 Mar 2025 00:29:32 GMT  
		Size: 2.0 MB (1990234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e5a516710b6cff860b2d98174d33225c28853466753ac68b6fa9ba032f120ce`  
		Last Modified: Tue, 04 Mar 2025 00:29:31 GMT  
		Size: 16.2 KB (16205 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e291829efc768081b9d7bac4c01d2dff15fb8be1ae1a9ef49679889b9ace1e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32557291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:251a51bac4252c9aeb6f74f5d2f33f11a9e480a7004a7bf5aaffe64765375519`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fc8223c5bfd2974f1e05403e6b16eef355b4b3272a34640a41ea3ce63e574b`  
		Last Modified: Tue, 04 Mar 2025 00:36:52 GMT  
		Size: 3.6 MB (3558575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202a930a686c00255d94fa75b714398830e2cc19fec0bb994159c2df89ea4c62`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13588764d7bbbcc04cc8341becaa22e0fc7076b43e2a4129198b5742c5fa025c`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86653a920a655d981fab36b40898b654a80b7d964bc158906a301770d57723f`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 102.5 KB (102510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b78c87c174f56887ff96d9b2ecdc24d27439258fc7cb4cc419556ed40d6fe92`  
		Last Modified: Tue, 04 Mar 2025 00:36:52 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6051271174c4d7ec656656806822b1b6b03cb04d0c0827d19a7dc94fda82a2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2007625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b9f88d616247e159dcafdb4e2e5c7dbaef05cac58c645928ada49cb667c82c`

```dockerfile
```

-	Layers:
	-	`sha256:930ce98a6f76f340688d7713fb219b0ca92b57d6dbf5c409b462f8361555c604`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 2.0 MB (1991279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece64be789c0181e0bf58fe02db6f0eb052643d0f0fda5ddf9fd41a8c402d345`  
		Last Modified: Tue, 04 Mar 2025 00:36:51 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:fe69c78b7324bb178dee86ba6feee10b12ce31ff043b238f974f8a6563650d1c
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
$ docker pull neurodebian@sha256:7e398bdf282bf7b2de959d4e7871a00efdba7a3b94315f38909d9ad9eaec37c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59853092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0b605439b5903c5bd63e29c9fb820b6abb0892ce58d30d207c979223b9ec1d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8384fb657fddabb65893303e0a8f3c12bff01fafe00408cb06cb59da23a5b77b`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 11.3 MB (11266799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af38886ee03781ededd4d9c12fae87ab80880ef72a9c2e172c8d5f219d9824f`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88ac60b75849f44596a182fc0d9c00455a3ec54a32e5b38069df6b450a74def`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbc24edec90455b4172e2932b5777bc5f1382faef1259e1e04ecc6bae4cbf98`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 93.1 KB (93129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29795a5744ab07889ef89525b2147edf8c116dcfe94fa2db1132658a2dd9ad0`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b87313acde5fcf89bf43bf7b3b5871cd545f8a3285587ed68bfb4b5b57e61579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53c6b4dc71ea8685a6a40ed80932879e4014a40561bdd1a447d5f358545ec1c`

```dockerfile
```

-	Layers:
	-	`sha256:6c9ecc685f67450b07394a41de82db9fbf4ad8d9e1893feceb4134ce6a4d0ac7`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 3.9 MB (3934212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b606bc0549f263243d00b7f86422fb054bfcddf31523519a277b3ef0a891815f`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:45ad749f9bcd8e51602bd81dbd4201d29678379baa897125f9bb7f77d20f8465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59656149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddecea2fbc72473b511ca2e1fd47d21929e18fb548c9d544c0ac01712e3f9ac`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce08a29378b322d580a290ac850ee07138f732ffb563fd5c9ced94337ecfadf`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 11.2 MB (11232654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c994ce850f986eb5546d5276357b320b7bde68728c6257f9f77b9539290f72`  
		Last Modified: Tue, 08 Apr 2025 06:36:08 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c982b1954d94fe6ee8540f3d265491f3cf0dd395d3534a72e93c4fad36fbd9`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1367d165818a29284a9956a4df5e0769d1e2307631fc56bb05d36b69ca141`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 93.4 KB (93402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4af8e57251ac91dbbc525315d0377b42e6a750861089644e6f83134df5f4cf7`  
		Last Modified: Tue, 08 Apr 2025 06:36:22 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:889d830f6f8c37bb97f6c577d74b44ac7134ecc7067b9e1659c0329b7051917b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0c4c6354a373d3e63afd8b8b68da58b7b301db319e4432a32787cf11bc2a36`

```dockerfile
```

-	Layers:
	-	`sha256:f1b36a946b7421c5d1db125ead18ecf82bd46dc1d400123d4f5a8799b10fec5d`  
		Last Modified: Tue, 08 Apr 2025 06:36:22 GMT  
		Size: 3.9 MB (3934466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10e4b44ba7973ffe780662ff642440c6f6ceb6d4d6578bbfded6f9aaf6ee4c5`  
		Last Modified: Tue, 08 Apr 2025 06:36:22 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:77c4a11b877bd3695148289f8a619cd0a20b104bf12de5acf55b239b72c0dc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fb6ad261db4fd2e52ce4f0d6ccf15f1d0a4db69e6b7dd032dcea490167ed52`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c608ceda0b7454a97d884128aeeaa0bbda21fdbdf8119d7d88369c9ad0b91dd`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 11.7 MB (11688951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76c42422411b6fa3e8310cda6b4848d0ce9e210ed01e9825da2fbda0d3aa64c`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6869c5c8538c781cc3026ff93a7d2bc201709cba9d62d71943d18c2656e5a614`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883527fb04daca1643441eac1d252402727d310a2f385e3bad00cc08e0a95ea4`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 93.2 KB (93216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0e418c69eea3da98ff7405c3faa74ae00a63913463d0cb139fea3d28916a4`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f231e6f1d97565b2e28c8e6e28278ae3ded47c6088092bba32ad9deafe1677d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48e2b84fd898e55805a1a87c6dc5ae8c4ed71d306e06cd096b5ffd8b0a9b40a`

```dockerfile
```

-	Layers:
	-	`sha256:50be1ac0d7eaa72054bc23932238bcb1c9ab939bad36afe36ddd2c47b82a387e`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 3.9 MB (3932129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e81fcc4d5a20ce3e7c427e156d5ebd3b43b59d07e310b47b711be387be00e8a`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json
