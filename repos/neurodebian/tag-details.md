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
$ docker pull neurodebian@sha256:1b8d92d3f95605dd791cc78598d2fc0664b306adc7ac16a74d121325bc53f864
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
$ docker pull neurodebian@sha256:e7beaf31077364243232dc2fbba0eb44266e4559b52e9501638ab5d4ae08f4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59829977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab17032466a8c007742a8f9848a79182bfca8e2376bf9894148129b16b9961f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fac63c7d9f7ef110a69d77fbe8182216d989e18f3fa90b631d4d0f82ec2d846`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 11.3 MB (11266804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b6747529bf8fc1a2bcfc006509fb8f20ce93d3013c4e62cd6c22f7a96b47c7`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9501f0564def637560b9a43f495ffe5eb6b36a0582b15289318bd03a1e0786b6`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ff8a7840cdab0d8fafa473a8206a44bd21f05ec8f7618c13a40b191222f90`  
		Last Modified: Mon, 17 Mar 2025 23:14:46 GMT  
		Size: 93.2 KB (93163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4de88b8cd6776389d9d4093b0956d512529dfe454805ecf854d4bc5e235d7e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46520d3b0a0b7122434db269818778d9c04d6bf6ef8aa1aa709ced28eb078824`

```dockerfile
```

-	Layers:
	-	`sha256:37649676f20c25aac3939a5931107fc6081d315df30b12f32a19d0bfe0e43996`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 3.9 MB (3932836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca4a38f1743d2b7e69328691bb1263d1b7bba2dfc21e3f372b02ecfdc3be7171`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e651935ca1f03939fe4ed9455800c3c1e8ef1612d42bd36995e03670e3384c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59633066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd1caab4861a9612fbb5f117ea9e9381404e7e0bb14a07fefcf03617ccdc64c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae967afd60b725a25b5331c9cbd34561c12da2a8301149a9639c98480a289de`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 11.2 MB (11232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198c54c780d253d7d0b4b86fb4897f07cd19e7204b2716b66a38a7b0c91394d6`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1ff626d1597d172c9a62957b7cd16bb94528c7b3bcc13d7b6ae48e55ac3d8f`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf94fd4ac50b6c92e2ea9fb5686379af98e14585c1fb021c63b31c3f93024ff`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 93.4 KB (93391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46d085013c014e2837557269b4b40ac8ecf252474c52b2c59240b75fe997cc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f0c34b48d331f616bde5abee0e6f645eea6f724a646cc55f12fa3a31f8049c`

```dockerfile
```

-	Layers:
	-	`sha256:43c0703f7acafaddf1bccdbfe31daa0d336feaa460b19e63bb09db9456e7cdec`  
		Last Modified: Tue, 18 Mar 2025 03:46:15 GMT  
		Size: 3.9 MB (3933090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74838dc6370fd63907944e920b3d8cee54a5a4c159f6d97737d95da082d6fb29`  
		Last Modified: Tue, 18 Mar 2025 03:46:15 GMT  
		Size: 14.5 KB (14452 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:845820d3cb18c53d7917d64acd4cdf435fc5e6e9d0665d673708145a76eead55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61238765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407ebe7e9e963870cf12226b6d730b5c5bd3474b5dc3749126c49d1d774d42d1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb27fab9db91706335a011f83fde5a35592a369f97cf21bbfde9353598995adf`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 11.7 MB (11688908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a99467902761ec4b28d838dd4f8ae200a6302e1f42c430209495d60f927aebd`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40f1c295b4ffbefbcf1cff56ad1af7fb30fc0425899d98c643e12886edfe8ce`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce5055b6aaf4f93465c5343859d563f693e9a1fb6f18a359da46ff3e77cdbf3`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 93.2 KB (93203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3d0e14e7fd72d80868c48becd300960bb2a3480422f9d1bab5f473c7045c9be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd47cb5fcb40aab35579339bbe1f842a713c6118b264972c4cfcf1b31125685`

```dockerfile
```

-	Layers:
	-	`sha256:69093413e29bbcb0dc43e20c42d776158212cea2f0926a4c75caccbf26161af4`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 3.9 MB (3930753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42342c086ca4c9be6a6f1ab7a4267e68585526df263f94ad060bc7e5ed30d28`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 14.3 KB (14282 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:7186bfa81bfcc94c51ec8ffa9e2c173bbf21dca13572b7d47fb74cd6df24664e
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
$ docker pull neurodebian@sha256:20a32f8567600d383fba6d77eab331b4a2141313734178651d628f2a47af6978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59830384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6200527a4aa8aa288ee0ec7ac1ce183bf610f802f99e77aa5388705673723ae`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5685004f5e733b959068a239ccd559409be891f72e0a4c3722650701b4376a`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 11.3 MB (11266762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3043d5c6b0762af59359511147e1809157cbf553c4aa5e6f4e2673a71d02abf9`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eedfcf6a2d59da3ef3f7c46a09cfa4bceef12887b159cf6897bb8eb43b01122`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e818ffd9ebbb5afc4129399d945779b7dfa6351f47aba92aa2a157c59bd10476`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 93.2 KB (93159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d52d04bb2c70895dccc6983c65df4f50ac2043c5df98cf733c34c5c8d3af7f`  
		Last Modified: Mon, 17 Mar 2025 23:18:45 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:96216fb906ca37d1c9754d369e90f507a94ec0319ed72594cf19382cd65dbf10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66ccaf1c4cfa6893873161b32f8f3294da071e3e82bf14a943fc4aab5568834`

```dockerfile
```

-	Layers:
	-	`sha256:7a54c1f8c9fe526384aa17481dd2ad4d7ccdacd55d955c05b183b595d9e12877`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 3.9 MB (3932876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c80f3d168e124ca109851fdbdde7b5bc8369fc9eadd378911b348031a5d356`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ad6c5aac60d20312f549c21a55a136a6cc2b89a954208f8f9f3ca49b3abe738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59633515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0631d2e0993ef0d963c84d727d9ed95ac6c49a94f377a150d99efae9e012803`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae967afd60b725a25b5331c9cbd34561c12da2a8301149a9639c98480a289de`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 11.2 MB (11232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198c54c780d253d7d0b4b86fb4897f07cd19e7204b2716b66a38a7b0c91394d6`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1ff626d1597d172c9a62957b7cd16bb94528c7b3bcc13d7b6ae48e55ac3d8f`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf94fd4ac50b6c92e2ea9fb5686379af98e14585c1fb021c63b31c3f93024ff`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 93.4 KB (93391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b9ec67286429f813bf30b35e2561966480dd756c24c8acf5de167f28176488`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5070743fdfe23e5d40f072b4e74ab31bc9e3adc903c2dc12e33dfad94676b7f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37da73cc0f98f5683a775400cbb2deb58f0d78c922714bf70cff7e58252a050`

```dockerfile
```

-	Layers:
	-	`sha256:57fa4c83b5616c7a1652dab19f4def7724b2a6f537e55374d7cfdedf96c63e49`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 3.9 MB (3933130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9148bc35099b52118024d5d4ebb44ef6eb1af74581160edfe5f2cf37c6a023dc`  
		Last Modified: Tue, 18 Mar 2025 03:46:00 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4946beff250a03b51713fbcf71c7869c5e466396892c429ec0e6fc4698d379c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61239222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0dedc62aff44a64042f83ebc2a504d4523a6246464072883d3ee5f52c62231`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ec2587db02dcc0c4ef5c57638ec607829d8294afe02f44d9968b0d0dad0946`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 11.7 MB (11688909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e410407700357dc5f4663b4dc00600f8905dfac028c01c3779efc170d9baac09`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c1547f5883513fa5c1107b9d2212f605c4f039d32e3dbc36ab39858a7ee7f1`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af79c8a29d4fd496693dc1ce9e3e6b5910801dc2ea305ff3f2fd23781b04f7c`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 93.2 KB (93209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d756415886c6fa8cb247b5f3fc186432ca659aef8a3ac7fd5116a54a6e69bc3d`  
		Last Modified: Mon, 17 Mar 2025 23:33:40 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:25c1819ae48659438eb884c26218d9cc7795dbbe8a51011c2b92c71bf71fb69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77049019a43b99e7b68a30df170163a40d71c91e30318f0bd861820eb4326cc`

```dockerfile
```

-	Layers:
	-	`sha256:864fba0b0ceeba292847cb330558a0f0295fe059586354f8a162d3ca900dad2b`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 3.9 MB (3930793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cebc96853d0a57d9b922acab079aa0e3df4a36e199de5b0ea36102128c9d4a6`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:5e4348397d03bb3313f634dc643a6baae493f3f21fdd65fd9a690600b6309767
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
$ docker pull neurodebian@sha256:860811d2c15c1407ed97efa1c36ac84c2888982a9241f61722eee23ca8ccc996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64949730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4650f76c36af11e5a43361da967517023f333404d72f969e6156b0999b23279e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e29c41fdd538beef4843548753f2897fd8ee37c1b1ecd54a295116b2e408ab9`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 11.1 MB (11105086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7386624ca20d9c133ef818f1a3000efee95a39c47deddd51a5a7f39bf124e8a`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b83b5d7c391b3d1e767f83d93259dc70a57f2b1864a5c2375f785fc9c9f187`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23d9bd42f1a3f1bf3cec77d2fa3872af68424a04507059889c9caa1b2e51d97`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 101.2 KB (101212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4a55a6b1b021a6d9d8dd1875e2643d599ec9f5adfa6034f06ffabbfb8a579a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6acfec77f3269388d747ad2526632c679ad7d6de058a64dbaac6538d9038301`

```dockerfile
```

-	Layers:
	-	`sha256:3dd3516dbabb4962a11d060a75f427fae6978d6a65aa40afeefa6115e5855e3f`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 4.2 MB (4232796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:707878b51818313a1d9aefcd05feff817a7014d816d062333d3509a4603e4f0f`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 14.0 KB (14008 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:48e1e794979ba43786bb8fb56d8bd6e2bf3394e94a732509133fc62001c650a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4022d8d914d6d1259ca87ca2e7b9e74df756a74c4da42a3bd6efe907b713be`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3882a7dd0a14bea13a77df5b4c510fe24b4731e60a214c2419a057b09f823`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 11.1 MB (11106035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee718847ca2a78d990086602ec053fb4093415d671b15ba9596f39fa04bc679d`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76a051cd4309c8457edf6b80401a713d6d6fc6449b6443891af1c92d43911af`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70248da80d442a8395b2ec921fbe2e7bcff12b435112dcf248d689354adb71cd`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 101.1 KB (101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b96a5e17ebe207ff9ce4d0a48c7b05604100ccf9ca3bbe7639ff51c4e4bf8468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676d85dae5e7c03df0ef81fad818458b86beeb8d0ef43d8145c99e26903d0e35`

```dockerfile
```

-	Layers:
	-	`sha256:b2a9966658fca6a00227443fcefb6a1195cfc0413de2a2b8fd3ea1112a6eb615`  
		Last Modified: Tue, 18 Mar 2025 03:46:59 GMT  
		Size: 4.2 MB (4232403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f3acd4e70a152bb8fe23396cb7a7d3bc616a6fea39169e3d61bf07c6697cfe5`  
		Last Modified: Tue, 18 Mar 2025 03:46:58 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:a2b0f232fb771740082de0711da947f053f78ad6c00c3313465abe7f7bdc0ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66282223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a19cce7a282a670f4c374e2058cb31f35ce4e9706d2b7c42ae17fba9ee577b5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b3719c2efa08a92bbb200fe6f3caa5cad165126c0bf9dce76050df0c4b48cc`  
		Last Modified: Mon, 17 Mar 2025 23:33:24 GMT  
		Size: 11.5 MB (11500358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de486dd70dc501d119721a391690d5d07a0f1ddec43da9be014e9b66e707ba78`  
		Last Modified: Mon, 17 Mar 2025 23:33:24 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a9107908f1b24fa9fb374f67a08b28ea7e740994f33202240320594804fe76`  
		Last Modified: Mon, 17 Mar 2025 23:33:24 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa366068e4f5a210b8283f46ff8da50b79208fa9db9233347f30d8d098ecef1f`  
		Last Modified: Mon, 17 Mar 2025 23:33:24 GMT  
		Size: 101.1 KB (101089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7d6346d0c4a1f9e910d5a43c78184b91f0a4d265ed0a18b591739a0b9747f4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4243239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fb62100087a161029504abfcdb60494f1b550848be31c07378a8a9a2b32b4d`

```dockerfile
```

-	Layers:
	-	`sha256:e881b0f380f976e9a1cae9e9440c3358573144f6f3f0f0ae3912e4b47cc58258`  
		Last Modified: Mon, 17 Mar 2025 23:33:24 GMT  
		Size: 4.2 MB (4229258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76264c44583833874ce8389b95628ee5578ff637fc8b0f7a5923397c470db99c`  
		Last Modified: Mon, 17 Mar 2025 23:33:24 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:41b89a804704044690226b9a583e897838fb160e0721cbee6197f00f38840c57
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
$ docker pull neurodebian@sha256:cf5a94ff2684dd6fb4f42d88b70d909325820350dc5bfa3987b3bb4eaa7c2e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64950083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a517de29675a25d6b150b4e7b4b4fb0556d110ebe7a17e5484da2598fbaf9f0c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2128041edefc21398ce0d5d3e76899100d6111b14754471c6d57f6a95663302`  
		Last Modified: Mon, 17 Mar 2025 23:47:31 GMT  
		Size: 11.1 MB (11105060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c911d4b2a647f09fcd0f7d3123491b76d4f4d22f8b6bec25518100d70a57bc`  
		Last Modified: Mon, 17 Mar 2025 23:47:30 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dc26b815c239ea7046418983685fba99002caac1570fe5ab8402e2baf7a6f6`  
		Last Modified: Mon, 17 Mar 2025 23:47:30 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe7980f9f45673702f0ca3f64b9da7c16958ec20f7eee42617328db1d0c5a16`  
		Last Modified: Mon, 17 Mar 2025 23:47:31 GMT  
		Size: 101.2 KB (101200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a2e33785086265a4120ee2984d150053ff7f5bd0a7127c08021bbdde63a76c`  
		Last Modified: Mon, 17 Mar 2025 23:47:31 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2af51f333f084a579d2a0e89f57835cadb526772903e96f88148caf2f715fb49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df31889e91d31841ea2ac95334c46b6f4804f8edc6592836cdfcdf27becd29e`

```dockerfile
```

-	Layers:
	-	`sha256:15ac0ccbd5914f2350853897dd95b2cb995675721e33d57376a35a0052752f63`  
		Last Modified: Mon, 17 Mar 2025 23:47:31 GMT  
		Size: 4.2 MB (4232832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1644d5174dc242228f6c170e8c6ae8d7fd7b24de1fc0dd060787f0b3099b0dec`  
		Last Modified: Mon, 17 Mar 2025 23:47:30 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d6450fb3eb05129d4687c51bcab5623db99b785f0cbabd26f700c155cd2f2240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63458104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d72fd46840fa0ac12e330617a792486e696c49775a791c82d144262a1e6175`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3882a7dd0a14bea13a77df5b4c510fe24b4731e60a214c2419a057b09f823`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 11.1 MB (11106035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee718847ca2a78d990086602ec053fb4093415d671b15ba9596f39fa04bc679d`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76a051cd4309c8457edf6b80401a713d6d6fc6449b6443891af1c92d43911af`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70248da80d442a8395b2ec921fbe2e7bcff12b435112dcf248d689354adb71cd`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 101.1 KB (101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af88f6b11190973280cd1f0ac3d93baadb144d0f78c29bb98f505deb764d2d3`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1359592cc092c24f8d650d5ce33d1e228e369c87aee73678f04271eaaa724d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3560fa229acbdb21f7c5819ee3defd03a0e18ff294bd4d6a4390ce156296a272`

```dockerfile
```

-	Layers:
	-	`sha256:b82a3bf24a817f178e6ff2ea7d9f041984143cca6d6e858d9335352ebd17371e`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 4.2 MB (4232439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eadd77ea4fd34eaf2d41afe92967fd20a98c1f00f41ab16400012ef4dab2b9d7`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:04f9df7957f7dd163d8de42d4bbb6dac2d1a9b4e4aacd4316b2e50ed99400644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66282618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176ae5c6f991141be1313e144a8caf7b593c67a1960f7e3198738d330df3cea1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc3b2414407ee0ce5350daa8d5da1bc6a5e939777bdd0d41aeb9bcfc797648c`  
		Last Modified: Mon, 17 Mar 2025 23:33:29 GMT  
		Size: 11.5 MB (11500353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8587a5bab6d44a420b50e2cbf96cf850b46c789149389f96adab1071ffa8ab74`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93102a533e7b7a65f775355be41fad351dd2e80c845a717f5b0939fd329395ee`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fe725953d5b29ac9c6e4edd57bb7453e54b9fef0b1993732b3d15f2848c1d`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 101.1 KB (101101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ee16d55a900518b9e036c04783e292e4d56974b53d3ed282278af3f8d09352`  
		Last Modified: Mon, 17 Mar 2025 23:33:29 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3b768c2edd91f9917ac196859b3929fc6f2f9132f85b71f2eb9c4cc4efe9bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1128898b329d434fb29e99f07d32f9cdb44c00a4711fe2a96488273c9fdfa99`

```dockerfile
```

-	Layers:
	-	`sha256:faafd4cf4c21575ee9f0d61ed6bdbaa6b10dfb85f631133282e111fcf6468373`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 4.2 MB (4229294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410f6ede58e127554018ce70ec907278dbd708226b3e7961b5f72e0542a41e29`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 16.0 KB (16007 bytes)  
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
$ docker pull neurodebian@sha256:1b8d92d3f95605dd791cc78598d2fc0664b306adc7ac16a74d121325bc53f864
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
$ docker pull neurodebian@sha256:e7beaf31077364243232dc2fbba0eb44266e4559b52e9501638ab5d4ae08f4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59829977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab17032466a8c007742a8f9848a79182bfca8e2376bf9894148129b16b9961f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fac63c7d9f7ef110a69d77fbe8182216d989e18f3fa90b631d4d0f82ec2d846`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 11.3 MB (11266804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b6747529bf8fc1a2bcfc006509fb8f20ce93d3013c4e62cd6c22f7a96b47c7`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9501f0564def637560b9a43f495ffe5eb6b36a0582b15289318bd03a1e0786b6`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ff8a7840cdab0d8fafa473a8206a44bd21f05ec8f7618c13a40b191222f90`  
		Last Modified: Mon, 17 Mar 2025 23:14:46 GMT  
		Size: 93.2 KB (93163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4de88b8cd6776389d9d4093b0956d512529dfe454805ecf854d4bc5e235d7e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46520d3b0a0b7122434db269818778d9c04d6bf6ef8aa1aa709ced28eb078824`

```dockerfile
```

-	Layers:
	-	`sha256:37649676f20c25aac3939a5931107fc6081d315df30b12f32a19d0bfe0e43996`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 3.9 MB (3932836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca4a38f1743d2b7e69328691bb1263d1b7bba2dfc21e3f372b02ecfdc3be7171`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e651935ca1f03939fe4ed9455800c3c1e8ef1612d42bd36995e03670e3384c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59633066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd1caab4861a9612fbb5f117ea9e9381404e7e0bb14a07fefcf03617ccdc64c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae967afd60b725a25b5331c9cbd34561c12da2a8301149a9639c98480a289de`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 11.2 MB (11232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198c54c780d253d7d0b4b86fb4897f07cd19e7204b2716b66a38a7b0c91394d6`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1ff626d1597d172c9a62957b7cd16bb94528c7b3bcc13d7b6ae48e55ac3d8f`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf94fd4ac50b6c92e2ea9fb5686379af98e14585c1fb021c63b31c3f93024ff`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 93.4 KB (93391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46d085013c014e2837557269b4b40ac8ecf252474c52b2c59240b75fe997cc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f0c34b48d331f616bde5abee0e6f645eea6f724a646cc55f12fa3a31f8049c`

```dockerfile
```

-	Layers:
	-	`sha256:43c0703f7acafaddf1bccdbfe31daa0d336feaa460b19e63bb09db9456e7cdec`  
		Last Modified: Tue, 18 Mar 2025 03:46:15 GMT  
		Size: 3.9 MB (3933090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74838dc6370fd63907944e920b3d8cee54a5a4c159f6d97737d95da082d6fb29`  
		Last Modified: Tue, 18 Mar 2025 03:46:15 GMT  
		Size: 14.5 KB (14452 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:845820d3cb18c53d7917d64acd4cdf435fc5e6e9d0665d673708145a76eead55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61238765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407ebe7e9e963870cf12226b6d730b5c5bd3474b5dc3749126c49d1d774d42d1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb27fab9db91706335a011f83fde5a35592a369f97cf21bbfde9353598995adf`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 11.7 MB (11688908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a99467902761ec4b28d838dd4f8ae200a6302e1f42c430209495d60f927aebd`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40f1c295b4ffbefbcf1cff56ad1af7fb30fc0425899d98c643e12886edfe8ce`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce5055b6aaf4f93465c5343859d563f693e9a1fb6f18a359da46ff3e77cdbf3`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 93.2 KB (93203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3d0e14e7fd72d80868c48becd300960bb2a3480422f9d1bab5f473c7045c9be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd47cb5fcb40aab35579339bbe1f842a713c6118b264972c4cfcf1b31125685`

```dockerfile
```

-	Layers:
	-	`sha256:69093413e29bbcb0dc43e20c42d776158212cea2f0926a4c75caccbf26161af4`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 3.9 MB (3930753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42342c086ca4c9be6a6f1ab7a4267e68585526df263f94ad060bc7e5ed30d28`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 14.3 KB (14282 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:5e4348397d03bb3313f634dc643a6baae493f3f21fdd65fd9a690600b6309767
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
$ docker pull neurodebian@sha256:860811d2c15c1407ed97efa1c36ac84c2888982a9241f61722eee23ca8ccc996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64949730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4650f76c36af11e5a43361da967517023f333404d72f969e6156b0999b23279e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e29c41fdd538beef4843548753f2897fd8ee37c1b1ecd54a295116b2e408ab9`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 11.1 MB (11105086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7386624ca20d9c133ef818f1a3000efee95a39c47deddd51a5a7f39bf124e8a`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b83b5d7c391b3d1e767f83d93259dc70a57f2b1864a5c2375f785fc9c9f187`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23d9bd42f1a3f1bf3cec77d2fa3872af68424a04507059889c9caa1b2e51d97`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 101.2 KB (101212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4a55a6b1b021a6d9d8dd1875e2643d599ec9f5adfa6034f06ffabbfb8a579a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6acfec77f3269388d747ad2526632c679ad7d6de058a64dbaac6538d9038301`

```dockerfile
```

-	Layers:
	-	`sha256:3dd3516dbabb4962a11d060a75f427fae6978d6a65aa40afeefa6115e5855e3f`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 4.2 MB (4232796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:707878b51818313a1d9aefcd05feff817a7014d816d062333d3509a4603e4f0f`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 14.0 KB (14008 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:48e1e794979ba43786bb8fb56d8bd6e2bf3394e94a732509133fc62001c650a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4022d8d914d6d1259ca87ca2e7b9e74df756a74c4da42a3bd6efe907b713be`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3882a7dd0a14bea13a77df5b4c510fe24b4731e60a214c2419a057b09f823`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 11.1 MB (11106035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee718847ca2a78d990086602ec053fb4093415d671b15ba9596f39fa04bc679d`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76a051cd4309c8457edf6b80401a713d6d6fc6449b6443891af1c92d43911af`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70248da80d442a8395b2ec921fbe2e7bcff12b435112dcf248d689354adb71cd`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 101.1 KB (101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b96a5e17ebe207ff9ce4d0a48c7b05604100ccf9ca3bbe7639ff51c4e4bf8468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4246537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676d85dae5e7c03df0ef81fad818458b86beeb8d0ef43d8145c99e26903d0e35`

```dockerfile
```

-	Layers:
	-	`sha256:b2a9966658fca6a00227443fcefb6a1195cfc0413de2a2b8fd3ea1112a6eb615`  
		Last Modified: Tue, 18 Mar 2025 03:46:59 GMT  
		Size: 4.2 MB (4232403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f3acd4e70a152bb8fe23396cb7a7d3bc616a6fea39169e3d61bf07c6697cfe5`  
		Last Modified: Tue, 18 Mar 2025 03:46:58 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:a2b0f232fb771740082de0711da947f053f78ad6c00c3313465abe7f7bdc0ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66282223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a19cce7a282a670f4c374e2058cb31f35ce4e9706d2b7c42ae17fba9ee577b5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b3719c2efa08a92bbb200fe6f3caa5cad165126c0bf9dce76050df0c4b48cc`  
		Last Modified: Mon, 17 Mar 2025 23:33:24 GMT  
		Size: 11.5 MB (11500358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de486dd70dc501d119721a391690d5d07a0f1ddec43da9be014e9b66e707ba78`  
		Last Modified: Mon, 17 Mar 2025 23:33:24 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a9107908f1b24fa9fb374f67a08b28ea7e740994f33202240320594804fe76`  
		Last Modified: Mon, 17 Mar 2025 23:33:24 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa366068e4f5a210b8283f46ff8da50b79208fa9db9233347f30d8d098ecef1f`  
		Last Modified: Mon, 17 Mar 2025 23:33:24 GMT  
		Size: 101.1 KB (101089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7d6346d0c4a1f9e910d5a43c78184b91f0a4d265ed0a18b591739a0b9747f4cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4243239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fb62100087a161029504abfcdb60494f1b550848be31c07378a8a9a2b32b4d`

```dockerfile
```

-	Layers:
	-	`sha256:e881b0f380f976e9a1cae9e9440c3358573144f6f3f0f0ae3912e4b47cc58258`  
		Last Modified: Mon, 17 Mar 2025 23:33:24 GMT  
		Size: 4.2 MB (4229258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76264c44583833874ce8389b95628ee5578ff637fc8b0f7a5923397c470db99c`  
		Last Modified: Mon, 17 Mar 2025 23:33:24 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:41b89a804704044690226b9a583e897838fb160e0721cbee6197f00f38840c57
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
$ docker pull neurodebian@sha256:cf5a94ff2684dd6fb4f42d88b70d909325820350dc5bfa3987b3bb4eaa7c2e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64950083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a517de29675a25d6b150b4e7b4b4fb0556d110ebe7a17e5484da2598fbaf9f0c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2128041edefc21398ce0d5d3e76899100d6111b14754471c6d57f6a95663302`  
		Last Modified: Mon, 17 Mar 2025 23:47:31 GMT  
		Size: 11.1 MB (11105060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c911d4b2a647f09fcd0f7d3123491b76d4f4d22f8b6bec25518100d70a57bc`  
		Last Modified: Mon, 17 Mar 2025 23:47:30 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dc26b815c239ea7046418983685fba99002caac1570fe5ab8402e2baf7a6f6`  
		Last Modified: Mon, 17 Mar 2025 23:47:30 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe7980f9f45673702f0ca3f64b9da7c16958ec20f7eee42617328db1d0c5a16`  
		Last Modified: Mon, 17 Mar 2025 23:47:31 GMT  
		Size: 101.2 KB (101200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a2e33785086265a4120ee2984d150053ff7f5bd0a7127c08021bbdde63a76c`  
		Last Modified: Mon, 17 Mar 2025 23:47:31 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2af51f333f084a579d2a0e89f57835cadb526772903e96f88148caf2f715fb49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df31889e91d31841ea2ac95334c46b6f4804f8edc6592836cdfcdf27becd29e`

```dockerfile
```

-	Layers:
	-	`sha256:15ac0ccbd5914f2350853897dd95b2cb995675721e33d57376a35a0052752f63`  
		Last Modified: Mon, 17 Mar 2025 23:47:31 GMT  
		Size: 4.2 MB (4232832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1644d5174dc242228f6c170e8c6ae8d7fd7b24de1fc0dd060787f0b3099b0dec`  
		Last Modified: Mon, 17 Mar 2025 23:47:30 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d6450fb3eb05129d4687c51bcab5623db99b785f0cbabd26f700c155cd2f2240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63458104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d72fd46840fa0ac12e330617a792486e696c49775a791c82d144262a1e6175`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb3882a7dd0a14bea13a77df5b4c510fe24b4731e60a214c2419a057b09f823`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 11.1 MB (11106035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee718847ca2a78d990086602ec053fb4093415d671b15ba9596f39fa04bc679d`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76a051cd4309c8457edf6b80401a713d6d6fc6449b6443891af1c92d43911af`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70248da80d442a8395b2ec921fbe2e7bcff12b435112dcf248d689354adb71cd`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 101.1 KB (101132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af88f6b11190973280cd1f0ac3d93baadb144d0f78c29bb98f505deb764d2d3`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1359592cc092c24f8d650d5ce33d1e228e369c87aee73678f04271eaaa724d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4248616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3560fa229acbdb21f7c5819ee3defd03a0e18ff294bd4d6a4390ce156296a272`

```dockerfile
```

-	Layers:
	-	`sha256:b82a3bf24a817f178e6ff2ea7d9f041984143cca6d6e858d9335352ebd17371e`  
		Last Modified: Tue, 18 Mar 2025 03:46:45 GMT  
		Size: 4.2 MB (4232439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eadd77ea4fd34eaf2d41afe92967fd20a98c1f00f41ab16400012ef4dab2b9d7`  
		Last Modified: Tue, 18 Mar 2025 03:46:44 GMT  
		Size: 16.2 KB (16177 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:04f9df7957f7dd163d8de42d4bbb6dac2d1a9b4e4aacd4316b2e50ed99400644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66282618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176ae5c6f991141be1313e144a8caf7b593c67a1960f7e3198738d330df3cea1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
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
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc3b2414407ee0ce5350daa8d5da1bc6a5e939777bdd0d41aeb9bcfc797648c`  
		Last Modified: Mon, 17 Mar 2025 23:33:29 GMT  
		Size: 11.5 MB (11500353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8587a5bab6d44a420b50e2cbf96cf850b46c789149389f96adab1071ffa8ab74`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93102a533e7b7a65f775355be41fad351dd2e80c845a717f5b0939fd329395ee`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9fe725953d5b29ac9c6e4edd57bb7453e54b9fef0b1993732b3d15f2848c1d`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 101.1 KB (101101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ee16d55a900518b9e036c04783e292e4d56974b53d3ed282278af3f8d09352`  
		Last Modified: Mon, 17 Mar 2025 23:33:29 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3b768c2edd91f9917ac196859b3929fc6f2f9132f85b71f2eb9c4cc4efe9bf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4245301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1128898b329d434fb29e99f07d32f9cdb44c00a4711fe2a96488273c9fdfa99`

```dockerfile
```

-	Layers:
	-	`sha256:faafd4cf4c21575ee9f0d61ed6bdbaa6b10dfb85f631133282e111fcf6468373`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 4.2 MB (4229294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410f6ede58e127554018ce70ec907278dbd708226b3e7961b5f72e0542a41e29`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:1b8d92d3f95605dd791cc78598d2fc0664b306adc7ac16a74d121325bc53f864
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
$ docker pull neurodebian@sha256:e7beaf31077364243232dc2fbba0eb44266e4559b52e9501638ab5d4ae08f4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59829977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab17032466a8c007742a8f9848a79182bfca8e2376bf9894148129b16b9961f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fac63c7d9f7ef110a69d77fbe8182216d989e18f3fa90b631d4d0f82ec2d846`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 11.3 MB (11266804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b6747529bf8fc1a2bcfc006509fb8f20ce93d3013c4e62cd6c22f7a96b47c7`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9501f0564def637560b9a43f495ffe5eb6b36a0582b15289318bd03a1e0786b6`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ff8a7840cdab0d8fafa473a8206a44bd21f05ec8f7618c13a40b191222f90`  
		Last Modified: Mon, 17 Mar 2025 23:14:46 GMT  
		Size: 93.2 KB (93163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4de88b8cd6776389d9d4093b0956d512529dfe454805ecf854d4bc5e235d7e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46520d3b0a0b7122434db269818778d9c04d6bf6ef8aa1aa709ced28eb078824`

```dockerfile
```

-	Layers:
	-	`sha256:37649676f20c25aac3939a5931107fc6081d315df30b12f32a19d0bfe0e43996`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 3.9 MB (3932836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca4a38f1743d2b7e69328691bb1263d1b7bba2dfc21e3f372b02ecfdc3be7171`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e651935ca1f03939fe4ed9455800c3c1e8ef1612d42bd36995e03670e3384c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59633066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd1caab4861a9612fbb5f117ea9e9381404e7e0bb14a07fefcf03617ccdc64c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae967afd60b725a25b5331c9cbd34561c12da2a8301149a9639c98480a289de`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 11.2 MB (11232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198c54c780d253d7d0b4b86fb4897f07cd19e7204b2716b66a38a7b0c91394d6`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1ff626d1597d172c9a62957b7cd16bb94528c7b3bcc13d7b6ae48e55ac3d8f`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf94fd4ac50b6c92e2ea9fb5686379af98e14585c1fb021c63b31c3f93024ff`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 93.4 KB (93391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46d085013c014e2837557269b4b40ac8ecf252474c52b2c59240b75fe997cc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f0c34b48d331f616bde5abee0e6f645eea6f724a646cc55f12fa3a31f8049c`

```dockerfile
```

-	Layers:
	-	`sha256:43c0703f7acafaddf1bccdbfe31daa0d336feaa460b19e63bb09db9456e7cdec`  
		Last Modified: Tue, 18 Mar 2025 03:46:15 GMT  
		Size: 3.9 MB (3933090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74838dc6370fd63907944e920b3d8cee54a5a4c159f6d97737d95da082d6fb29`  
		Last Modified: Tue, 18 Mar 2025 03:46:15 GMT  
		Size: 14.5 KB (14452 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:845820d3cb18c53d7917d64acd4cdf435fc5e6e9d0665d673708145a76eead55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61238765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407ebe7e9e963870cf12226b6d730b5c5bd3474b5dc3749126c49d1d774d42d1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb27fab9db91706335a011f83fde5a35592a369f97cf21bbfde9353598995adf`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 11.7 MB (11688908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a99467902761ec4b28d838dd4f8ae200a6302e1f42c430209495d60f927aebd`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40f1c295b4ffbefbcf1cff56ad1af7fb30fc0425899d98c643e12886edfe8ce`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce5055b6aaf4f93465c5343859d563f693e9a1fb6f18a359da46ff3e77cdbf3`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 93.2 KB (93203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3d0e14e7fd72d80868c48becd300960bb2a3480422f9d1bab5f473c7045c9be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd47cb5fcb40aab35579339bbe1f842a713c6118b264972c4cfcf1b31125685`

```dockerfile
```

-	Layers:
	-	`sha256:69093413e29bbcb0dc43e20c42d776158212cea2f0926a4c75caccbf26161af4`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 3.9 MB (3930753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42342c086ca4c9be6a6f1ab7a4267e68585526df263f94ad060bc7e5ed30d28`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 14.3 KB (14282 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:7186bfa81bfcc94c51ec8ffa9e2c173bbf21dca13572b7d47fb74cd6df24664e
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
$ docker pull neurodebian@sha256:20a32f8567600d383fba6d77eab331b4a2141313734178651d628f2a47af6978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59830384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6200527a4aa8aa288ee0ec7ac1ce183bf610f802f99e77aa5388705673723ae`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5685004f5e733b959068a239ccd559409be891f72e0a4c3722650701b4376a`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 11.3 MB (11266762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3043d5c6b0762af59359511147e1809157cbf553c4aa5e6f4e2673a71d02abf9`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eedfcf6a2d59da3ef3f7c46a09cfa4bceef12887b159cf6897bb8eb43b01122`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e818ffd9ebbb5afc4129399d945779b7dfa6351f47aba92aa2a157c59bd10476`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 93.2 KB (93159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d52d04bb2c70895dccc6983c65df4f50ac2043c5df98cf733c34c5c8d3af7f`  
		Last Modified: Mon, 17 Mar 2025 23:18:45 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:96216fb906ca37d1c9754d369e90f507a94ec0319ed72594cf19382cd65dbf10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66ccaf1c4cfa6893873161b32f8f3294da071e3e82bf14a943fc4aab5568834`

```dockerfile
```

-	Layers:
	-	`sha256:7a54c1f8c9fe526384aa17481dd2ad4d7ccdacd55d955c05b183b595d9e12877`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 3.9 MB (3932876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c80f3d168e124ca109851fdbdde7b5bc8369fc9eadd378911b348031a5d356`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ad6c5aac60d20312f549c21a55a136a6cc2b89a954208f8f9f3ca49b3abe738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59633515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0631d2e0993ef0d963c84d727d9ed95ac6c49a94f377a150d99efae9e012803`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae967afd60b725a25b5331c9cbd34561c12da2a8301149a9639c98480a289de`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 11.2 MB (11232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198c54c780d253d7d0b4b86fb4897f07cd19e7204b2716b66a38a7b0c91394d6`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1ff626d1597d172c9a62957b7cd16bb94528c7b3bcc13d7b6ae48e55ac3d8f`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf94fd4ac50b6c92e2ea9fb5686379af98e14585c1fb021c63b31c3f93024ff`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 93.4 KB (93391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b9ec67286429f813bf30b35e2561966480dd756c24c8acf5de167f28176488`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5070743fdfe23e5d40f072b4e74ab31bc9e3adc903c2dc12e33dfad94676b7f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37da73cc0f98f5683a775400cbb2deb58f0d78c922714bf70cff7e58252a050`

```dockerfile
```

-	Layers:
	-	`sha256:57fa4c83b5616c7a1652dab19f4def7724b2a6f537e55374d7cfdedf96c63e49`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 3.9 MB (3933130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9148bc35099b52118024d5d4ebb44ef6eb1af74581160edfe5f2cf37c6a023dc`  
		Last Modified: Tue, 18 Mar 2025 03:46:00 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4946beff250a03b51713fbcf71c7869c5e466396892c429ec0e6fc4698d379c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61239222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0dedc62aff44a64042f83ebc2a504d4523a6246464072883d3ee5f52c62231`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ec2587db02dcc0c4ef5c57638ec607829d8294afe02f44d9968b0d0dad0946`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 11.7 MB (11688909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e410407700357dc5f4663b4dc00600f8905dfac028c01c3779efc170d9baac09`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c1547f5883513fa5c1107b9d2212f605c4f039d32e3dbc36ab39858a7ee7f1`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af79c8a29d4fd496693dc1ce9e3e6b5910801dc2ea305ff3f2fd23781b04f7c`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 93.2 KB (93209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d756415886c6fa8cb247b5f3fc186432ca659aef8a3ac7fd5116a54a6e69bc3d`  
		Last Modified: Mon, 17 Mar 2025 23:33:40 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:25c1819ae48659438eb884c26218d9cc7795dbbe8a51011c2b92c71bf71fb69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77049019a43b99e7b68a30df170163a40d71c91e30318f0bd861820eb4326cc`

```dockerfile
```

-	Layers:
	-	`sha256:864fba0b0ceeba292847cb330558a0f0295fe059586354f8a162d3ca900dad2b`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 3.9 MB (3930793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cebc96853d0a57d9b922acab079aa0e3df4a36e199de5b0ea36102128c9d4a6`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
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
$ docker pull neurodebian@sha256:7186bfa81bfcc94c51ec8ffa9e2c173bbf21dca13572b7d47fb74cd6df24664e
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
$ docker pull neurodebian@sha256:20a32f8567600d383fba6d77eab331b4a2141313734178651d628f2a47af6978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59830384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6200527a4aa8aa288ee0ec7ac1ce183bf610f802f99e77aa5388705673723ae`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5685004f5e733b959068a239ccd559409be891f72e0a4c3722650701b4376a`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 11.3 MB (11266762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3043d5c6b0762af59359511147e1809157cbf553c4aa5e6f4e2673a71d02abf9`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eedfcf6a2d59da3ef3f7c46a09cfa4bceef12887b159cf6897bb8eb43b01122`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e818ffd9ebbb5afc4129399d945779b7dfa6351f47aba92aa2a157c59bd10476`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 93.2 KB (93159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d52d04bb2c70895dccc6983c65df4f50ac2043c5df98cf733c34c5c8d3af7f`  
		Last Modified: Mon, 17 Mar 2025 23:18:45 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:96216fb906ca37d1c9754d369e90f507a94ec0319ed72594cf19382cd65dbf10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66ccaf1c4cfa6893873161b32f8f3294da071e3e82bf14a943fc4aab5568834`

```dockerfile
```

-	Layers:
	-	`sha256:7a54c1f8c9fe526384aa17481dd2ad4d7ccdacd55d955c05b183b595d9e12877`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 3.9 MB (3932876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c80f3d168e124ca109851fdbdde7b5bc8369fc9eadd378911b348031a5d356`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ad6c5aac60d20312f549c21a55a136a6cc2b89a954208f8f9f3ca49b3abe738e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59633515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0631d2e0993ef0d963c84d727d9ed95ac6c49a94f377a150d99efae9e012803`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae967afd60b725a25b5331c9cbd34561c12da2a8301149a9639c98480a289de`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 11.2 MB (11232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198c54c780d253d7d0b4b86fb4897f07cd19e7204b2716b66a38a7b0c91394d6`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1ff626d1597d172c9a62957b7cd16bb94528c7b3bcc13d7b6ae48e55ac3d8f`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf94fd4ac50b6c92e2ea9fb5686379af98e14585c1fb021c63b31c3f93024ff`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 93.4 KB (93391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b9ec67286429f813bf30b35e2561966480dd756c24c8acf5de167f28176488`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5070743fdfe23e5d40f072b4e74ab31bc9e3adc903c2dc12e33dfad94676b7f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37da73cc0f98f5683a775400cbb2deb58f0d78c922714bf70cff7e58252a050`

```dockerfile
```

-	Layers:
	-	`sha256:57fa4c83b5616c7a1652dab19f4def7724b2a6f537e55374d7cfdedf96c63e49`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 3.9 MB (3933130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9148bc35099b52118024d5d4ebb44ef6eb1af74581160edfe5f2cf37c6a023dc`  
		Last Modified: Tue, 18 Mar 2025 03:46:00 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4946beff250a03b51713fbcf71c7869c5e466396892c429ec0e6fc4698d379c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61239222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0dedc62aff44a64042f83ebc2a504d4523a6246464072883d3ee5f52c62231`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ec2587db02dcc0c4ef5c57638ec607829d8294afe02f44d9968b0d0dad0946`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 11.7 MB (11688909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e410407700357dc5f4663b4dc00600f8905dfac028c01c3779efc170d9baac09`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c1547f5883513fa5c1107b9d2212f605c4f039d32e3dbc36ab39858a7ee7f1`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af79c8a29d4fd496693dc1ce9e3e6b5910801dc2ea305ff3f2fd23781b04f7c`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 93.2 KB (93209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d756415886c6fa8cb247b5f3fc186432ca659aef8a3ac7fd5116a54a6e69bc3d`  
		Last Modified: Mon, 17 Mar 2025 23:33:40 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:25c1819ae48659438eb884c26218d9cc7795dbbe8a51011c2b92c71bf71fb69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77049019a43b99e7b68a30df170163a40d71c91e30318f0bd861820eb4326cc`

```dockerfile
```

-	Layers:
	-	`sha256:864fba0b0ceeba292847cb330558a0f0295fe059586354f8a162d3ca900dad2b`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 3.9 MB (3930793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cebc96853d0a57d9b922acab079aa0e3df4a36e199de5b0ea36102128c9d4a6`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json
