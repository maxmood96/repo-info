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
$ docker pull neurodebian@sha256:702369457ba4f0a5e4669e6f26acfee0481973db03ad714e8dc1b08a36d413b7
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
$ docker pull neurodebian@sha256:365aa70bf498507787226c0d7383899d14db803ab0479cbec5dbc5c437049343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fadee2b2da5a6b02cd5d771d3c878b932b1dd725b747cee3d373dcf02b04cfc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:46:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8e0c4933455fc6e8436ccd1a3948e1690ff31ee75a4c911e36f195c9e8ba5`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 11.3 MB (11252926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96ccf4228f5ededbca88454df53e0a2102eaf263c1b2794174d6967279692ac`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334f3723ee4775a37b78eb03aa81e5997c3c1e0db8d9d64523a3babf5325980`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e236fb00fbfc3fa19ecca63a96047f5a436ab74240aa466a134a6de56e34f7`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 93.6 KB (93553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2c1f9b95d357e099089706379fe9045341634f3133a97550f62641ab5d1aa96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f564316b6416d5d9f5dd0db415fc439cc4879223077fb341bfcb0808ad3b201b`

```dockerfile
```

-	Layers:
	-	`sha256:f3deeaa1aae3fbcda8209dc59d5ec673ec7afe15fe63313fbed4af3b95c50871`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0dfe5345e8d635cac1bfdec83428fbb591c72ba7827803b3fed0136575d8ed`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 14.1 KB (14090 bytes)  
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
$ docker pull neurodebian@sha256:68087a05a6a7fb01e26f490193b166ef26f3b943d68e912500b8b5a34622fb73
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
$ docker pull neurodebian@sha256:9d1120aaac014085ce56a331d7ea575340d210fa6cf6bb93d8dd48b01bde2707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4aa0f2d93ab5a0ef749e44b75fe66d1d98716e61a59f33ec6b37262e1eaf99b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:46:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:49 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1419a29641a382bd5d008c79413b7a0d7f982afcc54d158356ebf834d777985f`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 11.3 MB (11252881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c3250ae94100eccecd5ddde9d4ffa62ee2b825e07429f002e2df72bb84619`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6291e28edd6e8f08470374ec8879c087c0fb691bf9c8dcec73c4a7d89a442520`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7511dcf0a8a93bc3c8c53587e7a674accd45ee7dc685cc3c31336ef424251476`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 93.5 KB (93514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89100960aea92e7ee71badc7ca255d4f2c6989d01f183b99c05d15a3f884e142`  
		Last Modified: Wed, 22 Apr 2026 01:47:00 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:65027bce3976a61075bd0f1ac2612aaebeb740f1f6f36c9db5340623ae6d2736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be843c3b23cb464a4fb68f900a751c67e0bddb7d266bee20b02a577d9d7f918f`

```dockerfile
```

-	Layers:
	-	`sha256:6ee6b5b3e6a0e40998662f831430bde4d01243d416c3eaba5e287204740ac7e7`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca90bb44921d010c885d204cb6665ada1449816de5bd1a1732874889f0de829`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 16.1 KB (16131 bytes)  
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
$ docker pull neurodebian@sha256:65376b9f385d5024af64d90ed8fdc5995507303dbf6fa4899bb756637188e5f4
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
$ docker pull neurodebian@sha256:1506b5eb3c91ddfabe3ce15c625abcf4f6b173160124ef880aeb1fe3f8922178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb07d0a1c67220cf5e80417b476a42f6ebd083909935aebcc88121647cad5635`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:46:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ed6df39abc7d594f94814fc149a6d12ce8e09d24460ec736a00c100e19ffdf`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
		Size: 11.1 MB (11109727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec667baba589573605c133826701cab34d84f096e1e91fa94e543e149924f91`  
		Last Modified: Wed, 22 Apr 2026 01:46:36 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1013b0e0636c96189cadc6bf6decbba384ac6e9ed98ff455d06ba7bfec473993`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5cd02b66d7b76cdc68bc6d1df382e683332c7cb55b4e15f19e3d0dced161c`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
		Size: 101.3 KB (101300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:54754071df71e040c8597ffaf6d760fe6be1cf9654e900cb74e49b322c7ae893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa89b23b03758493f1a04f87e158c59b1ef50d412362639d02e2b68e3fcea16`

```dockerfile
```

-	Layers:
	-	`sha256:4b8233d3d9b8a4e9a9923daab5c738a9ffa0a8add3097ab0455b285fd73cbe69`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39277cbd5fc62794898776a591fe1fc0bbfa2a1d5de76eb732de8469593fc4a9`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
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
$ docker pull neurodebian@sha256:3dc7a628b242a023115b59d7ec0fd4b0c0589c8f2e51da14899222e96aa1d882
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
$ docker pull neurodebian@sha256:ca2c3a23602a03460ca26b9f213125634e94c388063a32a14688d65217d6c3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db056d8cdcb4e95f441e800e13433a568632cd36316df6cf34c253006e4be25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:46:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:31 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfe1d2cc6d2e7bb43dae058bb8276b894a2be14a9f73e20702e37ada7e1fe5`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
		Size: 11.1 MB (11109842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a075bb8e87576480a25c5a254e0d519391be348067703b2d5f943763193ce0f`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bcc8d253eed27b4d4602843d761fed0df2781539a674a8a4b9106c6202f4cc`  
		Last Modified: Wed, 22 Apr 2026 01:46:38 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd09e3648df09d52a3ca93bd4b09431847db6762c78313e0d77f1063016d0f3`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
		Size: 101.3 KB (101302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2a249bd2b04f947ebe8b42357abb8bce3037999ed2382683016710fd8dcf18`  
		Last Modified: Wed, 22 Apr 2026 01:46:40 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:05469b94da86816694db020fbd8796a52b653a4b98636d838ed60d6edd48cbfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a111a28248ce005acab8e2fb2b881d722ab556227fbf28e89fa03563e4cb04`

```dockerfile
```

-	Layers:
	-	`sha256:74493f42a5664f6e345502e4b4592a060225154f0b5838ef5859a70bee364bcd`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4988e12d16a4ed5dac599982e9ffc5fe713452e61fd0d82004c31417b642c1b`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
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
$ docker pull neurodebian@sha256:0908ce7bfe7844fe534fbfbac29b7cffddefaac8b38ac6c262e0e70f3d292fc8
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
$ docker pull neurodebian@sha256:d06ccae3091ed09a8ae30333c7d276a6f642aafeeea4cea11f1bf031b4aa8b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59891472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd5074a15112d8cb2d177b08b5612f8a663484471bc7bf9542a51de6a168be4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:47:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:52be3b7a34a0f7d63c36fadfd1767c3f064e11b65df7fb6243fae9b94dd9f7c8`  
		Last Modified: Wed, 22 Apr 2026 00:16:24 GMT  
		Size: 48.7 MB (48726104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5485dd8aae8841a38986344914e8b98a52d91c938dbe8e06504266358b9ed5`  
		Last Modified: Wed, 22 Apr 2026 01:47:33 GMT  
		Size: 11.1 MB (11072463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cb28ea7c83094bfd4f4e19ca20afb0f66baa1525e7f242a4af7d4cdcdb4ed2`  
		Last Modified: Wed, 22 Apr 2026 01:47:33 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f0df2aec93af1384f14378283b7b073434539e24e756480672cd428d371f97`  
		Last Modified: Wed, 22 Apr 2026 01:47:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5222ef705721057fd9cf72eedff3b7e61a8f8645eeb34b8112c7350e560898`  
		Last Modified: Wed, 22 Apr 2026 01:47:33 GMT  
		Size: 90.0 KB (90002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6439a53fe8de0e935de0b56b291a11189a00d3a3d01c944b1779f32cf43e2fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa83cfad910d7f4f7b799928454a588567004a0d875948f6c26d43152950f6b`

```dockerfile
```

-	Layers:
	-	`sha256:eb55cb3368691582e59603c7869d519e67958d0aeb5d2e42b56393c6cf02ff5c`  
		Last Modified: Wed, 22 Apr 2026 01:47:33 GMT  
		Size: 3.6 MB (3559144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178f86fc886586b6be1b389b1fa01a8f02baab0623c5e079f0440a51de06d381`  
		Last Modified: Wed, 22 Apr 2026 01:47:33 GMT  
		Size: 14.1 KB (14056 bytes)  
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
$ docker pull neurodebian@sha256:e6908126761b3e7196115ddc87b46c2201308e7209a3042b704da61cad043f55
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
$ docker pull neurodebian@sha256:6d7a6edd87813c48d375346b592699af2955f0f278cc312604805857a95aaebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59891975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6831f1fbeaf0cdcee9d00103c5ca7c213f3866eb8319ba76e6c877144ba19992`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:47:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:15 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:52be3b7a34a0f7d63c36fadfd1767c3f064e11b65df7fb6243fae9b94dd9f7c8`  
		Last Modified: Wed, 22 Apr 2026 00:16:24 GMT  
		Size: 48.7 MB (48726104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f336c7b8d6a171e1ba01081442a12e792d77a568986ba209c9900dc791b5f51f`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 11.1 MB (11072548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00987222f36f6f8bd0a2550c59b0ac95c7b6366478f8fa574c9754958fec4b1`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cecec54a68e2d16c3c71a28eb7f95b5f390342c41b54d106a429ca35828ae6`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97bcdd63d58b53bdbd95358360b21a312367b268e808cf231e17a615bfe6eca`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 90.0 KB (89970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39283d2169655980d2ce8369af2c8c0e93a2ed385dfc17ac3345ab676898f2d`  
		Last Modified: Wed, 22 Apr 2026 01:47:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dab52e5226ca2bb1cbc353608b25cb665bb16d5385cbd9355942017c10ff6179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd717cc30fe1dc636877e07191efea9e7480004ed7907ce36643e559442da151`

```dockerfile
```

-	Layers:
	-	`sha256:a6bff3b434305a1949b393a3635d16e90e881bf3f7560f921253f54deb69275a`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 3.6 MB (3559180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a68a912c8c8374f021c1329e9fd2bafb5b9d9b174b468cd2f78e3f36e7d2c68`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
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
$ docker pull neurodebian@sha256:ba03f986f1681966bb6cc4ee7bab72c51cf598ce0494a31f8004a1d9af0d12b0
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
$ docker pull neurodebian@sha256:ddf98df98490a30e6516a88dad74c9080b4990b9c2dd7229976aa41fda2cf9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc0c31d568d638d16c30d49ab66bc22d6d5318f4d29fab71407e077e2360bff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:46:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:52 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fae4052bd9a699325323ae792a2e30b9fc72c278dc25917c9a9ff7e234d140`  
		Last Modified: Wed, 22 Apr 2026 01:47:04 GMT  
		Size: 10.1 MB (10077915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76798e07400dd767757ec8dfe9435d779d3f31d5250cea5c5ad5936cc22812c5`  
		Last Modified: Wed, 22 Apr 2026 01:47:03 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70054b902610f6938eb7928791800e9f2a039a25c54d2b3449c512416a689ec8`  
		Last Modified: Wed, 22 Apr 2026 01:47:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d86588e7392a3239165cbb6907456cd15e84c7f32816dfd781734bcee8f9bfc`  
		Last Modified: Wed, 22 Apr 2026 01:47:04 GMT  
		Size: 91.1 KB (91052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d5a814179fb90e34c30b10b430d6b39cf91995c4f927cd8fe9679ec12e6c445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d2f2dcfdf8aea1dd796ecf4aacf7f4a89d722ff014f142a470e282cdfd4e8b`

```dockerfile
```

-	Layers:
	-	`sha256:514f95074e01661cf09b5572aab47cebcbdb61047d81b284eb99088d73f4115d`  
		Last Modified: Wed, 22 Apr 2026 01:47:04 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:743fb056862ffb3e08c1e28962e2a9df02acf23fe830e5d5d5920c9dd786117f`  
		Last Modified: Wed, 22 Apr 2026 01:47:03 GMT  
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
$ docker pull neurodebian@sha256:d767f4c150fac95b8d78241bea39205c24160bfa465b6a45b00d197da0379306
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
$ docker pull neurodebian@sha256:0abd855e4cff87a36e4ebb8f40dd8654974639604b5b088d0fdc0dc03594cc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59878213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d58153bb476604bc2d7ad9631aa75339f5babe9720a507535e9efd3ed33ba69`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:47:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f7ead27882db0d1de6eb6e496d384f406d278f217abdf3e3c50a235ce7737146`  
		Last Modified: Wed, 22 Apr 2026 00:16:20 GMT  
		Size: 48.7 MB (48711371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c29ad565b922827657ac0f33a186ce40a940510fda76beb2d874d1d5b7030b`  
		Last Modified: Wed, 22 Apr 2026 01:47:31 GMT  
		Size: 11.1 MB (11073925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511be1a46ff384a862d72da9d2e226e22fe4006d712de763a4d58c7ef0495a`  
		Last Modified: Wed, 22 Apr 2026 01:47:30 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e85e5c905988a736f792021239cbf29a8923446a7b545160bb4951fa705bc6`  
		Last Modified: Wed, 22 Apr 2026 01:47:30 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d36acdff774458323d42437f75ecd32b46defc5c8138e7523766659b6add11`  
		Last Modified: Wed, 22 Apr 2026 01:47:30 GMT  
		Size: 90.0 KB (90013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:803f87020fee5bfd46a8f93d177b3e8185c32d355677bc1398a8f19ee75bb438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fad5403d40e355b0bdd69b6359195e04117ce9736be23c09e479169d238a54`

```dockerfile
```

-	Layers:
	-	`sha256:b14618e60abc7a7b62b9ae414e94d2e7ac1773cf504b8d3d5c3393cb4e59f7be`  
		Last Modified: Wed, 22 Apr 2026 01:47:31 GMT  
		Size: 3.6 MB (3559939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ada421d2dae55a1bba91151296ca8a6dcc4778247e367b54f5b9d54c99244784`  
		Last Modified: Wed, 22 Apr 2026 01:47:30 GMT  
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
$ docker pull neurodebian@sha256:d67dccd75d860b0cdc67165977678f763ee747fcbd7b04983fb3beea172bafbd
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
$ docker pull neurodebian@sha256:0438bccc7ba65c13d3e3e327154a9cd2374115c4704d3e8795269d86f0646c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59878527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4279b4d5fa39340181ad15329fe13cfe79cdfeaf7cff6f3cf4bbe2316dba283`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:47:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:23 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f7ead27882db0d1de6eb6e496d384f406d278f217abdf3e3c50a235ce7737146`  
		Last Modified: Wed, 22 Apr 2026 00:16:20 GMT  
		Size: 48.7 MB (48711371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290faf0d8556a0354ef08cc6b2ab575395ed75f67c1fb090833e5a9dcb73ebb5`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 11.1 MB (11073827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e113876b36cb35bc3449e3275bf2325cf4d135babc8a1eb1aeafb7093ac0fb22`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581a7489b1678da413f412188af43e189558ed028dba4cde7a97bd3748d481e2`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c9798ad62fe6e6987e01644fb45b9578749649d945ee49beaa1fe156eb09f0`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 90.0 KB (90011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b35ed8b319973962555182b86ee9acb8b47387a161933e48da8776e73065a`  
		Last Modified: Wed, 22 Apr 2026 01:47:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:230277e93b0c55a22f41fe71935f996eb01a41c1741dce3dae8e733a5772a7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde88c881e8e8378e262971e9b4d87678721d7d7c3a1849eef8a074db3155bd3`

```dockerfile
```

-	Layers:
	-	`sha256:5b9eb37b3235558f1c7819837058313695015c6375ebae6365c41d032bf4e805`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 3.6 MB (3559975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dedededbb1a459db24d72e128f27c8cdad198b22174403162acfab4a6716378`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
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
$ docker pull neurodebian@sha256:65376b9f385d5024af64d90ed8fdc5995507303dbf6fa4899bb756637188e5f4
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
$ docker pull neurodebian@sha256:1506b5eb3c91ddfabe3ce15c625abcf4f6b173160124ef880aeb1fe3f8922178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb07d0a1c67220cf5e80417b476a42f6ebd083909935aebcc88121647cad5635`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:46:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ed6df39abc7d594f94814fc149a6d12ce8e09d24460ec736a00c100e19ffdf`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
		Size: 11.1 MB (11109727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec667baba589573605c133826701cab34d84f096e1e91fa94e543e149924f91`  
		Last Modified: Wed, 22 Apr 2026 01:46:36 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1013b0e0636c96189cadc6bf6decbba384ac6e9ed98ff455d06ba7bfec473993`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5cd02b66d7b76cdc68bc6d1df382e683332c7cb55b4e15f19e3d0dced161c`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
		Size: 101.3 KB (101300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:54754071df71e040c8597ffaf6d760fe6be1cf9654e900cb74e49b322c7ae893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa89b23b03758493f1a04f87e158c59b1ef50d412362639d02e2b68e3fcea16`

```dockerfile
```

-	Layers:
	-	`sha256:4b8233d3d9b8a4e9a9923daab5c738a9ffa0a8add3097ab0455b285fd73cbe69`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39277cbd5fc62794898776a591fe1fc0bbfa2a1d5de76eb732de8469593fc4a9`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
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
$ docker pull neurodebian@sha256:3dc7a628b242a023115b59d7ec0fd4b0c0589c8f2e51da14899222e96aa1d882
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
$ docker pull neurodebian@sha256:ca2c3a23602a03460ca26b9f213125634e94c388063a32a14688d65217d6c3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db056d8cdcb4e95f441e800e13433a568632cd36316df6cf34c253006e4be25`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:46:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:31 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbfe1d2cc6d2e7bb43dae058bb8276b894a2be14a9f73e20702e37ada7e1fe5`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
		Size: 11.1 MB (11109842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a075bb8e87576480a25c5a254e0d519391be348067703b2d5f943763193ce0f`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bcc8d253eed27b4d4602843d761fed0df2781539a674a8a4b9106c6202f4cc`  
		Last Modified: Wed, 22 Apr 2026 01:46:38 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd09e3648df09d52a3ca93bd4b09431847db6762c78313e0d77f1063016d0f3`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
		Size: 101.3 KB (101302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2a249bd2b04f947ebe8b42357abb8bce3037999ed2382683016710fd8dcf18`  
		Last Modified: Wed, 22 Apr 2026 01:46:40 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:05469b94da86816694db020fbd8796a52b653a4b98636d838ed60d6edd48cbfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a111a28248ce005acab8e2fb2b881d722ab556227fbf28e89fa03563e4cb04`

```dockerfile
```

-	Layers:
	-	`sha256:74493f42a5664f6e345502e4b4592a060225154f0b5838ef5859a70bee364bcd`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4988e12d16a4ed5dac599982e9ffc5fe713452e61fd0d82004c31417b642c1b`  
		Last Modified: Wed, 22 Apr 2026 01:46:39 GMT  
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
$ docker pull neurodebian@sha256:702369457ba4f0a5e4669e6f26acfee0481973db03ad714e8dc1b08a36d413b7
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
$ docker pull neurodebian@sha256:365aa70bf498507787226c0d7383899d14db803ab0479cbec5dbc5c437049343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fadee2b2da5a6b02cd5d771d3c878b932b1dd725b747cee3d373dcf02b04cfc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:46:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8e0c4933455fc6e8436ccd1a3948e1690ff31ee75a4c911e36f195c9e8ba5`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 11.3 MB (11252926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96ccf4228f5ededbca88454df53e0a2102eaf263c1b2794174d6967279692ac`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334f3723ee4775a37b78eb03aa81e5997c3c1e0db8d9d64523a3babf5325980`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e236fb00fbfc3fa19ecca63a96047f5a436ab74240aa466a134a6de56e34f7`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 93.6 KB (93553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2c1f9b95d357e099089706379fe9045341634f3133a97550f62641ab5d1aa96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f564316b6416d5d9f5dd0db415fc439cc4879223077fb341bfcb0808ad3b201b`

```dockerfile
```

-	Layers:
	-	`sha256:f3deeaa1aae3fbcda8209dc59d5ec673ec7afe15fe63313fbed4af3b95c50871`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0dfe5345e8d635cac1bfdec83428fbb591c72ba7827803b3fed0136575d8ed`  
		Last Modified: Wed, 22 Apr 2026 01:46:43 GMT  
		Size: 14.1 KB (14090 bytes)  
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
$ docker pull neurodebian@sha256:68087a05a6a7fb01e26f490193b166ef26f3b943d68e912500b8b5a34622fb73
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
$ docker pull neurodebian@sha256:9d1120aaac014085ce56a331d7ea575340d210fa6cf6bb93d8dd48b01bde2707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4aa0f2d93ab5a0ef749e44b75fe66d1d98716e61a59f33ec6b37262e1eaf99b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:46:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:49 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1419a29641a382bd5d008c79413b7a0d7f982afcc54d158356ebf834d777985f`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 11.3 MB (11252881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c3250ae94100eccecd5ddde9d4ffa62ee2b825e07429f002e2df72bb84619`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6291e28edd6e8f08470374ec8879c087c0fb691bf9c8dcec73c4a7d89a442520`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7511dcf0a8a93bc3c8c53587e7a674accd45ee7dc685cc3c31336ef424251476`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 93.5 KB (93514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89100960aea92e7ee71badc7ca255d4f2c6989d01f183b99c05d15a3f884e142`  
		Last Modified: Wed, 22 Apr 2026 01:47:00 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:65027bce3976a61075bd0f1ac2612aaebeb740f1f6f36c9db5340623ae6d2736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be843c3b23cb464a4fb68f900a751c67e0bddb7d266bee20b02a577d9d7f918f`

```dockerfile
```

-	Layers:
	-	`sha256:6ee6b5b3e6a0e40998662f831430bde4d01243d416c3eaba5e287204740ac7e7`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca90bb44921d010c885d204cb6665ada1449816de5bd1a1732874889f0de829`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 16.1 KB (16131 bytes)  
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
$ docker pull neurodebian@sha256:ba03f986f1681966bb6cc4ee7bab72c51cf598ce0494a31f8004a1d9af0d12b0
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
$ docker pull neurodebian@sha256:ddf98df98490a30e6516a88dad74c9080b4990b9c2dd7229976aa41fda2cf9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc0c31d568d638d16c30d49ab66bc22d6d5318f4d29fab71407e077e2360bff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:46:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:52 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fae4052bd9a699325323ae792a2e30b9fc72c278dc25917c9a9ff7e234d140`  
		Last Modified: Wed, 22 Apr 2026 01:47:04 GMT  
		Size: 10.1 MB (10077915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76798e07400dd767757ec8dfe9435d779d3f31d5250cea5c5ad5936cc22812c5`  
		Last Modified: Wed, 22 Apr 2026 01:47:03 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70054b902610f6938eb7928791800e9f2a039a25c54d2b3449c512416a689ec8`  
		Last Modified: Wed, 22 Apr 2026 01:47:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d86588e7392a3239165cbb6907456cd15e84c7f32816dfd781734bcee8f9bfc`  
		Last Modified: Wed, 22 Apr 2026 01:47:04 GMT  
		Size: 91.1 KB (91052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d5a814179fb90e34c30b10b430d6b39cf91995c4f927cd8fe9679ec12e6c445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d2f2dcfdf8aea1dd796ecf4aacf7f4a89d722ff014f142a470e282cdfd4e8b`

```dockerfile
```

-	Layers:
	-	`sha256:514f95074e01661cf09b5572aab47cebcbdb61047d81b284eb99088d73f4115d`  
		Last Modified: Wed, 22 Apr 2026 01:47:04 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:743fb056862ffb3e08c1e28962e2a9df02acf23fe830e5d5d5920c9dd786117f`  
		Last Modified: Wed, 22 Apr 2026 01:47:03 GMT  
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
$ docker pull neurodebian@sha256:ad5d2f61f3d1f525eb2ee043f6d38c9b96c53609053c5cd507f12605a6ae2842
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
$ docker pull neurodebian@sha256:35db093e893965b321e500a19b13a08c38a98bcfaf8db74afe317dc124424ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da558016f9205e93d34f32a5166ec7a06437d03877e34aed408c149e9c648447`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:47:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f90c124219ac63e6ca4182bdd4c2653b8a17b51c1dd6073dde0a04bf307be04`  
		Last Modified: Wed, 22 Apr 2026 01:47:16 GMT  
		Size: 10.1 MB (10077914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1badf29e5c2a597ddcf7fe324b32372733daf9ce51497be05ed4833df0c06c54`  
		Last Modified: Wed, 22 Apr 2026 01:47:15 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b631d97fbb3447b3bbd187358e3ce04dea463d731b5818c0062d00ce19228d`  
		Last Modified: Wed, 22 Apr 2026 01:47:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81846552464d05a25ecc2d01db73c8a4e651cd8b376be38e41b0287424eb94a`  
		Last Modified: Wed, 22 Apr 2026 01:47:16 GMT  
		Size: 91.0 KB (91039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a509f25023663972466eb8dffac4e4e60e13b981133ebf160c139a5226e028d7`  
		Last Modified: Wed, 22 Apr 2026 01:47:17 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46939ff2dbb3a1a312a9003767f0e2df16f89ae836d55df7ab343a91fc10e8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0639fa8d8a99a339cbf4d9ddb582d1cfbc8b93a7022a2f46a1978a07107139ca`

```dockerfile
```

-	Layers:
	-	`sha256:bd5a0786c67374fa94b8e30d4388ae2e54aa952bb44142350845406a5f747a8a`  
		Last Modified: Wed, 22 Apr 2026 01:47:16 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d186259dd51b62f91d02172d0bcc0145d8ad61c07476353b8452e0a312195f`  
		Last Modified: Wed, 22 Apr 2026 01:47:16 GMT  
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
$ docker pull neurodebian@sha256:0908ce7bfe7844fe534fbfbac29b7cffddefaac8b38ac6c262e0e70f3d292fc8
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
$ docker pull neurodebian@sha256:d06ccae3091ed09a8ae30333c7d276a6f642aafeeea4cea11f1bf031b4aa8b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59891472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd5074a15112d8cb2d177b08b5612f8a663484471bc7bf9542a51de6a168be4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:47:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:52be3b7a34a0f7d63c36fadfd1767c3f064e11b65df7fb6243fae9b94dd9f7c8`  
		Last Modified: Wed, 22 Apr 2026 00:16:24 GMT  
		Size: 48.7 MB (48726104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5485dd8aae8841a38986344914e8b98a52d91c938dbe8e06504266358b9ed5`  
		Last Modified: Wed, 22 Apr 2026 01:47:33 GMT  
		Size: 11.1 MB (11072463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4cb28ea7c83094bfd4f4e19ca20afb0f66baa1525e7f242a4af7d4cdcdb4ed2`  
		Last Modified: Wed, 22 Apr 2026 01:47:33 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f0df2aec93af1384f14378283b7b073434539e24e756480672cd428d371f97`  
		Last Modified: Wed, 22 Apr 2026 01:47:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5222ef705721057fd9cf72eedff3b7e61a8f8645eeb34b8112c7350e560898`  
		Last Modified: Wed, 22 Apr 2026 01:47:33 GMT  
		Size: 90.0 KB (90002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6439a53fe8de0e935de0b56b291a11189a00d3a3d01c944b1779f32cf43e2fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa83cfad910d7f4f7b799928454a588567004a0d875948f6c26d43152950f6b`

```dockerfile
```

-	Layers:
	-	`sha256:eb55cb3368691582e59603c7869d519e67958d0aeb5d2e42b56393c6cf02ff5c`  
		Last Modified: Wed, 22 Apr 2026 01:47:33 GMT  
		Size: 3.6 MB (3559144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178f86fc886586b6be1b389b1fa01a8f02baab0623c5e079f0440a51de06d381`  
		Last Modified: Wed, 22 Apr 2026 01:47:33 GMT  
		Size: 14.1 KB (14056 bytes)  
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
$ docker pull neurodebian@sha256:e6908126761b3e7196115ddc87b46c2201308e7209a3042b704da61cad043f55
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
$ docker pull neurodebian@sha256:6d7a6edd87813c48d375346b592699af2955f0f278cc312604805857a95aaebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59891975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6831f1fbeaf0cdcee9d00103c5ca7c213f3866eb8319ba76e6c877144ba19992`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:47:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:15 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:52be3b7a34a0f7d63c36fadfd1767c3f064e11b65df7fb6243fae9b94dd9f7c8`  
		Last Modified: Wed, 22 Apr 2026 00:16:24 GMT  
		Size: 48.7 MB (48726104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f336c7b8d6a171e1ba01081442a12e792d77a568986ba209c9900dc791b5f51f`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 11.1 MB (11072548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00987222f36f6f8bd0a2550c59b0ac95c7b6366478f8fa574c9754958fec4b1`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cecec54a68e2d16c3c71a28eb7f95b5f390342c41b54d106a429ca35828ae6`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97bcdd63d58b53bdbd95358360b21a312367b268e808cf231e17a615bfe6eca`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 90.0 KB (89970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39283d2169655980d2ce8369af2c8c0e93a2ed385dfc17ac3345ab676898f2d`  
		Last Modified: Wed, 22 Apr 2026 01:47:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dab52e5226ca2bb1cbc353608b25cb665bb16d5385cbd9355942017c10ff6179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd717cc30fe1dc636877e07191efea9e7480004ed7907ce36643e559442da151`

```dockerfile
```

-	Layers:
	-	`sha256:a6bff3b434305a1949b393a3635d16e90e881bf3f7560f921253f54deb69275a`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
		Size: 3.6 MB (3559180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a68a912c8c8374f021c1329e9fd2bafb5b9d9b174b468cd2f78e3f36e7d2c68`  
		Last Modified: Wed, 22 Apr 2026 01:47:26 GMT  
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
$ docker pull neurodebian@sha256:ad5d2f61f3d1f525eb2ee043f6d38c9b96c53609053c5cd507f12605a6ae2842
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
$ docker pull neurodebian@sha256:35db093e893965b321e500a19b13a08c38a98bcfaf8db74afe317dc124424ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da558016f9205e93d34f32a5166ec7a06437d03877e34aed408c149e9c648447`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:47:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f90c124219ac63e6ca4182bdd4c2653b8a17b51c1dd6073dde0a04bf307be04`  
		Last Modified: Wed, 22 Apr 2026 01:47:16 GMT  
		Size: 10.1 MB (10077914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1badf29e5c2a597ddcf7fe324b32372733daf9ce51497be05ed4833df0c06c54`  
		Last Modified: Wed, 22 Apr 2026 01:47:15 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b631d97fbb3447b3bbd187358e3ce04dea463d731b5818c0062d00ce19228d`  
		Last Modified: Wed, 22 Apr 2026 01:47:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81846552464d05a25ecc2d01db73c8a4e651cd8b376be38e41b0287424eb94a`  
		Last Modified: Wed, 22 Apr 2026 01:47:16 GMT  
		Size: 91.0 KB (91039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a509f25023663972466eb8dffac4e4e60e13b981133ebf160c139a5226e028d7`  
		Last Modified: Wed, 22 Apr 2026 01:47:17 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46939ff2dbb3a1a312a9003767f0e2df16f89ae836d55df7ab343a91fc10e8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0639fa8d8a99a339cbf4d9ddb582d1cfbc8b93a7022a2f46a1978a07107139ca`

```dockerfile
```

-	Layers:
	-	`sha256:bd5a0786c67374fa94b8e30d4388ae2e54aa952bb44142350845406a5f747a8a`  
		Last Modified: Wed, 22 Apr 2026 01:47:16 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d186259dd51b62f91d02172d0bcc0145d8ad61c07476353b8452e0a312195f`  
		Last Modified: Wed, 22 Apr 2026 01:47:16 GMT  
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
$ docker pull neurodebian@sha256:d767f4c150fac95b8d78241bea39205c24160bfa465b6a45b00d197da0379306
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
$ docker pull neurodebian@sha256:0abd855e4cff87a36e4ebb8f40dd8654974639604b5b088d0fdc0dc03594cc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59878213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d58153bb476604bc2d7ad9631aa75339f5babe9720a507535e9efd3ed33ba69`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:47:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f7ead27882db0d1de6eb6e496d384f406d278f217abdf3e3c50a235ce7737146`  
		Last Modified: Wed, 22 Apr 2026 00:16:20 GMT  
		Size: 48.7 MB (48711371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c29ad565b922827657ac0f33a186ce40a940510fda76beb2d874d1d5b7030b`  
		Last Modified: Wed, 22 Apr 2026 01:47:31 GMT  
		Size: 11.1 MB (11073925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511be1a46ff384a862d72da9d2e226e22fe4006d712de763a4d58c7ef0495a`  
		Last Modified: Wed, 22 Apr 2026 01:47:30 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e85e5c905988a736f792021239cbf29a8923446a7b545160bb4951fa705bc6`  
		Last Modified: Wed, 22 Apr 2026 01:47:30 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d36acdff774458323d42437f75ecd32b46defc5c8138e7523766659b6add11`  
		Last Modified: Wed, 22 Apr 2026 01:47:30 GMT  
		Size: 90.0 KB (90013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:803f87020fee5bfd46a8f93d177b3e8185c32d355677bc1398a8f19ee75bb438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fad5403d40e355b0bdd69b6359195e04117ce9736be23c09e479169d238a54`

```dockerfile
```

-	Layers:
	-	`sha256:b14618e60abc7a7b62b9ae414e94d2e7ac1773cf504b8d3d5c3393cb4e59f7be`  
		Last Modified: Wed, 22 Apr 2026 01:47:31 GMT  
		Size: 3.6 MB (3559939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ada421d2dae55a1bba91151296ca8a6dcc4778247e367b54f5b9d54c99244784`  
		Last Modified: Wed, 22 Apr 2026 01:47:30 GMT  
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
$ docker pull neurodebian@sha256:d67dccd75d860b0cdc67165977678f763ee747fcbd7b04983fb3beea172bafbd
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
$ docker pull neurodebian@sha256:0438bccc7ba65c13d3e3e327154a9cd2374115c4704d3e8795269d86f0646c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59878527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4279b4d5fa39340181ad15329fe13cfe79cdfeaf7cff6f3cf4bbe2316dba283`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:47:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:23 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f7ead27882db0d1de6eb6e496d384f406d278f217abdf3e3c50a235ce7737146`  
		Last Modified: Wed, 22 Apr 2026 00:16:20 GMT  
		Size: 48.7 MB (48711371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290faf0d8556a0354ef08cc6b2ab575395ed75f67c1fb090833e5a9dcb73ebb5`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 11.1 MB (11073827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e113876b36cb35bc3449e3275bf2325cf4d135babc8a1eb1aeafb7093ac0fb22`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581a7489b1678da413f412188af43e189558ed028dba4cde7a97bd3748d481e2`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c9798ad62fe6e6987e01644fb45b9578749649d945ee49beaa1fe156eb09f0`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 90.0 KB (90011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b35ed8b319973962555182b86ee9acb8b47387a161933e48da8776e73065a`  
		Last Modified: Wed, 22 Apr 2026 01:47:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:230277e93b0c55a22f41fe71935f996eb01a41c1741dce3dae8e733a5772a7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde88c881e8e8378e262971e9b4d87678721d7d7c3a1849eef8a074db3155bd3`

```dockerfile
```

-	Layers:
	-	`sha256:5b9eb37b3235558f1c7819837058313695015c6375ebae6365c41d032bf4e805`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 3.6 MB (3559975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dedededbb1a459db24d72e128f27c8cdad198b22174403162acfab4a6716378`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
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
$ docker pull neurodebian@sha256:ba03f986f1681966bb6cc4ee7bab72c51cf598ce0494a31f8004a1d9af0d12b0
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
$ docker pull neurodebian@sha256:ddf98df98490a30e6516a88dad74c9080b4990b9c2dd7229976aa41fda2cf9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc0c31d568d638d16c30d49ab66bc22d6d5318f4d29fab71407e077e2360bff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:46:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:52 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fae4052bd9a699325323ae792a2e30b9fc72c278dc25917c9a9ff7e234d140`  
		Last Modified: Wed, 22 Apr 2026 01:47:04 GMT  
		Size: 10.1 MB (10077915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76798e07400dd767757ec8dfe9435d779d3f31d5250cea5c5ad5936cc22812c5`  
		Last Modified: Wed, 22 Apr 2026 01:47:03 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70054b902610f6938eb7928791800e9f2a039a25c54d2b3449c512416a689ec8`  
		Last Modified: Wed, 22 Apr 2026 01:47:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d86588e7392a3239165cbb6907456cd15e84c7f32816dfd781734bcee8f9bfc`  
		Last Modified: Wed, 22 Apr 2026 01:47:04 GMT  
		Size: 91.1 KB (91052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d5a814179fb90e34c30b10b430d6b39cf91995c4f927cd8fe9679ec12e6c445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d2f2dcfdf8aea1dd796ecf4aacf7f4a89d722ff014f142a470e282cdfd4e8b`

```dockerfile
```

-	Layers:
	-	`sha256:514f95074e01661cf09b5572aab47cebcbdb61047d81b284eb99088d73f4115d`  
		Last Modified: Wed, 22 Apr 2026 01:47:04 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:743fb056862ffb3e08c1e28962e2a9df02acf23fe830e5d5d5920c9dd786117f`  
		Last Modified: Wed, 22 Apr 2026 01:47:03 GMT  
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
$ docker pull neurodebian@sha256:ad5d2f61f3d1f525eb2ee043f6d38c9b96c53609053c5cd507f12605a6ae2842
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
$ docker pull neurodebian@sha256:35db093e893965b321e500a19b13a08c38a98bcfaf8db74afe317dc124424ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da558016f9205e93d34f32a5166ec7a06437d03877e34aed408c149e9c648447`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:47:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:08 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f90c124219ac63e6ca4182bdd4c2653b8a17b51c1dd6073dde0a04bf307be04`  
		Last Modified: Wed, 22 Apr 2026 01:47:16 GMT  
		Size: 10.1 MB (10077914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1badf29e5c2a597ddcf7fe324b32372733daf9ce51497be05ed4833df0c06c54`  
		Last Modified: Wed, 22 Apr 2026 01:47:15 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b631d97fbb3447b3bbd187358e3ce04dea463d731b5818c0062d00ce19228d`  
		Last Modified: Wed, 22 Apr 2026 01:47:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81846552464d05a25ecc2d01db73c8a4e651cd8b376be38e41b0287424eb94a`  
		Last Modified: Wed, 22 Apr 2026 01:47:16 GMT  
		Size: 91.0 KB (91039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a509f25023663972466eb8dffac4e4e60e13b981133ebf160c139a5226e028d7`  
		Last Modified: Wed, 22 Apr 2026 01:47:17 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46939ff2dbb3a1a312a9003767f0e2df16f89ae836d55df7ab343a91fc10e8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0639fa8d8a99a339cbf4d9ddb582d1cfbc8b93a7022a2f46a1978a07107139ca`

```dockerfile
```

-	Layers:
	-	`sha256:bd5a0786c67374fa94b8e30d4388ae2e54aa952bb44142350845406a5f747a8a`  
		Last Modified: Wed, 22 Apr 2026 01:47:16 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d186259dd51b62f91d02172d0bcc0145d8ad61c07476353b8452e0a312195f`  
		Last Modified: Wed, 22 Apr 2026 01:47:16 GMT  
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
