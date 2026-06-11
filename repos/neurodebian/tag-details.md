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
$ docker pull neurodebian@sha256:89a4466817847379c1cf72eb498339e79eaa7e8ac5d55cf358d0bc3b97b34d1d
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
$ docker pull neurodebian@sha256:8ab30383b3edb838a10b6bb2d7ae90a5f99ec6535024f27a4d2a864a430e3933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59871032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c10bd53e758eb76947bdac99b308a015e38d901b5f882ec63566e81f70c18a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5823007860ad5138e7ab5fdc785a41af7cc872ba69852060b4b1eac4ee55c4f5`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 11.3 MB (11273427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60650ff41dd99d0a7b13a2ca9ba9a13d360e3d5678fd4db87281bc0b756a7cd`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c243edd52bbca60408e5285aac5d978e1405eb4c3a37e2efb89680cb9f4b5af`  
		Last Modified: Thu, 11 Jun 2026 00:46:00 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922168382be72127bd6f11f9ad8b17c7432d028cd28ad15cc368d27050c00d8c`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 93.4 KB (93392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:675f2564cb071be958213e88bb135d7187dd1f2de73beb2b7cfede23c24de338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9978cc983011da1d93277693b1cbe3b5d2f8c94012907ef6558c00a5bac2daa`

```dockerfile
```

-	Layers:
	-	`sha256:4e384ce82895a9419db3e268a63878b228bb5e07568ab6082bcb301b02ed9a86`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e7dd3355c262265ee0b8187c68369282e3afb3ad1413958381f842df9b0f3c`  
		Last Modified: Thu, 11 Jun 2026 00:46:00 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:47123181987e52ef981cfc5f7d75a17df2009656b0dfd20321f52e5dbf6adbd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59737697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0432667e276c1f96a58ad559d013ee8547e585ee6ac984de02db5e06dd8b04e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:47:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a735ebda1e0cf248011c01a7676af282efac17cec145ba6e198c0ead226a04a8`  
		Last Modified: Thu, 11 Jun 2026 00:47:31 GMT  
		Size: 11.3 MB (11252911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3cd29dcf4276f3390bb7c591a4b35e0db081a8ba88fc8ba2e0c2c37ef3ac4d`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d3622219a2a21ed6e957b57d9177dc02dd5859ffea8adae6dbdb315b7b5545`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae554063421f6d5273c9bf4d90ff55c337368094d308c785ff3ecc37f680628`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 93.6 KB (93602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:032fe2cae497ecb4e1bf5c8fdae524790d8b0fae9a6992eac2fa672eb10c14c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fbc693151be7e6a990a99eb3f13a04f175a8958f517585bfe910b2816f799d`

```dockerfile
```

-	Layers:
	-	`sha256:0ce295b9ec41e4b2923bfabf2680b01575c86088cb8d940538e8990c1d24ee2a`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbbff94d7b81988058a9e96b4d083f4b6c305bf5f90a75982d002aa3c6a0b2ca`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:af82dfbac2ace1c12de220644198bca9fa60d14ae4030ec0ea0ee6820773708f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61279895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9023421816137e807cba98c35b5e49c6833ade9d8d1166cd0493359a13b00a0d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:08773a2e9b0fe592ef47b4e93c883d32a351ff89ea9cd33f1ad47abd4081b4ca`  
		Last Modified: Wed, 10 Jun 2026 23:39:44 GMT  
		Size: 49.5 MB (49491206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb1065defaf3cd332a8079a5865ad7223b8ff7972245037bd5380e7e8cdf00a`  
		Last Modified: Thu, 11 Jun 2026 00:45:56 GMT  
		Size: 11.7 MB (11693094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34b8aaa341edc9665c3c824c40ca2c6224c1ad6c75d4589f7c23d5484caac27`  
		Last Modified: Thu, 11 Jun 2026 00:45:56 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae62d2e3ac929f0770447d245feeb45696a6a615f08f56e8419b6eed5742593`  
		Last Modified: Thu, 11 Jun 2026 00:45:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40664b1013e9fcb14bd829208b53e052b428c71092da56d56c717c19aabfb03c`  
		Last Modified: Thu, 11 Jun 2026 00:45:56 GMT  
		Size: 93.4 KB (93422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:34307a842c8422da5331720c0ed84c4ff0eec84331daaebf85c8a521b0b48d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1353e56e5b05e076badc6692d815901c99204d8cd59ad56691146d4079855b`

```dockerfile
```

-	Layers:
	-	`sha256:ee2bdc57053bac6e88e164b84fdb6e7fe81f75f5b061890443395b7765376a29`  
		Last Modified: Thu, 11 Jun 2026 00:45:56 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f965de7b88a579f2e41cee3af9b50bb79e6b36b928855a3d984fec4dfd937c2`  
		Last Modified: Thu, 11 Jun 2026 00:45:56 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:66a48b7ccd20aecc1e9c9e01ebfdab2ea7295615de73b51bcf9d8ed7309f87cd
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
$ docker pull neurodebian@sha256:cb08d6507f123ee954428276008e9c83d04d678754198d693e50c143cd0b54c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59871456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b85951aa7d121d082ba9654faa3848cc4d7abf9356e2b05af37bf3798ee4a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316bf023637e8f75e24e3831fc88deec444a7edd9790e0f9f3402d9b29c326f`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 11.3 MB (11273410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c8c4f5224dcc00c21540e9ea367e0aa62a4761dce0b1fb4bb55e9ea5b3cdd8`  
		Last Modified: Thu, 11 Jun 2026 00:46:13 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6638a85f4456b72d34de42e7458e7601f3aaa7cb32e4f085f5d08630aeadca8`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5858bb9b664153533d17afecd315d9a495a8a206b90c5efb794f7c4092c1ffc9`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 93.4 KB (93384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38110510a4edc98696657cec2c2800964ccfc836ec056480be42cca91b0590df`  
		Last Modified: Thu, 11 Jun 2026 00:46:15 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef56c80fa9e728c7024ac666c2bf5202d16a781191412562676f1d6f20996382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24b93a1caca4355cbd5126916038afee65708be0cc9931b6318251c3a3be743`

```dockerfile
```

-	Layers:
	-	`sha256:9ef2dc0010e4906a38178c6a2967e978008ea697bdedf904b98653f49cfe61f4`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 4.1 MB (4075951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7730b62570a8ef5981814ef338e673077fa401a6a2344f13053e1964058ca884`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:790fdbd7c2371eb8b5a4027250b8a4b74df108263ee34284598e48689aa3d001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59737987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4997f84d1e861b3e56a7fcb35962903ed6088d800caf72b7705c80a7d0b9c2ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:47:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152f2e93026566c42f24a52213782e990addaef08acafed5aba4a4f0e9fba3d0`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 11.3 MB (11252819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5448acce891289851311b76fb4d92d758cda828f3c1df7f4e8055522e44a35a`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84827aab7e6cfbbe8fb22eb54023ada3db2c55f6c590f10460f04331d83a4b14`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fe5708fd6c1d49b9eb0bb8f71f6d6a7ce682aebe87de418fead20b403f39c6`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 93.5 KB (93528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40247c8de7fd661db84c3da66fac073f9af9b4e5ec60d78e06137a39f9bbb31a`  
		Last Modified: Thu, 11 Jun 2026 00:47:52 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c65b1c9f2a93cd41d6d12d3d078c3331d4a1300f4a3fc845c881942a25a4371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3d815e24ba35c3f2fe46f25e2b34685792def1dd62f2676edfb9032b4fc84b`

```dockerfile
```

-	Layers:
	-	`sha256:f14973f21ebd27849c67760c0605d4fd69ad40f3b377db94b406ceaaef164e24`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 4.1 MB (4076193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dab5eb8c34bd4bef3fa1de4b045659db9b0779ab5147ed7c0beb579e96e5f5e`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:916e6a70fbb08f3fecc0d5bb863f975a1fad071a1f0e71cfd96c6b0fab0dbe6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61280300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb2a0631090e80b21116193e79024329d08135c8e8716bf02fb7c1e283d1b77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:08773a2e9b0fe592ef47b4e93c883d32a351ff89ea9cd33f1ad47abd4081b4ca`  
		Last Modified: Wed, 10 Jun 2026 23:39:44 GMT  
		Size: 49.5 MB (49491206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e810ad9db6f2b469efd6a3dc32f01d8bbee996fc9cf249f536349c428f775171`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 11.7 MB (11693049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4517a2fd68626a4b7d37f1281a4b8493f6bff6cf362388c70809494bf22763cc`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938bb31a07854edb8f445c0fbc48ceecba7c48afc745853f8166b847acd1f7e4`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8d694a50b5688ee05e4e6c70630b58d4a74b7e69244a495d9d6da6884f5988`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 93.4 KB (93427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d110e3d514a17608c947489dd7fcc1594c428802e040f83436725aa0326d819`  
		Last Modified: Thu, 11 Jun 2026 00:46:11 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:47006af36b58aff1f1d48edf468a341fe26cdb11c3f666f1ae7069444f6c4179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13db9167b04fc22de7de27b41be6646812bf36993db6a0cbe491979ac625d01d`

```dockerfile
```

-	Layers:
	-	`sha256:f293d710adabf57b11d93c677d8ec53b76b7dc7cdd43a0dd4638b26ed17742df`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 4.1 MB (4073918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9bf6c5d9a5fb8ec5c22c16692a1369bc9a9c93f4bedabc2e43c616ff5439475`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:d8499e8b46e0655ce15feb736d6646f4c0a2128e80279004b66f993ad841db46
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
$ docker pull neurodebian@sha256:73aa7beb900b2b857f3c4e97b3768980b2e079cefb4fd543c9ca356573ab6caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbf106e61f2132667a8e9ac996027d6929275f246acd22030c0255eff5946b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:45:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3a4f7cc0717582c2f3c6148a1e85b8dac860ba9d316c50151e8fc2dcf24e33`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 11.1 MB (11103447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16f0eefbaae0196bde0bf762bda663256e23157799b4e3139952d3cc719550d`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789b4402e52242b672cbe6b5b1a6387c64225f3e55c7450e3f117d1d68f9dec4`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e70122fd1bac8ad54f5ade4c5092064824cb18e49265fabdd64d5cc7e546655`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 101.4 KB (101389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a16eeb6ef64d1a380b22a910ea4466843a9d8e0f3b95a548601375bbac95335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe56286e7a99287cff1ae93f70f0f65b90bd59b20187c884659a3c9f2e62b003`

```dockerfile
```

-	Layers:
	-	`sha256:178a957cbfb1c5b27a4238fdac26baba7e17da0c95f747fa841d4bbb582e2b7f`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 4.4 MB (4367918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:725bab1b25497fd016971b729a2493af95f6dfe7858e00793b91ae2aaa7bc0ed`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0964dc7edd5968e5463c8d308c19bc81457bd15b028ad513be5b3ec1450b1d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63477463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbb8774384c869137df0894a6ace3cbb906552911f2524f6c7421c055e7d476`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:47:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2478139d0786de2aee4b1dcaa1cf029f85acd978f95dbfa7a0aacc5c3057f1f2`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 11.1 MB (11109904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286b2901c8bad4d6c2369e254e93ed71f6cefce38556113f956fc7fc4fecc1b1`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4971bc72e136ea404c0dcf45d3e13567288c6c38674c9bd86aa34eacb2c4570e`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9ece72ba9b9f5b1452547498613d7bfa4b34c414087b11fa187117c2bc2818`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 101.3 KB (101286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a82b1f17237127ba4ca6fc91917e6549e7c67760c9982aea3d9ad90906584677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971afaf909e83b24a05309f9b3a950507ee08ca4c48135c1a0ff7bb0da5c5931`

```dockerfile
```

-	Layers:
	-	`sha256:14a53dd714448eace56b3c2cb11cd120d635a97615facfdfdd8073942f9a591d`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 4.4 MB (4367525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946581dc6b334d33c918daa2c33425c1e15a95bc39d3352f86420a0c7d647450`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:177001282dc54d461853f07708f22f134ad2ba848f6605cb73a8bcf511cdf9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66318635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfbead96266eabcb3e6dc47637e716f6c315f017b4a198c61f81202ee285ab0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:45:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa94b3659141003eaf4c6c1ec8d2e2140d97afd4e23da5fb64936eff3ddbe795`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 54.7 MB (54712857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de40a8efdbb710eeeb369826e1a843a9c7ca4cedc5830be54bec9a4c04821d8`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 11.5 MB (11502372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035a7ead740086997dcaf6944ceafe496330e0f19f6dd3b1c5da4cca8c1c93c1`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0bb1942aed2f10b661ee389529e90a2c3382ee9b8352495bb9f8e15036bafa`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e1266b6a8fdb893c7711ff9efa76426630140426fe129839b84e775d9d6321`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 101.2 KB (101249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c5016b6665cebe115adc388bf52b0f549711f8986423f177ed551138732afcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574b0780e44a485315b1a3b753bd3604de4cca26a68462267b4fcb172f659235`

```dockerfile
```

-	Layers:
	-	`sha256:3ed797e12ca446c70d177753899e05649a218c9caeafa78589ab38aabc867c83`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 4.4 MB (4364437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73493f351af6e15279a38dcc882e04149790290a41966ef74581934d4d7dea0b`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:c1e8a9907c9692a2d8eb4d928f1aefec63938fbf94b7ca14a5ad9711a18a93a7
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
$ docker pull neurodebian@sha256:8f9ff1ebd5c472b4426d607cc07971c22e2bf5bad4d6d606de40b2d890e46a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64979065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd98d76f08c16ec4990e9f61a3ac3caa3ec79c409488e00695d7810dd59b477`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:45:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9981861713d98df05d7f547a36e5538556e8acbec7bd877edc0dd7993fe81863`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 11.1 MB (11103365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678a8c2c315d7c2004f34b79f34d5a5dd42c5e3280e38124979c08592da36437`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7faebae933191c95abaf487d33f1eb63b4d96868295eaa6b233e3646b5a6edf`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e33875f4ce4b42c4b83282de288a8b46dbc815d4c91b75fc67496c60cc50a9`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 101.4 KB (101385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4af7eabcef6f6d21f23d675c0f72d225daada2975c5707e1005847cfb81e26`  
		Last Modified: Thu, 11 Jun 2026 00:46:02 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:be4f972c9d26a3670c1eaa5c57cea6b5c2ec00f243e8e90eda928e119fb1b7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0740d9f0a724b025b94ec77233003ce1f313a1a044642fee83619469e38315c`

```dockerfile
```

-	Layers:
	-	`sha256:67725c13a7747a2a89253b7bef171a279d77536b72fefee7e6d066ca7f17e0b3`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 4.4 MB (4367954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c5f799e9aaa132fa1f8e59a2fcfbbaa3acee314b7dfeab533ccf376747870a`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0f6973a526abfa5aa64033c68e2339dead9400d7d3583214eaf9b67dcfecd1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63477866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7fdafafad7f39ff6339fd0937d939fbe1254c6a002d4db291b5748f7d36015`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:47:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9b5af5e4a2d9cf379b3845400efaac90cfdcf08652cfb47e8eacd1b326cf38`  
		Last Modified: Thu, 11 Jun 2026 00:47:33 GMT  
		Size: 11.1 MB (11109924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118c21db13adf2a7275b56854f237f9a0ecb6087b823d8ae0b8b1c2fda19c649`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17306412c7fd596ae38e8a3f5953b14a9ab1ba0c1407f778b807e3dee8f7f02`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97341d516dcc446e4e57b1e6d23781a5287793340dbf15b385a694230a24473`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 101.3 KB (101279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bc0d75d6e94011362e701158a8fab375ced03d20c5bba23e88ede331f4bfe6`  
		Last Modified: Thu, 11 Jun 2026 00:47:34 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a55fea1517b08a1a7852b99d3e895beaa4de0646af1d53784b6bc3aaa442b60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7933225ad3f8c35c6b1af8b493b8c89edae9c666c21e62d4cd3382ccd4d696ba`

```dockerfile
```

-	Layers:
	-	`sha256:22f1d97419c0a41b97eade5795164af3b34d7e54b1001df4f3298cd26f3b80cc`  
		Last Modified: Thu, 11 Jun 2026 00:47:33 GMT  
		Size: 4.4 MB (4367561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d3e96c9f17ea483f929a4f340951e4e6caddc8c891849704255c24b5ddd1bd`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6898e68eec990afef9e8e941ae475a6e6ba9a7c89d1569015326302fc85dcfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66318901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b96db0eb400856d9b433a74f7ea4a06d3bc9652109f52f9cae74de43474f6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:45:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fa94b3659141003eaf4c6c1ec8d2e2140d97afd4e23da5fb64936eff3ddbe795`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 54.7 MB (54712857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5431d75034b78174b62a23408161498c4408116fec0cfbafac129d42f0e94cfe`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 11.5 MB (11502228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c7da2715bd36e224998cfb7872b10d6ec78a79f0ff89b70efe80caa5d71fd5`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a37c05c9b88b6b246537e6834721e590a62a7b061add25adc0166d822938ac`  
		Last Modified: Thu, 11 Jun 2026 00:45:49 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbcc0a810f7dbc1da929c8af13f18de2d0e9a1fc46fd8e93e7c421885f6f78e`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 101.3 KB (101272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69c86e8eaf936891d2d5bd628df1f381fc68d3f61b41070615e12cead6ce08b`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:572913f9f8b3584a32002da1cd705b096a86166c536eeb2e5e6bc1a1b85673b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8627f4038e578e722de05074c970b82764f21a2849a92d2c1129e91bcc9b5e`

```dockerfile
```

-	Layers:
	-	`sha256:38b0af99d61a4f4256208de3c94529a49ad3a3a726f68f0f188ff7e8b195e752`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 4.4 MB (4364473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e2479089dbf204ece3399229ee5fa2b425ec9bb713e627746b2311062b5e6cb`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:a50cc336e20a764cd963952e7c8d29ffdaf44286f332042da8001adb23a53499
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
$ docker pull neurodebian@sha256:a9560d4b868b489de7cc083ebc56092bae1a8be0b98d429f8823f2881b80e3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60270784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee40384bed7687c3fde3550aa90fe0bf52fb225a6ea762db63f9aba9cb10b4e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:46:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5721d6b62cfc7a7bfa692b95ea547e4ea39b5e2bfe1bd3e1a88886f80c2846e4`  
		Last Modified: Wed, 10 Jun 2026 23:40:06 GMT  
		Size: 48.8 MB (48779274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dd20d64a6c9c73fdbdd9abec84fecd075db437c4798b0bef377514410abb8e`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 11.4 MB (11399228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb2d7895f6cc503a3c75f0ab087eb2584e6322fc057533fb4e00c0b3b1f4472`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288413eea6b9f9875d894a238c3011a38834b38013491f522118fc98a55435f2`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fc3b9def0538c4c122e90bb4d4867322832d167cd48eef7f34b0b680916a59`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 89.4 KB (89380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:732c33527b8b7880c98718d0d8514d7c0b57027ffb9301500e3dcc54364be44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c09e1a49472b4e52cda50b589839475bf6161a29ea40e0ef47be682d70457fb`

```dockerfile
```

-	Layers:
	-	`sha256:b852ad2779cb9865bbb16d2e1eeb08e6b790460a01f952ca78414a56d41cfb68`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 3.6 MB (3562578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba46853a915a467431c01953255c08713eaf58bd037c7c07e8bdb0f02b66f9d`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:eb0803a087f9dd2a0452cc49b4c1f2068e993fb49d8c8fa477e3e5a428629100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59981823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885a2677d3ede8cfc1255a17497f7bb3c0e4a2a108dbc98852d0f00c83b7e6f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:47:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dbdf5115192d6ba17e54d5f2d3cd16e18cba052a9281223f09caff8a3d00462b`  
		Last Modified: Wed, 10 Jun 2026 23:40:03 GMT  
		Size: 48.8 MB (48795608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a795a3ba9535eccc0edd2ea21f47aeddf42a3a46cdb85280817a4355306194`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 11.1 MB (11093292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6008b62a31c2fbb1a2977ee676c7578c105279fdaa473fd968ddd3384d3af4`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd26e10e2b3776525cd5efaed604687ef1481c14bb311ebbb49825f60e5ccaa8`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0328ad9cb5fdce2ee901dcf0f9eb71c48d8280e5da2c5ec0b260dd3f08d497`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 90.0 KB (90022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d84fa4d0588b23eaa115f89023172a606234d7a493c3ca52c7dce95ba2d79582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2caba5e2d2f83631946694397423d270d2dddd19dc9521cf2d36a4876d0e462`

```dockerfile
```

-	Layers:
	-	`sha256:faa1a3015fb7d8a9813079851b447a5fc3aa38284b01ce089368481b034ca413`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 3.6 MB (3567283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4cba479120802c02d469950a86bb842bfae0700093bd27406c8702aceaae337`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:bbffa1bd869a4e9d65db7c1b0dd07339fd9386da0609c1cb034b0781c106ae31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61798673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56222e02abc1cc73d9e73d9e0e32ae195aad8c02e4969cb73d949f053e7cb8aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:46:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6a4be7a6be3ed3c4d92863f22edf1e7aa21046c79f8c96f534040141953aff3`  
		Last Modified: Wed, 10 Jun 2026 23:40:24 GMT  
		Size: 50.1 MB (50076810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbd140d2127fdfd9c232ed33b621b07bbed40f4963bd2b993623d39d97b9902`  
		Last Modified: Thu, 11 Jun 2026 00:46:38 GMT  
		Size: 11.6 MB (11629307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94017d4e25c5d8373a5357a0308db71819426070d5f4b9271b34b8a5fda4b0c4`  
		Last Modified: Thu, 11 Jun 2026 00:46:37 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ec5ad79fc64e2d05acf5c43a5ccf41d7a8a2deed1cf2a1bcd108f1752bd624`  
		Last Modified: Thu, 11 Jun 2026 00:46:37 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcca141c6b524c2209a88f0639b3fa4bed54440bebd8d43e515b96a54eb254d`  
		Last Modified: Thu, 11 Jun 2026 00:46:37 GMT  
		Size: 89.7 KB (89653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f2d165b4710ec4c5b81914974e3af4daf7f15d5f3cd3ef35fd598ded2bbc4ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a044606ea432cc5a812b1bc3c4a10d7f2dda86d2ab761c045bb302eb4ce5a5f`

```dockerfile
```

-	Layers:
	-	`sha256:362a4c99421d747069d17ef85f9df927093a7af634aa2df6d81d064b6c5894d0`  
		Last Modified: Thu, 11 Jun 2026 00:46:38 GMT  
		Size: 3.6 MB (3560528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a20fddc90098bb0d6cdebbcb87264c7c9ce653aa53c026edbf70f278ef558eb8`  
		Last Modified: Thu, 11 Jun 2026 00:46:37 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:37264e9014e928cf0bfda64869302438443988e6d0b8c9d6005e7f60d6cfffbc
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
$ docker pull neurodebian@sha256:798c059e8dc4c8074ba03a170658b96b1b6def955002bdb1bd5abd315fe3319d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60271205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967f1f20d5f480494e6014001acbc38aff48d42d4ec0ac6351768fd541058d66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:46:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5721d6b62cfc7a7bfa692b95ea547e4ea39b5e2bfe1bd3e1a88886f80c2846e4`  
		Last Modified: Wed, 10 Jun 2026 23:40:06 GMT  
		Size: 48.8 MB (48779274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a95da46269214aaa1d7237827dc71f5b5d8069dfd47fc510bc12bfd608acd7`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 11.4 MB (11399216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb2d7895f6cc503a3c75f0ab087eb2584e6322fc057533fb4e00c0b3b1f4472`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288413eea6b9f9875d894a238c3011a38834b38013491f522118fc98a55435f2`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411295c6069be613044d1319c9f54b3590cdc5e10b3aace199bb072cfd62be68`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 89.4 KB (89366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc95558a2b42225eb9e88d79e8becb9d84ddd839869c67835da9b77b53233ce2`  
		Last Modified: Thu, 11 Jun 2026 00:46:28 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cc82c554bf9c7436fcda1864d1b7a76221113c13842dc5020f4610325e81ea5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3578572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b68e3571054ad0151dfcb082a8a66da630e7142baf98899dcc74e926c517fa1`

```dockerfile
```

-	Layers:
	-	`sha256:335aad9da067ca64dacd08bd25766189ee283be0697c324e298c4d29de9d600b`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 3.6 MB (3562614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929848b26f9d1ea5e95bdd50689a4efd60d82cf1efcfba8397db62fc8458812`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 16.0 KB (15958 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c2fffa659dea9ac21c972d44d982d9e92fed478e02cea8d27d65902ed0acb2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59982196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca3b0896e8a800b0c4b4953ce852818802be1e08c89be74b5e5b3b28cba052f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:47:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:dbdf5115192d6ba17e54d5f2d3cd16e18cba052a9281223f09caff8a3d00462b`  
		Last Modified: Wed, 10 Jun 2026 23:40:03 GMT  
		Size: 48.8 MB (48795608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521f1c00810ede4b0c96988ae55b20fa413409b82a6e190d89816b03fc5a765f`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 11.1 MB (11093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3426a165d11ed3c48c1235f57c55e908c0038c6711048075e2f52785512761`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd26e10e2b3776525cd5efaed604687ef1481c14bb311ebbb49825f60e5ccaa8`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca93d601b6a3978a4bbc3b5591aede6efdf93a3ddb432a1761c30cbf0be0a3d`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 90.0 KB (89999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6e5214750a7948bc5252a9accebd4699c3c518b3fe689bceefde2960613b2a`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1f94ce78ff663c717b15eda02d399f935a34aa0c328854c686ab9e4ab00b6c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341c8dd593efaf733c616fa33b61fe15cbbfb12102bc3f1d5a289ad3b9afc664`

```dockerfile
```

-	Layers:
	-	`sha256:815740f746f6fd00353b2cdf9ef1b64be736b95fadade3c0760410e8b8492e5e`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 3.6 MB (3567319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fced8e5795241aa8c06ee963dd4d74b0a962b1d76f736a720db51337099821a8`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ac7573e1a964cedc92762f1764c74e516f1ad3746228ed0c08651568cdee1c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61799181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fddba0f6579ebe47327071a3618c0aba6177f33aeb4a8cea77ce865ae3d4f04`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:46:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d6a4be7a6be3ed3c4d92863f22edf1e7aa21046c79f8c96f534040141953aff3`  
		Last Modified: Wed, 10 Jun 2026 23:40:24 GMT  
		Size: 50.1 MB (50076810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b472a6d8b7727a486701a1080e4d0e8b17435c83bab23bd2ec2b916a22b5a7`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 11.6 MB (11629359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056b0eb9c4e41949da3ec5420b12975ae7a0907918f66ccfd3a65482da204979`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a07b7219afe18068ac7164b86637e0a1dccb746ed0acdb1b0278a72d506c09`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615ed529cf578cb6a5ab9693f16045ee70cd90a54524463364191b5ed9c2ad2a`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 89.7 KB (89662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde751c374c1d4871c1deed9148e8dd53e68ef7ea748a3ec4e9e6159cc6cd128`  
		Last Modified: Thu, 11 Jun 2026 00:46:44 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b041bd8f4c37b1374e71d2e430366895c2266d010e122ea2c8f86a72be2b3cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4077abd8c2df574289455d03f7a6c0bbd1a5fc03a069961dc263bbde41be797`

```dockerfile
```

-	Layers:
	-	`sha256:a0b3dfec3b714a0f3659f3df8424dac0141979ed49efd25ed4e92a8d5461d602`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 3.6 MB (3560564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a422575041a54c249ce448c1da2996daaad5e1140dcf52109f78af6c2fb992`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 15.9 KB (15928 bytes)  
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
$ docker pull neurodebian@sha256:57bf3a66ea98601be74660a4a7797276d3badc3b433b84be07822173c01a7d42
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
$ docker pull neurodebian@sha256:0f10c55925c7daa6986178bd929a59c328e73b14d33e638b933d343ada75bffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59704614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32d537529d69d344d0eb896c9f97232c3d86f4bf97570473e3fc59c980acd6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab8a23fa26af0a8cc76053873ce7f2f4972656e8f0fce2094d6a666e3be7772`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 10.3 MB (10294155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6332aa2ff8b6e8865f809e22829bc2fa69b14363252518a815b841a1f1e96903`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d07151946d2a0886dd871c29d5af1c81bcfc8b58b498e8e10191f9018b2566`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9b52337e56a0c8b560c3f38b88a4043b2f81e9b7787f91fe3e15d9df02b94f`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 90.4 KB (90436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:253280c8c43c2b210aa41b9932a9d65d4b1937e1cc592889552a887ddf9d0c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d78b8f51492931a4c575295e525c37e9368e45303be897d48ac5cc9e6ddb266`

```dockerfile
```

-	Layers:
	-	`sha256:391817222b355feaf88eba1d4e2ec5b9e43b8395e7ba2cdde60a0a46a41e5a18`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 3.6 MB (3614164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a2708db03fe47ab7d21c2de25cd8c8bbb2d7ac4d9a3dba9f126c55a2f3bbfea`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4d733fa6ff08050595170e47efccfe107fa7fbf6d920d166495fa1ac2c2bfa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59851304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4c08654723853eb5602234bae5feb235f2fdf5852a0bd21e23861a7de27bc5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:47:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8663f66a97521bf18781b6a8ebb14fef9360e63aed5744a8826c46b6e955ff`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 10.1 MB (10079209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898f78772560357ad8f1982fcc959f06700ed89aae96a065a560a906236d8cf7`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646d242c23c90ed9667d2fbcfebc5fa2ff61e602411007d42b67903ef19ea3d`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0366805b83dc22dbed788828fe85a31e7d2925bac97277ead3789e69ec670bcb`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 91.0 KB (91025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d09bad896d54687ddebe1648238e4e9ecffc205b3697da54d7432644747a8ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee44725acd45051b6ab2baa0a69bb183c202e5f01eb0bb9fa46dec30e9fb02e`

```dockerfile
```

-	Layers:
	-	`sha256:6b665e7bbede387f1cc367505a144eced1dcf9237f7bfe90cddd631df2f08035`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 3.6 MB (3615054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b382e18a90a184f236343b396eace7da5a3cb00b4f6f8f273322d39f408687a`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:69272e86cbda3b80360145b7035894858f8cfbea157d8ecb1dc592ff7f95706d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61397435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d156e7bcf79c18dd9eba9d5b14acb9798c93bfe93b50dec402f6a054d7cd0a4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96262f3a6afeeffe35b7ae82c64e4411332dadbfc81b4e151d05d1ae95ef0e5f`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 10.5 MB (10468195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9803f3a3cbbb4fa8e0527752d2fe446742a844b364b659fd3471c1412c7de7ae`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328489f211ae28ef4a19ffab0576631bbadef0b960df6e7cb234806fed854cbb`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480857bb2368ea3670f8a8b5dfce2c9a13b1b59414ec77b0efa36c938bfdac56`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 90.8 KB (90776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fcb451aa5bef61bed7700ef1c06e8f31e746f268f0ac340de5e44aad5b38345e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd93bbcf1197ba8c7cdbf851083e591e6ed5f96d4de0e879b2dfc99dc636cdc`

```dockerfile
```

-	Layers:
	-	`sha256:098c6beadc9d4944f26eb9ae6a78f28d6e0c48a29e9e44e2c14f28ded1b73576`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 3.6 MB (3612112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b5e77ec315284c66927105a56c707e59dd8c54f41091f07f9381cc23d970ce`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:65004333205e19d05539cccbe46a3d577ff04794119b52be74dc32abf570ec7a
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
$ docker pull neurodebian@sha256:ae287380c24223f57660150b7da71cdf4eb84270f620831b0d4efac16f74bd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60294002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e26bb2b04a99e8f535ff8fbed986163a3ee4d770e5e51d70b77820d74abe0b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:46:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bdd122fd70d19475cad994fa0bd624dc1524d2143c57c7c1f3f9e23fe40ddb0a`  
		Last Modified: Wed, 10 Jun 2026 23:40:10 GMT  
		Size: 48.8 MB (48801212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacf64a88439387b1c0eba23bcec29b6672837e395a0256976be744e995b3bad`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 11.4 MB (11400511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a7e10f751eff090cf764c44d9e5001c1570eb8ebb01f32410ca89370ebe19`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac08f4684991e1cefeb83a94bca5bd073dd502e21dba3d833745e37cff385d`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf49cc7e499d5a430ab888113f99e87e81e51393c55d0894e75cc2769295e6c`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2fd3e58ad348dcac794bb0741eeeb37199ca52fda2ccf9b746d91970d2dbc571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8420cb3d0490b285b0fc8a31fc14d839e9c7aad6895787277fc06946bf1e51f3`

```dockerfile
```

-	Layers:
	-	`sha256:90f7545d094de3aa23907f01f890bc1935142a968c4e73f6e4fe2f64f889331c`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 3.6 MB (3561769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2b880c5f3b746d7c60d4781081d48c83adc6a95cefdb282dc6a4fb808c6148f`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b52d4611b34a2bc915f7402bf07b7c0ed611ac77167147a1fa579671e533f20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60005272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8e718cf8135c7a7dbaf28de21e4a599de708b5e737331e8374f470d67a4325`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:48:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:48:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:48:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f216cfca8681658c5c6a7a8b3653ba38754d80730e4760fa07c5af0c77dbafdc`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 11.1 MB (11093783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c245f33d403e20631db07d85c7949c38d447f59151983e6ccd177844c70b2da`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f20446e70687694e58be96b1e8dee8abbbffc8a86361dfef1e2c9933a7e172`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c777496248e833ab9ee2388720300b95430fe7f379a711f6d0d603d2bb9dced`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 90.0 KB (90032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:af5bdee722473dfe53afb51c4052273ce01321dc38891ad423a777cd3eed1950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3580503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e931479eeae972f6d3393eb1fc52d4600aaed088476de284ac64185006b8aaf7`

```dockerfile
```

-	Layers:
	-	`sha256:c667f4c018696b0a60c8e913790fd50a5b7b27861cbb09b150589add99b16396`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 3.6 MB (3566474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0311325e77f970962d6ac2bd4c71cc3ede59589e9266f3b563c2edb9fff8ae2`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:db288142cd7d03a71eb88cbd8fb467d9f3ca884ad08869345b93321c856a5b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61827288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fbd236a7dc10eb614ef42c3c69921831585f25fd8f562daf47b4f118f10e9e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:46:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a32252638de41825057387ef73b5d4de843fa9726fc243c76636da258263cc3f`  
		Last Modified: Wed, 10 Jun 2026 23:40:40 GMT  
		Size: 50.1 MB (50105399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8850820ce6bf3267c5c91d1c3f79a074463665cbda406eaaf4872b08667ff727`  
		Last Modified: Thu, 11 Jun 2026 00:46:56 GMT  
		Size: 11.6 MB (11629301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59643bfcfdc7a07558763212315a14034a0faf6cf046e4b65a4278d1a4350591`  
		Last Modified: Thu, 11 Jun 2026 00:46:55 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb1e2903a9eeea6791fb0d68c37cbf3059a41978f7908ce04558f3867b97445`  
		Last Modified: Thu, 11 Jun 2026 00:46:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2661a0f39769c7e60845ac8a9aa10871123e6734e4b74318b0c3fbd81ef8bed4`  
		Last Modified: Thu, 11 Jun 2026 00:46:55 GMT  
		Size: 89.7 KB (89684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0f22da5598552d7251e27607c800ca0ba8ad53f7423889371241c2eac8a99ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c747cbce286794184c87c0320eb3afd3967006a7f54c4d662c9c2419e8968315`

```dockerfile
```

-	Layers:
	-	`sha256:047574fa684a7608b854d9059022f5fd70b7d4348bbaae00257b8d38cd15d2e4`  
		Last Modified: Thu, 11 Jun 2026 00:46:55 GMT  
		Size: 3.6 MB (3559720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d689c1ab4807b8753e1d617ae91ee28b3eddcd00c7b493fdd4a2e51ba1357d`  
		Last Modified: Thu, 11 Jun 2026 00:46:55 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:790f3f37a60945a425379d9bbf7514dc38a6bde3459cc4fe95d2d2564c6300b0
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
$ docker pull neurodebian@sha256:e668949d99fdcaa776069a8dcabcc7f92c06280add74b6d2d44a986fffa458f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60294471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9baa11b9e2318de0932554bc6ce85f2b70bd43b4c6f63259ef1faef75e61a3ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:46:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bdd122fd70d19475cad994fa0bd624dc1524d2143c57c7c1f3f9e23fe40ddb0a`  
		Last Modified: Wed, 10 Jun 2026 23:40:10 GMT  
		Size: 48.8 MB (48801212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385a8564f579f25f1fa0091862faf1667f9d99bb57eb2d8d7d231e688a08ffb0`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 11.4 MB (11400554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fe6276a8f981a19cd267153efbd887e1960863e79415cc84f633d529be36ca`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f3d40ae033a5792a73f7042effbbbdb2c11e9c80d8e9242cb1bbc60372528f`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511c208cfebfaa8583dca48701b1de701916b85218fa6ca8d48a1ccf959989b3`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 89.4 KB (89383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfc8b61e4dc23cb303141daa73f93b5c3785184d487db0082a1eb1d756342b9`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c50a6fe2698c56337d96ba11f7b43114a0ddc059e6d6ff43299875cb2d8b4d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a4a2e0f7bb8530b6dff8701621957b864d0a23b2ae31c1ac981467dfbfd4cf`

```dockerfile
```

-	Layers:
	-	`sha256:da398cbf39c8fb41c6479f9a87ceb3f464cdfe56c93863ecbd56d3d42ebe1ed9`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 3.6 MB (3561805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9b4303c20ddff766e93d5ff40b68f06cf15ff76fb8dc3071c8f5a7447912547`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6b76a8baa5e5703b782986d03054140bb5f9c51a3f219cd3bbdfdb6e097b48b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60005540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ea7c2561889afebbba75f286331ba1118bdb81f98d193534f48e1183424a4d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:48:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:48:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:48:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f29437b24e4b4586fe357af3b6e2a0cd2bb4523e6dee73c3187fe1b261eeea`  
		Last Modified: Thu, 11 Jun 2026 00:48:31 GMT  
		Size: 11.1 MB (11093649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b2458ad9ad4a37d3870ee0be7b56fffd958237766aa0449ca76f2346e8d821`  
		Last Modified: Thu, 11 Jun 2026 00:48:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8c8f9d3d89dd50d605bacf929e2688267d93bf13ee4564d5dc39d004c7fff9`  
		Last Modified: Thu, 11 Jun 2026 00:48:31 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41c04a7fefd630d6ba41d8dea40c9bbf56c5bf080b069b449f6cfb2690e5431`  
		Last Modified: Thu, 11 Jun 2026 00:48:30 GMT  
		Size: 90.0 KB (90015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0f18be5600368b9aa251fc55917de6789bae5c62a407fac437536f84b7172f`  
		Last Modified: Thu, 11 Jun 2026 00:48:32 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c6ed9d6eb6d7be9b9b47cb3806493b95923bc062ac7e26b861f609264ac51edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3582581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2245c7f439db7a99cfc8d20357dc097d1272f3b902a7752a9aab0b8d48463c`

```dockerfile
```

-	Layers:
	-	`sha256:6cdc695a05d47bf2586613a897a82ca07f5b1afb508fc9deb9ae266b89134533`  
		Last Modified: Thu, 11 Jun 2026 00:48:31 GMT  
		Size: 3.6 MB (3566510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8984122e7bf9687e2fe6539b0f98adfb683076c15eae433a55c4b06a7e94f35`  
		Last Modified: Thu, 11 Jun 2026 00:48:30 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4c8cd0da45340fc16fe6fa498ab416e5612d234ee5454eed60ef2fbaada4a6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61827691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e041853d010700cdb92fa67e280982338cf0fbcd3ac4e17bb362c4ccb6352ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:46:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a32252638de41825057387ef73b5d4de843fa9726fc243c76636da258263cc3f`  
		Last Modified: Wed, 10 Jun 2026 23:40:40 GMT  
		Size: 50.1 MB (50105399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9985fd0b18c9239f0ab31829976aeb109a49fd849bfd9a60236038042b9bf44e`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 11.6 MB (11629273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea4f4dda4b51b86cdf991c17ef19d9ec22bd23e1f83387c2a0a394af0171e60`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f14c15c1caaffdf6e712eb73cd67310f04db2b7f87d96808966faa0f9afbab3`  
		Last Modified: Thu, 11 Jun 2026 00:47:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f9dabe2674a7076fb586746dadf0251dafb312b34d09feedd1acac58026bd4`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 89.7 KB (89702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a8a745ea0d9c0a691481e4260da9b612159d1fbde02376618d61a65cdb6a6f`  
		Last Modified: Thu, 11 Jun 2026 00:47:06 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c64d7bcacbbd0d616fce071f4378b1e5fef0e66a3b2d7ecda1ff220339bfad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc0c1b4b48591db8ce8d09e831614dcc796be68744723ba7f71ada9c5148b78`

```dockerfile
```

-	Layers:
	-	`sha256:61ad8ecc20551e74c4214e7eb23ae8b0f075b0a45a9ce71574ecb7f55ab81464`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 3.6 MB (3559756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f2c487982789bd00ebaf87c0a4bb2e5538523f01eecb2517a960e0f1e6db19`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:d8499e8b46e0655ce15feb736d6646f4c0a2128e80279004b66f993ad841db46
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
$ docker pull neurodebian@sha256:73aa7beb900b2b857f3c4e97b3768980b2e079cefb4fd543c9ca356573ab6caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbf106e61f2132667a8e9ac996027d6929275f246acd22030c0255eff5946b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:45:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3a4f7cc0717582c2f3c6148a1e85b8dac860ba9d316c50151e8fc2dcf24e33`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 11.1 MB (11103447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16f0eefbaae0196bde0bf762bda663256e23157799b4e3139952d3cc719550d`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789b4402e52242b672cbe6b5b1a6387c64225f3e55c7450e3f117d1d68f9dec4`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e70122fd1bac8ad54f5ade4c5092064824cb18e49265fabdd64d5cc7e546655`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 101.4 KB (101389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a16eeb6ef64d1a380b22a910ea4466843a9d8e0f3b95a548601375bbac95335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe56286e7a99287cff1ae93f70f0f65b90bd59b20187c884659a3c9f2e62b003`

```dockerfile
```

-	Layers:
	-	`sha256:178a957cbfb1c5b27a4238fdac26baba7e17da0c95f747fa841d4bbb582e2b7f`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 4.4 MB (4367918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:725bab1b25497fd016971b729a2493af95f6dfe7858e00793b91ae2aaa7bc0ed`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0964dc7edd5968e5463c8d308c19bc81457bd15b028ad513be5b3ec1450b1d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63477463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbb8774384c869137df0894a6ace3cbb906552911f2524f6c7421c055e7d476`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:47:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2478139d0786de2aee4b1dcaa1cf029f85acd978f95dbfa7a0aacc5c3057f1f2`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 11.1 MB (11109904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286b2901c8bad4d6c2369e254e93ed71f6cefce38556113f956fc7fc4fecc1b1`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4971bc72e136ea404c0dcf45d3e13567288c6c38674c9bd86aa34eacb2c4570e`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9ece72ba9b9f5b1452547498613d7bfa4b34c414087b11fa187117c2bc2818`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 101.3 KB (101286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a82b1f17237127ba4ca6fc91917e6549e7c67760c9982aea3d9ad90906584677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971afaf909e83b24a05309f9b3a950507ee08ca4c48135c1a0ff7bb0da5c5931`

```dockerfile
```

-	Layers:
	-	`sha256:14a53dd714448eace56b3c2cb11cd120d635a97615facfdfdd8073942f9a591d`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 4.4 MB (4367525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946581dc6b334d33c918daa2c33425c1e15a95bc39d3352f86420a0c7d647450`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:177001282dc54d461853f07708f22f134ad2ba848f6605cb73a8bcf511cdf9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66318635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfbead96266eabcb3e6dc47637e716f6c315f017b4a198c61f81202ee285ab0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:45:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa94b3659141003eaf4c6c1ec8d2e2140d97afd4e23da5fb64936eff3ddbe795`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 54.7 MB (54712857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de40a8efdbb710eeeb369826e1a843a9c7ca4cedc5830be54bec9a4c04821d8`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 11.5 MB (11502372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035a7ead740086997dcaf6944ceafe496330e0f19f6dd3b1c5da4cca8c1c93c1`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0bb1942aed2f10b661ee389529e90a2c3382ee9b8352495bb9f8e15036bafa`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e1266b6a8fdb893c7711ff9efa76426630140426fe129839b84e775d9d6321`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 101.2 KB (101249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c5016b6665cebe115adc388bf52b0f549711f8986423f177ed551138732afcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574b0780e44a485315b1a3b753bd3604de4cca26a68462267b4fcb172f659235`

```dockerfile
```

-	Layers:
	-	`sha256:3ed797e12ca446c70d177753899e05649a218c9caeafa78589ab38aabc867c83`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 4.4 MB (4364437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73493f351af6e15279a38dcc882e04149790290a41966ef74581934d4d7dea0b`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:c1e8a9907c9692a2d8eb4d928f1aefec63938fbf94b7ca14a5ad9711a18a93a7
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
$ docker pull neurodebian@sha256:8f9ff1ebd5c472b4426d607cc07971c22e2bf5bad4d6d606de40b2d890e46a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64979065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd98d76f08c16ec4990e9f61a3ac3caa3ec79c409488e00695d7810dd59b477`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:45:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9981861713d98df05d7f547a36e5538556e8acbec7bd877edc0dd7993fe81863`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 11.1 MB (11103365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678a8c2c315d7c2004f34b79f34d5a5dd42c5e3280e38124979c08592da36437`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7faebae933191c95abaf487d33f1eb63b4d96868295eaa6b233e3646b5a6edf`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e33875f4ce4b42c4b83282de288a8b46dbc815d4c91b75fc67496c60cc50a9`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 101.4 KB (101385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4af7eabcef6f6d21f23d675c0f72d225daada2975c5707e1005847cfb81e26`  
		Last Modified: Thu, 11 Jun 2026 00:46:02 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:be4f972c9d26a3670c1eaa5c57cea6b5c2ec00f243e8e90eda928e119fb1b7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0740d9f0a724b025b94ec77233003ce1f313a1a044642fee83619469e38315c`

```dockerfile
```

-	Layers:
	-	`sha256:67725c13a7747a2a89253b7bef171a279d77536b72fefee7e6d066ca7f17e0b3`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 4.4 MB (4367954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c5f799e9aaa132fa1f8e59a2fcfbbaa3acee314b7dfeab533ccf376747870a`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0f6973a526abfa5aa64033c68e2339dead9400d7d3583214eaf9b67dcfecd1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63477866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7fdafafad7f39ff6339fd0937d939fbe1254c6a002d4db291b5748f7d36015`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:47:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9b5af5e4a2d9cf379b3845400efaac90cfdcf08652cfb47e8eacd1b326cf38`  
		Last Modified: Thu, 11 Jun 2026 00:47:33 GMT  
		Size: 11.1 MB (11109924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118c21db13adf2a7275b56854f237f9a0ecb6087b823d8ae0b8b1c2fda19c649`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17306412c7fd596ae38e8a3f5953b14a9ab1ba0c1407f778b807e3dee8f7f02`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97341d516dcc446e4e57b1e6d23781a5287793340dbf15b385a694230a24473`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 101.3 KB (101279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bc0d75d6e94011362e701158a8fab375ced03d20c5bba23e88ede331f4bfe6`  
		Last Modified: Thu, 11 Jun 2026 00:47:34 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a55fea1517b08a1a7852b99d3e895beaa4de0646af1d53784b6bc3aaa442b60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7933225ad3f8c35c6b1af8b493b8c89edae9c666c21e62d4cd3382ccd4d696ba`

```dockerfile
```

-	Layers:
	-	`sha256:22f1d97419c0a41b97eade5795164af3b34d7e54b1001df4f3298cd26f3b80cc`  
		Last Modified: Thu, 11 Jun 2026 00:47:33 GMT  
		Size: 4.4 MB (4367561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d3e96c9f17ea483f929a4f340951e4e6caddc8c891849704255c24b5ddd1bd`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6898e68eec990afef9e8e941ae475a6e6ba9a7c89d1569015326302fc85dcfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66318901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b96db0eb400856d9b433a74f7ea4a06d3bc9652109f52f9cae74de43474f6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:45:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fa94b3659141003eaf4c6c1ec8d2e2140d97afd4e23da5fb64936eff3ddbe795`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 54.7 MB (54712857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5431d75034b78174b62a23408161498c4408116fec0cfbafac129d42f0e94cfe`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 11.5 MB (11502228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c7da2715bd36e224998cfb7872b10d6ec78a79f0ff89b70efe80caa5d71fd5`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a37c05c9b88b6b246537e6834721e590a62a7b061add25adc0166d822938ac`  
		Last Modified: Thu, 11 Jun 2026 00:45:49 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbcc0a810f7dbc1da929c8af13f18de2d0e9a1fc46fd8e93e7c421885f6f78e`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 101.3 KB (101272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69c86e8eaf936891d2d5bd628df1f381fc68d3f61b41070615e12cead6ce08b`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:572913f9f8b3584a32002da1cd705b096a86166c536eeb2e5e6bc1a1b85673b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8627f4038e578e722de05074c970b82764f21a2849a92d2c1129e91bcc9b5e`

```dockerfile
```

-	Layers:
	-	`sha256:38b0af99d61a4f4256208de3c94529a49ad3a3a726f68f0f188ff7e8b195e752`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 4.4 MB (4364473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e2479089dbf204ece3399229ee5fa2b425ec9bb713e627746b2311062b5e6cb`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:89a4466817847379c1cf72eb498339e79eaa7e8ac5d55cf358d0bc3b97b34d1d
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
$ docker pull neurodebian@sha256:8ab30383b3edb838a10b6bb2d7ae90a5f99ec6535024f27a4d2a864a430e3933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59871032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c10bd53e758eb76947bdac99b308a015e38d901b5f882ec63566e81f70c18a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5823007860ad5138e7ab5fdc785a41af7cc872ba69852060b4b1eac4ee55c4f5`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 11.3 MB (11273427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60650ff41dd99d0a7b13a2ca9ba9a13d360e3d5678fd4db87281bc0b756a7cd`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c243edd52bbca60408e5285aac5d978e1405eb4c3a37e2efb89680cb9f4b5af`  
		Last Modified: Thu, 11 Jun 2026 00:46:00 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922168382be72127bd6f11f9ad8b17c7432d028cd28ad15cc368d27050c00d8c`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 93.4 KB (93392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:675f2564cb071be958213e88bb135d7187dd1f2de73beb2b7cfede23c24de338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9978cc983011da1d93277693b1cbe3b5d2f8c94012907ef6558c00a5bac2daa`

```dockerfile
```

-	Layers:
	-	`sha256:4e384ce82895a9419db3e268a63878b228bb5e07568ab6082bcb301b02ed9a86`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e7dd3355c262265ee0b8187c68369282e3afb3ad1413958381f842df9b0f3c`  
		Last Modified: Thu, 11 Jun 2026 00:46:00 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:47123181987e52ef981cfc5f7d75a17df2009656b0dfd20321f52e5dbf6adbd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59737697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0432667e276c1f96a58ad559d013ee8547e585ee6ac984de02db5e06dd8b04e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:47:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a735ebda1e0cf248011c01a7676af282efac17cec145ba6e198c0ead226a04a8`  
		Last Modified: Thu, 11 Jun 2026 00:47:31 GMT  
		Size: 11.3 MB (11252911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3cd29dcf4276f3390bb7c591a4b35e0db081a8ba88fc8ba2e0c2c37ef3ac4d`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 1.9 KB (1897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d3622219a2a21ed6e957b57d9177dc02dd5859ffea8adae6dbdb315b7b5545`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae554063421f6d5273c9bf4d90ff55c337368094d308c785ff3ecc37f680628`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 93.6 KB (93602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:032fe2cae497ecb4e1bf5c8fdae524790d8b0fae9a6992eac2fa672eb10c14c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fbc693151be7e6a990a99eb3f13a04f175a8958f517585bfe910b2816f799d`

```dockerfile
```

-	Layers:
	-	`sha256:0ce295b9ec41e4b2923bfabf2680b01575c86088cb8d940538e8990c1d24ee2a`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbbff94d7b81988058a9e96b4d083f4b6c305bf5f90a75982d002aa3c6a0b2ca`  
		Last Modified: Thu, 11 Jun 2026 00:47:30 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:af82dfbac2ace1c12de220644198bca9fa60d14ae4030ec0ea0ee6820773708f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61279895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9023421816137e807cba98c35b5e49c6833ade9d8d1166cd0493359a13b00a0d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:08773a2e9b0fe592ef47b4e93c883d32a351ff89ea9cd33f1ad47abd4081b4ca`  
		Last Modified: Wed, 10 Jun 2026 23:39:44 GMT  
		Size: 49.5 MB (49491206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb1065defaf3cd332a8079a5865ad7223b8ff7972245037bd5380e7e8cdf00a`  
		Last Modified: Thu, 11 Jun 2026 00:45:56 GMT  
		Size: 11.7 MB (11693094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34b8aaa341edc9665c3c824c40ca2c6224c1ad6c75d4589f7c23d5484caac27`  
		Last Modified: Thu, 11 Jun 2026 00:45:56 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae62d2e3ac929f0770447d245feeb45696a6a615f08f56e8419b6eed5742593`  
		Last Modified: Thu, 11 Jun 2026 00:45:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40664b1013e9fcb14bd829208b53e052b428c71092da56d56c717c19aabfb03c`  
		Last Modified: Thu, 11 Jun 2026 00:45:56 GMT  
		Size: 93.4 KB (93422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:34307a842c8422da5331720c0ed84c4ff0eec84331daaebf85c8a521b0b48d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1353e56e5b05e076badc6692d815901c99204d8cd59ad56691146d4079855b`

```dockerfile
```

-	Layers:
	-	`sha256:ee2bdc57053bac6e88e164b84fdb6e7fe81f75f5b061890443395b7765376a29`  
		Last Modified: Thu, 11 Jun 2026 00:45:56 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f965de7b88a579f2e41cee3af9b50bb79e6b36b928855a3d984fec4dfd937c2`  
		Last Modified: Thu, 11 Jun 2026 00:45:56 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:66a48b7ccd20aecc1e9c9e01ebfdab2ea7295615de73b51bcf9d8ed7309f87cd
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
$ docker pull neurodebian@sha256:cb08d6507f123ee954428276008e9c83d04d678754198d693e50c143cd0b54c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59871456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b85951aa7d121d082ba9654faa3848cc4d7abf9356e2b05af37bf3798ee4a3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c316bf023637e8f75e24e3831fc88deec444a7edd9790e0f9f3402d9b29c326f`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 11.3 MB (11273410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c8c4f5224dcc00c21540e9ea367e0aa62a4761dce0b1fb4bb55e9ea5b3cdd8`  
		Last Modified: Thu, 11 Jun 2026 00:46:13 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6638a85f4456b72d34de42e7458e7601f3aaa7cb32e4f085f5d08630aeadca8`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5858bb9b664153533d17afecd315d9a495a8a206b90c5efb794f7c4092c1ffc9`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 93.4 KB (93384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38110510a4edc98696657cec2c2800964ccfc836ec056480be42cca91b0590df`  
		Last Modified: Thu, 11 Jun 2026 00:46:15 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef56c80fa9e728c7024ac666c2bf5202d16a781191412562676f1d6f20996382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24b93a1caca4355cbd5126916038afee65708be0cc9931b6318251c3a3be743`

```dockerfile
```

-	Layers:
	-	`sha256:9ef2dc0010e4906a38178c6a2967e978008ea697bdedf904b98653f49cfe61f4`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 4.1 MB (4075951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7730b62570a8ef5981814ef338e673077fa401a6a2344f13053e1964058ca884`  
		Last Modified: Thu, 11 Jun 2026 00:46:14 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:790fdbd7c2371eb8b5a4027250b8a4b74df108263ee34284598e48689aa3d001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59737987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4997f84d1e861b3e56a7fcb35962903ed6088d800caf72b7705c80a7d0b9c2ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:47:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152f2e93026566c42f24a52213782e990addaef08acafed5aba4a4f0e9fba3d0`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 11.3 MB (11252819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5448acce891289851311b76fb4d92d758cda828f3c1df7f4e8055522e44a35a`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84827aab7e6cfbbe8fb22eb54023ada3db2c55f6c590f10460f04331d83a4b14`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fe5708fd6c1d49b9eb0bb8f71f6d6a7ce682aebe87de418fead20b403f39c6`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 93.5 KB (93528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40247c8de7fd661db84c3da66fac073f9af9b4e5ec60d78e06137a39f9bbb31a`  
		Last Modified: Thu, 11 Jun 2026 00:47:52 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c65b1c9f2a93cd41d6d12d3d078c3331d4a1300f4a3fc845c881942a25a4371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3d815e24ba35c3f2fe46f25e2b34685792def1dd62f2676edfb9032b4fc84b`

```dockerfile
```

-	Layers:
	-	`sha256:f14973f21ebd27849c67760c0605d4fd69ad40f3b377db94b406ceaaef164e24`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 4.1 MB (4076193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dab5eb8c34bd4bef3fa1de4b045659db9b0779ab5147ed7c0beb579e96e5f5e`  
		Last Modified: Thu, 11 Jun 2026 00:47:51 GMT  
		Size: 16.1 KB (16132 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:916e6a70fbb08f3fecc0d5bb863f975a1fad071a1f0e71cfd96c6b0fab0dbe6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61280300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb2a0631090e80b21116193e79024329d08135c8e8716bf02fb7c1e283d1b77`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:45:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:08773a2e9b0fe592ef47b4e93c883d32a351ff89ea9cd33f1ad47abd4081b4ca`  
		Last Modified: Wed, 10 Jun 2026 23:39:44 GMT  
		Size: 49.5 MB (49491206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e810ad9db6f2b469efd6a3dc32f01d8bbee996fc9cf249f536349c428f775171`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 11.7 MB (11693049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4517a2fd68626a4b7d37f1281a4b8493f6bff6cf362388c70809494bf22763cc`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938bb31a07854edb8f445c0fbc48ceecba7c48afc745853f8166b847acd1f7e4`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8d694a50b5688ee05e4e6c70630b58d4a74b7e69244a495d9d6da6884f5988`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 93.4 KB (93427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d110e3d514a17608c947489dd7fcc1594c428802e040f83436725aa0326d819`  
		Last Modified: Thu, 11 Jun 2026 00:46:11 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:47006af36b58aff1f1d48edf468a341fe26cdb11c3f666f1ae7069444f6c4179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13db9167b04fc22de7de27b41be6646812bf36993db6a0cbe491979ac625d01d`

```dockerfile
```

-	Layers:
	-	`sha256:f293d710adabf57b11d93c677d8ec53b76b7dc7cdd43a0dd4638b26ed17742df`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 4.1 MB (4073918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9bf6c5d9a5fb8ec5c22c16692a1369bc9a9c93f4bedabc2e43c616ff5439475`  
		Last Modified: Thu, 11 Jun 2026 00:46:10 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:57bf3a66ea98601be74660a4a7797276d3badc3b433b84be07822173c01a7d42
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
$ docker pull neurodebian@sha256:0f10c55925c7daa6986178bd929a59c328e73b14d33e638b933d343ada75bffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59704614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32d537529d69d344d0eb896c9f97232c3d86f4bf97570473e3fc59c980acd6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab8a23fa26af0a8cc76053873ce7f2f4972656e8f0fce2094d6a666e3be7772`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 10.3 MB (10294155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6332aa2ff8b6e8865f809e22829bc2fa69b14363252518a815b841a1f1e96903`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d07151946d2a0886dd871c29d5af1c81bcfc8b58b498e8e10191f9018b2566`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9b52337e56a0c8b560c3f38b88a4043b2f81e9b7787f91fe3e15d9df02b94f`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 90.4 KB (90436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:253280c8c43c2b210aa41b9932a9d65d4b1937e1cc592889552a887ddf9d0c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d78b8f51492931a4c575295e525c37e9368e45303be897d48ac5cc9e6ddb266`

```dockerfile
```

-	Layers:
	-	`sha256:391817222b355feaf88eba1d4e2ec5b9e43b8395e7ba2cdde60a0a46a41e5a18`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 3.6 MB (3614164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a2708db03fe47ab7d21c2de25cd8c8bbb2d7ac4d9a3dba9f126c55a2f3bbfea`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4d733fa6ff08050595170e47efccfe107fa7fbf6d920d166495fa1ac2c2bfa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59851304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4c08654723853eb5602234bae5feb235f2fdf5852a0bd21e23861a7de27bc5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:47:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8663f66a97521bf18781b6a8ebb14fef9360e63aed5744a8826c46b6e955ff`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 10.1 MB (10079209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898f78772560357ad8f1982fcc959f06700ed89aae96a065a560a906236d8cf7`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646d242c23c90ed9667d2fbcfebc5fa2ff61e602411007d42b67903ef19ea3d`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0366805b83dc22dbed788828fe85a31e7d2925bac97277ead3789e69ec670bcb`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 91.0 KB (91025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d09bad896d54687ddebe1648238e4e9ecffc205b3697da54d7432644747a8ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee44725acd45051b6ab2baa0a69bb183c202e5f01eb0bb9fa46dec30e9fb02e`

```dockerfile
```

-	Layers:
	-	`sha256:6b665e7bbede387f1cc367505a144eced1dcf9237f7bfe90cddd631df2f08035`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 3.6 MB (3615054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b382e18a90a184f236343b396eace7da5a3cb00b4f6f8f273322d39f408687a`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:69272e86cbda3b80360145b7035894858f8cfbea157d8ecb1dc592ff7f95706d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61397435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d156e7bcf79c18dd9eba9d5b14acb9798c93bfe93b50dec402f6a054d7cd0a4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96262f3a6afeeffe35b7ae82c64e4411332dadbfc81b4e151d05d1ae95ef0e5f`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 10.5 MB (10468195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9803f3a3cbbb4fa8e0527752d2fe446742a844b364b659fd3471c1412c7de7ae`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328489f211ae28ef4a19ffab0576631bbadef0b960df6e7cb234806fed854cbb`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480857bb2368ea3670f8a8b5dfce2c9a13b1b59414ec77b0efa36c938bfdac56`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 90.8 KB (90776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fcb451aa5bef61bed7700ef1c06e8f31e746f268f0ac340de5e44aad5b38345e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd93bbcf1197ba8c7cdbf851083e591e6ed5f96d4de0e879b2dfc99dc636cdc`

```dockerfile
```

-	Layers:
	-	`sha256:098c6beadc9d4944f26eb9ae6a78f28d6e0c48a29e9e44e2c14f28ded1b73576`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 3.6 MB (3612112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b5e77ec315284c66927105a56c707e59dd8c54f41091f07f9381cc23d970ce`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:9a1e78ff7194ccd99640b7d1d86bc7c8cb0466427157f45b873500c0fe7886f8
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
$ docker pull neurodebian@sha256:9b74c3202ff1d28a9bc492b31b8ea9e8c9b9be6b63bcb68e0aa15fe63e173047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59704925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733c6cc1679ff8846e1c2db00fdfa0a14c44d7830f4ddbc5241391dc645b802f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:11 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9443e90dd36b4d7df0ce4d2bd3a9f86ccde7df420c85200869452e1d2c310a3f`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 10.3 MB (10294066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b311040279a30f28e966f2a5f173993093cbd64887ef01d6e4aaa7d6c49715d4`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8afd3a0920f39400ad7fb5ad3a3d14689c9cc1c7252860a938da81870f71c5`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118da0436bfad5757b22eb7483dfb8d4caa8dce58fda3d5e745f38892404501a`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 90.4 KB (90387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaade245ece996568fb7645f92a893e7db0b8361b850a93fccfd2a9d94a7675c`  
		Last Modified: Thu, 11 Jun 2026 00:46:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:28e7c75fee510a7acd4fc200e0d667d9cfd91e9ab8cca5e946e378b1b1e4ec9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2eca42e82561b2771d46a87c47c776316b6e839cd802e995555cbfc8465b7`

```dockerfile
```

-	Layers:
	-	`sha256:36cd5b6c3434365f2cf71c0b9bd5700b02ac52aca67b173355b3f58bc1f7948c`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 3.6 MB (3614204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4b92efa6ac90e31135660a7259903bca1ded723e7162654d117bc591dd1faa`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4f735a295bf56114dc844067c8559b447376008a394f05dc7bfa19b3cedb5fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59851751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1fe4fe93d83961ba13a917f6bc125e566db9df7f299c05d3b878ae060062c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:47:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607d619e0dd73deeb9db2b25df205732643c98352d9d7155abdaa4c445585b7`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 10.1 MB (10079193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f03c6928c07168f2bf548e6930872e19baf37abc1cf0af526897654a7d8b4b`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac685d980ae5b64951b7260afeea4aff7557f31fd69a01a970bbbb9446a664b`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0675ff08b6519b01acde1fd7cae45036ddd625bd1f8ad29726f13b0c2d8e9550`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 91.0 KB (91040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf2d6bd6dd274b0fc66d385da6ef377cbbf87c7b53b2ffd1d82140014e913c5`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a992e0d49e73cfc21fa6db8235421e67f6a92ebdb3674d279e7dbbb82500f94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472593d75487081cd96f86808b920d371d5794341e8330a5b48716f70fa189a6`

```dockerfile
```

-	Layers:
	-	`sha256:e942ca8eb7f884ac336651d2badfbba2ae0e1c3b2707ceb693a8dafcfed43268`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 3.6 MB (3615094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a70c74b7bec526e65bb31fe6513941cd08cd11448342af81a777e368b4903c`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ba55fdf29b76d9a6fa3fcc409bbd8b25ca5da3b0b13997a30956548b570f4eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61397904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da215c6f0c8bbf5f29e85a3b18a4a168e3f9553a236d8b28fdf5cc034dbe57f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e738cb1ceb88ca93b48e46391fca14a2453c6b28bf04b3f259957845d2c1285`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 10.5 MB (10468197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3813de1d4b6737b778cb0481960ad48ab76a08b846ba22ecc73667dd9b0be5`  
		Last Modified: Thu, 11 Jun 2026 00:46:25 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5a5db62ce6cc0853e2fbd0c2e8b7fb72243739d8e72332ac093939d5bf056`  
		Last Modified: Thu, 11 Jun 2026 00:46:25 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92a3c19bfcf828486f3d3d24bc65e7437d50bdcd54dd7faa442507acd9d6df6`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 90.8 KB (90796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662812f973b46690ce7067465584113462b5024e4883fa7e369c49fa3f84702`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:44f16607b3a5a7c4f7d6d76c92f2a6e911daa38609723e409e3e2ac59a9c15af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfa1cf9f73b3e9d51454fc87de8e5a66a7e3332691e74f4cf0852e92b4fc61a`

```dockerfile
```

-	Layers:
	-	`sha256:e1f89e434cba8fb4d15664a2a2521718c5372c01aa9e91b27a3b96090417cd8e`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 3.6 MB (3612152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f80982c64577a8144c703637517361a23b157ec5d3538836f1ea2e98208d9d4`  
		Last Modified: Thu, 11 Jun 2026 00:46:25 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:a50cc336e20a764cd963952e7c8d29ffdaf44286f332042da8001adb23a53499
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
$ docker pull neurodebian@sha256:a9560d4b868b489de7cc083ebc56092bae1a8be0b98d429f8823f2881b80e3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60270784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee40384bed7687c3fde3550aa90fe0bf52fb225a6ea762db63f9aba9cb10b4e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:46:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5721d6b62cfc7a7bfa692b95ea547e4ea39b5e2bfe1bd3e1a88886f80c2846e4`  
		Last Modified: Wed, 10 Jun 2026 23:40:06 GMT  
		Size: 48.8 MB (48779274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dd20d64a6c9c73fdbdd9abec84fecd075db437c4798b0bef377514410abb8e`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 11.4 MB (11399228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb2d7895f6cc503a3c75f0ab087eb2584e6322fc057533fb4e00c0b3b1f4472`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288413eea6b9f9875d894a238c3011a38834b38013491f522118fc98a55435f2`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fc3b9def0538c4c122e90bb4d4867322832d167cd48eef7f34b0b680916a59`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 89.4 KB (89380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:732c33527b8b7880c98718d0d8514d7c0b57027ffb9301500e3dcc54364be44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c09e1a49472b4e52cda50b589839475bf6161a29ea40e0ef47be682d70457fb`

```dockerfile
```

-	Layers:
	-	`sha256:b852ad2779cb9865bbb16d2e1eeb08e6b790460a01f952ca78414a56d41cfb68`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 3.6 MB (3562578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cba46853a915a467431c01953255c08713eaf58bd037c7c07e8bdb0f02b66f9d`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:eb0803a087f9dd2a0452cc49b4c1f2068e993fb49d8c8fa477e3e5a428629100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59981823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885a2677d3ede8cfc1255a17497f7bb3c0e4a2a108dbc98852d0f00c83b7e6f9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:47:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dbdf5115192d6ba17e54d5f2d3cd16e18cba052a9281223f09caff8a3d00462b`  
		Last Modified: Wed, 10 Jun 2026 23:40:03 GMT  
		Size: 48.8 MB (48795608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a795a3ba9535eccc0edd2ea21f47aeddf42a3a46cdb85280817a4355306194`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 11.1 MB (11093292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6008b62a31c2fbb1a2977ee676c7578c105279fdaa473fd968ddd3384d3af4`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd26e10e2b3776525cd5efaed604687ef1481c14bb311ebbb49825f60e5ccaa8`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0328ad9cb5fdce2ee901dcf0f9eb71c48d8280e5da2c5ec0b260dd3f08d497`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 90.0 KB (90022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d84fa4d0588b23eaa115f89023172a606234d7a493c3ca52c7dce95ba2d79582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2caba5e2d2f83631946694397423d270d2dddd19dc9521cf2d36a4876d0e462`

```dockerfile
```

-	Layers:
	-	`sha256:faa1a3015fb7d8a9813079851b447a5fc3aa38284b01ce089368481b034ca413`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 3.6 MB (3567283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4cba479120802c02d469950a86bb842bfae0700093bd27406c8702aceaae337`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; 386

```console
$ docker pull neurodebian@sha256:bbffa1bd869a4e9d65db7c1b0dd07339fd9386da0609c1cb034b0781c106ae31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61798673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56222e02abc1cc73d9e73d9e0e32ae195aad8c02e4969cb73d949f053e7cb8aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:46:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6a4be7a6be3ed3c4d92863f22edf1e7aa21046c79f8c96f534040141953aff3`  
		Last Modified: Wed, 10 Jun 2026 23:40:24 GMT  
		Size: 50.1 MB (50076810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbd140d2127fdfd9c232ed33b621b07bbed40f4963bd2b993623d39d97b9902`  
		Last Modified: Thu, 11 Jun 2026 00:46:38 GMT  
		Size: 11.6 MB (11629307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94017d4e25c5d8373a5357a0308db71819426070d5f4b9271b34b8a5fda4b0c4`  
		Last Modified: Thu, 11 Jun 2026 00:46:37 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ec5ad79fc64e2d05acf5c43a5ccf41d7a8a2deed1cf2a1bcd108f1752bd624`  
		Last Modified: Thu, 11 Jun 2026 00:46:37 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcca141c6b524c2209a88f0639b3fa4bed54440bebd8d43e515b96a54eb254d`  
		Last Modified: Thu, 11 Jun 2026 00:46:37 GMT  
		Size: 89.7 KB (89653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f2d165b4710ec4c5b81914974e3af4daf7f15d5f3cd3ef35fd598ded2bbc4ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a044606ea432cc5a812b1bc3c4a10d7f2dda86d2ab761c045bb302eb4ce5a5f`

```dockerfile
```

-	Layers:
	-	`sha256:362a4c99421d747069d17ef85f9df927093a7af634aa2df6d81d064b6c5894d0`  
		Last Modified: Thu, 11 Jun 2026 00:46:38 GMT  
		Size: 3.6 MB (3560528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a20fddc90098bb0d6cdebbcb87264c7c9ce653aa53c026edbf70f278ef558eb8`  
		Last Modified: Thu, 11 Jun 2026 00:46:37 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:37264e9014e928cf0bfda64869302438443988e6d0b8c9d6005e7f60d6cfffbc
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
$ docker pull neurodebian@sha256:798c059e8dc4c8074ba03a170658b96b1b6def955002bdb1bd5abd315fe3319d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60271205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:967f1f20d5f480494e6014001acbc38aff48d42d4ec0ac6351768fd541058d66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:46:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:16 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:19 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:19 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5721d6b62cfc7a7bfa692b95ea547e4ea39b5e2bfe1bd3e1a88886f80c2846e4`  
		Last Modified: Wed, 10 Jun 2026 23:40:06 GMT  
		Size: 48.8 MB (48779274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a95da46269214aaa1d7237827dc71f5b5d8069dfd47fc510bc12bfd608acd7`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 11.4 MB (11399216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb2d7895f6cc503a3c75f0ab087eb2584e6322fc057533fb4e00c0b3b1f4472`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288413eea6b9f9875d894a238c3011a38834b38013491f522118fc98a55435f2`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411295c6069be613044d1319c9f54b3590cdc5e10b3aace199bb072cfd62be68`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 89.4 KB (89366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc95558a2b42225eb9e88d79e8becb9d84ddd839869c67835da9b77b53233ce2`  
		Last Modified: Thu, 11 Jun 2026 00:46:28 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cc82c554bf9c7436fcda1864d1b7a76221113c13842dc5020f4610325e81ea5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3578572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b68e3571054ad0151dfcb082a8a66da630e7142baf98899dcc74e926c517fa1`

```dockerfile
```

-	Layers:
	-	`sha256:335aad9da067ca64dacd08bd25766189ee283be0697c324e298c4d29de9d600b`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 3.6 MB (3562614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929848b26f9d1ea5e95bdd50689a4efd60d82cf1efcfba8397db62fc8458812`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 16.0 KB (15958 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c2fffa659dea9ac21c972d44d982d9e92fed478e02cea8d27d65902ed0acb2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59982196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca3b0896e8a800b0c4b4953ce852818802be1e08c89be74b5e5b3b28cba052f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:47:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:dbdf5115192d6ba17e54d5f2d3cd16e18cba052a9281223f09caff8a3d00462b`  
		Last Modified: Wed, 10 Jun 2026 23:40:03 GMT  
		Size: 48.8 MB (48795608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521f1c00810ede4b0c96988ae55b20fa413409b82a6e190d89816b03fc5a765f`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 11.1 MB (11093241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3426a165d11ed3c48c1235f57c55e908c0038c6711048075e2f52785512761`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd26e10e2b3776525cd5efaed604687ef1481c14bb311ebbb49825f60e5ccaa8`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca93d601b6a3978a4bbc3b5591aede6efdf93a3ddb432a1761c30cbf0be0a3d`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 90.0 KB (89999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6e5214750a7948bc5252a9accebd4699c3c518b3fe689bceefde2960613b2a`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1f94ce78ff663c717b15eda02d399f935a34aa0c328854c686ab9e4ab00b6c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3583418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341c8dd593efaf733c616fa33b61fe15cbbfb12102bc3f1d5a289ad3b9afc664`

```dockerfile
```

-	Layers:
	-	`sha256:815740f746f6fd00353b2cdf9ef1b64be736b95fadade3c0760410e8b8492e5e`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 3.6 MB (3567319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fced8e5795241aa8c06ee963dd4d74b0a962b1d76f736a720db51337099821a8`  
		Last Modified: Thu, 11 Jun 2026 00:48:02 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ac7573e1a964cedc92762f1764c74e516f1ad3746228ed0c08651568cdee1c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61799181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fddba0f6579ebe47327071a3618c0aba6177f33aeb4a8cea77ce865ae3d4f04`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:46:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:36 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d6a4be7a6be3ed3c4d92863f22edf1e7aa21046c79f8c96f534040141953aff3`  
		Last Modified: Wed, 10 Jun 2026 23:40:24 GMT  
		Size: 50.1 MB (50076810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b472a6d8b7727a486701a1080e4d0e8b17435c83bab23bd2ec2b916a22b5a7`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 11.6 MB (11629359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056b0eb9c4e41949da3ec5420b12975ae7a0907918f66ccfd3a65482da204979`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a07b7219afe18068ac7164b86637e0a1dccb746ed0acdb1b0278a72d506c09`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615ed529cf578cb6a5ab9693f16045ee70cd90a54524463364191b5ed9c2ad2a`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 89.7 KB (89662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde751c374c1d4871c1deed9148e8dd53e68ef7ea748a3ec4e9e6159cc6cd128`  
		Last Modified: Thu, 11 Jun 2026 00:46:44 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b041bd8f4c37b1374e71d2e430366895c2266d010e122ea2c8f86a72be2b3cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4077abd8c2df574289455d03f7a6c0bbd1a5fc03a069961dc263bbde41be797`

```dockerfile
```

-	Layers:
	-	`sha256:a0b3dfec3b714a0f3659f3df8424dac0141979ed49efd25ed4e92a8d5461d602`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 3.6 MB (3560564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a422575041a54c249ce448c1da2996daaad5e1140dcf52109f78af6c2fb992`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 15.9 KB (15928 bytes)  
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
$ docker pull neurodebian@sha256:9a1e78ff7194ccd99640b7d1d86bc7c8cb0466427157f45b873500c0fe7886f8
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
$ docker pull neurodebian@sha256:9b74c3202ff1d28a9bc492b31b8ea9e8c9b9be6b63bcb68e0aa15fe63e173047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59704925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733c6cc1679ff8846e1c2db00fdfa0a14c44d7830f4ddbc5241391dc645b802f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:11 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9443e90dd36b4d7df0ce4d2bd3a9f86ccde7df420c85200869452e1d2c310a3f`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 10.3 MB (10294066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b311040279a30f28e966f2a5f173993093cbd64887ef01d6e4aaa7d6c49715d4`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8afd3a0920f39400ad7fb5ad3a3d14689c9cc1c7252860a938da81870f71c5`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118da0436bfad5757b22eb7483dfb8d4caa8dce58fda3d5e745f38892404501a`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 90.4 KB (90387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaade245ece996568fb7645f92a893e7db0b8361b850a93fccfd2a9d94a7675c`  
		Last Modified: Thu, 11 Jun 2026 00:46:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:28e7c75fee510a7acd4fc200e0d667d9cfd91e9ab8cca5e946e378b1b1e4ec9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2eca42e82561b2771d46a87c47c776316b6e839cd802e995555cbfc8465b7`

```dockerfile
```

-	Layers:
	-	`sha256:36cd5b6c3434365f2cf71c0b9bd5700b02ac52aca67b173355b3f58bc1f7948c`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 3.6 MB (3614204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4b92efa6ac90e31135660a7259903bca1ded723e7162654d117bc591dd1faa`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4f735a295bf56114dc844067c8559b447376008a394f05dc7bfa19b3cedb5fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59851751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1fe4fe93d83961ba13a917f6bc125e566db9df7f299c05d3b878ae060062c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:47:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607d619e0dd73deeb9db2b25df205732643c98352d9d7155abdaa4c445585b7`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 10.1 MB (10079193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f03c6928c07168f2bf548e6930872e19baf37abc1cf0af526897654a7d8b4b`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac685d980ae5b64951b7260afeea4aff7557f31fd69a01a970bbbb9446a664b`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0675ff08b6519b01acde1fd7cae45036ddd625bd1f8ad29726f13b0c2d8e9550`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 91.0 KB (91040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf2d6bd6dd274b0fc66d385da6ef377cbbf87c7b53b2ffd1d82140014e913c5`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a992e0d49e73cfc21fa6db8235421e67f6a92ebdb3674d279e7dbbb82500f94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472593d75487081cd96f86808b920d371d5794341e8330a5b48716f70fa189a6`

```dockerfile
```

-	Layers:
	-	`sha256:e942ca8eb7f884ac336651d2badfbba2ae0e1c3b2707ceb693a8dafcfed43268`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 3.6 MB (3615094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a70c74b7bec526e65bb31fe6513941cd08cd11448342af81a777e368b4903c`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ba55fdf29b76d9a6fa3fcc409bbd8b25ca5da3b0b13997a30956548b570f4eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61397904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da215c6f0c8bbf5f29e85a3b18a4a168e3f9553a236d8b28fdf5cc034dbe57f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e738cb1ceb88ca93b48e46391fca14a2453c6b28bf04b3f259957845d2c1285`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 10.5 MB (10468197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3813de1d4b6737b778cb0481960ad48ab76a08b846ba22ecc73667dd9b0be5`  
		Last Modified: Thu, 11 Jun 2026 00:46:25 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5a5db62ce6cc0853e2fbd0c2e8b7fb72243739d8e72332ac093939d5bf056`  
		Last Modified: Thu, 11 Jun 2026 00:46:25 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92a3c19bfcf828486f3d3d24bc65e7437d50bdcd54dd7faa442507acd9d6df6`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 90.8 KB (90796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662812f973b46690ce7067465584113462b5024e4883fa7e369c49fa3f84702`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:44f16607b3a5a7c4f7d6d76c92f2a6e911daa38609723e409e3e2ac59a9c15af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfa1cf9f73b3e9d51454fc87de8e5a66a7e3332691e74f4cf0852e92b4fc61a`

```dockerfile
```

-	Layers:
	-	`sha256:e1f89e434cba8fb4d15664a2a2521718c5372c01aa9e91b27a3b96090417cd8e`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 3.6 MB (3612152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f80982c64577a8144c703637517361a23b157ec5d3538836f1ea2e98208d9d4`  
		Last Modified: Thu, 11 Jun 2026 00:46:25 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:65004333205e19d05539cccbe46a3d577ff04794119b52be74dc32abf570ec7a
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
$ docker pull neurodebian@sha256:ae287380c24223f57660150b7da71cdf4eb84270f620831b0d4efac16f74bd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60294002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90e26bb2b04a99e8f535ff8fbed986163a3ee4d770e5e51d70b77820d74abe0b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:46:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:29 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bdd122fd70d19475cad994fa0bd624dc1524d2143c57c7c1f3f9e23fe40ddb0a`  
		Last Modified: Wed, 10 Jun 2026 23:40:10 GMT  
		Size: 48.8 MB (48801212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacf64a88439387b1c0eba23bcec29b6672837e395a0256976be744e995b3bad`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 11.4 MB (11400511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38a7e10f751eff090cf764c44d9e5001c1570eb8ebb01f32410ca89370ebe19`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ac08f4684991e1cefeb83a94bca5bd073dd502e21dba3d833745e37cff385d`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf49cc7e499d5a430ab888113f99e87e81e51393c55d0894e75cc2769295e6c`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 89.4 KB (89379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2fd3e58ad348dcac794bb0741eeeb37199ca52fda2ccf9b746d91970d2dbc571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8420cb3d0490b285b0fc8a31fc14d839e9c7aad6895787277fc06946bf1e51f3`

```dockerfile
```

-	Layers:
	-	`sha256:90f7545d094de3aa23907f01f890bc1935142a968c4e73f6e4fe2f64f889331c`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 3.6 MB (3561769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2b880c5f3b746d7c60d4781081d48c83adc6a95cefdb282dc6a4fb808c6148f`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b52d4611b34a2bc915f7402bf07b7c0ed611ac77167147a1fa579671e533f20f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60005272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8e718cf8135c7a7dbaf28de21e4a599de708b5e737331e8374f470d67a4325`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:48:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:48:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:48:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f216cfca8681658c5c6a7a8b3653ba38754d80730e4760fa07c5af0c77dbafdc`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 11.1 MB (11093783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c245f33d403e20631db07d85c7949c38d447f59151983e6ccd177844c70b2da`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f20446e70687694e58be96b1e8dee8abbbffc8a86361dfef1e2c9933a7e172`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c777496248e833ab9ee2388720300b95430fe7f379a711f6d0d603d2bb9dced`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 90.0 KB (90032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:af5bdee722473dfe53afb51c4052273ce01321dc38891ad423a777cd3eed1950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3580503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e931479eeae972f6d3393eb1fc52d4600aaed088476de284ac64185006b8aaf7`

```dockerfile
```

-	Layers:
	-	`sha256:c667f4c018696b0a60c8e913790fd50a5b7b27861cbb09b150589add99b16396`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 3.6 MB (3566474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0311325e77f970962d6ac2bd4c71cc3ede59589e9266f3b563c2edb9fff8ae2`  
		Last Modified: Thu, 11 Jun 2026 00:48:20 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:db288142cd7d03a71eb88cbd8fb467d9f3ca884ad08869345b93321c856a5b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61827288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fbd236a7dc10eb614ef42c3c69921831585f25fd8f562daf47b4f118f10e9e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:46:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:47 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a32252638de41825057387ef73b5d4de843fa9726fc243c76636da258263cc3f`  
		Last Modified: Wed, 10 Jun 2026 23:40:40 GMT  
		Size: 50.1 MB (50105399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8850820ce6bf3267c5c91d1c3f79a074463665cbda406eaaf4872b08667ff727`  
		Last Modified: Thu, 11 Jun 2026 00:46:56 GMT  
		Size: 11.6 MB (11629301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59643bfcfdc7a07558763212315a14034a0faf6cf046e4b65a4278d1a4350591`  
		Last Modified: Thu, 11 Jun 2026 00:46:55 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb1e2903a9eeea6791fb0d68c37cbf3059a41978f7908ce04558f3867b97445`  
		Last Modified: Thu, 11 Jun 2026 00:46:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2661a0f39769c7e60845ac8a9aa10871123e6734e4b74318b0c3fbd81ef8bed4`  
		Last Modified: Thu, 11 Jun 2026 00:46:55 GMT  
		Size: 89.7 KB (89684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0f22da5598552d7251e27607c800ca0ba8ad53f7423889371241c2eac8a99ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c747cbce286794184c87c0320eb3afd3967006a7f54c4d662c9c2419e8968315`

```dockerfile
```

-	Layers:
	-	`sha256:047574fa684a7608b854d9059022f5fd70b7d4348bbaae00257b8d38cd15d2e4`  
		Last Modified: Thu, 11 Jun 2026 00:46:55 GMT  
		Size: 3.6 MB (3559720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d689c1ab4807b8753e1d617ae91ee28b3eddcd00c7b493fdd4a2e51ba1357d`  
		Last Modified: Thu, 11 Jun 2026 00:46:55 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:790f3f37a60945a425379d9bbf7514dc38a6bde3459cc4fe95d2d2564c6300b0
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
$ docker pull neurodebian@sha256:e668949d99fdcaa776069a8dcabcc7f92c06280add74b6d2d44a986fffa458f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60294471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9baa11b9e2318de0932554bc6ce85f2b70bd43b4c6f63259ef1faef75e61a3ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:46:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bdd122fd70d19475cad994fa0bd624dc1524d2143c57c7c1f3f9e23fe40ddb0a`  
		Last Modified: Wed, 10 Jun 2026 23:40:10 GMT  
		Size: 48.8 MB (48801212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385a8564f579f25f1fa0091862faf1667f9d99bb57eb2d8d7d231e688a08ffb0`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 11.4 MB (11400554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fe6276a8f981a19cd267153efbd887e1960863e79415cc84f633d529be36ca`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f3d40ae033a5792a73f7042effbbbdb2c11e9c80d8e9242cb1bbc60372528f`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511c208cfebfaa8583dca48701b1de701916b85218fa6ca8d48a1ccf959989b3`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 89.4 KB (89383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfc8b61e4dc23cb303141daa73f93b5c3785184d487db0082a1eb1d756342b9`  
		Last Modified: Thu, 11 Jun 2026 00:46:43 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c50a6fe2698c56337d96ba11f7b43114a0ddc059e6d6ff43299875cb2d8b4d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a4a2e0f7bb8530b6dff8701621957b864d0a23b2ae31c1ac981467dfbfd4cf`

```dockerfile
```

-	Layers:
	-	`sha256:da398cbf39c8fb41c6479f9a87ceb3f464cdfe56c93863ecbd56d3d42ebe1ed9`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 3.6 MB (3561805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9b4303c20ddff766e93d5ff40b68f06cf15ff76fb8dc3071c8f5a7447912547`  
		Last Modified: Thu, 11 Jun 2026 00:46:42 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6b76a8baa5e5703b782986d03054140bb5f9c51a3f219cd3bbdfdb6e097b48b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60005540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ea7c2561889afebbba75f286331ba1118bdb81f98d193534f48e1183424a4d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:48:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:48:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:48:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:48:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f29437b24e4b4586fe357af3b6e2a0cd2bb4523e6dee73c3187fe1b261eeea`  
		Last Modified: Thu, 11 Jun 2026 00:48:31 GMT  
		Size: 11.1 MB (11093649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b2458ad9ad4a37d3870ee0be7b56fffd958237766aa0449ca76f2346e8d821`  
		Last Modified: Thu, 11 Jun 2026 00:48:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8c8f9d3d89dd50d605bacf929e2688267d93bf13ee4564d5dc39d004c7fff9`  
		Last Modified: Thu, 11 Jun 2026 00:48:31 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41c04a7fefd630d6ba41d8dea40c9bbf56c5bf080b069b449f6cfb2690e5431`  
		Last Modified: Thu, 11 Jun 2026 00:48:30 GMT  
		Size: 90.0 KB (90015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0f18be5600368b9aa251fc55917de6789bae5c62a407fac437536f84b7172f`  
		Last Modified: Thu, 11 Jun 2026 00:48:32 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c6ed9d6eb6d7be9b9b47cb3806493b95923bc062ac7e26b861f609264ac51edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3582581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2245c7f439db7a99cfc8d20357dc097d1272f3b902a7752a9aab0b8d48463c`

```dockerfile
```

-	Layers:
	-	`sha256:6cdc695a05d47bf2586613a897a82ca07f5b1afb508fc9deb9ae266b89134533`  
		Last Modified: Thu, 11 Jun 2026 00:48:31 GMT  
		Size: 3.6 MB (3566510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8984122e7bf9687e2fe6539b0f98adfb683076c15eae433a55c4b06a7e94f35`  
		Last Modified: Thu, 11 Jun 2026 00:48:30 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4c8cd0da45340fc16fe6fa498ab416e5612d234ee5454eed60ef2fbaada4a6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61827691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e041853d010700cdb92fa67e280982338cf0fbcd3ac4e17bb362c4ccb6352ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:46:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a32252638de41825057387ef73b5d4de843fa9726fc243c76636da258263cc3f`  
		Last Modified: Wed, 10 Jun 2026 23:40:40 GMT  
		Size: 50.1 MB (50105399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9985fd0b18c9239f0ab31829976aeb109a49fd849bfd9a60236038042b9bf44e`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 11.6 MB (11629273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea4f4dda4b51b86cdf991c17ef19d9ec22bd23e1f83387c2a0a394af0171e60`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f14c15c1caaffdf6e712eb73cd67310f04db2b7f87d96808966faa0f9afbab3`  
		Last Modified: Thu, 11 Jun 2026 00:47:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f9dabe2674a7076fb586746dadf0251dafb312b34d09feedd1acac58026bd4`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 89.7 KB (89702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a8a745ea0d9c0a691481e4260da9b612159d1fbde02376618d61a65cdb6a6f`  
		Last Modified: Thu, 11 Jun 2026 00:47:06 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c64d7bcacbbd0d616fce071f4378b1e5fef0e66a3b2d7ecda1ff220339bfad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc0c1b4b48591db8ce8d09e831614dcc796be68744723ba7f71ada9c5148b78`

```dockerfile
```

-	Layers:
	-	`sha256:61ad8ecc20551e74c4214e7eb23ae8b0f075b0a45a9ce71574ecb7f55ab81464`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 3.6 MB (3559756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34f2c487982789bd00ebaf87c0a4bb2e5538523f01eecb2517a960e0f1e6db19`  
		Last Modified: Thu, 11 Jun 2026 00:47:05 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:57bf3a66ea98601be74660a4a7797276d3badc3b433b84be07822173c01a7d42
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
$ docker pull neurodebian@sha256:0f10c55925c7daa6986178bd929a59c328e73b14d33e638b933d343ada75bffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59704614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32d537529d69d344d0eb896c9f97232c3d86f4bf97570473e3fc59c980acd6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab8a23fa26af0a8cc76053873ce7f2f4972656e8f0fce2094d6a666e3be7772`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 10.3 MB (10294155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6332aa2ff8b6e8865f809e22829bc2fa69b14363252518a815b841a1f1e96903`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d07151946d2a0886dd871c29d5af1c81bcfc8b58b498e8e10191f9018b2566`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9b52337e56a0c8b560c3f38b88a4043b2f81e9b7787f91fe3e15d9df02b94f`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 90.4 KB (90436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:253280c8c43c2b210aa41b9932a9d65d4b1937e1cc592889552a887ddf9d0c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d78b8f51492931a4c575295e525c37e9368e45303be897d48ac5cc9e6ddb266`

```dockerfile
```

-	Layers:
	-	`sha256:391817222b355feaf88eba1d4e2ec5b9e43b8395e7ba2cdde60a0a46a41e5a18`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 3.6 MB (3614164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a2708db03fe47ab7d21c2de25cd8c8bbb2d7ac4d9a3dba9f126c55a2f3bbfea`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4d733fa6ff08050595170e47efccfe107fa7fbf6d920d166495fa1ac2c2bfa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59851304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4c08654723853eb5602234bae5feb235f2fdf5852a0bd21e23861a7de27bc5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:47:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8663f66a97521bf18781b6a8ebb14fef9360e63aed5744a8826c46b6e955ff`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 10.1 MB (10079209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898f78772560357ad8f1982fcc959f06700ed89aae96a065a560a906236d8cf7`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646d242c23c90ed9667d2fbcfebc5fa2ff61e602411007d42b67903ef19ea3d`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0366805b83dc22dbed788828fe85a31e7d2925bac97277ead3789e69ec670bcb`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 91.0 KB (91025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d09bad896d54687ddebe1648238e4e9ecffc205b3697da54d7432644747a8ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee44725acd45051b6ab2baa0a69bb183c202e5f01eb0bb9fa46dec30e9fb02e`

```dockerfile
```

-	Layers:
	-	`sha256:6b665e7bbede387f1cc367505a144eced1dcf9237f7bfe90cddd631df2f08035`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 3.6 MB (3615054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b382e18a90a184f236343b396eace7da5a3cb00b4f6f8f273322d39f408687a`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:69272e86cbda3b80360145b7035894858f8cfbea157d8ecb1dc592ff7f95706d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61397435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d156e7bcf79c18dd9eba9d5b14acb9798c93bfe93b50dec402f6a054d7cd0a4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96262f3a6afeeffe35b7ae82c64e4411332dadbfc81b4e151d05d1ae95ef0e5f`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 10.5 MB (10468195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9803f3a3cbbb4fa8e0527752d2fe446742a844b364b659fd3471c1412c7de7ae`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328489f211ae28ef4a19ffab0576631bbadef0b960df6e7cb234806fed854cbb`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480857bb2368ea3670f8a8b5dfce2c9a13b1b59414ec77b0efa36c938bfdac56`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 90.8 KB (90776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fcb451aa5bef61bed7700ef1c06e8f31e746f268f0ac340de5e44aad5b38345e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd93bbcf1197ba8c7cdbf851083e591e6ed5f96d4de0e879b2dfc99dc636cdc`

```dockerfile
```

-	Layers:
	-	`sha256:098c6beadc9d4944f26eb9ae6a78f28d6e0c48a29e9e44e2c14f28ded1b73576`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 3.6 MB (3612112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b5e77ec315284c66927105a56c707e59dd8c54f41091f07f9381cc23d970ce`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:9a1e78ff7194ccd99640b7d1d86bc7c8cb0466427157f45b873500c0fe7886f8
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
$ docker pull neurodebian@sha256:9b74c3202ff1d28a9bc492b31b8ea9e8c9b9be6b63bcb68e0aa15fe63e173047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59704925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733c6cc1679ff8846e1c2db00fdfa0a14c44d7830f4ddbc5241391dc645b802f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:11 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9443e90dd36b4d7df0ce4d2bd3a9f86ccde7df420c85200869452e1d2c310a3f`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 10.3 MB (10294066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b311040279a30f28e966f2a5f173993093cbd64887ef01d6e4aaa7d6c49715d4`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8afd3a0920f39400ad7fb5ad3a3d14689c9cc1c7252860a938da81870f71c5`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118da0436bfad5757b22eb7483dfb8d4caa8dce58fda3d5e745f38892404501a`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 90.4 KB (90387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaade245ece996568fb7645f92a893e7db0b8361b850a93fccfd2a9d94a7675c`  
		Last Modified: Thu, 11 Jun 2026 00:46:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:28e7c75fee510a7acd4fc200e0d667d9cfd91e9ab8cca5e946e378b1b1e4ec9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2eca42e82561b2771d46a87c47c776316b6e839cd802e995555cbfc8465b7`

```dockerfile
```

-	Layers:
	-	`sha256:36cd5b6c3434365f2cf71c0b9bd5700b02ac52aca67b173355b3f58bc1f7948c`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 3.6 MB (3614204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4b92efa6ac90e31135660a7259903bca1ded723e7162654d117bc591dd1faa`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4f735a295bf56114dc844067c8559b447376008a394f05dc7bfa19b3cedb5fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59851751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1fe4fe93d83961ba13a917f6bc125e566db9df7f299c05d3b878ae060062c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:47:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607d619e0dd73deeb9db2b25df205732643c98352d9d7155abdaa4c445585b7`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 10.1 MB (10079193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f03c6928c07168f2bf548e6930872e19baf37abc1cf0af526897654a7d8b4b`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac685d980ae5b64951b7260afeea4aff7557f31fd69a01a970bbbb9446a664b`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0675ff08b6519b01acde1fd7cae45036ddd625bd1f8ad29726f13b0c2d8e9550`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 91.0 KB (91040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf2d6bd6dd274b0fc66d385da6ef377cbbf87c7b53b2ffd1d82140014e913c5`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a992e0d49e73cfc21fa6db8235421e67f6a92ebdb3674d279e7dbbb82500f94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472593d75487081cd96f86808b920d371d5794341e8330a5b48716f70fa189a6`

```dockerfile
```

-	Layers:
	-	`sha256:e942ca8eb7f884ac336651d2badfbba2ae0e1c3b2707ceb693a8dafcfed43268`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 3.6 MB (3615094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a70c74b7bec526e65bb31fe6513941cd08cd11448342af81a777e368b4903c`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ba55fdf29b76d9a6fa3fcc409bbd8b25ca5da3b0b13997a30956548b570f4eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61397904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da215c6f0c8bbf5f29e85a3b18a4a168e3f9553a236d8b28fdf5cc034dbe57f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e738cb1ceb88ca93b48e46391fca14a2453c6b28bf04b3f259957845d2c1285`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 10.5 MB (10468197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3813de1d4b6737b778cb0481960ad48ab76a08b846ba22ecc73667dd9b0be5`  
		Last Modified: Thu, 11 Jun 2026 00:46:25 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5a5db62ce6cc0853e2fbd0c2e8b7fb72243739d8e72332ac093939d5bf056`  
		Last Modified: Thu, 11 Jun 2026 00:46:25 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92a3c19bfcf828486f3d3d24bc65e7437d50bdcd54dd7faa442507acd9d6df6`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 90.8 KB (90796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662812f973b46690ce7067465584113462b5024e4883fa7e369c49fa3f84702`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:44f16607b3a5a7c4f7d6d76c92f2a6e911daa38609723e409e3e2ac59a9c15af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfa1cf9f73b3e9d51454fc87de8e5a66a7e3332691e74f4cf0852e92b4fc61a`

```dockerfile
```

-	Layers:
	-	`sha256:e1f89e434cba8fb4d15664a2a2521718c5372c01aa9e91b27a3b96090417cd8e`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 3.6 MB (3612152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f80982c64577a8144c703637517361a23b157ec5d3538836f1ea2e98208d9d4`  
		Last Modified: Thu, 11 Jun 2026 00:46:25 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
