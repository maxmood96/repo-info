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
$ docker pull neurodebian@sha256:e68b01fb0dea971fa4cfd39d8feb687c3fe2aa4bd228ca5e72189d11d8c78908
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:ec026f26f90a1da8ffc3ba59281854c0bb1a0b5f166e58e75d57f34e8424bd0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa3d04109e9bf85dbba55e27e2b0055d3c73ba8b1f21907acb2c7bdb223320`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
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
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabac9a159eac99d387c3b1a92d15536e78c12f6596c2dbd37f29d0b63d5dffe`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 5.4 MB (5362390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e9f035d7685c2fdb1e905a640424e5ad669ee2970a32cbec7f8d889e3625f1`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb125018a09465c3a7d0200be55fc6435a06fe742fd5a7a7ef39a0fb83cfbf6`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab46b9b7320bd76241047fcf77910ba82992b5e91e204eefe5390b265739db65`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 105.4 KB (105439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed731be31bff11d448e1a27d734e900b2e674625af668b3f9b87ba45b1a8f3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fb983f465508bd38f2970b20fcfd3052779b73f8d3b436c6ab4ff79915307d`

```dockerfile
```

-	Layers:
	-	`sha256:079d7ce90a22f0bd844b80ccfaee90ce51150b4f1244f3519448f12bf6c83630`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 2.0 MB (2017825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d275b201a8175e6493a6207f8e73ff2b18780007de8ef8e54adc086578431b8d`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:39c9bfd66371de386419abe34cd806357a534145fbce48504409d1f8f396a4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31428044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45aed6d0d9e4f56fcf7aaaad06b6a747462168128f4a0d1f3e2084772af72fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Sat, 01 Mar 2025 01:29:10 GMT
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
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfea6f96cd3c0c4d3ef57f10961124979c910ce593821968c85de9d48b52bca`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 5.3 MB (5342712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb3a85d8318dcd1870169782a64e5bacdbfb980f3a540727b8e48f3535792c`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925eadc6c6b51b14149f7e93def87f6fa91ec4696c9836fedc3690164ac803f`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10f701523b10a388f198e7017b2652f57269ac92c532a36cd50ff87d23b2d64`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 105.5 KB (105511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2952dad8358145d90322cccd4047ea733f93fc11fed56791f2817ddc6d99d545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0237cdae437eaedee949f6af64e985420e981a9dfa9474fce1bb2e9aa7fbb8fd`

```dockerfile
```

-	Layers:
	-	`sha256:f307ef0a8e38175dd6e3ceb807d756938a14b991426d356ef4e8432d33ab7e37`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 2.0 MB (2018054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8946cab190197295b0fd0de39d4d1f5d0e06793a5eb36d0073e79597d9fd10d1`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:4c1ed82e5488cc7a87a4035c84b91368bf439418f76c388be8923760e27cc034
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5b5f12c95fa70eba84ed0d9a8cfd320ff1f928e0f4ecc665553188865bc1fdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77302996458a5ea42a30e362fe60a32b80399042312ed4461165057feaadc3a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
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
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09894bd673fc3443fa4aac9c04f3790e80821023e1b647cb36b0dbb3295685a1`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 5.4 MB (5362436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b567f68d429f42a824fdac7d380831ff3ee4e919d2c1f56ac4ba2d5c728dab9`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe211eff3c4623dbc046e34c08495b6c3665295d30178fc8053cd5baff9b469`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd93ed51b316d633e53abd6403ccacb66bf2b80b807810d40df2342572077415`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 105.4 KB (105442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ca65e65a74419b6f595b799268195de974952d7e1558d9a39092265337398f`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:451612c81608c2bebc8d3e36a6a521b28025afe8d027348134cdac02a7ec34d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81e43683e94761e4cae4d1f50b39b3b1ced64f4fb773232eb29f20df0b386bb`

```dockerfile
```

-	Layers:
	-	`sha256:79b4a3ef3b60d9c20c2340237fe4236376a35581ce8f29f76d044ea8920b97d3`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 2.0 MB (2017861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd949e8f808ff83620701f51061d8dc60e04b6e7afc9a968a71e3ed0ef991e1`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b31849bda994a89ea1e43d1ee83490728e5c84d98e21bb02362919c0ee14a139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31428326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9884153e1d1e0355067632367672016383e04b73464a2d8661e4d01f7cf3d14`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Sat, 01 Mar 2025 01:29:10 GMT
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
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfea6f96cd3c0c4d3ef57f10961124979c910ce593821968c85de9d48b52bca`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 5.3 MB (5342712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb3a85d8318dcd1870169782a64e5bacdbfb980f3a540727b8e48f3535792c`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925eadc6c6b51b14149f7e93def87f6fa91ec4696c9836fedc3690164ac803f`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10f701523b10a388f198e7017b2652f57269ac92c532a36cd50ff87d23b2d64`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 105.5 KB (105511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8215c91245c0463263d03909dc6267e663f8bc6ca035c5fa1478e3632affb97f`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8e0dd953f78b0d8045d26f7afb42c726a2cc4e07a96a2b3b741316ca99534d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea7d3f1b864509ea868bded897bb9ca30f452582999b77e73c6bfc798dd9443`

```dockerfile
```

-	Layers:
	-	`sha256:1fcbe13a76f25efb5f459970d227c4628a1a8f71064188a5cd94ffb6874dd526`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 2.0 MB (2018090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8dac00fd22e65ab791eda65319d76e0834a665f17c3cf1d1784f781fa3bcd68`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:26f539327816198b90ed431924fec2ff158a98aa745b593bdfb2b2ae8c0cdb4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:5ca7d2535708de52e59146391a85e3222685b2101bcf6fbc69c6feaf164fa8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf1b0c7fa661952a44369df7910143a9f46830a62c9ee24693812478330d276`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7502f8f384c9e39101e17b46acf0f303f53f00c3076b70089bf8b5293c14a4e`  
		Last Modified: Wed, 09 Apr 2025 01:19:25 GMT  
		Size: 3.6 MB (3623789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305875cc34b35c47d97f34abae20428fc4785a556dfebcb1e04c18a29117c3`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6ad9396ff5157816c245d94d7dabb054e837511ea47b307ed3762318e74bfe`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ac9ef6b50c230c07920e2ccb263260c5218521277d00c0b20f9baebd17b8ff`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 110.7 KB (110667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:810ca171bbe3a461ad3f9c0c841ca6a05c8ceb604c62f05408e5d9b9fb683cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992fa750bd033c67b1276168605e2c584b3fbd033a0f2ae6979168542be25358`

```dockerfile
```

-	Layers:
	-	`sha256:364e84565c06cba8f2e91059f991c8688d269b08155b49077e48c4f2494fec78`  
		Last Modified: Wed, 09 Apr 2025 01:19:25 GMT  
		Size: 2.1 MB (2055399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e73795a9937a5c5f7a6f43e8dcdc653d5018d6e430e3b67b8783a422fc7c17`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4bfdcd9bb99802a608520d891d99b9a896b9e519c3fc710f5da8a3c92e29e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5203958ef9579128f347a4bff0aa2c110790666b706dcff91afdf58e7071c151`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff69349668077007180f865cd316b1438d2244cfb6b5877a93d2ef957fae893`  
		Last Modified: Wed, 09 Apr 2025 08:38:35 GMT  
		Size: 3.6 MB (3595245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ba73de0fee7dddc1e560209decbfbb8b8bfdcfc88bbab92fa5c475aea44d6`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f3443353aec912c7886b00a30c1cbded982093a0100e7b31360469c9bc243d`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607d514962ad10eec887ec71fc1184b491c71747421dc4270402e4b0789bbf9`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 110.5 KB (110487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f47f5e2a24302ecae11fa9f56b627034c206301bfc142a63a03ba0ba63a2761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4792f4614d130d88d6574df8a599739fe6f52d661775cb0d3124c95e3f72c8c0`

```dockerfile
```

-	Layers:
	-	`sha256:aeb0c1d1d0fdd14937cc58efd46f5290c63cc757662509258f20fa18fadf548f`  
		Last Modified: Wed, 09 Apr 2025 08:38:35 GMT  
		Size: 2.1 MB (2055659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a2eafa98dff300a61f97ed986282c056145cd6a289464d241a3947fc933ce2`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:e67dd8274275cc1bc4ccc9c495df2cba487d4c057261a5bbe3a675fc905f7b25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2ea75232b46889271617dc481821e1909d05ce5e92545bbba1227bab364999f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d461c6f7b13738c6b4f1a89ee7e24ecff7dc5c5a5bbc035480235c5bff84a0`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b515f437b37abbbf80a20851603ea0e660cc33ed3133ce6e83a3a5001b47cfa8`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 3.6 MB (3623809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eac336a51090a23cc0914f157aeca298493cf6392d5a7bf98a11285541c58de`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89e1a0218ea67a334a752b5e3a2de2d7fce6f8229c537fed384ce40a6c73eef`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad56d373af038e98991e376e180b79cefcac28fcd50c4691e4936c45c0b2c83`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 110.6 KB (110648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ed4506459d767c55f263519a1a8867dcc18b98989376d59aa73bb765358090`  
		Last Modified: Wed, 09 Apr 2025 01:19:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8083f260db3c7a548cbc86e95fe014cd17b417e18f266dc7177bb5a53f7d906f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c20ab0ef254c9cc608600b01f7841ed992b3760200c569b0a4dbabffb2f87a`

```dockerfile
```

-	Layers:
	-	`sha256:c5dec75c2040837c9f93ab3fe9b47cf1145215b4e726a25573ebf5efff863796`  
		Last Modified: Wed, 09 Apr 2025 01:19:18 GMT  
		Size: 2.1 MB (2055435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d34f17d0e8739af8fb593e06c8d6482c9edbf64bcd81892b92387c37fe99cc`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d7d3fe31084430bceba93d5ef8c36791c06f81aaba37fd3061e605640cc21799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21edc9ced3f14de6089c514ea712e115634ea4f472b6bade77784b66e285b19d`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff69349668077007180f865cd316b1438d2244cfb6b5877a93d2ef957fae893`  
		Last Modified: Wed, 09 Apr 2025 08:38:35 GMT  
		Size: 3.6 MB (3595245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ba73de0fee7dddc1e560209decbfbb8b8bfdcfc88bbab92fa5c475aea44d6`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f3443353aec912c7886b00a30c1cbded982093a0100e7b31360469c9bc243d`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607d514962ad10eec887ec71fc1184b491c71747421dc4270402e4b0789bbf9`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 110.5 KB (110487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa8c2eec598bd3e1f629937728f657e829a66175aebd83ec75955e0610b7d70`  
		Last Modified: Wed, 09 Apr 2025 08:38:47 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2a65e2f92ef29328dde9fa680fb2ba4202004cebd5d59beb8d6dfb27e06937fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88aea1a112a0452f1a588ced51bfba8be8fd61b854ae3a85f7f56b9bc1757a1e`

```dockerfile
```

-	Layers:
	-	`sha256:72ffbab84cded574356793b5cc86203486b55dd41f91eac101c436104bcd477b`  
		Last Modified: Wed, 09 Apr 2025 08:38:47 GMT  
		Size: 2.1 MB (2055695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0936d3750f33d18090c78dc9e1806e9c95d79d56b2cd5a5a2ea94dac2b22ec`  
		Last Modified: Wed, 09 Apr 2025 08:38:46 GMT  
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
$ docker pull neurodebian@sha256:e68b01fb0dea971fa4cfd39d8feb687c3fe2aa4bd228ca5e72189d11d8c78908
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:ec026f26f90a1da8ffc3ba59281854c0bb1a0b5f166e58e75d57f34e8424bd0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68aa3d04109e9bf85dbba55e27e2b0055d3c73ba8b1f21907acb2c7bdb223320`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
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
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabac9a159eac99d387c3b1a92d15536e78c12f6596c2dbd37f29d0b63d5dffe`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 5.4 MB (5362390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e9f035d7685c2fdb1e905a640424e5ad669ee2970a32cbec7f8d889e3625f1`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb125018a09465c3a7d0200be55fc6435a06fe742fd5a7a7ef39a0fb83cfbf6`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab46b9b7320bd76241047fcf77910ba82992b5e91e204eefe5390b265739db65`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 105.4 KB (105439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed731be31bff11d448e1a27d734e900b2e674625af668b3f9b87ba45b1a8f3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fb983f465508bd38f2970b20fcfd3052779b73f8d3b436c6ab4ff79915307d`

```dockerfile
```

-	Layers:
	-	`sha256:079d7ce90a22f0bd844b80ccfaee90ce51150b4f1244f3519448f12bf6c83630`  
		Last Modified: Wed, 09 Apr 2025 01:19:33 GMT  
		Size: 2.0 MB (2017825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d275b201a8175e6493a6207f8e73ff2b18780007de8ef8e54adc086578431b8d`  
		Last Modified: Wed, 09 Apr 2025 01:19:32 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:39c9bfd66371de386419abe34cd806357a534145fbce48504409d1f8f396a4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31428044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c45aed6d0d9e4f56fcf7aaaad06b6a747462168128f4a0d1f3e2084772af72fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Sat, 01 Mar 2025 01:29:10 GMT
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
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfea6f96cd3c0c4d3ef57f10961124979c910ce593821968c85de9d48b52bca`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 5.3 MB (5342712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb3a85d8318dcd1870169782a64e5bacdbfb980f3a540727b8e48f3535792c`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925eadc6c6b51b14149f7e93def87f6fa91ec4696c9836fedc3690164ac803f`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10f701523b10a388f198e7017b2652f57269ac92c532a36cd50ff87d23b2d64`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 105.5 KB (105511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2952dad8358145d90322cccd4047ea733f93fc11fed56791f2817ddc6d99d545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2032155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0237cdae437eaedee949f6af64e985420e981a9dfa9474fce1bb2e9aa7fbb8fd`

```dockerfile
```

-	Layers:
	-	`sha256:f307ef0a8e38175dd6e3ceb807d756938a14b991426d356ef4e8432d33ab7e37`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 2.0 MB (2018054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8946cab190197295b0fd0de39d4d1f5d0e06793a5eb36d0073e79597d9fd10d1`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:4c1ed82e5488cc7a87a4035c84b91368bf439418f76c388be8923760e27cc034
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5b5f12c95fa70eba84ed0d9a8cfd320ff1f928e0f4ecc665553188865bc1fdb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32980712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77302996458a5ea42a30e362fe60a32b80399042312ed4461165057feaadc3a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Sat, 01 Mar 2025 01:29:10 GMT
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
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09894bd673fc3443fa4aac9c04f3790e80821023e1b647cb36b0dbb3295685a1`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 5.4 MB (5362436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b567f68d429f42a824fdac7d380831ff3ee4e919d2c1f56ac4ba2d5c728dab9`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe211eff3c4623dbc046e34c08495b6c3665295d30178fc8053cd5baff9b469`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd93ed51b316d633e53abd6403ccacb66bf2b80b807810d40df2342572077415`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 105.4 KB (105442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ca65e65a74419b6f595b799268195de974952d7e1558d9a39092265337398f`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:451612c81608c2bebc8d3e36a6a521b28025afe8d027348134cdac02a7ec34d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81e43683e94761e4cae4d1f50b39b3b1ced64f4fb773232eb29f20df0b386bb`

```dockerfile
```

-	Layers:
	-	`sha256:79b4a3ef3b60d9c20c2340237fe4236376a35581ce8f29f76d044ea8920b97d3`  
		Last Modified: Wed, 09 Apr 2025 01:19:27 GMT  
		Size: 2.0 MB (2017861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd949e8f808ff83620701f51061d8dc60e04b6e7afc9a968a71e3ed0ef991e1`  
		Last Modified: Wed, 09 Apr 2025 01:19:26 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b31849bda994a89ea1e43d1ee83490728e5c84d98e21bb02362919c0ee14a139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31428326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9884153e1d1e0355067632367672016383e04b73464a2d8661e4d01f7cf3d14`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
ARG RELEASE
# Sat, 01 Mar 2025 01:29:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 01 Mar 2025 01:29:10 GMT
LABEL org.opencontainers.image.version=20.04
# Sat, 01 Mar 2025 01:29:10 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Sat, 01 Mar 2025 01:29:10 GMT
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
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bfea6f96cd3c0c4d3ef57f10961124979c910ce593821968c85de9d48b52bca`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 5.3 MB (5342712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eb3a85d8318dcd1870169782a64e5bacdbfb980f3a540727b8e48f3535792c`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4925eadc6c6b51b14149f7e93def87f6fa91ec4696c9836fedc3690164ac803f`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10f701523b10a388f198e7017b2652f57269ac92c532a36cd50ff87d23b2d64`  
		Last Modified: Wed, 09 Apr 2025 08:37:58 GMT  
		Size: 105.5 KB (105511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8215c91245c0463263d03909dc6267e663f8bc6ca035c5fa1478e3632affb97f`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8e0dd953f78b0d8045d26f7afb42c726a2cc4e07a96a2b3b741316ca99534d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea7d3f1b864509ea868bded897bb9ca30f452582999b77e73c6bfc798dd9443`

```dockerfile
```

-	Layers:
	-	`sha256:1fcbe13a76f25efb5f459970d227c4628a1a8f71064188a5cd94ffb6874dd526`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 2.0 MB (2018090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8dac00fd22e65ab791eda65319d76e0834a665f17c3cf1d1784f781fa3bcd68`  
		Last Modified: Wed, 09 Apr 2025 08:38:10 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:26f539327816198b90ed431924fec2ff158a98aa745b593bdfb2b2ae8c0cdb4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:5ca7d2535708de52e59146391a85e3222685b2101bcf6fbc69c6feaf164fa8c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf1b0c7fa661952a44369df7910143a9f46830a62c9ee24693812478330d276`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7502f8f384c9e39101e17b46acf0f303f53f00c3076b70089bf8b5293c14a4e`  
		Last Modified: Wed, 09 Apr 2025 01:19:25 GMT  
		Size: 3.6 MB (3623789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8305875cc34b35c47d97f34abae20428fc4785a556dfebcb1e04c18a29117c3`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6ad9396ff5157816c245d94d7dabb054e837511ea47b307ed3762318e74bfe`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ac9ef6b50c230c07920e2ccb263260c5218521277d00c0b20f9baebd17b8ff`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 110.7 KB (110667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:810ca171bbe3a461ad3f9c0c841ca6a05c8ceb604c62f05408e5d9b9fb683cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992fa750bd033c67b1276168605e2c584b3fbd033a0f2ae6979168542be25358`

```dockerfile
```

-	Layers:
	-	`sha256:364e84565c06cba8f2e91059f991c8688d269b08155b49077e48c4f2494fec78`  
		Last Modified: Wed, 09 Apr 2025 01:19:25 GMT  
		Size: 2.1 MB (2055399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e73795a9937a5c5f7a6f43e8dcdc653d5018d6e430e3b67b8783a422fc7c17`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4bfdcd9bb99802a608520d891d99b9a896b9e519c3fc710f5da8a3c92e29e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5203958ef9579128f347a4bff0aa2c110790666b706dcff91afdf58e7071c151`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff69349668077007180f865cd316b1438d2244cfb6b5877a93d2ef957fae893`  
		Last Modified: Wed, 09 Apr 2025 08:38:35 GMT  
		Size: 3.6 MB (3595245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ba73de0fee7dddc1e560209decbfbb8b8bfdcfc88bbab92fa5c475aea44d6`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f3443353aec912c7886b00a30c1cbded982093a0100e7b31360469c9bc243d`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607d514962ad10eec887ec71fc1184b491c71747421dc4270402e4b0789bbf9`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 110.5 KB (110487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f47f5e2a24302ecae11fa9f56b627034c206301bfc142a63a03ba0ba63a2761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4792f4614d130d88d6574df8a599739fe6f52d661775cb0d3124c95e3f72c8c0`

```dockerfile
```

-	Layers:
	-	`sha256:aeb0c1d1d0fdd14937cc58efd46f5290c63cc757662509258f20fa18fadf548f`  
		Last Modified: Wed, 09 Apr 2025 08:38:35 GMT  
		Size: 2.1 MB (2055659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58a2eafa98dff300a61f97ed986282c056145cd6a289464d241a3947fc933ce2`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:e67dd8274275cc1bc4ccc9c495df2cba487d4c057261a5bbe3a675fc905f7b25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2ea75232b46889271617dc481821e1909d05ce5e92545bbba1227bab364999f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d461c6f7b13738c6b4f1a89ee7e24ecff7dc5c5a5bbc035480235c5bff84a0`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b515f437b37abbbf80a20851603ea0e660cc33ed3133ce6e83a3a5001b47cfa8`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 3.6 MB (3623809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eac336a51090a23cc0914f157aeca298493cf6392d5a7bf98a11285541c58de`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89e1a0218ea67a334a752b5e3a2de2d7fce6f8229c537fed384ce40a6c73eef`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad56d373af038e98991e376e180b79cefcac28fcd50c4691e4936c45c0b2c83`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 110.6 KB (110648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ed4506459d767c55f263519a1a8867dcc18b98989376d59aa73bb765358090`  
		Last Modified: Wed, 09 Apr 2025 01:19:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8083f260db3c7a548cbc86e95fe014cd17b417e18f266dc7177bb5a53f7d906f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2071641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c20ab0ef254c9cc608600b01f7841ed992b3760200c569b0a4dbabffb2f87a`

```dockerfile
```

-	Layers:
	-	`sha256:c5dec75c2040837c9f93ab3fe9b47cf1145215b4e726a25573ebf5efff863796`  
		Last Modified: Wed, 09 Apr 2025 01:19:18 GMT  
		Size: 2.1 MB (2055435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d34f17d0e8739af8fb593e06c8d6482c9edbf64bcd81892b92387c37fe99cc`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d7d3fe31084430bceba93d5ef8c36791c06f81aaba37fd3061e605640cc21799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31062426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21edc9ced3f14de6089c514ea712e115634ea4f472b6bade77784b66e285b19d`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff69349668077007180f865cd316b1438d2244cfb6b5877a93d2ef957fae893`  
		Last Modified: Wed, 09 Apr 2025 08:38:35 GMT  
		Size: 3.6 MB (3595245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ba73de0fee7dddc1e560209decbfbb8b8bfdcfc88bbab92fa5c475aea44d6`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f3443353aec912c7886b00a30c1cbded982093a0100e7b31360469c9bc243d`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607d514962ad10eec887ec71fc1184b491c71747421dc4270402e4b0789bbf9`  
		Last Modified: Wed, 09 Apr 2025 08:38:34 GMT  
		Size: 110.5 KB (110487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa8c2eec598bd3e1f629937728f657e829a66175aebd83ec75955e0610b7d70`  
		Last Modified: Wed, 09 Apr 2025 08:38:47 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2a65e2f92ef29328dde9fa680fb2ba4202004cebd5d59beb8d6dfb27e06937fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2072041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88aea1a112a0452f1a588ced51bfba8be8fd61b854ae3a85f7f56b9bc1757a1e`

```dockerfile
```

-	Layers:
	-	`sha256:72ffbab84cded574356793b5cc86203486b55dd41f91eac101c436104bcd477b`  
		Last Modified: Wed, 09 Apr 2025 08:38:47 GMT  
		Size: 2.1 MB (2055695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0936d3750f33d18090c78dc9e1806e9c95d79d56b2cd5a5a2ea94dac2b22ec`  
		Last Modified: Wed, 09 Apr 2025 08:38:46 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:3933533efbcb36dce4797805ffac1fbd558f96a4f39af547cb98b2789c01a6d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:feb563112d19fff419ebaaf53bc5ebbc34dcc9040aa628f096c64581a1456e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34deb8132c5a1686ec9d58286361410699754a2f529baa356730c46175a0c4cc`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0dec45a929850354a090e228dca34ea64770e73d857734d9a726740b48821f`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 3.6 MB (3561457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f089d3e9c9757e05c4d1311a2d6aba13c856f4a573071a44317b2a6ba0fd4f`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7634be1479388a2b7edb17be8f8a1f9b6aa3c208bf603334d8e09a171c1ce3a`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a839418267feaba920430528a06b30b3cfb66c0f07340f224de25719c9ce7e`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 102.8 KB (102754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cf4d8c29a06175b0473d2537cb5752dbd70d4448bf0158b28648dc07c6123f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2cd8ab6147458d6a82473940a41794b24d350ba03b1ac233e56c1158b53577`

```dockerfile
```

-	Layers:
	-	`sha256:bfb767ec62c3e301f953ba7598a86e910a45e3aee0d5e36d0c80f3b4d7f1d956`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 2.0 MB (1988003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81811e8647f0d03d6ec1be3d5d5e90a149eed9376838f9d536643e9fe7e4b8a9`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:14e68a1ef1499774ab0ff0549fb20c7f0834529679bcc7eae47638bcec32576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d970e55ec6b45eb6d0019fca0ed0c912ec1eb0d52993192334d6119b2740ef10`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3a6fe8ef82163d62cf9479c2af31f1dee76721ce7bdb1467f9784054fb5170`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 3.6 MB (3560005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7393046cfa6f68b53023c0509639d45a59706d5588f4480400d1b5f4d1d51c`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85eb7bd55d65f923168a612b75ca3362461569117659348df33de167f110e2de`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3b50d982d93658713726dd5112aa3092e61c54100c34a8400e31f062b0cb54`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 103.3 KB (103335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ab743af2d7bb08cc2c69eebc7eb51f7fdd2f5e7af502f6be85cbc87edaa281d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea7034c60b178ec24c97c8ca6c23f5e8bab3222ca1ddf30c46652b3ff1f9d01`

```dockerfile
```

-	Layers:
	-	`sha256:931bad7ad10f121b5bbe0f215058463c976a98a44f9b02f27f056603d1cd0f2e`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 2.0 MB (1989048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f27bf5833a0ccc06e9de9d76d1c100cce0c517576ebad70a34e924f9f8b96f`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:bb1f2ac5fe5f0fe5344c7f6e87115a959354b486f5c522e7b3bbd2c528825f45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdd4ee60546b3456f3198b0a327b0fd78e7c7da13ff05c7aab8954206e6704f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223dbadc92923109c96d9fc8fc28e5c04ff90f64ebff061e9659599ef2a5cee3`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d3be5c72d2ebd1930b95e38b510610cdb291c3324059c55a09596571ba4c4`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 3.6 MB (3561362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de97d0aaf79df6e4cbb6915e4d4a0928c52bd14bfe06eb96dbcb17f26769fc2e`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b3caeb47db1287e5ec5631a60249266bbb9fdcc9a9922d551ff47aae973d8`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cef7682edab5bfa56738f780bb24e3f66449d19e8dce0cf54a9a9cd94233456`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 102.7 KB (102726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ecec4fcbc6ac0c3f46667ce1f223ee30d6e450aa0631e5b43427c23477be7d`  
		Last Modified: Wed, 09 Apr 2025 01:19:18 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b9f65e539e873578da361c2db1d91aaadc2d8500c4025e4c8c60887b496e2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2162866fd4065055a2a1233c4456c060395e802d2823a032dd2c1f773090b6be`

```dockerfile
```

-	Layers:
	-	`sha256:ad9ad816620dd1b17b44cf321ed4c092277da0053c029ec00b44f8fa4dbd15c2`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 2.0 MB (1988039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fa6831df1b93fe94bb9fdf856d3714daa7e72a01c7bbe7c77fcb0f869036229`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0b5d43d5d0aeea5fa8470c82bc076f4904af80272d015abc891445aaa063dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad171fc77df47499dbb19577f4ebfa52637116d2d4e09ab016e39f034ec6e09`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3a6fe8ef82163d62cf9479c2af31f1dee76721ce7bdb1467f9784054fb5170`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 3.6 MB (3560005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7393046cfa6f68b53023c0509639d45a59706d5588f4480400d1b5f4d1d51c`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85eb7bd55d65f923168a612b75ca3362461569117659348df33de167f110e2de`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3b50d982d93658713726dd5112aa3092e61c54100c34a8400e31f062b0cb54`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 103.3 KB (103335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de88003e696aae6b7a25af242820bdfcb0c3f13c1cbdf716fb4522a068a91914`  
		Last Modified: Wed, 09 Apr 2025 08:39:24 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f224288087f656c2eecdcd327493c0110109c09f2e48320cc65c0fa9753c9200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d95a2c9aa6c999e08927bc4cfed6d4e0661f00a0f0e4991edde130e1faeb567`

```dockerfile
```

-	Layers:
	-	`sha256:05fac35361e74846c81e121b1c4498c97998ed8c8decd8931379676aa5f76396`  
		Last Modified: Wed, 09 Apr 2025 08:39:24 GMT  
		Size: 2.0 MB (1989084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dc577001764b48ee81ae794e79b54c0083061dd7294dec97e301105bafa0f08`  
		Last Modified: Wed, 09 Apr 2025 08:39:24 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:3933533efbcb36dce4797805ffac1fbd558f96a4f39af547cb98b2789c01a6d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:feb563112d19fff419ebaaf53bc5ebbc34dcc9040aa628f096c64581a1456e3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34deb8132c5a1686ec9d58286361410699754a2f529baa356730c46175a0c4cc`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0dec45a929850354a090e228dca34ea64770e73d857734d9a726740b48821f`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 3.6 MB (3561457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f089d3e9c9757e05c4d1311a2d6aba13c856f4a573071a44317b2a6ba0fd4f`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7634be1479388a2b7edb17be8f8a1f9b6aa3c208bf603334d8e09a171c1ce3a`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a839418267feaba920430528a06b30b3cfb66c0f07340f224de25719c9ce7e`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 102.8 KB (102754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cf4d8c29a06175b0473d2537cb5752dbd70d4448bf0158b28648dc07c6123f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2001979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2cd8ab6147458d6a82473940a41794b24d350ba03b1ac233e56c1158b53577`

```dockerfile
```

-	Layers:
	-	`sha256:bfb767ec62c3e301f953ba7598a86e910a45e3aee0d5e36d0c80f3b4d7f1d956`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 2.0 MB (1988003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81811e8647f0d03d6ec1be3d5d5e90a149eed9376838f9d536643e9fe7e4b8a9`  
		Last Modified: Wed, 09 Apr 2025 01:19:15 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:14e68a1ef1499774ab0ff0549fb20c7f0834529679bcc7eae47638bcec32576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d970e55ec6b45eb6d0019fca0ed0c912ec1eb0d52993192334d6119b2740ef10`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3a6fe8ef82163d62cf9479c2af31f1dee76721ce7bdb1467f9784054fb5170`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 3.6 MB (3560005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7393046cfa6f68b53023c0509639d45a59706d5588f4480400d1b5f4d1d51c`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85eb7bd55d65f923168a612b75ca3362461569117659348df33de167f110e2de`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3b50d982d93658713726dd5112aa3092e61c54100c34a8400e31f062b0cb54`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 103.3 KB (103335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ab743af2d7bb08cc2c69eebc7eb51f7fdd2f5e7af502f6be85cbc87edaa281d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea7034c60b178ec24c97c8ca6c23f5e8bab3222ca1ddf30c46652b3ff1f9d01`

```dockerfile
```

-	Layers:
	-	`sha256:931bad7ad10f121b5bbe0f215058463c976a98a44f9b02f27f056603d1cd0f2e`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 2.0 MB (1989048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f27bf5833a0ccc06e9de9d76d1c100cce0c517576ebad70a34e924f9f8b96f`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 14.1 KB (14101 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:bb1f2ac5fe5f0fe5344c7f6e87115a959354b486f5c522e7b3bbd2c528825f45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdd4ee60546b3456f3198b0a327b0fd78e7c7da13ff05c7aab8954206e6704f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33384346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223dbadc92923109c96d9fc8fc28e5c04ff90f64ebff061e9659599ef2a5cee3`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d3be5c72d2ebd1930b95e38b510610cdb291c3324059c55a09596571ba4c4`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 3.6 MB (3561362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de97d0aaf79df6e4cbb6915e4d4a0928c52bd14bfe06eb96dbcb17f26769fc2e`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b3caeb47db1287e5ec5631a60249266bbb9fdcc9a9922d551ff47aae973d8`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cef7682edab5bfa56738f780bb24e3f66449d19e8dce0cf54a9a9cd94233456`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 102.7 KB (102726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ecec4fcbc6ac0c3f46667ce1f223ee30d6e450aa0631e5b43427c23477be7d`  
		Last Modified: Wed, 09 Apr 2025 01:19:18 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b9f65e539e873578da361c2db1d91aaadc2d8500c4025e4c8c60887b496e2ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2162866fd4065055a2a1233c4456c060395e802d2823a032dd2c1f773090b6be`

```dockerfile
```

-	Layers:
	-	`sha256:ad9ad816620dd1b17b44cf321ed4c092277da0053c029ec00b44f8fa4dbd15c2`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 2.0 MB (1988039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fa6831df1b93fe94bb9fdf856d3714daa7e72a01c7bbe7c77fcb0f869036229`  
		Last Modified: Wed, 09 Apr 2025 01:19:17 GMT  
		Size: 16.2 KB (16206 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0b5d43d5d0aeea5fa8470c82bc076f4904af80272d015abc891445aaa063dfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32512906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad171fc77df47499dbb19577f4ebfa52637116d2d4e09ab016e39f034ec6e09`
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
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
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
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3a6fe8ef82163d62cf9479c2af31f1dee76721ce7bdb1467f9784054fb5170`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 3.6 MB (3560005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7393046cfa6f68b53023c0509639d45a59706d5588f4480400d1b5f4d1d51c`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85eb7bd55d65f923168a612b75ca3362461569117659348df33de167f110e2de`  
		Last Modified: Wed, 09 Apr 2025 08:39:11 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3b50d982d93658713726dd5112aa3092e61c54100c34a8400e31f062b0cb54`  
		Last Modified: Wed, 09 Apr 2025 08:39:12 GMT  
		Size: 103.3 KB (103335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de88003e696aae6b7a25af242820bdfcb0c3f13c1cbdf716fb4522a068a91914`  
		Last Modified: Wed, 09 Apr 2025 08:39:24 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f224288087f656c2eecdcd327493c0110109c09f2e48320cc65c0fa9753c9200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2005430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d95a2c9aa6c999e08927bc4cfed6d4e0661f00a0f0e4991edde130e1faeb567`

```dockerfile
```

-	Layers:
	-	`sha256:05fac35361e74846c81e121b1c4498c97998ed8c8decd8931379676aa5f76396`  
		Last Modified: Wed, 09 Apr 2025 08:39:24 GMT  
		Size: 2.0 MB (1989084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dc577001764b48ee81ae794e79b54c0083061dd7294dec97e301105bafa0f08`  
		Last Modified: Wed, 09 Apr 2025 08:39:24 GMT  
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
