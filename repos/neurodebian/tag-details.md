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
$ docker pull neurodebian@sha256:f25a14cd042e8f406521801107486ccc509a87ac933b09a12d429c6638ed0834
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
$ docker pull neurodebian@sha256:774f937a033e82ec79ed5efdc524cc60f359b1b4578f1fe4f7a90b3a4b378ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3025f51a5e1acbf6054583346525cafa3bd7ca82cd43160ebb36811e1daa5171`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:43:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3666961b6d8a250dea41e73593bb3b314425613763ef952df72a2210e3c9db4e`  
		Last Modified: Wed, 22 Apr 2026 01:44:14 GMT  
		Size: 11.3 MB (11273365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6cdd6bbdfee34d91d0fd4ea0fa6b4706aa25b44d362635dd3e91dfb9770821`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e195f58e61236402a05c20b3ca9a451789af8cfb3e1c12867b223461107e745`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33104a23ec2785413870f721ee969d98f2eba62377bfd3becfb8b9c049d52061`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 93.4 KB (93403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:56e34690ed311f09247f5dbc2483f0257259f2ca934b4aba64ca6a1ca19957d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dda936e5d2e3d4600ddbea0f9c91de89ad2d94e7b306e7e9ea16f25c5a79350`

```dockerfile
```

-	Layers:
	-	`sha256:52a2c953c3a0537c47a81aa029093121fe18618db5cea6819dca6816208ab171`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e210200a09eaeed334b94d7f6f33309c0879fad0c85624f972f547671479418d`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c383b1c8bcc59487007ea946c97be72b381f54ee51d5fd892cf0629fdeb1c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628c1e90e3da7350faabb21fc74a0c88da8663666dd19dbdb74ba907e12ef2b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbeab365177c9b941a081ba0b6d957ba147319fe32dff22aa2624a53a06f29b`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 11.3 MB (11252933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fa205d0d4d9ff7d136faa66f376fb23aff6334613faa278f84518f8e5c01ff`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14309867687b534670e51c1d96567476c0f1aaed795f789d0445fab07399b4d`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89033d9b2184954874f8f00b5a17aecc6b429a80a8e0038b84aa6ee81ff3383`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 93.5 KB (93546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ede2b6186f52eb37d412780815c7330d58d6faa9837786a7e5c79b52f572fd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ee394c617722eaa31b6265fd68e7ac215a0a018ff4f39c2985bca8c06e3347`

```dockerfile
```

-	Layers:
	-	`sha256:d4b4657e224bc234c23ab66a4c0a2fe772e905a9fe22fae905f739583d04c417`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29aedf8be25ddf5a7975ddb70961e5bb9c8359ec72bba50cbb2e61f0f256a671`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 14.1 KB (14088 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:5fc238140262f53118929824ba430e3f0b7979a132cd8de5a362c29017787166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b675a907be02445819e41f56368d40c152b80121abda8e1bbefae9dd78926d26`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:43:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:43:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f607c56991d572a9c9e62692330777522b959fe17a14367be35d12959214fa4`  
		Last Modified: Wed, 22 Apr 2026 00:16:17 GMT  
		Size: 49.5 MB (49477718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2c9d6696a3b3db58c324a6862fbc2cd52cbe3b89b6e6f0bce3bf2a4e56202b`  
		Last Modified: Wed, 22 Apr 2026 01:44:02 GMT  
		Size: 11.7 MB (11692983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557955c0b0a3f5532ff7ed95be47c99d54964f54442e2a391332f755cd2ab255`  
		Last Modified: Wed, 22 Apr 2026 01:44:02 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3165092047810227052b1a2879d085156c89d784d281b3f0e72f5cd38cbf43`  
		Last Modified: Wed, 22 Apr 2026 01:44:02 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5684e4be91c395c0648bc93df42a048e7b60636cbf89d1aef495ef8c66e08c8c`  
		Last Modified: Wed, 22 Apr 2026 01:44:02 GMT  
		Size: 93.4 KB (93410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73db3da4c5b46785cb76f45bb4b2825507a37af6996fb9a24def8e205ad09e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed9ae811d0aad7fdf51336ca7a7ce5c8c78b33dc963138eff67d7abc63c357e`

```dockerfile
```

-	Layers:
	-	`sha256:8f829d49c7ebeed50174636f6d2dcc620e3b7e1ce2c929e01b853fb8de7799b7`  
		Last Modified: Wed, 22 Apr 2026 01:44:02 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e67fdf566a0f64a1b29c67deb65e498edaeb18f85b97a6ac368e8bb97ce098`  
		Last Modified: Wed, 22 Apr 2026 01:44:02 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:f68c8548da8486214f14894daa7005640c5cfb8982cea9d147400aded59f53e9
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
$ docker pull neurodebian@sha256:2c4cb4e49d32e0800ccab1b383c4df2c0507d6232aa910100bacae012ccc80be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a98c800a04fa92beeebb45cece13dc9a5a2bb2afacd3fe6b49a6af4c345f54a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:44:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5c6f68a47f6aafe93c229c3fa17bd8f9eca8dbcb82026f265892037a7e7ca8`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 11.3 MB (11273308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d79daf0cf6757e31a1107175cd1e7462256549e1d3d30fcce502bd6b523440`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acd65166e3ebd350cc72a3012913c626286396db1340b7ea63e94bf18f645be`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccad9b7d786b644e59a626a14638210a2ea9aff44f74ec61dbf6eee0101215`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 93.4 KB (93400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e4d2762c39b83ebeb647c5d5a01a7535bb73003d5cfdc730cbd58dda43cb37`  
		Last Modified: Wed, 22 Apr 2026 01:44:17 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a894ea750272941947bceba5b021cb9f1323c9effce5f027b01b101eaf12b7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7391f965c78c1414439c34110a9ddf1fc2954c0ab321306169ec35348f65b3b`

```dockerfile
```

-	Layers:
	-	`sha256:438e2af1d3add7733f1e2b743bd1418519d72549264d12b537bed012abfeec97`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebde2f39b24d1676597cba7a414b48ddb0418b77cd09adc479774d0c97715acd`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9ce456a29d55af753754c81bcf6c489b588e4ef8d345a25a1185ac4ed38d7067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83671130319d212529fed9657df2275a72b7a9972a90c7d4eeb3087a8c2e780`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297af71f398d804e9824bb6964f5f84de1d86338b03a2c087345a9e6adeae9e7`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 11.3 MB (11252932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbc6e93f45b3f4cf455734139898464377b66e14251b76f3361f3d34ed49b9d`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2bd671e957e80374283f5fb64814dafa746ed40e7cf68d7972fffd7054de17`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58c4f363214c80dee9f62e6d8d410c16b88764ef3e641e1d8bc9231b3d9cae7`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 93.6 KB (93575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1d2f24bc5c69d6c727ad3568cbc4addea466c9b6cc928ea044b626717466f`  
		Last Modified: Fri, 08 May 2026 19:46:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f29b6635607465a6f03d6780e7c09679fb49ac9bb340deaae75b283f8ed832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3acb1d5d8d6cb02f7c1e8bd1cb80b8eb98d8808fa839c362abc1fbb0ad92f8`

```dockerfile
```

-	Layers:
	-	`sha256:c992b9778cd7c443812a6eca47e360178d13695c8043203be74e9562afd8f30e`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5d86f16916b238e87145c3058d5b9f4308cb209db7450c1e9f13152f33e5b9`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:520ee5a44ddfe1fdc8c29908c80cd33fa4b80e61e0a6a7fea2236f8acf57e63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39b44109263a95adccf888e8d1877cb1c7e34ee47ad75e1bb7a63abc65c9a72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:43:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:43:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1f607c56991d572a9c9e62692330777522b959fe17a14367be35d12959214fa4`  
		Last Modified: Wed, 22 Apr 2026 00:16:17 GMT  
		Size: 49.5 MB (49477718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c950f45f1a3bfc61a9c1480c4ea9fde2a03316cd953138ce00699c9f7a3b045b`  
		Last Modified: Wed, 22 Apr 2026 01:44:05 GMT  
		Size: 11.7 MB (11692996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06407c79badd50171efc07c97a8e73ce7ea48d39d2677a386a47b60804ab9c00`  
		Last Modified: Wed, 22 Apr 2026 01:44:04 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed8f9d4838a2b0037c69af61b838c7a681ec221f106d08be8c0d589f82cefc8`  
		Last Modified: Wed, 22 Apr 2026 01:44:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b48decc6dfccfbac4be598308637f9bd32f75d105fe1a9e2d50ddaad525978f`  
		Last Modified: Wed, 22 Apr 2026 01:44:04 GMT  
		Size: 93.4 KB (93406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d828cfd13f00eab171bc955be08af42ecb017a4fc01a54804cf008f7b9c0a95b`  
		Last Modified: Wed, 22 Apr 2026 01:44:05 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:12a5b425515756459b282bc12e754da5d18f9654f7f594d3ab5fa131fccddcd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d688f4c176cb5073364ce52b334f75aeb3cacd7da06b77e3e2e68fa02a1b7b99`

```dockerfile
```

-	Layers:
	-	`sha256:7f4fa81df859d5217bb07cfb2ca3a6026136a42f1b4d5beb2b7d4ee8d75117c8`  
		Last Modified: Wed, 22 Apr 2026 01:44:05 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be869ef59e935c1c52547a4769be7bb9ba422296f6d77f409abddf7bf2567ce`  
		Last Modified: Wed, 22 Apr 2026 01:44:04 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:443c0020b56d7e47a8970f9cc9a86ca79e0a67bdfd756f8fd6b4d95a26d6a6c7
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
$ docker pull neurodebian@sha256:48b978dd2f847654f39cd8f1776daa4aa9df89f142414d40f5676f7b97bc8370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002d5b89a4707f51717893785ccc02875837ce31f701bfa352334058bda856c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:17:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:17:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 02:17:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 02:17:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c72d0fa0f448323831012892fcfa3fcab666bcfd3f5dffde9845c3fcff1a5c`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 11.1 MB (11103538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f9437b17831a4574865078d6d6f2735530dd5df4d98bdf4cf80ecbe1eacb9f`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a07c90585c91a04ece397b0b7c2aa7103ad950e701ca4fbc90e9031dc945452`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9e0d3d2c3d046339e5eafeda28eb07678ebf29523f1cc7311ca0f4366b5a69`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 101.4 KB (101428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:11f07afbbbe928a378281a2e4e9aa71232f720ed8c10015d2a68898a8f42f783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ac64d62683665c45e0891c0b9483a646131f67f43e3d7c13640436e90407b`

```dockerfile
```

-	Layers:
	-	`sha256:8c4be9b8444a505246705c3f67d140f0953839be0a6106ab4b93c9696fb8f504`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:610c4abfd3a816fbc742987c537a656800f8939c7bf19bab75263e3fa00aec50`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:62347cb324bd70e5569c022cf36e136aa8e826f40f1c2238889b719f8cc66a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088aaba085173fd83cbf817a16c6e4af04bdc9ae9eedb10afd7c44e3489ddef4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:45:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49da93cc2679b1db042cd202e875060e5e3220e87732350bd5904898892e8b8`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 11.1 MB (11109914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b825eee855070f51dfefec4cf70685dd607f1dc1402855869b4bbcaf7b576135`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3209c067378d18d75a18203938000ce323b7b747348cca016301c372c516e6a7`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0c848bef723aca7f046b18ce448a4097239a1da120f540e52dd1c9a68a4b31`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 101.3 KB (101279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4243308f1b786a75f6a0506780d5c7b33ac30f8511fccca56aec4dea210c21b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e762402feeb4d06253b996167883d80d3641bf9e0680cf01273d11c016d6d5`

```dockerfile
```

-	Layers:
	-	`sha256:b14f0dcc1c2ef0142185e8793a6e22f9422570c4ba9d2b6abb2cb7125ce110f1`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2aa08681f076f24ce71cb639cc4949a46b91a1a127541e91c515a501664465`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:536a24ed300f7097dfcf2172b256af1fac92e8330df1d13d872c307189bbec8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66310669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9dd43c77bd5d638de962eb7e18c7f249ab4e2bdca5a094b9bcd978505640864`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:43:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:43:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:737d996bc05c156425b11be5deec8366db5d7a009f49d85b480b1daec555cf4a`  
		Last Modified: Wed, 22 Apr 2026 00:16:40 GMT  
		Size: 54.7 MB (54705161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972b7c8adf2a27a1f8aafa4b3116bdcbf1f1d0f8a6aef3490cddfa4590ac906e`  
		Last Modified: Wed, 22 Apr 2026 01:43:42 GMT  
		Size: 11.5 MB (11502060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f0dfa0a8ed6ad0cb09e36854d5422976effffcfbd936ac5a4a113b16e6bf2d`  
		Last Modified: Wed, 22 Apr 2026 01:43:41 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9893d72ec7e08c0258b1055d94509241c3d4ce544fd7b4e302997e97a707dd9`  
		Last Modified: Wed, 22 Apr 2026 01:43:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dde940fe9dc18128c53ba66b638ac94ba0781292661c734238dbe93390fa86`  
		Last Modified: Wed, 22 Apr 2026 01:43:42 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ece6d734ac81ab2b79479e0bc686630400733ac99fec541329be113734278f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699476441be45f0a6f814f470afb8e48404ae6f80347c2e4589de20a7c098cea`

```dockerfile
```

-	Layers:
	-	`sha256:0c074ec835c373fe44220d2d54c37558332aaa81aa1bc9e5b60da7dedcd8a426`  
		Last Modified: Wed, 22 Apr 2026 01:43:42 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b80984558c97b94a7c30b55c0b69f2841ccd87cad8b0879ad0a1c1b470d9df4`  
		Last Modified: Wed, 22 Apr 2026 01:43:41 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:a3cbd7ca8039c13e7eb7e557f96439de19b426e31ca2d13b56dde94b07020624
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
$ docker pull neurodebian@sha256:555440ecc7c6f655a1f24cb37b25ac77f16f360a99049d9ea7a9c5c136dba234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38937761e563f02f1a8d4ba92e24ea94cdcd83de4203265bb370625eeda2fd05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:44:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0802b439ba506ee42b40891edfe6f9b4eb3055ea7d81ecbc3d1c87a08b141de`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 11.1 MB (11103547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42ee071305f1b461b88de5416fff15b4f7563a181be72046ad6dcbe2c446b02`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f9afea8b6181ada18a56edd636f0726aed91cc8382c81977739411f231524f`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386ec5b98b370be832b747e784e7effe8e6a952f7ce138c4def942bcc243d7f1`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 101.4 KB (101353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c47ebcb0a700e2b6652dbc7de864c41d2126d949ebd0bca7ed3acfc9d8b614a`  
		Last Modified: Wed, 22 Apr 2026 01:44:12 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ace222ba3da95f703da60158d587e1157e099ecbbae7f02da2f2877bb04ba743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54135d0cb4cdfc7dfac0b8beb5954939cb79280fe680f47eec5643ad0f6e7346`

```dockerfile
```

-	Layers:
	-	`sha256:e768aa59b6fdb62033d29df462af080e0ce18d30ba88640f432b6cfaeb7aa0eb`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b29bfc03bd2c77e02f21088f2cda163050d8f828320dfa8b1d23037ce926f25`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d72cd51fb944fbeefc59dbcfd9207dd62d6b1409175dc0b62c30c20f9723340d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c72a73a81907cd10f4ed9d514fe1d0c96154b13d775360ec1f4e578b4b7c08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4d4853c366ae1d8a6092357fdeceb46f1af7fb6971f30fb5bac64d2816093`  
		Last Modified: Fri, 08 May 2026 19:46:12 GMT  
		Size: 11.1 MB (11109872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0860e8ce6527c5e5eb574f904941f9d5fd1ac72704eec1e19c9667591571cda7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2407a0ee518c92a25d491c4909ce3ed0cb4f84524941a201a7cf2bfd943c1ed7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86985c6bd9a382f6fe79e55952fe846b9dac4b331da91606603aeebec797fb71`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 101.3 KB (101294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a645068ae63614955aa0cce30edd178a25de8ca2dd269f25af6a34467cb6d54c`  
		Last Modified: Fri, 08 May 2026 19:46:12 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e79ba75ecd78047e815efee9fa2ef478d94689d9d1ab9f20fb7ba7bf72a022e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aae72f0e29b5b3a88976fb346afe0082117da0014a70001d64ee3963b586eab`

```dockerfile
```

-	Layers:
	-	`sha256:97a48df79af5e64bcca963ffbc0947249e8e2964559cd3a0216d0b5fe3a662f7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7ecf2ecbf82b72a416e1ef61bc9ea6fe75d4c000ee213c306b6148414a9521`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:be20e7b0e215c4deec6aa2de282c6b428f0d9d78dfa2e9a48a21a04aa1309aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66311074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271902e4ce05784fc0ff5d6e016a0845b149c59c943cd5951bb641ac145378f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:43:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:43:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:737d996bc05c156425b11be5deec8366db5d7a009f49d85b480b1daec555cf4a`  
		Last Modified: Wed, 22 Apr 2026 00:16:40 GMT  
		Size: 54.7 MB (54705161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1516c79839462487ebf969fa4a5a0db19d5af6adf507a4fc9cc33e702e252f68`  
		Last Modified: Wed, 22 Apr 2026 01:43:41 GMT  
		Size: 11.5 MB (11502096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc24b7ff3fb59cab3e8b089d3e98f3aeeeebc1a716fe7e4b4710a8f2c57f89ce`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ed96c6739d01a12337c6c9b40fe1c07118326d0531824658d69a8239253bbb`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1c6f719a9e92fa099ce6018f4fe86fc6cd03baeb042f11c1d662042c50bf9`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 101.3 KB (101271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4755ffa1449a1b0999111b69e5bd22eb4db3b4de5dd016f94f99c635cd80148f`  
		Last Modified: Wed, 22 Apr 2026 01:43:42 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8d9b3ca1ff285715b70ca7072ee3070c4f5c341311035c12b90f3bacbc8db176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d03e6338a4f4cda9497f14486e3ba04f901974153fba8b8ee489b3574a9899`

```dockerfile
```

-	Layers:
	-	`sha256:06c69fd2a19c9907618c9ace118aa384a7baf2562e3fb8fd3747926c796f47ae`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e13d9295d1f7ceb76e6efe645bb726797d1bbf0ea08d285d5bf4fd07015d0ca5`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:62b75019dc174623fafe7826699ae6fd8cb48e69d17d111c45755361e2951049
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
$ docker pull neurodebian@sha256:002f7fb8429812eb25298710a7653a0a06f2c9b122c6f1e6cdec699025eb2bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60158655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f010db1188288b639deb5a145a8914aa4fb9a0fcc1608fbaaa7f848463f1c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:44:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a35d765211154bb582ec48d2d95cc0c5953f360f8d0a39b91475c8b05f9c59a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.7 MB (48697651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1747df0eb464e2466f732dbdce6dd13594b17aa4954ff2de6661db9bba7dc57f`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 11.4 MB (11368698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e9bbb5347613d12ad4629ce58ff03d6518d863d196c566ffe2b9438dbc2b81`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1358388c23a9da6d99c35767f0729ddcc9c8f5e34e1546ab07fda207f7f76442`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d52213fc877026fddaa9702eec5a54aaf090a257a494c9ec1a1ef372507e5`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 89.4 KB (89404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2a8511cf9858d39b173407e9f856956399afd006e514085607b952ba32adffcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f0196c883ebecb3e2e7e3daedcbd349d965708a2b495f6cf3eea2b727f1f67`

```dockerfile
```

-	Layers:
	-	`sha256:915ce8fda991d89afb68659ee3ea0879aba0c9c6ddff49a99f3fea9ad8cbc4a4`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 3.6 MB (3553159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9b9ff0b8b58c94f8e910399c0d59d0516bc0f14000931a33590243c7214e270`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4445a9b88c3aba497a2008d7c26ab7680dc4cc162d8bc18e7fdd2abe797929b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59812002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a6e9a7461b3bd032f5da0f32d43b6ef28490fb1b2a094321029284aea38845`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:46:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38be54f67917d094862e34ed83d9f5b14050260224cc43c64865734d5907fd67`  
		Last Modified: Fri, 08 May 2026 19:46:46 GMT  
		Size: 11.1 MB (11059291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bc2a856e734427e804ed50a73e236f216b87a5f0fe32affedbf2c2fdb7e367`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb5943e9f00792ba990c85877f68cd02fb0f955ac2c056c784d0a7f5efe7b7`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148505e68f723384842e9256ab27a20502fb933a703a02c8a8387a13fde81fa5`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 90.1 KB (90057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ffe6c1be02db912c32558802a1cee4640d3337a3f6da771c03c12a11baeb264d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dfd5864f60dfab734040f18b26d324ec7edae066ea58ce1f03dbf96587f3bb`

```dockerfile
```

-	Layers:
	-	`sha256:750cd9e0c7163f4d2f76ca439df028cb8f7e095be5f57e672cf6e8101639d6c2`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 3.6 MB (3561592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b03532524e5b66cb48a0b22ed5257ca466acb5e304ca5e4b016ba269a51762ec`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:b567de47734aea954e69749f970c22cd0f406919965309bbf6d7c1953e1bd1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61677567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b92b36195779b20947ea0839f37cc7e60ac4d4aa7d1113a2f5650d754f24975`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:44:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8e493ed078c2b75bcf190124b24d66f817692d9bedad987963efb47f7e3eef1b`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 50.0 MB (49982635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94360959d5618e11b69bfb91964671f70c91fa97cbb4ad10b760740c4cc979be`  
		Last Modified: Wed, 22 Apr 2026 01:44:29 GMT  
		Size: 11.6 MB (11602325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4683bd159b0c9f566c030f14f72e6d3ba56b3cd2ddd32e1630167162a9c9d7`  
		Last Modified: Wed, 22 Apr 2026 01:44:29 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b06cc379d25490ffb55ea59c8417d210d0f528df47378712912f6d7e3856fb`  
		Last Modified: Wed, 22 Apr 2026 01:44:29 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb01b835391e89f64bfca9573a159fe54f95da2fdf8948c539f4502b7d3a7409`  
		Last Modified: Wed, 22 Apr 2026 01:44:29 GMT  
		Size: 89.7 KB (89704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6a77f69582bbe97730c275583eb9c2eed87887536b5dc12a7128910a1e2884f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a959c2f4ffcb98d19449150ce6db04baf526061065992b94b2117175fd461a`

```dockerfile
```

-	Layers:
	-	`sha256:51c7a16af329829a73895da1767c1e1a856d0630b20d7742475982daa909f240`  
		Last Modified: Wed, 22 Apr 2026 01:44:29 GMT  
		Size: 3.6 MB (3551109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a78f62e68271ed5862995e221ae7b2bb60c57f03d1b84cb7054a823a89f72a3`  
		Last Modified: Wed, 22 Apr 2026 01:44:29 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:ed7602929a16feb77c64d999157e6faa174867845d23be61bab915f7fa103912
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
$ docker pull neurodebian@sha256:cb78772f90833a757dc6802286e148cf3c5fdd530666ccbac0f50d07cd172653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60159012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2defa8836dcf6459cf443a2e3c73a1fd010958213510f963cd5c1931d8a97569`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a35d765211154bb582ec48d2d95cc0c5953f360f8d0a39b91475c8b05f9c59a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.7 MB (48697651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6776c7f73607461d5327de460aaf62de8b210cf5cbabd275c1527eff4955c3a`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 11.4 MB (11368639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fbbad51860c6c845e5d68293c56ed4d8041346dea6accc934bfd7afa5b04ea`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d47c55cd565e841baa3ec307cb01da37a958fb06b13982b82d4e1f04004da1b`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bd9aacf74bf4e163d7b40d6119ee3d8d48b3b2cc7078db0ce2a4c407aee1e9`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 89.4 KB (89368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7587b914565a5c0df3372adb2b48d808f6dd8d77481e277a8328669fe85f5a2d`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9fe49f9a5928025f88824469880a77736da4d7fd080ce7922107878270963dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad29b1f5f6319081ccdb52337076454a4d4aadf77bd661e55aaa98e33f4c32f`

```dockerfile
```

-	Layers:
	-	`sha256:b505af5a4b755ede91f3606295650585caeafcd0f080f4b5e6a7ad0bb04fedef`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 3.6 MB (3553195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfe9ebd24f1ab7fef1b09817ad0758a918d9b82241a822a3d85aa1887562effa`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7c5f596c4bf8c0ccc478841c47092c4a4dad71a015d664685dc1c4b96dc058b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59812168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9528113b20964df2f7a7b1284f55ba0993cab2d96ad5485be40a46fb10c581f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:46:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be64bdc407e7e3b95b79a3ffa508782d23c39791fc66237b6b9ac0079e6f8e5`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 11.1 MB (11059006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a038166bca6013ff60ba5efd623dbb4e5fe1ee3d4446048b568c45cd48f1f4`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc2ed7a3a505ca3103c47fba46d5e291e08d49ee72ba39dedef20b1008f326`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a68e5868a8cbc24ca18677d15c10aa94f4c51fb3e1f19e418a98acd77848b6`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0446785ebbf74532dcba92825c6decba78dcf6a16420b18506b2ed57f7928eb`  
		Last Modified: Fri, 08 May 2026 19:46:56 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b0d5416b6794a636e42304fdb74a53a9ee53950b35de114de8bbb04947b6043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bac42a5873dea8825b57dc7136a3a27ca3ab5b4fcb1501abbb9798be97ed00`

```dockerfile
```

-	Layers:
	-	`sha256:24443809fcc31ff23bd314ca750f0f95a8effe8849bd1131390892d2ec92e5a6`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 3.6 MB (3561628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a27081017521680b89fcfa70690d05d07b6f2c8103aaa1557dbe8917649d344`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:68c8caaa525fb7223385d32365035d951af0a3cc72b4e66b7d6cfe5c566afb02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61677937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa17230452c876a2d8a3c5576a8fd1bed30d1edb5a39ba11ce261aa6798a0b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:44:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8e493ed078c2b75bcf190124b24d66f817692d9bedad987963efb47f7e3eef1b`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 50.0 MB (49982635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d662fdb158408b2fedf0e40b496565b70491d8294bf1c490553c3dfda6195ed8`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 11.6 MB (11602262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f78d4a1b4d2014b2edbdb4fccc21825590436c931b9e0f83fb963975b07944`  
		Last Modified: Wed, 22 Apr 2026 01:44:32 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a4e93492a9888476101da3c86d785101e184400f602205dbed1e959478beb8`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81242bb0274bd2fa6ff5b612f329761a3e36e90e6c8014ad4dffb5bbf8f19c15`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 89.7 KB (89686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5455fa89b26cd82935fd1de8324fdd96fd098ee9cbfb2e706521e60b8dee73`  
		Last Modified: Wed, 22 Apr 2026 01:44:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bbd9aa4b5708608a45a6cdd8dfdcd329e96786dbe49d94fc30576bb1a4b36cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af604f7169325a941fea2a219908462b6f83dc4385aab437c6a10ee4b931f1fb`

```dockerfile
```

-	Layers:
	-	`sha256:6667e66f263848cf3b7fbbe831ca021279975fc3afea3506804a05fa97621020`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 3.6 MB (3551145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a30d397fdc35c8ecec80224e63ece1557a301a9bc58960549bfd3070dfebd1`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:f6fa659c57cd3501016ca1ed8eb1db84d3b3b1a226cc366e7e61d96ae5155ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:2f0fd821940ff2c5c6a43627a339ff2778da6884f1e657b872528dba13a5f109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39abd8158df6cb8261ed5d7f1dd2e9698859f3784b92904a525780402bf869d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:45:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:45:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:45:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:45:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a0d00c0f0430cb54741bf28ef6804e56a7f81ab1d0d9cbe6305c9384e9cd3b`  
		Last Modified: Wed, 15 Apr 2026 20:45:53 GMT  
		Size: 3.6 MB (3624576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c442d951a1dae3285e65c64d3639b59d1b0f0ec02d6c9a31cc5d78505c6267b`  
		Last Modified: Wed, 15 Apr 2026 20:45:53 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9806153fbdc7d8043ddc9aa77c25c22431d4c2b4ea2aca9f10905296fef88641`  
		Last Modified: Wed, 15 Apr 2026 20:45:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750b458c10864bc191b40b013fc3894e80f9fcea0e4618239e4cd21160e66e8`  
		Last Modified: Wed, 15 Apr 2026 20:45:53 GMT  
		Size: 111.2 KB (111217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5a594aff365d025e0beec6d868b6d8ee84c3efa3ee40055f9dfd29022464e9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b69e2efd639b37425c6e5f24dcfa96ed1efaa47ecc599c4a7b800ef1d8486c1`

```dockerfile
```

-	Layers:
	-	`sha256:8fe91db8a5c91118251ccfe3efdcceea34b6b913103d99b48281ddbe21877422`  
		Last Modified: Wed, 15 Apr 2026 20:45:53 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb36725f84b3e51d2fe1e91b28dec76e3e56a9f63d3c2c99531ef97775296e4f`  
		Last Modified: Wed, 15 Apr 2026 20:45:53 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f698b46d1d08de638206641fe7292d966a89bda4f76354373726ebfe50ceafa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31324627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2f457de228566f84d49473bb23d255c5c9d6bcaab9d71afb6bb93725b12c4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:45:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:45:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:45:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:45:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d34255c98036c824f92e03dc6cab06104f7d55ee33597f2b10563c03df48ec`  
		Last Modified: Wed, 15 Apr 2026 20:46:01 GMT  
		Size: 3.6 MB (3604782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876d199b2fe0e952e7bec9b14a9191f336fd819a14bd5950fc1df9db1907d30b`  
		Last Modified: Wed, 15 Apr 2026 20:46:00 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45eeafd8c0c5f917c80e9fbdf4cd4d70bf776e67e0251deaf2575057ab6b46a6`  
		Last Modified: Wed, 15 Apr 2026 20:46:01 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d878197d20824c7d6693f154f4fe1a487f85c661b96ccdf6a356a3828aa1d3`  
		Last Modified: Wed, 15 Apr 2026 20:46:01 GMT  
		Size: 111.1 KB (111125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ff35bdc7471720aea26ad4910c21e3da279a0326608750174ba3dff8252354ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f762f3cae1b7b310ec6ed1f6f1ce432c84511a2f0aff2db33a312587f393acd`

```dockerfile
```

-	Layers:
	-	`sha256:e8531d2d611253702ec4df47223456adbdd6ee0b8a7cf16278c9662e3ae995c3`  
		Last Modified: Wed, 15 Apr 2026 20:46:01 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916c2b2bae4508bba8dd0dffca31c2f85d813cd1e6f70e268b858e8509b4a2ca`  
		Last Modified: Wed, 15 Apr 2026 20:46:01 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:c99116c09bc8de746040c2075d4e228007e55e9ed617672993ab707d10667f0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:0210e74aafbafdbbea9d4ef776a5996a2067729b8bf25f454bcb840b134eafa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee27c67466d8b19910dcd33bfdedaf76194c457fb9dfdb7b790f432eb6c952c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a29f30d01ad1b7ac766ba5ca34b8f5a45d21dc37b38867a848dfe0ad68b089`  
		Last Modified: Wed, 15 Apr 2026 20:46:25 GMT  
		Size: 3.6 MB (3624543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e24e6031036fd6fb768c5b117e7dee8621544ff233abcbf157ca8c54ca6f1d1`  
		Last Modified: Wed, 15 Apr 2026 20:46:25 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d1883baa964f4986793298b8ba0db3bb52ea06760d67d466092d09253c4f5f`  
		Last Modified: Wed, 15 Apr 2026 20:46:24 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46d27056f4ebaa04ac8db48dc4a339d3e77860ee1afd8afaa90b364aa3d6d89`  
		Last Modified: Wed, 15 Apr 2026 20:46:25 GMT  
		Size: 111.2 KB (111188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a924c9f32b1c3806c42bb0ddbbabb2d21def11c10ae3da2bc7a03afffaf00bdb`  
		Last Modified: Wed, 15 Apr 2026 20:46:26 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ddef23b2c200fe7f523743d30fd5fb95946e12b8848b1af643a9618993a912f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc14c06ee05e522f567b1847a03c26e7a96dd248f3fd28d05cffc4e81832434`

```dockerfile
```

-	Layers:
	-	`sha256:be89bd56a11cb767460fe7ee0107b216a24eaa075bb4aa803e09302d195cca11`  
		Last Modified: Wed, 15 Apr 2026 20:46:25 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:676cb338aa29814dfc8a756d531624bb0ed4ddb8e0a8f3f88aa30dc396c165fc`  
		Last Modified: Wed, 15 Apr 2026 20:46:25 GMT  
		Size: 16.2 KB (16162 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a25bf5b430df7a724bcd552368f360f71eb7b4eb78bad71d86ce15585d675a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31324832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b733fad0a4e174154aa0cd6d066c75222853c9619932088de36f26585519c049`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4af860fda3286fd466167fd26a750fb9bb84a11685a1e2e5d4690eac8a8299`  
		Last Modified: Wed, 15 Apr 2026 20:46:16 GMT  
		Size: 3.6 MB (3604742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fc05f2f5e0c35a94e53c90be993999af2c3065821e5eaebb9cc14c8701237e`  
		Last Modified: Wed, 15 Apr 2026 20:46:16 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ef84648ee9071cf202c749de9748c4af8dd40d7da6e532247fb0eed488fc88`  
		Last Modified: Wed, 15 Apr 2026 20:46:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ff721cb1a4d62af2989ecfa4646378a3595fd9c8e2e6180199da0dccf8c0b2`  
		Last Modified: Wed, 15 Apr 2026 20:46:16 GMT  
		Size: 111.1 KB (111086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5105e46c729a2e49e28fddeecf3b120f300687d30bce7fa63ced21afe76164e5`  
		Last Modified: Wed, 15 Apr 2026 20:46:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:39bacafc37c022a99c64ee865201dba5b7f61cd4e8783c6a29799a9a89fe019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef95d9acc8263a0222f2fb04b2d60d26031556137f9d86d2848939e93128a6c3`

```dockerfile
```

-	Layers:
	-	`sha256:1582ab48ecda6e5d90f3d89636c69037efc877dcc06eb6065fc08d5a4fc97d59`  
		Last Modified: Wed, 15 Apr 2026 20:46:16 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7a51a4258f653457a04b98fa228415b8ba0afbcafc7903aa9db8dada175068`  
		Last Modified: Wed, 15 Apr 2026 20:46:16 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:94d74707cddecdabb1b66675cf4bc1295d51dcce9b54ca1cc84f8753163c374c
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
$ docker pull neurodebian@sha256:7d39bdb049d63a02c3df2dd7c78552151cd335dfc073402fe68bebfcb0371a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59688225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3841c96179deaba2f3b7dd01df80bc3d441d7468d7f714c9d74d25d9b5f1af6c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7b07652ba0b5b42398fd9d4133dbf46fc8d5475a7803c682e5d68fae669ae8`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 10.3 MB (10292834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68609610d977281523a6d91534dd2a98a6262c5ce9219fbf52ee5d428d272117`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704da151269ac996fe5183c92901832119273bd56759fcfdcda086da74ca77f`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a0d5c4a276204f2213d846b598ad5d1f09dbb4f3c7b30c399e59c91eda1597`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 90.4 KB (90388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2075e251f251eeba52911348c5d809b65c7de868f4cc0c92cbbdd4e2f92b63ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8af64b9f3ed93290a526738e1cef88ad71e120871908f6f6df96b209c049490`

```dockerfile
```

-	Layers:
	-	`sha256:e671d5b382d3a8fc0a6b85f6fa5b3664ee884f295967583f816d456347ddf56a`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5af09e767338438f7cfcee3f0e371bdf9cce1eb908c3cb0f2ad26adb28fe76`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d503ee17e4a04127673e873eadb5e238338d8534e69de76f9a2834dea00068f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d388d64eed3a472d75c0230a0f7e0ec18ea76b7a49cf2f265fc7b87ba9fbbad9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c629af507dca062ea56f93574fa391e844b4d6e1b5cd11cad63be92b46a1d6`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 10.1 MB (10078011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abab8ca898857514fc5bd463e6e97a767bbca2cb8aea60e359cd6acaaa15751`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a787e0f5c6e783915e7fc9afa550e0bcf87b812188a88bfe09536d428841b0`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac226701451e2fd232f7351b186bb36b4f7e1742f26e18192509106d28c45ec3`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 91.0 KB (91035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dc047d2f30ed6ac4ec61cc1afcc3087048f8b38a8af931444118db41c4d4566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfb1e88be3ddf79970c3f161eee07195b0acfc24a53e5306704d479fd7126a7`

```dockerfile
```

-	Layers:
	-	`sha256:4d576367898d58cb2af04ebc67ca27c1a684572a74fe8c3a8c3fa9d91bb20031`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349d03efc82e58b0fabaeba13d01e95372d1322c71cdcb42706cd4ee07d99898`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:b93692a0d27abf858e7a70728b423918b63b4c28684b86f83619864eb34bafbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a962688ba052c54db63b75fb9fa483376cf556ba0a010682baca43c66eff9da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911b68cd92ec09b4f3e51e44040daa939ffe29ebafb7b3dbe1d070e2a5eb2858`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 10.5 MB (10467016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0273b8fe2b0a620955891d6bd4e97501e44926bfb62fb882e13a16278dedceb`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cac839167dc6c1253dd4afdc68fa5bdf1ed97b1b3e09b0e47aad451c1c320e`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30f71f5f1eff1e9d1498ffa21b42cdd8089783d49cdacb85c9fecdd17ac7335`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 90.8 KB (90755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb3de53c6290e3572e8909fb096f8bf06cfc34cfecbbb0e67425ac7022c3645b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0d4b4784c953a39e988218e0bd8c6d2abbc3ee0b636b1f2fb27a0550f82b53`

```dockerfile
```

-	Layers:
	-	`sha256:d9d94578c173d477959d8c4eae4e8acf6a0e46cb977d3addb084721bb028a36f`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f6073c1f07e93781814a1153d3cd5b025a40ac08ae799c9998f6f8305b0e4a`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 14.2 KB (14217 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:e104106f660546d667426a24f12ea3c97aeca1793ebffc238c73b16197ce61bd
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
$ docker pull neurodebian@sha256:4579804f9c875206d578d7270319dc28a643d4aa34b4a2367fc01971c611b3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60132047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c41acaf6f627e96a8a6c80d06069c338667c22f85a7d97f1e84ef7a31090bdf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:44:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:27 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a10f86d641494b5e6b1c3b8b85409baab7c4d325c9d6b292a94180331dd6b765`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 48.7 MB (48670580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3323d1feb76ec39412cdc7d5e6f45ca2ae177c89aa55e93ac5b44a2b6d906a5`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 11.4 MB (11369205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c437c44f17b74c9f33cf3e8e09521e142cce4eca24916441e07fe0bb3c6761e`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdebad56288aa68c2c0d31e441aa24dc3377cb17a75fadca678055d5a9b8037`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595eea0b749305f483189db566fdd77c036708c287c2826ffea185e7ec4aef28`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 89.4 KB (89361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5416e419aee655489a1463c82274d016822c2e5580d33624857a086b5efa2e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d239d728c5941ccb90be7991659b301e96754d13cf2e657566205ab9865d2930`

```dockerfile
```

-	Layers:
	-	`sha256:e113e9ad631fc85d20909c5fe6734ab6769af5809a286fde81aa8eddfcfba9fb`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 3.6 MB (3553954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b311560e14d5ed28de590f0d425f27f4f3767dda4686161f9a858af8bf7073af`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8d042e0c6b2b0bdc7bd6088a54197a0062b4e77fef4e334f0b514b42ce76bf43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59920057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca4e48d28afe7d23765196f54fdea60741801af0f6b198d4f1d7aff164ec43b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:46:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2a6841249cc037385aca9cb88bc26e07cfa8ed2a3f883ffdea8ae1be354b5a`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 11.1 MB (11092978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938906dfc842f7becc351af1835f05072b61776a354569f75a22d1f1e6ac299`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0668f71f67e7f7a552b9af4850f0941fb6afd56c29cadc4acd358584bd8a7518`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c06c9c91f639614d4952e3ed20b59bf97c833709c3620987f812909d74f82f`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 90.0 KB (90027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1515e7f8ac45bd3a4a536ba87d58574f9beedb409c59fc72752b88164c944056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36672cedf692ab9b354876cbf435214d90917c05080107060f25e608acf9f045`

```dockerfile
```

-	Layers:
	-	`sha256:1aa37ce6e70e12258b02b458c1845581d86ecdd450c40a6a59c724b75463cf93`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 3.6 MB (3560939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da2b316ca48ed77a2b1aa0ced2f3d8e67b58143d8135f7f24e5168d05f49127`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:044f83a3d7eb0b8c55409b58a1f42685deca14fbe335dd8caa00f5f372d9bfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61673915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc23870d7b84a7c15f4e2f712545287a06f7569ec1c73fa77cd088f2bddcd7fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:44:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:23 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a68ed28706ac755be40447c885e7277b571939be826b0bcf8abd61cb9be646c1`  
		Last Modified: Wed, 22 Apr 2026 00:17:10 GMT  
		Size: 50.0 MB (49978211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd6f22b6390e0b2749fca38f9bb2fd609f4420f88c6ef086f4d2a6c3c71c7f8`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 11.6 MB (11603049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be5abcee47f182db20cd39e6c87b5f6253d17d004ca4cc49437e874b1331770`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3352681e10ff29c43254c025849efec18d6b5dd5ad9f3031cd9b43ed4f1b4932`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575874e7db5cb895159b72c29b91e0ab22a06e4a74312556d1ff14e5925bbdf0`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 89.8 KB (89754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c30220cbd31e8748b077b77cfc95c1630d8f2c4dc27f35c5c089a9a36bcee31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25903a975556a7d320dfd4c4b4ef0fe89a1b7f9e5f9a10269a8520fe75b6ee3`

```dockerfile
```

-	Layers:
	-	`sha256:60a8019be1efe3a65435f58733997d2b65f94549ca8d9d7b5364942ced6e9904`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 3.6 MB (3551903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c745709d65d1864c614cdb8c10c0a67e3faf129b909cc387e1c03227688a1344`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:d70ce4038c2f2be6f5cd739ab937f6602f0cc3d3c3a803af2ff38aa82371d5f0
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
$ docker pull neurodebian@sha256:8254b96416c8ed428becd6efb7cdbc2a3723a8848c7832b166e8d11b0e9afd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60132721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142695fdea8a00a7f5e049cd7e3d16d3f45c60ec3c83408e71540e5afe7425b2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:44:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a10f86d641494b5e6b1c3b8b85409baab7c4d325c9d6b292a94180331dd6b765`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 48.7 MB (48670580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee90c31e0b15f4e954828cc2f0d46688fe82416349686f56dec0c166678f5638`  
		Last Modified: Wed, 22 Apr 2026 01:44:41 GMT  
		Size: 11.4 MB (11369466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e4cb1c64ac9255bf58f619be961961ee174ea76890f76f7618aaae17d36ea8`  
		Last Modified: Wed, 22 Apr 2026 01:44:41 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1e9d2b4d9826d726772bce260874a2643d684a679d886c0261c13de59f8488`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92e25aa604374b2020c0332b1b6dc98904a02655ccfb3ed6f6f811a9aef26c6`  
		Last Modified: Wed, 22 Apr 2026 01:44:41 GMT  
		Size: 89.4 KB (89358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fea64fe3bebafb63bdbd3ba66eb0e5464d11fb4a8d75e97934c70c7ed99021d`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5bfff5564e0573ee9c4d10642f18ff643d102ebd4d9912360c21faf5362ca8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4ea5287434c12cbe0d87060dca1b8110c2968791cdba5c3f94ab8fda1a6504`

```dockerfile
```

-	Layers:
	-	`sha256:524e5639afe25e0ba933e92eed8a89dad80f88d9ef7624eebf1cdc79bb7fd552`  
		Last Modified: Wed, 22 Apr 2026 01:44:41 GMT  
		Size: 3.6 MB (3553990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a93ebe9eccb230ade1d8700be8f427026ffdb634abf6a5ef474b0208902b13f`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bc374f952257e26453ff7836ddfaedb60bcb7b8567066896a59a1dc6235eafc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59920570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33147fd5038a8f3c7854dd92f9f80f55966afc35978f38770149742f5fcb876e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:46:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364834fc8139dd37c03942d4ae776f1690a19fa2aadbf6286e0c696c77f02654`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 11.1 MB (11093047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce88d73a7e0fe050bda503e936cec378bffa4e11cf99f44f3547a9bb9550e9b`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042248e359b2ca8c613f492ddea03664e1f5545d422f89ca2eb579ec4fe36cf8`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d05b1b5889373a2ff082dcc562fe9b6c87f4dc954311c07a9235161b5b8348a`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 90.0 KB (90047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb1a6769325f550371ea3eda25df8162e96ffd9d1e724c04e9fd6a53a5b15d3`  
		Last Modified: Fri, 08 May 2026 19:47:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:38f1246a7857ae16f1ee50ce83dd99f709d82307b1ac48db4580cdd4ec7ea6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3237ed235baeb7082f0151c28c4714dc3f510674f4b363afa9a12ad73cdc2a00`

```dockerfile
```

-	Layers:
	-	`sha256:d51df37178d40b9b383e7bec1cacfb104cebafc298e749ac1e0fe3566149be4c`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 3.6 MB (3560975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fef56e4295a87c65f8c4cda5532f9cef3a17c374c89cd048b622e0afe8df15d8`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:5164af7768687649b18fe93a5992d4a0024df733a66f8b02596fde9e8dcda1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61674235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a5a6ba8b32631c0e82985b0c51df6185372015fb3e8cf77b77ee456d1a75ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:44:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a68ed28706ac755be40447c885e7277b571939be826b0bcf8abd61cb9be646c1`  
		Last Modified: Wed, 22 Apr 2026 00:17:10 GMT  
		Size: 50.0 MB (49978211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880bc6e7d430abb8a6ef2d8705a91aa0e43894a1c630b37d5a10b23cd36b0c70`  
		Last Modified: Wed, 22 Apr 2026 01:44:52 GMT  
		Size: 11.6 MB (11602999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d87cf4bc4f5fecdcdfe3a6a62fb1b07da675a417909df6d6a6e1dca26cccf8`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0781201189a8dfd0b453ce46cce647390e66eb32c4311f35e87bccd757dc2820`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e4c6b35978a2d1f7aabfe5b6e8eb013ce3eeecb0d5b21091356ba3b8ddc893`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 89.7 KB (89705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7400f42191ea101aeabc19397e96f4aa24e7c153d04899e4e5971b3bf435fa9`  
		Last Modified: Wed, 22 Apr 2026 01:44:52 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:78129261531fb1c60d6bd44f21b001f3c940728bc776e8e3c61bcf3a3210c3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cf5872a91f89295c3884443f2c314ec3d0648e920c08ab2fc034a0d03122f4`

```dockerfile
```

-	Layers:
	-	`sha256:d55e913d71eef96fab9791a630c39238eff4ee5e9ace508b97b4df1c24716e67`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 3.6 MB (3551939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942f6867a08a89dac43be49a8d7c02797c05dda7bbd9ee3ee17ecc3c05101c3d`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:443c0020b56d7e47a8970f9cc9a86ca79e0a67bdfd756f8fd6b4d95a26d6a6c7
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
$ docker pull neurodebian@sha256:48b978dd2f847654f39cd8f1776daa4aa9df89f142414d40f5676f7b97bc8370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002d5b89a4707f51717893785ccc02875837ce31f701bfa352334058bda856c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:17:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:17:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 02:17:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 02:17:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c72d0fa0f448323831012892fcfa3fcab666bcfd3f5dffde9845c3fcff1a5c`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 11.1 MB (11103538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f9437b17831a4574865078d6d6f2735530dd5df4d98bdf4cf80ecbe1eacb9f`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a07c90585c91a04ece397b0b7c2aa7103ad950e701ca4fbc90e9031dc945452`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9e0d3d2c3d046339e5eafeda28eb07678ebf29523f1cc7311ca0f4366b5a69`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 101.4 KB (101428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:11f07afbbbe928a378281a2e4e9aa71232f720ed8c10015d2a68898a8f42f783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ac64d62683665c45e0891c0b9483a646131f67f43e3d7c13640436e90407b`

```dockerfile
```

-	Layers:
	-	`sha256:8c4be9b8444a505246705c3f67d140f0953839be0a6106ab4b93c9696fb8f504`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:610c4abfd3a816fbc742987c537a656800f8939c7bf19bab75263e3fa00aec50`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:62347cb324bd70e5569c022cf36e136aa8e826f40f1c2238889b719f8cc66a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088aaba085173fd83cbf817a16c6e4af04bdc9ae9eedb10afd7c44e3489ddef4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:45:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49da93cc2679b1db042cd202e875060e5e3220e87732350bd5904898892e8b8`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 11.1 MB (11109914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b825eee855070f51dfefec4cf70685dd607f1dc1402855869b4bbcaf7b576135`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3209c067378d18d75a18203938000ce323b7b747348cca016301c372c516e6a7`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0c848bef723aca7f046b18ce448a4097239a1da120f540e52dd1c9a68a4b31`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 101.3 KB (101279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4243308f1b786a75f6a0506780d5c7b33ac30f8511fccca56aec4dea210c21b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e762402feeb4d06253b996167883d80d3641bf9e0680cf01273d11c016d6d5`

```dockerfile
```

-	Layers:
	-	`sha256:b14f0dcc1c2ef0142185e8793a6e22f9422570c4ba9d2b6abb2cb7125ce110f1`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2aa08681f076f24ce71cb639cc4949a46b91a1a127541e91c515a501664465`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:536a24ed300f7097dfcf2172b256af1fac92e8330df1d13d872c307189bbec8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66310669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9dd43c77bd5d638de962eb7e18c7f249ab4e2bdca5a094b9bcd978505640864`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:43:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:43:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:737d996bc05c156425b11be5deec8366db5d7a009f49d85b480b1daec555cf4a`  
		Last Modified: Wed, 22 Apr 2026 00:16:40 GMT  
		Size: 54.7 MB (54705161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972b7c8adf2a27a1f8aafa4b3116bdcbf1f1d0f8a6aef3490cddfa4590ac906e`  
		Last Modified: Wed, 22 Apr 2026 01:43:42 GMT  
		Size: 11.5 MB (11502060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f0dfa0a8ed6ad0cb09e36854d5422976effffcfbd936ac5a4a113b16e6bf2d`  
		Last Modified: Wed, 22 Apr 2026 01:43:41 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9893d72ec7e08c0258b1055d94509241c3d4ce544fd7b4e302997e97a707dd9`  
		Last Modified: Wed, 22 Apr 2026 01:43:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5dde940fe9dc18128c53ba66b638ac94ba0781292661c734238dbe93390fa86`  
		Last Modified: Wed, 22 Apr 2026 01:43:42 GMT  
		Size: 101.3 KB (101289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ece6d734ac81ab2b79479e0bc686630400733ac99fec541329be113734278f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699476441be45f0a6f814f470afb8e48404ae6f80347c2e4589de20a7c098cea`

```dockerfile
```

-	Layers:
	-	`sha256:0c074ec835c373fe44220d2d54c37558332aaa81aa1bc9e5b60da7dedcd8a426`  
		Last Modified: Wed, 22 Apr 2026 01:43:42 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b80984558c97b94a7c30b55c0b69f2841ccd87cad8b0879ad0a1c1b470d9df4`  
		Last Modified: Wed, 22 Apr 2026 01:43:41 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:a3cbd7ca8039c13e7eb7e557f96439de19b426e31ca2d13b56dde94b07020624
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
$ docker pull neurodebian@sha256:555440ecc7c6f655a1f24cb37b25ac77f16f360a99049d9ea7a9c5c136dba234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38937761e563f02f1a8d4ba92e24ea94cdcd83de4203265bb370625eeda2fd05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:44:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0802b439ba506ee42b40891edfe6f9b4eb3055ea7d81ecbc3d1c87a08b141de`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 11.1 MB (11103547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42ee071305f1b461b88de5416fff15b4f7563a181be72046ad6dcbe2c446b02`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f9afea8b6181ada18a56edd636f0726aed91cc8382c81977739411f231524f`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386ec5b98b370be832b747e784e7effe8e6a952f7ce138c4def942bcc243d7f1`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 101.4 KB (101353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c47ebcb0a700e2b6652dbc7de864c41d2126d949ebd0bca7ed3acfc9d8b614a`  
		Last Modified: Wed, 22 Apr 2026 01:44:12 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ace222ba3da95f703da60158d587e1157e099ecbbae7f02da2f2877bb04ba743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54135d0cb4cdfc7dfac0b8beb5954939cb79280fe680f47eec5643ad0f6e7346`

```dockerfile
```

-	Layers:
	-	`sha256:e768aa59b6fdb62033d29df462af080e0ce18d30ba88640f432b6cfaeb7aa0eb`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b29bfc03bd2c77e02f21088f2cda163050d8f828320dfa8b1d23037ce926f25`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d72cd51fb944fbeefc59dbcfd9207dd62d6b1409175dc0b62c30c20f9723340d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c72a73a81907cd10f4ed9d514fe1d0c96154b13d775360ec1f4e578b4b7c08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4d4853c366ae1d8a6092357fdeceb46f1af7fb6971f30fb5bac64d2816093`  
		Last Modified: Fri, 08 May 2026 19:46:12 GMT  
		Size: 11.1 MB (11109872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0860e8ce6527c5e5eb574f904941f9d5fd1ac72704eec1e19c9667591571cda7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2407a0ee518c92a25d491c4909ce3ed0cb4f84524941a201a7cf2bfd943c1ed7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86985c6bd9a382f6fe79e55952fe846b9dac4b331da91606603aeebec797fb71`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 101.3 KB (101294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a645068ae63614955aa0cce30edd178a25de8ca2dd269f25af6a34467cb6d54c`  
		Last Modified: Fri, 08 May 2026 19:46:12 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e79ba75ecd78047e815efee9fa2ef478d94689d9d1ab9f20fb7ba7bf72a022e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aae72f0e29b5b3a88976fb346afe0082117da0014a70001d64ee3963b586eab`

```dockerfile
```

-	Layers:
	-	`sha256:97a48df79af5e64bcca963ffbc0947249e8e2964559cd3a0216d0b5fe3a662f7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7ecf2ecbf82b72a416e1ef61bc9ea6fe75d4c000ee213c306b6148414a9521`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:be20e7b0e215c4deec6aa2de282c6b428f0d9d78dfa2e9a48a21a04aa1309aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66311074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271902e4ce05784fc0ff5d6e016a0845b149c59c943cd5951bb641ac145378f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:43:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:43:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:737d996bc05c156425b11be5deec8366db5d7a009f49d85b480b1daec555cf4a`  
		Last Modified: Wed, 22 Apr 2026 00:16:40 GMT  
		Size: 54.7 MB (54705161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1516c79839462487ebf969fa4a5a0db19d5af6adf507a4fc9cc33e702e252f68`  
		Last Modified: Wed, 22 Apr 2026 01:43:41 GMT  
		Size: 11.5 MB (11502096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc24b7ff3fb59cab3e8b089d3e98f3aeeeebc1a716fe7e4b4710a8f2c57f89ce`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ed96c6739d01a12337c6c9b40fe1c07118326d0531824658d69a8239253bbb`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1c6f719a9e92fa099ce6018f4fe86fc6cd03baeb042f11c1d662042c50bf9`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 101.3 KB (101271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4755ffa1449a1b0999111b69e5bd22eb4db3b4de5dd016f94f99c635cd80148f`  
		Last Modified: Wed, 22 Apr 2026 01:43:42 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8d9b3ca1ff285715b70ca7072ee3070c4f5c341311035c12b90f3bacbc8db176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d03e6338a4f4cda9497f14486e3ba04f901974153fba8b8ee489b3574a9899`

```dockerfile
```

-	Layers:
	-	`sha256:06c69fd2a19c9907618c9ace118aa384a7baf2562e3fb8fd3747926c796f47ae`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e13d9295d1f7ceb76e6efe645bb726797d1bbf0ea08d285d5bf4fd07015d0ca5`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:f25a14cd042e8f406521801107486ccc509a87ac933b09a12d429c6638ed0834
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
$ docker pull neurodebian@sha256:774f937a033e82ec79ed5efdc524cc60f359b1b4578f1fe4f7a90b3a4b378ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3025f51a5e1acbf6054583346525cafa3bd7ca82cd43160ebb36811e1daa5171`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:43:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3666961b6d8a250dea41e73593bb3b314425613763ef952df72a2210e3c9db4e`  
		Last Modified: Wed, 22 Apr 2026 01:44:14 GMT  
		Size: 11.3 MB (11273365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6cdd6bbdfee34d91d0fd4ea0fa6b4706aa25b44d362635dd3e91dfb9770821`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e195f58e61236402a05c20b3ca9a451789af8cfb3e1c12867b223461107e745`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33104a23ec2785413870f721ee969d98f2eba62377bfd3becfb8b9c049d52061`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 93.4 KB (93403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:56e34690ed311f09247f5dbc2483f0257259f2ca934b4aba64ca6a1ca19957d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dda936e5d2e3d4600ddbea0f9c91de89ad2d94e7b306e7e9ea16f25c5a79350`

```dockerfile
```

-	Layers:
	-	`sha256:52a2c953c3a0537c47a81aa029093121fe18618db5cea6819dca6816208ab171`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e210200a09eaeed334b94d7f6f33309c0879fad0c85624f972f547671479418d`  
		Last Modified: Wed, 22 Apr 2026 01:44:13 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c383b1c8bcc59487007ea946c97be72b381f54ee51d5fd892cf0629fdeb1c9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628c1e90e3da7350faabb21fc74a0c88da8663666dd19dbdb74ba907e12ef2b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbeab365177c9b941a081ba0b6d957ba147319fe32dff22aa2624a53a06f29b`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 11.3 MB (11252933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fa205d0d4d9ff7d136faa66f376fb23aff6334613faa278f84518f8e5c01ff`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14309867687b534670e51c1d96567476c0f1aaed795f789d0445fab07399b4d`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89033d9b2184954874f8f00b5a17aecc6b429a80a8e0038b84aa6ee81ff3383`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 93.5 KB (93546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ede2b6186f52eb37d412780815c7330d58d6faa9837786a7e5c79b52f572fd93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ee394c617722eaa31b6265fd68e7ac215a0a018ff4f39c2985bca8c06e3347`

```dockerfile
```

-	Layers:
	-	`sha256:d4b4657e224bc234c23ab66a4c0a2fe772e905a9fe22fae905f739583d04c417`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29aedf8be25ddf5a7975ddb70961e5bb9c8359ec72bba50cbb2e61f0f256a671`  
		Last Modified: Fri, 08 May 2026 19:46:09 GMT  
		Size: 14.1 KB (14088 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:5fc238140262f53118929824ba430e3f0b7979a132cd8de5a362c29017787166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b675a907be02445819e41f56368d40c152b80121abda8e1bbefae9dd78926d26`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:43:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:43:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f607c56991d572a9c9e62692330777522b959fe17a14367be35d12959214fa4`  
		Last Modified: Wed, 22 Apr 2026 00:16:17 GMT  
		Size: 49.5 MB (49477718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2c9d6696a3b3db58c324a6862fbc2cd52cbe3b89b6e6f0bce3bf2a4e56202b`  
		Last Modified: Wed, 22 Apr 2026 01:44:02 GMT  
		Size: 11.7 MB (11692983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557955c0b0a3f5532ff7ed95be47c99d54964f54442e2a391332f755cd2ab255`  
		Last Modified: Wed, 22 Apr 2026 01:44:02 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3165092047810227052b1a2879d085156c89d784d281b3f0e72f5cd38cbf43`  
		Last Modified: Wed, 22 Apr 2026 01:44:02 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5684e4be91c395c0648bc93df42a048e7b60636cbf89d1aef495ef8c66e08c8c`  
		Last Modified: Wed, 22 Apr 2026 01:44:02 GMT  
		Size: 93.4 KB (93410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73db3da4c5b46785cb76f45bb4b2825507a37af6996fb9a24def8e205ad09e13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed9ae811d0aad7fdf51336ca7a7ce5c8c78b33dc963138eff67d7abc63c357e`

```dockerfile
```

-	Layers:
	-	`sha256:8f829d49c7ebeed50174636f6d2dcc620e3b7e1ce2c929e01b853fb8de7799b7`  
		Last Modified: Wed, 22 Apr 2026 01:44:02 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39e67fdf566a0f64a1b29c67deb65e498edaeb18f85b97a6ac368e8bb97ce098`  
		Last Modified: Wed, 22 Apr 2026 01:44:02 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:f68c8548da8486214f14894daa7005640c5cfb8982cea9d147400aded59f53e9
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
$ docker pull neurodebian@sha256:2c4cb4e49d32e0800ccab1b383c4df2c0507d6232aa910100bacae012ccc80be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a98c800a04fa92beeebb45cece13dc9a5a2bb2afacd3fe6b49a6af4c345f54a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:44:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5c6f68a47f6aafe93c229c3fa17bd8f9eca8dbcb82026f265892037a7e7ca8`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 11.3 MB (11273308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d79daf0cf6757e31a1107175cd1e7462256549e1d3d30fcce502bd6b523440`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acd65166e3ebd350cc72a3012913c626286396db1340b7ea63e94bf18f645be`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccad9b7d786b644e59a626a14638210a2ea9aff44f74ec61dbf6eee0101215`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 93.4 KB (93400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e4d2762c39b83ebeb647c5d5a01a7535bb73003d5cfdc730cbd58dda43cb37`  
		Last Modified: Wed, 22 Apr 2026 01:44:17 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a894ea750272941947bceba5b021cb9f1323c9effce5f027b01b101eaf12b7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7391f965c78c1414439c34110a9ddf1fc2954c0ab321306169ec35348f65b3b`

```dockerfile
```

-	Layers:
	-	`sha256:438e2af1d3add7733f1e2b743bd1418519d72549264d12b537bed012abfeec97`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebde2f39b24d1676597cba7a414b48ddb0418b77cd09adc479774d0c97715acd`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9ce456a29d55af753754c81bcf6c489b588e4ef8d345a25a1185ac4ed38d7067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83671130319d212529fed9657df2275a72b7a9972a90c7d4eeb3087a8c2e780`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:46:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297af71f398d804e9824bb6964f5f84de1d86338b03a2c087345a9e6adeae9e7`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 11.3 MB (11252932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbc6e93f45b3f4cf455734139898464377b66e14251b76f3361f3d34ed49b9d`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2bd671e957e80374283f5fb64814dafa746ed40e7cf68d7972fffd7054de17`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58c4f363214c80dee9f62e6d8d410c16b88764ef3e641e1d8bc9231b3d9cae7`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 93.6 KB (93575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1d2f24bc5c69d6c727ad3568cbc4addea466c9b6cc928ea044b626717466f`  
		Last Modified: Fri, 08 May 2026 19:46:28 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f29b6635607465a6f03d6780e7c09679fb49ac9bb340deaae75b283f8ed832d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3acb1d5d8d6cb02f7c1e8bd1cb80b8eb98d8808fa839c362abc1fbb0ad92f8`

```dockerfile
```

-	Layers:
	-	`sha256:c992b9778cd7c443812a6eca47e360178d13695c8043203be74e9562afd8f30e`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee5d86f16916b238e87145c3058d5b9f4308cb209db7450c1e9f13152f33e5b9`  
		Last Modified: Fri, 08 May 2026 19:46:27 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:520ee5a44ddfe1fdc8c29908c80cd33fa4b80e61e0a6a7fea2236f8acf57e63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39b44109263a95adccf888e8d1877cb1c7e34ee47ad75e1bb7a63abc65c9a72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:43:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:43:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1f607c56991d572a9c9e62692330777522b959fe17a14367be35d12959214fa4`  
		Last Modified: Wed, 22 Apr 2026 00:16:17 GMT  
		Size: 49.5 MB (49477718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c950f45f1a3bfc61a9c1480c4ea9fde2a03316cd953138ce00699c9f7a3b045b`  
		Last Modified: Wed, 22 Apr 2026 01:44:05 GMT  
		Size: 11.7 MB (11692996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06407c79badd50171efc07c97a8e73ce7ea48d39d2677a386a47b60804ab9c00`  
		Last Modified: Wed, 22 Apr 2026 01:44:04 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed8f9d4838a2b0037c69af61b838c7a681ec221f106d08be8c0d589f82cefc8`  
		Last Modified: Wed, 22 Apr 2026 01:44:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b48decc6dfccfbac4be598308637f9bd32f75d105fe1a9e2d50ddaad525978f`  
		Last Modified: Wed, 22 Apr 2026 01:44:04 GMT  
		Size: 93.4 KB (93406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d828cfd13f00eab171bc955be08af42ecb017a4fc01a54804cf008f7b9c0a95b`  
		Last Modified: Wed, 22 Apr 2026 01:44:05 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:12a5b425515756459b282bc12e754da5d18f9654f7f594d3ab5fa131fccddcd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d688f4c176cb5073364ce52b334f75aeb3cacd7da06b77e3e2e68fa02a1b7b99`

```dockerfile
```

-	Layers:
	-	`sha256:7f4fa81df859d5217bb07cfb2ca3a6026136a42f1b4d5beb2b7d4ee8d75117c8`  
		Last Modified: Wed, 22 Apr 2026 01:44:05 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be869ef59e935c1c52547a4769be7bb9ba422296f6d77f409abddf7bf2567ce`  
		Last Modified: Wed, 22 Apr 2026 01:44:04 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:94d74707cddecdabb1b66675cf4bc1295d51dcce9b54ca1cc84f8753163c374c
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
$ docker pull neurodebian@sha256:7d39bdb049d63a02c3df2dd7c78552151cd335dfc073402fe68bebfcb0371a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59688225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3841c96179deaba2f3b7dd01df80bc3d441d7468d7f714c9d74d25d9b5f1af6c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7b07652ba0b5b42398fd9d4133dbf46fc8d5475a7803c682e5d68fae669ae8`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 10.3 MB (10292834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68609610d977281523a6d91534dd2a98a6262c5ce9219fbf52ee5d428d272117`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704da151269ac996fe5183c92901832119273bd56759fcfdcda086da74ca77f`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a0d5c4a276204f2213d846b598ad5d1f09dbb4f3c7b30c399e59c91eda1597`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 90.4 KB (90388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2075e251f251eeba52911348c5d809b65c7de868f4cc0c92cbbdd4e2f92b63ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8af64b9f3ed93290a526738e1cef88ad71e120871908f6f6df96b209c049490`

```dockerfile
```

-	Layers:
	-	`sha256:e671d5b382d3a8fc0a6b85f6fa5b3664ee884f295967583f816d456347ddf56a`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5af09e767338438f7cfcee3f0e371bdf9cce1eb908c3cb0f2ad26adb28fe76`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d503ee17e4a04127673e873eadb5e238338d8534e69de76f9a2834dea00068f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d388d64eed3a472d75c0230a0f7e0ec18ea76b7a49cf2f265fc7b87ba9fbbad9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c629af507dca062ea56f93574fa391e844b4d6e1b5cd11cad63be92b46a1d6`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 10.1 MB (10078011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abab8ca898857514fc5bd463e6e97a767bbca2cb8aea60e359cd6acaaa15751`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a787e0f5c6e783915e7fc9afa550e0bcf87b812188a88bfe09536d428841b0`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac226701451e2fd232f7351b186bb36b4f7e1742f26e18192509106d28c45ec3`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 91.0 KB (91035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dc047d2f30ed6ac4ec61cc1afcc3087048f8b38a8af931444118db41c4d4566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfb1e88be3ddf79970c3f161eee07195b0acfc24a53e5306704d479fd7126a7`

```dockerfile
```

-	Layers:
	-	`sha256:4d576367898d58cb2af04ebc67ca27c1a684572a74fe8c3a8c3fa9d91bb20031`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349d03efc82e58b0fabaeba13d01e95372d1322c71cdcb42706cd4ee07d99898`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:b93692a0d27abf858e7a70728b423918b63b4c28684b86f83619864eb34bafbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a962688ba052c54db63b75fb9fa483376cf556ba0a010682baca43c66eff9da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911b68cd92ec09b4f3e51e44040daa939ffe29ebafb7b3dbe1d070e2a5eb2858`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 10.5 MB (10467016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0273b8fe2b0a620955891d6bd4e97501e44926bfb62fb882e13a16278dedceb`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cac839167dc6c1253dd4afdc68fa5bdf1ed97b1b3e09b0e47aad451c1c320e`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30f71f5f1eff1e9d1498ffa21b42cdd8089783d49cdacb85c9fecdd17ac7335`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 90.8 KB (90755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb3de53c6290e3572e8909fb096f8bf06cfc34cfecbbb0e67425ac7022c3645b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0d4b4784c953a39e988218e0bd8c6d2abbc3ee0b636b1f2fb27a0550f82b53`

```dockerfile
```

-	Layers:
	-	`sha256:d9d94578c173d477959d8c4eae4e8acf6a0e46cb977d3addb084721bb028a36f`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f6073c1f07e93781814a1153d3cd5b025a40ac08ae799c9998f6f8305b0e4a`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 14.2 KB (14217 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:7c25850f13514bb5f7076fc80bbef82ca88fa43e206d06b995215fdeba6734ee
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
$ docker pull neurodebian@sha256:fa0a0c59897f568dbd24d22d1ffad43f3d2d486c87b322decf55010e63ebe7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59688741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6e757416a31a10fe456fbce9f65637fcd410ae9060094eff8b83d22d495f08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736e5ef169f8956ac3ddd8962c7f3ac33358eefd1d409b540f9de34c4124d4f5`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 10.3 MB (10292878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5324f86f94a30d26738538cdcc77789cffc104c7224bf71ffd4f31880bcf978d`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ff8367d18ed54d7ef38179813a30136e56e90bdddf8538bd5d9e3bba79031e`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ff0e6d854abd5c8c1d58fe100dfa1ffc15291a14f8ba6667e78804e781dd23`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 90.4 KB (90418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dec1851547d03be0d4ac2b715a78ea782afcc8e622301546cbe2328b38c329`  
		Last Modified: Wed, 22 Apr 2026 01:44:45 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:662b1464f8f9fa2c56d9cf9b316bfc2d3763dd83b9636c49b55af1ad3f4301f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9a0958715426078c5d0edc833bbc12b2940a6f1bbecdea77f2ead608daf66d`

```dockerfile
```

-	Layers:
	-	`sha256:2b4f598d075bd78774768313e704b93fab3addc68198641beb64a73415ac06fc`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15201318cfc195a091a4d18d26e19b91e30563b7e8eb5245d56e2c91e87825db`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 16.3 KB (16281 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:57b13c1e50963a6187b7e20ca9c973fe30970f06aa206a968c81ed3e3aea7ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32a80663dcc17719bc1935a712da2852657de51fc94f60eaaa9ccc05276764`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77348ea04670cc60ed3fd70e8a942379a3a778401a47da14bddddaedbbcd473`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 10.1 MB (10077993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4f986dcc8620c40bddb431aed2820d258c0ba86a933a572cfb5aea1b7c8d1`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484764866e70b0d12ffdf225ed2ef6dc9af0cfbae6d1ffc072bc54f2bbd8710c`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13df355aa2411e3cab96fecc0b4927c1a75301419531a535765c87be27bdcc72`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 91.0 KB (91046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb102d2bb0e4b299a1747924f034d561048a35b0c3ad22fb08df099037f5e1e`  
		Last Modified: Fri, 08 May 2026 19:46:38 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4a7fc429753a5755b5ee64226c7038ce723951b0fe08eabbc3fba8e4a1697e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c66c6f71d2cc072b4de445c3593012348006787233156dcc732fecc292ecf16`

```dockerfile
```

-	Layers:
	-	`sha256:4d3e70240cf4968ed03616db1c20e456abae7c75f133eabd39d8fea05bf2ab22`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac819a829dd4e682388cbb13c01e4c3ee1c2e11f1c959436f84e286ee2fb631`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:fff406f046666fb4890c9d913ff9ba736422f2c6bdf8b908cd141bd6b2533580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377248caa6dfe840a39a0840a6918be642ebb10883f356f9bcfcd3b49da05559`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70486075489439e2cd8bc3d19b95f151daa410ec96b0b5ec410607342a763f`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 10.5 MB (10467058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce5ba82bfe696b9b1e74d40cfc00fd3f4af6d09d2c28b0c41aa4ff6199d5ff9`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5396f55357f76f8761749a573ebca269a5ca3856757532ea722b50f24c7b5e83`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a642280bee42260dfea7eb3563d5dd6be3c1ee1adad589b34545dccc50afc2f`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 90.7 KB (90737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb80dabacc2bef1a453fe4101f563092b2cfc66ed5d6694c1a5b44e3977c5b3d`  
		Last Modified: Wed, 22 Apr 2026 01:44:24 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c5c41f2d533954b0f70e97ce3faf5170feb5b028c3422a65a51b999044ef5687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07e627a3eebcd70224cb60daafb4b40d62d9550259916dc98eaa08114b81127`

```dockerfile
```

-	Layers:
	-	`sha256:648cc1a4dd4d99fca873e35292f97d65299d49dc771c22a38f4660698a9c562f`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859385b3b4616b5fda752ed466aa158e53610e52f42c433757a2154725095aee`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:62b75019dc174623fafe7826699ae6fd8cb48e69d17d111c45755361e2951049
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
$ docker pull neurodebian@sha256:002f7fb8429812eb25298710a7653a0a06f2c9b122c6f1e6cdec699025eb2bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60158655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f010db1188288b639deb5a145a8914aa4fb9a0fcc1608fbaaa7f848463f1c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:44:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a35d765211154bb582ec48d2d95cc0c5953f360f8d0a39b91475c8b05f9c59a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.7 MB (48697651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1747df0eb464e2466f732dbdce6dd13594b17aa4954ff2de6661db9bba7dc57f`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 11.4 MB (11368698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e9bbb5347613d12ad4629ce58ff03d6518d863d196c566ffe2b9438dbc2b81`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1358388c23a9da6d99c35767f0729ddcc9c8f5e34e1546ab07fda207f7f76442`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d52213fc877026fddaa9702eec5a54aaf090a257a494c9ec1a1ef372507e5`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 89.4 KB (89404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2a8511cf9858d39b173407e9f856956399afd006e514085607b952ba32adffcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f0196c883ebecb3e2e7e3daedcbd349d965708a2b495f6cf3eea2b727f1f67`

```dockerfile
```

-	Layers:
	-	`sha256:915ce8fda991d89afb68659ee3ea0879aba0c9c6ddff49a99f3fea9ad8cbc4a4`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 3.6 MB (3553159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9b9ff0b8b58c94f8e910399c0d59d0516bc0f14000931a33590243c7214e270`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4445a9b88c3aba497a2008d7c26ab7680dc4cc162d8bc18e7fdd2abe797929b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59812002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a6e9a7461b3bd032f5da0f32d43b6ef28490fb1b2a094321029284aea38845`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:46:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38be54f67917d094862e34ed83d9f5b14050260224cc43c64865734d5907fd67`  
		Last Modified: Fri, 08 May 2026 19:46:46 GMT  
		Size: 11.1 MB (11059291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bc2a856e734427e804ed50a73e236f216b87a5f0fe32affedbf2c2fdb7e367`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb5943e9f00792ba990c85877f68cd02fb0f955ac2c056c784d0a7f5efe7b7`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148505e68f723384842e9256ab27a20502fb933a703a02c8a8387a13fde81fa5`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 90.1 KB (90057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ffe6c1be02db912c32558802a1cee4640d3337a3f6da771c03c12a11baeb264d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52dfd5864f60dfab734040f18b26d324ec7edae066ea58ce1f03dbf96587f3bb`

```dockerfile
```

-	Layers:
	-	`sha256:750cd9e0c7163f4d2f76ca439df028cb8f7e095be5f57e672cf6e8101639d6c2`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 3.6 MB (3561592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b03532524e5b66cb48a0b22ed5257ca466acb5e304ca5e4b016ba269a51762ec`  
		Last Modified: Fri, 08 May 2026 19:46:45 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; 386

```console
$ docker pull neurodebian@sha256:b567de47734aea954e69749f970c22cd0f406919965309bbf6d7c1953e1bd1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61677567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b92b36195779b20947ea0839f37cc7e60ac4d4aa7d1113a2f5650d754f24975`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:44:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8e493ed078c2b75bcf190124b24d66f817692d9bedad987963efb47f7e3eef1b`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 50.0 MB (49982635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94360959d5618e11b69bfb91964671f70c91fa97cbb4ad10b760740c4cc979be`  
		Last Modified: Wed, 22 Apr 2026 01:44:29 GMT  
		Size: 11.6 MB (11602325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4683bd159b0c9f566c030f14f72e6d3ba56b3cd2ddd32e1630167162a9c9d7`  
		Last Modified: Wed, 22 Apr 2026 01:44:29 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b06cc379d25490ffb55ea59c8417d210d0f528df47378712912f6d7e3856fb`  
		Last Modified: Wed, 22 Apr 2026 01:44:29 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb01b835391e89f64bfca9573a159fe54f95da2fdf8948c539f4502b7d3a7409`  
		Last Modified: Wed, 22 Apr 2026 01:44:29 GMT  
		Size: 89.7 KB (89704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6a77f69582bbe97730c275583eb9c2eed87887536b5dc12a7128910a1e2884f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a959c2f4ffcb98d19449150ce6db04baf526061065992b94b2117175fd461a`

```dockerfile
```

-	Layers:
	-	`sha256:51c7a16af329829a73895da1767c1e1a856d0630b20d7742475982daa909f240`  
		Last Modified: Wed, 22 Apr 2026 01:44:29 GMT  
		Size: 3.6 MB (3551109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a78f62e68271ed5862995e221ae7b2bb60c57f03d1b84cb7054a823a89f72a3`  
		Last Modified: Wed, 22 Apr 2026 01:44:29 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:ed7602929a16feb77c64d999157e6faa174867845d23be61bab915f7fa103912
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
$ docker pull neurodebian@sha256:cb78772f90833a757dc6802286e148cf3c5fdd530666ccbac0f50d07cd172653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60159012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2defa8836dcf6459cf443a2e3c73a1fd010958213510f963cd5c1931d8a97569`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a35d765211154bb582ec48d2d95cc0c5953f360f8d0a39b91475c8b05f9c59a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.7 MB (48697651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6776c7f73607461d5327de460aaf62de8b210cf5cbabd275c1527eff4955c3a`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 11.4 MB (11368639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fbbad51860c6c845e5d68293c56ed4d8041346dea6accc934bfd7afa5b04ea`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d47c55cd565e841baa3ec307cb01da37a958fb06b13982b82d4e1f04004da1b`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bd9aacf74bf4e163d7b40d6119ee3d8d48b3b2cc7078db0ce2a4c407aee1e9`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 89.4 KB (89368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7587b914565a5c0df3372adb2b48d808f6dd8d77481e277a8328669fe85f5a2d`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9fe49f9a5928025f88824469880a77736da4d7fd080ce7922107878270963dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad29b1f5f6319081ccdb52337076454a4d4aadf77bd661e55aaa98e33f4c32f`

```dockerfile
```

-	Layers:
	-	`sha256:b505af5a4b755ede91f3606295650585caeafcd0f080f4b5e6a7ad0bb04fedef`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 3.6 MB (3553195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfe9ebd24f1ab7fef1b09817ad0758a918d9b82241a822a3d85aa1887562effa`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7c5f596c4bf8c0ccc478841c47092c4a4dad71a015d664685dc1c4b96dc058b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59812168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9528113b20964df2f7a7b1284f55ba0993cab2d96ad5485be40a46fb10c581f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:46:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:47 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be64bdc407e7e3b95b79a3ffa508782d23c39791fc66237b6b9ac0079e6f8e5`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 11.1 MB (11059006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a038166bca6013ff60ba5efd623dbb4e5fe1ee3d4446048b568c45cd48f1f4`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bc2ed7a3a505ca3103c47fba46d5e291e08d49ee72ba39dedef20b1008f326`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a68e5868a8cbc24ca18677d15c10aa94f4c51fb3e1f19e418a98acd77848b6`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 90.1 KB (90060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0446785ebbf74532dcba92825c6decba78dcf6a16420b18506b2ed57f7928eb`  
		Last Modified: Fri, 08 May 2026 19:46:56 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b0d5416b6794a636e42304fdb74a53a9ee53950b35de114de8bbb04947b6043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bac42a5873dea8825b57dc7136a3a27ca3ab5b4fcb1501abbb9798be97ed00`

```dockerfile
```

-	Layers:
	-	`sha256:24443809fcc31ff23bd314ca750f0f95a8effe8849bd1131390892d2ec92e5a6`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 3.6 MB (3561628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a27081017521680b89fcfa70690d05d07b6f2c8103aaa1557dbe8917649d344`  
		Last Modified: Fri, 08 May 2026 19:46:55 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:68c8caaa525fb7223385d32365035d951af0a3cc72b4e66b7d6cfe5c566afb02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61677937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa17230452c876a2d8a3c5576a8fd1bed30d1edb5a39ba11ce261aa6798a0b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:44:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8e493ed078c2b75bcf190124b24d66f817692d9bedad987963efb47f7e3eef1b`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 50.0 MB (49982635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d662fdb158408b2fedf0e40b496565b70491d8294bf1c490553c3dfda6195ed8`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 11.6 MB (11602262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f78d4a1b4d2014b2edbdb4fccc21825590436c931b9e0f83fb963975b07944`  
		Last Modified: Wed, 22 Apr 2026 01:44:32 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a4e93492a9888476101da3c86d785101e184400f602205dbed1e959478beb8`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81242bb0274bd2fa6ff5b612f329761a3e36e90e6c8014ad4dffb5bbf8f19c15`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 89.7 KB (89686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5455fa89b26cd82935fd1de8324fdd96fd098ee9cbfb2e706521e60b8dee73`  
		Last Modified: Wed, 22 Apr 2026 01:44:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bbd9aa4b5708608a45a6cdd8dfdcd329e96786dbe49d94fc30576bb1a4b36cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af604f7169325a941fea2a219908462b6f83dc4385aab437c6a10ee4b931f1fb`

```dockerfile
```

-	Layers:
	-	`sha256:6667e66f263848cf3b7fbbe831ca021279975fc3afea3506804a05fa97621020`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 3.6 MB (3551145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a30d397fdc35c8ecec80224e63ece1557a301a9bc58960549bfd3070dfebd1`  
		Last Modified: Wed, 22 Apr 2026 01:44:33 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:f6fa659c57cd3501016ca1ed8eb1db84d3b3b1a226cc366e7e61d96ae5155ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:2f0fd821940ff2c5c6a43627a339ff2778da6884f1e657b872528dba13a5f109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39abd8158df6cb8261ed5d7f1dd2e9698859f3784b92904a525780402bf869d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:45:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:45:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:45:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:45:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a0d00c0f0430cb54741bf28ef6804e56a7f81ab1d0d9cbe6305c9384e9cd3b`  
		Last Modified: Wed, 15 Apr 2026 20:45:53 GMT  
		Size: 3.6 MB (3624576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c442d951a1dae3285e65c64d3639b59d1b0f0ec02d6c9a31cc5d78505c6267b`  
		Last Modified: Wed, 15 Apr 2026 20:45:53 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9806153fbdc7d8043ddc9aa77c25c22431d4c2b4ea2aca9f10905296fef88641`  
		Last Modified: Wed, 15 Apr 2026 20:45:53 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750b458c10864bc191b40b013fc3894e80f9fcea0e4618239e4cd21160e66e8`  
		Last Modified: Wed, 15 Apr 2026 20:45:53 GMT  
		Size: 111.2 KB (111217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5a594aff365d025e0beec6d868b6d8ee84c3efa3ee40055f9dfd29022464e9ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b69e2efd639b37425c6e5f24dcfa96ed1efaa47ecc599c4a7b800ef1d8486c1`

```dockerfile
```

-	Layers:
	-	`sha256:8fe91db8a5c91118251ccfe3efdcceea34b6b913103d99b48281ddbe21877422`  
		Last Modified: Wed, 15 Apr 2026 20:45:53 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb36725f84b3e51d2fe1e91b28dec76e3e56a9f63d3c2c99531ef97775296e4f`  
		Last Modified: Wed, 15 Apr 2026 20:45:53 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f698b46d1d08de638206641fe7292d966a89bda4f76354373726ebfe50ceafa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31324627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2f457de228566f84d49473bb23d255c5c9d6bcaab9d71afb6bb93725b12c4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:45:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:45:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:45:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:45:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d34255c98036c824f92e03dc6cab06104f7d55ee33597f2b10563c03df48ec`  
		Last Modified: Wed, 15 Apr 2026 20:46:01 GMT  
		Size: 3.6 MB (3604782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876d199b2fe0e952e7bec9b14a9191f336fd819a14bd5950fc1df9db1907d30b`  
		Last Modified: Wed, 15 Apr 2026 20:46:00 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45eeafd8c0c5f917c80e9fbdf4cd4d70bf776e67e0251deaf2575057ab6b46a6`  
		Last Modified: Wed, 15 Apr 2026 20:46:01 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d878197d20824c7d6693f154f4fe1a487f85c661b96ccdf6a356a3828aa1d3`  
		Last Modified: Wed, 15 Apr 2026 20:46:01 GMT  
		Size: 111.1 KB (111125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ff35bdc7471720aea26ad4910c21e3da279a0326608750174ba3dff8252354ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f762f3cae1b7b310ec6ed1f6f1ce432c84511a2f0aff2db33a312587f393acd`

```dockerfile
```

-	Layers:
	-	`sha256:e8531d2d611253702ec4df47223456adbdd6ee0b8a7cf16278c9662e3ae995c3`  
		Last Modified: Wed, 15 Apr 2026 20:46:01 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916c2b2bae4508bba8dd0dffca31c2f85d813cd1e6f70e268b858e8509b4a2ca`  
		Last Modified: Wed, 15 Apr 2026 20:46:01 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:c99116c09bc8de746040c2075d4e228007e55e9ed617672993ab707d10667f0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:0210e74aafbafdbbea9d4ef776a5996a2067729b8bf25f454bcb840b134eafa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 MB (33474689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee27c67466d8b19910dcd33bfdedaf76194c457fb9dfdb7b790f432eb6c952c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a29f30d01ad1b7ac766ba5ca34b8f5a45d21dc37b38867a848dfe0ad68b089`  
		Last Modified: Wed, 15 Apr 2026 20:46:25 GMT  
		Size: 3.6 MB (3624543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e24e6031036fd6fb768c5b117e7dee8621544ff233abcbf157ca8c54ca6f1d1`  
		Last Modified: Wed, 15 Apr 2026 20:46:25 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d1883baa964f4986793298b8ba0db3bb52ea06760d67d466092d09253c4f5f`  
		Last Modified: Wed, 15 Apr 2026 20:46:24 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46d27056f4ebaa04ac8db48dc4a339d3e77860ee1afd8afaa90b364aa3d6d89`  
		Last Modified: Wed, 15 Apr 2026 20:46:25 GMT  
		Size: 111.2 KB (111188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a924c9f32b1c3806c42bb0ddbbabb2d21def11c10ae3da2bc7a03afffaf00bdb`  
		Last Modified: Wed, 15 Apr 2026 20:46:26 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ddef23b2c200fe7f523743d30fd5fb95946e12b8848b1af643a9618993a912f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc14c06ee05e522f567b1847a03c26e7a96dd248f3fd28d05cffc4e81832434`

```dockerfile
```

-	Layers:
	-	`sha256:be89bd56a11cb767460fe7ee0107b216a24eaa075bb4aa803e09302d195cca11`  
		Last Modified: Wed, 15 Apr 2026 20:46:25 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:676cb338aa29814dfc8a756d531624bb0ed4ddb8e0a8f3f88aa30dc396c165fc`  
		Last Modified: Wed, 15 Apr 2026 20:46:25 GMT  
		Size: 16.2 KB (16162 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a25bf5b430df7a724bcd552368f360f71eb7b4eb78bad71d86ce15585d675a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31324832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b733fad0a4e174154aa0cd6d066c75222853c9619932088de36f26585519c049`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:46:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 15 Apr 2026 20:46:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 15 Apr 2026 20:46:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:46:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4af860fda3286fd466167fd26a750fb9bb84a11685a1e2e5d4690eac8a8299`  
		Last Modified: Wed, 15 Apr 2026 20:46:16 GMT  
		Size: 3.6 MB (3604742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fc05f2f5e0c35a94e53c90be993999af2c3065821e5eaebb9cc14c8701237e`  
		Last Modified: Wed, 15 Apr 2026 20:46:16 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ef84648ee9071cf202c749de9748c4af8dd40d7da6e532247fb0eed488fc88`  
		Last Modified: Wed, 15 Apr 2026 20:46:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ff721cb1a4d62af2989ecfa4646378a3595fd9c8e2e6180199da0dccf8c0b2`  
		Last Modified: Wed, 15 Apr 2026 20:46:16 GMT  
		Size: 111.1 KB (111086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5105e46c729a2e49e28fddeecf3b120f300687d30bce7fa63ced21afe76164e5`  
		Last Modified: Wed, 15 Apr 2026 20:46:18 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:39bacafc37c022a99c64ee865201dba5b7f61cd4e8783c6a29799a9a89fe019a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef95d9acc8263a0222f2fb04b2d60d26031556137f9d86d2848939e93128a6c3`

```dockerfile
```

-	Layers:
	-	`sha256:1582ab48ecda6e5d90f3d89636c69037efc877dcc06eb6065fc08d5a4fc97d59`  
		Last Modified: Wed, 15 Apr 2026 20:46:16 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7a51a4258f653457a04b98fa228415b8ba0afbcafc7903aa9db8dada175068`  
		Last Modified: Wed, 15 Apr 2026 20:46:16 GMT  
		Size: 16.3 KB (16303 bytes)  
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
$ docker pull neurodebian@sha256:7c25850f13514bb5f7076fc80bbef82ca88fa43e206d06b995215fdeba6734ee
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
$ docker pull neurodebian@sha256:fa0a0c59897f568dbd24d22d1ffad43f3d2d486c87b322decf55010e63ebe7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59688741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6e757416a31a10fe456fbce9f65637fcd410ae9060094eff8b83d22d495f08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736e5ef169f8956ac3ddd8962c7f3ac33358eefd1d409b540f9de34c4124d4f5`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 10.3 MB (10292878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5324f86f94a30d26738538cdcc77789cffc104c7224bf71ffd4f31880bcf978d`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ff8367d18ed54d7ef38179813a30136e56e90bdddf8538bd5d9e3bba79031e`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ff0e6d854abd5c8c1d58fe100dfa1ffc15291a14f8ba6667e78804e781dd23`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 90.4 KB (90418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dec1851547d03be0d4ac2b715a78ea782afcc8e622301546cbe2328b38c329`  
		Last Modified: Wed, 22 Apr 2026 01:44:45 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:662b1464f8f9fa2c56d9cf9b316bfc2d3763dd83b9636c49b55af1ad3f4301f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9a0958715426078c5d0edc833bbc12b2940a6f1bbecdea77f2ead608daf66d`

```dockerfile
```

-	Layers:
	-	`sha256:2b4f598d075bd78774768313e704b93fab3addc68198641beb64a73415ac06fc`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15201318cfc195a091a4d18d26e19b91e30563b7e8eb5245d56e2c91e87825db`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 16.3 KB (16281 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:57b13c1e50963a6187b7e20ca9c973fe30970f06aa206a968c81ed3e3aea7ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32a80663dcc17719bc1935a712da2852657de51fc94f60eaaa9ccc05276764`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77348ea04670cc60ed3fd70e8a942379a3a778401a47da14bddddaedbbcd473`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 10.1 MB (10077993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4f986dcc8620c40bddb431aed2820d258c0ba86a933a572cfb5aea1b7c8d1`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484764866e70b0d12ffdf225ed2ef6dc9af0cfbae6d1ffc072bc54f2bbd8710c`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13df355aa2411e3cab96fecc0b4927c1a75301419531a535765c87be27bdcc72`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 91.0 KB (91046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb102d2bb0e4b299a1747924f034d561048a35b0c3ad22fb08df099037f5e1e`  
		Last Modified: Fri, 08 May 2026 19:46:38 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4a7fc429753a5755b5ee64226c7038ce723951b0fe08eabbc3fba8e4a1697e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c66c6f71d2cc072b4de445c3593012348006787233156dcc732fecc292ecf16`

```dockerfile
```

-	Layers:
	-	`sha256:4d3e70240cf4968ed03616db1c20e456abae7c75f133eabd39d8fea05bf2ab22`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac819a829dd4e682388cbb13c01e4c3ee1c2e11f1c959436f84e286ee2fb631`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:fff406f046666fb4890c9d913ff9ba736422f2c6bdf8b908cd141bd6b2533580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377248caa6dfe840a39a0840a6918be642ebb10883f356f9bcfcd3b49da05559`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70486075489439e2cd8bc3d19b95f151daa410ec96b0b5ec410607342a763f`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 10.5 MB (10467058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce5ba82bfe696b9b1e74d40cfc00fd3f4af6d09d2c28b0c41aa4ff6199d5ff9`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5396f55357f76f8761749a573ebca269a5ca3856757532ea722b50f24c7b5e83`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a642280bee42260dfea7eb3563d5dd6be3c1ee1adad589b34545dccc50afc2f`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 90.7 KB (90737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb80dabacc2bef1a453fe4101f563092b2cfc66ed5d6694c1a5b44e3977c5b3d`  
		Last Modified: Wed, 22 Apr 2026 01:44:24 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c5c41f2d533954b0f70e97ce3faf5170feb5b028c3422a65a51b999044ef5687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07e627a3eebcd70224cb60daafb4b40d62d9550259916dc98eaa08114b81127`

```dockerfile
```

-	Layers:
	-	`sha256:648cc1a4dd4d99fca873e35292f97d65299d49dc771c22a38f4660698a9c562f`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859385b3b4616b5fda752ed466aa158e53610e52f42c433757a2154725095aee`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:e104106f660546d667426a24f12ea3c97aeca1793ebffc238c73b16197ce61bd
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
$ docker pull neurodebian@sha256:4579804f9c875206d578d7270319dc28a643d4aa34b4a2367fc01971c611b3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60132047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c41acaf6f627e96a8a6c80d06069c338667c22f85a7d97f1e84ef7a31090bdf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:44:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:27 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a10f86d641494b5e6b1c3b8b85409baab7c4d325c9d6b292a94180331dd6b765`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 48.7 MB (48670580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3323d1feb76ec39412cdc7d5e6f45ca2ae177c89aa55e93ac5b44a2b6d906a5`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 11.4 MB (11369205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c437c44f17b74c9f33cf3e8e09521e142cce4eca24916441e07fe0bb3c6761e`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdebad56288aa68c2c0d31e441aa24dc3377cb17a75fadca678055d5a9b8037`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595eea0b749305f483189db566fdd77c036708c287c2826ffea185e7ec4aef28`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 89.4 KB (89361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5416e419aee655489a1463c82274d016822c2e5580d33624857a086b5efa2e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d239d728c5941ccb90be7991659b301e96754d13cf2e657566205ab9865d2930`

```dockerfile
```

-	Layers:
	-	`sha256:e113e9ad631fc85d20909c5fe6734ab6769af5809a286fde81aa8eddfcfba9fb`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 3.6 MB (3553954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b311560e14d5ed28de590f0d425f27f4f3767dda4686161f9a858af8bf7073af`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8d042e0c6b2b0bdc7bd6088a54197a0062b4e77fef4e334f0b514b42ce76bf43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59920057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca4e48d28afe7d23765196f54fdea60741801af0f6b198d4f1d7aff164ec43b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:46:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2a6841249cc037385aca9cb88bc26e07cfa8ed2a3f883ffdea8ae1be354b5a`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 11.1 MB (11092978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938906dfc842f7becc351af1835f05072b61776a354569f75a22d1f1e6ac299`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0668f71f67e7f7a552b9af4850f0941fb6afd56c29cadc4acd358584bd8a7518`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c06c9c91f639614d4952e3ed20b59bf97c833709c3620987f812909d74f82f`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 90.0 KB (90027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1515e7f8ac45bd3a4a536ba87d58574f9beedb409c59fc72752b88164c944056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36672cedf692ab9b354876cbf435214d90917c05080107060f25e608acf9f045`

```dockerfile
```

-	Layers:
	-	`sha256:1aa37ce6e70e12258b02b458c1845581d86ecdd450c40a6a59c724b75463cf93`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 3.6 MB (3560939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da2b316ca48ed77a2b1aa0ced2f3d8e67b58143d8135f7f24e5168d05f49127`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:044f83a3d7eb0b8c55409b58a1f42685deca14fbe335dd8caa00f5f372d9bfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61673915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc23870d7b84a7c15f4e2f712545287a06f7569ec1c73fa77cd088f2bddcd7fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:44:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:23 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a68ed28706ac755be40447c885e7277b571939be826b0bcf8abd61cb9be646c1`  
		Last Modified: Wed, 22 Apr 2026 00:17:10 GMT  
		Size: 50.0 MB (49978211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd6f22b6390e0b2749fca38f9bb2fd609f4420f88c6ef086f4d2a6c3c71c7f8`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 11.6 MB (11603049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be5abcee47f182db20cd39e6c87b5f6253d17d004ca4cc49437e874b1331770`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3352681e10ff29c43254c025849efec18d6b5dd5ad9f3031cd9b43ed4f1b4932`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575874e7db5cb895159b72c29b91e0ab22a06e4a74312556d1ff14e5925bbdf0`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 89.8 KB (89754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c30220cbd31e8748b077b77cfc95c1630d8f2c4dc27f35c5c089a9a36bcee31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25903a975556a7d320dfd4c4b4ef0fe89a1b7f9e5f9a10269a8520fe75b6ee3`

```dockerfile
```

-	Layers:
	-	`sha256:60a8019be1efe3a65435f58733997d2b65f94549ca8d9d7b5364942ced6e9904`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 3.6 MB (3551903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c745709d65d1864c614cdb8c10c0a67e3faf129b909cc387e1c03227688a1344`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:d70ce4038c2f2be6f5cd739ab937f6602f0cc3d3c3a803af2ff38aa82371d5f0
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
$ docker pull neurodebian@sha256:8254b96416c8ed428becd6efb7cdbc2a3723a8848c7832b166e8d11b0e9afd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60132721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142695fdea8a00a7f5e049cd7e3d16d3f45c60ec3c83408e71540e5afe7425b2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:44:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a10f86d641494b5e6b1c3b8b85409baab7c4d325c9d6b292a94180331dd6b765`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 48.7 MB (48670580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee90c31e0b15f4e954828cc2f0d46688fe82416349686f56dec0c166678f5638`  
		Last Modified: Wed, 22 Apr 2026 01:44:41 GMT  
		Size: 11.4 MB (11369466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e4cb1c64ac9255bf58f619be961961ee174ea76890f76f7618aaae17d36ea8`  
		Last Modified: Wed, 22 Apr 2026 01:44:41 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1e9d2b4d9826d726772bce260874a2643d684a679d886c0261c13de59f8488`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92e25aa604374b2020c0332b1b6dc98904a02655ccfb3ed6f6f811a9aef26c6`  
		Last Modified: Wed, 22 Apr 2026 01:44:41 GMT  
		Size: 89.4 KB (89358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fea64fe3bebafb63bdbd3ba66eb0e5464d11fb4a8d75e97934c70c7ed99021d`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5bfff5564e0573ee9c4d10642f18ff643d102ebd4d9912360c21faf5362ca8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4ea5287434c12cbe0d87060dca1b8110c2968791cdba5c3f94ab8fda1a6504`

```dockerfile
```

-	Layers:
	-	`sha256:524e5639afe25e0ba933e92eed8a89dad80f88d9ef7624eebf1cdc79bb7fd552`  
		Last Modified: Wed, 22 Apr 2026 01:44:41 GMT  
		Size: 3.6 MB (3553990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a93ebe9eccb230ade1d8700be8f427026ffdb634abf6a5ef474b0208902b13f`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bc374f952257e26453ff7836ddfaedb60bcb7b8567066896a59a1dc6235eafc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59920570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33147fd5038a8f3c7854dd92f9f80f55966afc35978f38770149742f5fcb876e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:46:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364834fc8139dd37c03942d4ae776f1690a19fa2aadbf6286e0c696c77f02654`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 11.1 MB (11093047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce88d73a7e0fe050bda503e936cec378bffa4e11cf99f44f3547a9bb9550e9b`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042248e359b2ca8c613f492ddea03664e1f5545d422f89ca2eb579ec4fe36cf8`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d05b1b5889373a2ff082dcc562fe9b6c87f4dc954311c07a9235161b5b8348a`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 90.0 KB (90047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb1a6769325f550371ea3eda25df8162e96ffd9d1e724c04e9fd6a53a5b15d3`  
		Last Modified: Fri, 08 May 2026 19:47:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:38f1246a7857ae16f1ee50ce83dd99f709d82307b1ac48db4580cdd4ec7ea6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3237ed235baeb7082f0151c28c4714dc3f510674f4b363afa9a12ad73cdc2a00`

```dockerfile
```

-	Layers:
	-	`sha256:d51df37178d40b9b383e7bec1cacfb104cebafc298e749ac1e0fe3566149be4c`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 3.6 MB (3560975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fef56e4295a87c65f8c4cda5532f9cef3a17c374c89cd048b622e0afe8df15d8`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:5164af7768687649b18fe93a5992d4a0024df733a66f8b02596fde9e8dcda1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61674235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a5a6ba8b32631c0e82985b0c51df6185372015fb3e8cf77b77ee456d1a75ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:44:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a68ed28706ac755be40447c885e7277b571939be826b0bcf8abd61cb9be646c1`  
		Last Modified: Wed, 22 Apr 2026 00:17:10 GMT  
		Size: 50.0 MB (49978211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880bc6e7d430abb8a6ef2d8705a91aa0e43894a1c630b37d5a10b23cd36b0c70`  
		Last Modified: Wed, 22 Apr 2026 01:44:52 GMT  
		Size: 11.6 MB (11602999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d87cf4bc4f5fecdcdfe3a6a62fb1b07da675a417909df6d6a6e1dca26cccf8`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0781201189a8dfd0b453ce46cce647390e66eb32c4311f35e87bccd757dc2820`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e4c6b35978a2d1f7aabfe5b6e8eb013ce3eeecb0d5b21091356ba3b8ddc893`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 89.7 KB (89705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7400f42191ea101aeabc19397e96f4aa24e7c153d04899e4e5971b3bf435fa9`  
		Last Modified: Wed, 22 Apr 2026 01:44:52 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:78129261531fb1c60d6bd44f21b001f3c940728bc776e8e3c61bcf3a3210c3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cf5872a91f89295c3884443f2c314ec3d0648e920c08ab2fc034a0d03122f4`

```dockerfile
```

-	Layers:
	-	`sha256:d55e913d71eef96fab9791a630c39238eff4ee5e9ace508b97b4df1c24716e67`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 3.6 MB (3551939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942f6867a08a89dac43be49a8d7c02797c05dda7bbd9ee3ee17ecc3c05101c3d`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:94d74707cddecdabb1b66675cf4bc1295d51dcce9b54ca1cc84f8753163c374c
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
$ docker pull neurodebian@sha256:7d39bdb049d63a02c3df2dd7c78552151cd335dfc073402fe68bebfcb0371a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59688225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3841c96179deaba2f3b7dd01df80bc3d441d7468d7f714c9d74d25d9b5f1af6c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7b07652ba0b5b42398fd9d4133dbf46fc8d5475a7803c682e5d68fae669ae8`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 10.3 MB (10292834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68609610d977281523a6d91534dd2a98a6262c5ce9219fbf52ee5d428d272117`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704da151269ac996fe5183c92901832119273bd56759fcfdcda086da74ca77f`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a0d5c4a276204f2213d846b598ad5d1f09dbb4f3c7b30c399e59c91eda1597`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 90.4 KB (90388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2075e251f251eeba52911348c5d809b65c7de868f4cc0c92cbbdd4e2f92b63ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8af64b9f3ed93290a526738e1cef88ad71e120871908f6f6df96b209c049490`

```dockerfile
```

-	Layers:
	-	`sha256:e671d5b382d3a8fc0a6b85f6fa5b3664ee884f295967583f816d456347ddf56a`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5af09e767338438f7cfcee3f0e371bdf9cce1eb908c3cb0f2ad26adb28fe76`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d503ee17e4a04127673e873eadb5e238338d8534e69de76f9a2834dea00068f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d388d64eed3a472d75c0230a0f7e0ec18ea76b7a49cf2f265fc7b87ba9fbbad9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c629af507dca062ea56f93574fa391e844b4d6e1b5cd11cad63be92b46a1d6`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 10.1 MB (10078011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abab8ca898857514fc5bd463e6e97a767bbca2cb8aea60e359cd6acaaa15751`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a787e0f5c6e783915e7fc9afa550e0bcf87b812188a88bfe09536d428841b0`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac226701451e2fd232f7351b186bb36b4f7e1742f26e18192509106d28c45ec3`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 91.0 KB (91035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dc047d2f30ed6ac4ec61cc1afcc3087048f8b38a8af931444118db41c4d4566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfb1e88be3ddf79970c3f161eee07195b0acfc24a53e5306704d479fd7126a7`

```dockerfile
```

-	Layers:
	-	`sha256:4d576367898d58cb2af04ebc67ca27c1a684572a74fe8c3a8c3fa9d91bb20031`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349d03efc82e58b0fabaeba13d01e95372d1322c71cdcb42706cd4ee07d99898`  
		Last Modified: Fri, 08 May 2026 19:46:35 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:b93692a0d27abf858e7a70728b423918b63b4c28684b86f83619864eb34bafbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a962688ba052c54db63b75fb9fa483376cf556ba0a010682baca43c66eff9da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911b68cd92ec09b4f3e51e44040daa939ffe29ebafb7b3dbe1d070e2a5eb2858`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 10.5 MB (10467016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0273b8fe2b0a620955891d6bd4e97501e44926bfb62fb882e13a16278dedceb`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cac839167dc6c1253dd4afdc68fa5bdf1ed97b1b3e09b0e47aad451c1c320e`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30f71f5f1eff1e9d1498ffa21b42cdd8089783d49cdacb85c9fecdd17ac7335`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 90.8 KB (90755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb3de53c6290e3572e8909fb096f8bf06cfc34cfecbbb0e67425ac7022c3645b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0d4b4784c953a39e988218e0bd8c6d2abbc3ee0b636b1f2fb27a0550f82b53`

```dockerfile
```

-	Layers:
	-	`sha256:d9d94578c173d477959d8c4eae4e8acf6a0e46cb977d3addb084721bb028a36f`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f6073c1f07e93781814a1153d3cd5b025a40ac08ae799c9998f6f8305b0e4a`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 14.2 KB (14217 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:7c25850f13514bb5f7076fc80bbef82ca88fa43e206d06b995215fdeba6734ee
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
$ docker pull neurodebian@sha256:fa0a0c59897f568dbd24d22d1ffad43f3d2d486c87b322decf55010e63ebe7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59688741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6e757416a31a10fe456fbce9f65637fcd410ae9060094eff8b83d22d495f08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736e5ef169f8956ac3ddd8962c7f3ac33358eefd1d409b540f9de34c4124d4f5`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 10.3 MB (10292878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5324f86f94a30d26738538cdcc77789cffc104c7224bf71ffd4f31880bcf978d`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ff8367d18ed54d7ef38179813a30136e56e90bdddf8538bd5d9e3bba79031e`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ff0e6d854abd5c8c1d58fe100dfa1ffc15291a14f8ba6667e78804e781dd23`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 90.4 KB (90418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dec1851547d03be0d4ac2b715a78ea782afcc8e622301546cbe2328b38c329`  
		Last Modified: Wed, 22 Apr 2026 01:44:45 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:662b1464f8f9fa2c56d9cf9b316bfc2d3763dd83b9636c49b55af1ad3f4301f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9a0958715426078c5d0edc833bbc12b2940a6f1bbecdea77f2ead608daf66d`

```dockerfile
```

-	Layers:
	-	`sha256:2b4f598d075bd78774768313e704b93fab3addc68198641beb64a73415ac06fc`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15201318cfc195a091a4d18d26e19b91e30563b7e8eb5245d56e2c91e87825db`  
		Last Modified: Wed, 22 Apr 2026 01:44:44 GMT  
		Size: 16.3 KB (16281 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:57b13c1e50963a6187b7e20ca9c973fe30970f06aa206a968c81ed3e3aea7ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32a80663dcc17719bc1935a712da2852657de51fc94f60eaaa9ccc05276764`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:29 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77348ea04670cc60ed3fd70e8a942379a3a778401a47da14bddddaedbbcd473`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 10.1 MB (10077993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae4f986dcc8620c40bddb431aed2820d258c0ba86a933a572cfb5aea1b7c8d1`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484764866e70b0d12ffdf225ed2ef6dc9af0cfbae6d1ffc072bc54f2bbd8710c`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13df355aa2411e3cab96fecc0b4927c1a75301419531a535765c87be27bdcc72`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 91.0 KB (91046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb102d2bb0e4b299a1747924f034d561048a35b0c3ad22fb08df099037f5e1e`  
		Last Modified: Fri, 08 May 2026 19:46:38 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4a7fc429753a5755b5ee64226c7038ce723951b0fe08eabbc3fba8e4a1697e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c66c6f71d2cc072b4de445c3593012348006787233156dcc732fecc292ecf16`

```dockerfile
```

-	Layers:
	-	`sha256:4d3e70240cf4968ed03616db1c20e456abae7c75f133eabd39d8fea05bf2ab22`  
		Last Modified: Fri, 08 May 2026 19:46:37 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac819a829dd4e682388cbb13c01e4c3ee1c2e11f1c959436f84e286ee2fb631`  
		Last Modified: Fri, 08 May 2026 19:46:36 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:fff406f046666fb4890c9d913ff9ba736422f2c6bdf8b908cd141bd6b2533580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377248caa6dfe840a39a0840a6918be642ebb10883f356f9bcfcd3b49da05559`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:15 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f70486075489439e2cd8bc3d19b95f151daa410ec96b0b5ec410607342a763f`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 10.5 MB (10467058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce5ba82bfe696b9b1e74d40cfc00fd3f4af6d09d2c28b0c41aa4ff6199d5ff9`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5396f55357f76f8761749a573ebca269a5ca3856757532ea722b50f24c7b5e83`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a642280bee42260dfea7eb3563d5dd6be3c1ee1adad589b34545dccc50afc2f`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 90.7 KB (90737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb80dabacc2bef1a453fe4101f563092b2cfc66ed5d6694c1a5b44e3977c5b3d`  
		Last Modified: Wed, 22 Apr 2026 01:44:24 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c5c41f2d533954b0f70e97ce3faf5170feb5b028c3422a65a51b999044ef5687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07e627a3eebcd70224cb60daafb4b40d62d9550259916dc98eaa08114b81127`

```dockerfile
```

-	Layers:
	-	`sha256:648cc1a4dd4d99fca873e35292f97d65299d49dc771c22a38f4660698a9c562f`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859385b3b4616b5fda752ed466aa158e53610e52f42c433757a2154725095aee`  
		Last Modified: Wed, 22 Apr 2026 01:44:23 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
