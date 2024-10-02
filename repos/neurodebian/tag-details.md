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
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd130`](#neurodebiannd130)
-	[`neurodebian:nd130-non-free`](#neurodebiannd130-non-free)
-	[`neurodebian:nd20.04`](#neurodebiannd2004)
-	[`neurodebian:nd20.04-non-free`](#neurodebiannd2004-non-free)
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
$ docker pull neurodebian@sha256:8bac7605cb4e07975ae616c6bc573d5504ebb9e0fd4a658c7523008554f1bbfd
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
$ docker pull neurodebian@sha256:c8664a96795b166095b204fa54dbf0f48b5e6e4978643e8b763bb7c05b2dae1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb0c3b1ce774b89533bd30de564feff9ba4dc520f740d46ae423bc2653ea8f0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffec6389bcbf6537d5f6a384d29b76f4fcfd4cc7522491bbc0e1e95e5c3eb722`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 11.3 MB (11266554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc93f4d62109e8a5d2f564ccd69d7bef7d80a32aa7a410bc6363888daa816a5`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d017be4b2180bbb56d6789d0382e398768bd1b3e8f19973efa1578db0296c75`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9ced1a1a098fd13cc5a63fe69b80bbeb7435fa6bbdc8331b130d68a6b87ba8`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 93.1 KB (93127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9f8466efd911fc1b98e6f430f3b1aab449dad4490a17f294deec380b6afab020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78075cb443a7999c807e8fb4699f6f1c0086f081b30c2d93be94680e05390300`

```dockerfile
```

-	Layers:
	-	`sha256:f1b4f0b3cc2badb64712a79a6915ffb632e856347854c52ff14ad2fe57846900`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 3.9 MB (3924252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69c5d58fafb7ead8986e2f8e1a098fcb901d06df3df04978588846236a6382f`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4fdd7ad22ad58df80dd10606683277af81322d374dbe350d38dbce0bfaa51734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6e1d9ae380cac43aaec2a703a38e8ca2e44cdcd644eb36255f1f87d3bc82da`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18398593d4c19c61fc775e0592d0d8a432ee6462e9a8f7b8810a361333b485d`  
		Last Modified: Fri, 27 Sep 2024 15:28:29 GMT  
		Size: 11.2 MB (11232110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621de790ca72d0c42672a6a2ac731249ca406772328f8c3edd3d594f1f53f616`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b740e3d498ccc528d88bab38ee97183e394cdd50200b197502891dfb79ad4d1`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d5924f9901e2c8fcebcabc13a32cffd7e420213b1cf345f0e63ad1b70c157a`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 93.4 KB (93387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f6ddc4bef2a814ec4ed7ce137104c95355755aac94051ed2584e34c15d404348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec69833b161c4bfa7f5aae8110f38fd2534d0eb4d60817d5964fba9c789e44fe`

```dockerfile
```

-	Layers:
	-	`sha256:87a491eec926a01d51a0debed8c655c03fb443b6f954214fb0edf652bbdc5aa2`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 3.9 MB (3924505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be7392fcbd46d7179e2d77dd05520aba986c86d512f530902813ccf43c8a0fc0`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:6f06396dc77df5aac7320e6bbcf41a9994b200af40152dc6f2b1beb413f4da7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62360889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b454d9deddbaabc3b5e02402eaa5f36a6be6259d44d6f8f72b5635b284103c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b1802271ac5d573454388f4b70f4fbf4c217201a945a93e0682016e0b72363`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 11.7 MB (11689049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf63c47b065cbd544258be1ebb9c5677961a78ea9665467b070dd9e49b0a84`  
		Last Modified: Fri, 27 Sep 2024 09:04:13 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb09482f4c8db1430432478c291d716f8650fcca2c06c1617dff7feed224325`  
		Last Modified: Fri, 27 Sep 2024 09:04:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8069bf4bd59ce87b9f7bddcc213dee0cc9fab0c5b2fe2d66a271fea87b0a7ff`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 93.2 KB (93214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c53a5d4284554f73cee25e179165b4524528fc92fe1463caeb2763650227007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e75c7c021c242c4245bbbc2862e7a9c31a87afb3a2c0c6aa8d03f52be423472`

```dockerfile
```

-	Layers:
	-	`sha256:f3893b520c615b816af2a0700758df15452667d74c4ffe1ba97bc012e3f200fd`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 3.9 MB (3922169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c45cdb3c5a2d2164a75474bb428b49b69c600c314b0d44c6e356ffeb5d3dfe1`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:4c31540c4a47420fa5e9600cc5da4d3453175aa5a25a37860129f18bb5876da6
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
$ docker pull neurodebian@sha256:b48d6272400457ab71668d983cf66e3677f8df417b405a16646a77398ba08d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60917184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f348d52d0a30c0875589c2a9119a552d0157a52592558ed41ab0bfd3e3c77a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9051ff7592ebdf57081bea4813d054f179c10baf88e8edb1b1eb0503dc57a398`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 11.3 MB (11266587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b7d938f0d1f711b7744833ba75d25ef22f306b38fed3f791d43c283332c29d`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d8d64e9f86a243cadef1fab89c4bc283c6ab4b4d7acd3c713da0063cfbc7f8`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45240937643905b587fa479f7122727e4da480a63dc938c4d4e680049d4fd520`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 93.1 KB (93133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca5c0ab742bba3e582138550e8f5870657e878200808229861aaeff5b17eddd`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8be6a251f01d60f7c79d8354d52a880631b39d9b5e7686fa2e26ec2df80aeac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcc537a8cec282d091e002e6f0a1e677c36051a6c61478e3e8eb0454c94a884`

```dockerfile
```

-	Layers:
	-	`sha256:11250ff6b4c7bc963acdf419c612cf7ee613254e2246c5b3d2a533583138de69`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 3.9 MB (3924292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50bdef147161d65fa6df17b8f42d4d1bc566bd2ca0efeceae14bea0caf771bed`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1bf2ad888a05ef807d67508a9f6926ad1786f54786c4acea708e393305d3e908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f9c69de5373e2c9f69164910ff1d44257dc2596d2f0d7d3cfc67a0c584d68c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18398593d4c19c61fc775e0592d0d8a432ee6462e9a8f7b8810a361333b485d`  
		Last Modified: Fri, 27 Sep 2024 15:28:29 GMT  
		Size: 11.2 MB (11232110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621de790ca72d0c42672a6a2ac731249ca406772328f8c3edd3d594f1f53f616`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b740e3d498ccc528d88bab38ee97183e394cdd50200b197502891dfb79ad4d1`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d5924f9901e2c8fcebcabc13a32cffd7e420213b1cf345f0e63ad1b70c157a`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 93.4 KB (93387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c007be9f3baa091742dc1aebd0ae0a6e3cea7a4b810f0b8e43f15eb877896e70`  
		Last Modified: Fri, 27 Sep 2024 15:28:52 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a5037ed0757501393c215f764e0ae006eb95c5b18a1b83e29856a21a86f904f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a21e19ca8c5ff905338308a88e40f5a3e1df607f032725531e296e5de2077dd`

```dockerfile
```

-	Layers:
	-	`sha256:b824964735f0d18f63657b8d91305ccedf77807feae3a5161f131d57be3295f5`  
		Last Modified: Fri, 27 Sep 2024 15:28:52 GMT  
		Size: 3.9 MB (3924545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c864375c20088fe814094af1263b5d464fc676e095599494c207463caa2967`  
		Last Modified: Fri, 27 Sep 2024 15:28:51 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bee081949cf57ceaecb3135aafb92afa4570a49981637c3417a17b32403c4a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57394c8777f825902239d56e9004bd008fafe81bc34862a6a73b3642af4eb655`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ab7367486539cc2d6c35ad3018714f9ff4f1c097f65527882cda7ba2c4c48b`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 11.7 MB (11689049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47dd5e31a5ba70c7cbc3d81c9ac82a70b05d13aa142f333016a30c7c728d6fa`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92a1687c24021dd12f46d38e9eefe255336343473332498d5da65afd4da1a80`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109102859cc8b950870f53e366f28846943d199769ba5a2dd573058136b2dfa4`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 93.2 KB (93204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d3b5d7d64269625fae11e5e669b00c675b3beec6db5b29738bc55b876f48a9`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8125292b6b7515ef1a26096899be0b264288a183078b74c5c9be5b43c677a730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c852d546e62718c86e124fd2031e53b49ffc7e18124bd0ea1aa2c86f1c2c99`

```dockerfile
```

-	Layers:
	-	`sha256:5c1069382d1d1988c0a11261be34df46f7f5c1a229c8c1b93d7cc8711f94f922`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 3.9 MB (3922209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724f78771fbec7e294d02422660c6c79e3db21f706773c18f10c9c77d42bb59b`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:a17b10e295be5c5b338b4b17803adbddd3acf9afac4e31acb5f095fba51d5866
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
$ docker pull neurodebian@sha256:74236c937c5b037ad60fc432ebc254c1e580993ab29f478a9b300daa626bb915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3adae40b3c213aa1ae0712e9060a41aaf499df6ccdbd746f19223f35ec6827e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfb0a6060b8b0998db2e10892443ef142934b0ef2830beee3e3e7cfe4514bd9`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 11.1 MB (11104992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd7fed0f8636459064f9f964188e4826469f925ed396341fb68ce62fb315377`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d5910828d32d02f070dba4e7945868769def79e0f9902c66830608d68aa481`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be85d64ab216d005b467f6308b5615d673e978f19c236082f992bdaf4ad93bc8`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 101.2 KB (101161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0bc6eb256921208f76e8b28589cf11cc18adca9cfe24fed607071a4661686462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56e3b7a65d4bc869c344278645e4b1720f997dbd966ddf3e536b74e2805f59`

```dockerfile
```

-	Layers:
	-	`sha256:29d56d4669ef53c2f9a8c6678f2b9a0ae5aca6a32c1944ff8aec60b1b297320a`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 4.2 MB (4223717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2583fb1f95ef1984a58e4586f792e94a80ff50ed736cd3b33c28bfd5be697f3f`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c1b307e80b0cca5d827f4fabca1b7fa68b2b5355d5eb816307e602219abbe3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64942766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501b37618933e9a7aa46b7820cff2e1cf2ee72529381c2b78215280f7c3c780a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fa9c49640a7a5333f3fea4cc6c5d10542a152ab8c5aa29cf3ce4e3238ef84`  
		Last Modified: Fri, 27 Sep 2024 15:27:29 GMT  
		Size: 11.1 MB (11105819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378f59383dbb4959374257665f63dc2bbb1a4b567e04ad57c7117f913c3b10ff`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e727a822f540249948c259f1aa14d33f2495d123ea9d71a46ae031dad3f2dfa`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605ac67eae58773d4ea2de3dbfe0fcd786ceb75b482cf2659454fc879955761a`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7496f749100a45e28a3cdf8b2c59c5ad5939df1baa7881b1e7db4809f87848af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a7e6672fbfd29db7a51de1d8a00b2c6c2945bee3352f8756d399494e8cf9b1`

```dockerfile
```

-	Layers:
	-	`sha256:f876fc9bb684c370d22243f71b7ab52c17c25168ec40a4e9baa82d45f345d9b3`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 4.2 MB (4223322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9967484c6a14ab3b598f1bd55d7bcb3796edf2c9752a473fc9b46a4c7375920`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 13.8 KB (13758 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:a0c3413d700fac3c2e42b3f3fb0a8094e86e55c396b294d4ef45cd257bf8017f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3913d138958cf56a3033fa33d1450a349acb1c26ffa3932174a0318873c12c24`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318fc0dffd0bbcbfbc3e8d1d7f4d6def79401d87b65941185a17d9d1621c4d51`  
		Last Modified: Fri, 27 Sep 2024 09:03:34 GMT  
		Size: 11.5 MB (11500045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e44d55f6736d033b09c6de41794ac0876512c0254e0a7cf845c02611523d3c`  
		Last Modified: Fri, 27 Sep 2024 09:03:34 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608e2076f93b2b34b8ddf699dc8a3daba615a06aa6d734ba3626867ae98b79ae`  
		Last Modified: Fri, 27 Sep 2024 09:03:34 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbe956af8ef5282640aadbcb531f993aaa65aa2e8435fdbddbb51a6e2d06d0`  
		Last Modified: Fri, 27 Sep 2024 09:03:34 GMT  
		Size: 101.1 KB (101088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7b541d7d372bff707cee02bc3310942652abaabf7ebe5e122303bc7d905eb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4233629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c40a7055f6236b69bbb7bf4f19b33a2076cfe8f5e18477da2785386a059de7`

```dockerfile
```

-	Layers:
	-	`sha256:4c19184f99cc6404558624d58879f7507e207ce417c6a94e67504645b15ab9af`  
		Last Modified: Fri, 27 Sep 2024 09:03:34 GMT  
		Size: 4.2 MB (4220177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecaccf43adcb981ab7c46da53e39947d5b9f1db41289ffadab1f6e97e1bea1c4`  
		Last Modified: Fri, 27 Sep 2024 09:03:34 GMT  
		Size: 13.5 KB (13452 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:dd06c71912068499b62ddd2f8d1c48c8aa05aec07878fb276f79252feba79ac2
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
$ docker pull neurodebian@sha256:7f5088398c7f011e8097a29cd701f675a1080cc500196391c4b6794022b8a9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdfcd7ff9d894bb20277f777c30089d05e6bee15278a392b84be6561a744ef7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781057eafc4c33d419ac01788ae0f4708e6c8b9b42b4c0efa58265084ba5c337`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 11.1 MB (11105021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca9f0b8cb73e5762cef8aad324e1ee6e0a020348d975fcf9a1b709b4c3fe925`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297557466a2385d9af17a8e5e0acc6b5876c310f8717e40aa3661b00dcd1149`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0755dc4a01fa569e141b166f027a20446a1bbb2e769b0548ef4ddb92083bae`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 101.2 KB (101182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a4483fab3e6ba8071f141c5125469123ab6dcbd2c5b2d7d419005489a71053`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2af657dc55a7ddc9f14035295ebd2f147736d2fb0fab02638830682adf4479ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc49ad2aa5db65dc48910c228539fe3ce366263eeafc62176ba3c49fa58b7e06`

```dockerfile
```

-	Layers:
	-	`sha256:1c2d01c9aa9c1e38c274b4f75b13960fb53e6223ec48d13adfc84fb8419989a8`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 4.2 MB (4223753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad25678c39510df32b23c842ca8358063f7fc4eb6fc0befe7ae6135f725771ce`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cc787f8d6b0791659d572b06a5fa980290626e3bc3a421b9acb3f75d23234707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64943125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cccdc0177ad7abcdb5602cd2d8f3a5013b464ca19336c1f0bfa4ba7e2c0bf60`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fa9c49640a7a5333f3fea4cc6c5d10542a152ab8c5aa29cf3ce4e3238ef84`  
		Last Modified: Fri, 27 Sep 2024 15:27:29 GMT  
		Size: 11.1 MB (11105819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378f59383dbb4959374257665f63dc2bbb1a4b567e04ad57c7117f913c3b10ff`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e727a822f540249948c259f1aa14d33f2495d123ea9d71a46ae031dad3f2dfa`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605ac67eae58773d4ea2de3dbfe0fcd786ceb75b482cf2659454fc879955761a`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b2d89999965d2abe6c3956d01d734a83db7ed22ad6c44fca949da5078f4f62`  
		Last Modified: Fri, 27 Sep 2024 15:27:50 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:21e3436984d7178e7def5e7e4340ac7bd783a5bb22e2932260859cfb022df1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01956dd7fe8e6a0fa7565f0faeb9c3a9e40c6dedb154aff74302501140fee8f`

```dockerfile
```

-	Layers:
	-	`sha256:739059f3f6be9798d36c6fb5e157680422f75fadd6056dda7b1d8c65264fe269`  
		Last Modified: Fri, 27 Sep 2024 15:27:51 GMT  
		Size: 4.2 MB (4223358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d13d210d4aedef2e5938d87c57ae119eea6ea34c896e00f27667ae499ba66f8d`  
		Last Modified: Fri, 27 Sep 2024 15:27:50 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a847974e93e911586570ee1d7e8f6254ae6933e4ff60a5a4eafc0a59e752e40f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67680032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76250fa78ef11613685bfbfcd9362128fbf96968b7ef1346163d86c43dba7967`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef6e128fe253e9e92df878bdf6679d19c4c795a0ad5b4e2763d98dc38d52397`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 11.5 MB (11500106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ec30e15c8071ee1dd2c285d9e9180cbd765125f72712cde12b1e30609cd7d`  
		Last Modified: Fri, 27 Sep 2024 09:03:39 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3df436804194d27d1205da4b1b5b92b11b5e9dd37789901d1bb7054b49941e`  
		Last Modified: Fri, 27 Sep 2024 09:03:39 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec155c5566b8bfd54cb4ff20ed3df4ebe932bc0414cdb7a5a1686c9f2943d4c4`  
		Last Modified: Fri, 27 Sep 2024 09:03:39 GMT  
		Size: 101.1 KB (101076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f013ea1ffa93929d5f3fc804f87adaa36164ab369bb17de0daf168773747c7e`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0b8a94eaa507d01e918eb51c1691cc17c03ac6f5f39042bdd87316f86c7f4526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f97f8b8941aa00985d47d71e1ca26088ec2cf233814c1fcca8257344690427`

```dockerfile
```

-	Layers:
	-	`sha256:c13ac2c7f8d63495afdaca68139efd3b9e9e5363a3043024ca9ad151326111ac`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 4.2 MB (4220213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44468e83d9ce5d88b4eb7b5dc138e35d4e8586e0dddd16c82cdd5f9c45b443fb`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 15.5 KB (15484 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:bccb027a7ee6016c0a98560e51caf98f68f947b948222c7bbcf90884f08a2f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:33321bd67f5c4092724b3cd7c84390a44effe62f516fa528cf835068466ea750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7712d68e6912e2dadede90156365035ed83ba26b955c56a9b6743bb689ebb8d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930f573b2289c54f50a7b09f6d9445bd27f0cb1a48348833d5e6e0986d46da3f`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 5.4 MB (5360160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56884c4edd0cbca3617ec0ab7f4eb2f2db8594b9b0cac16d907a38c0fc6c5a`  
		Last Modified: Wed, 02 Oct 2024 01:58:10 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dfcba298667a425ac0464a6b4a731a25e47be2f31f0a80c882d1cca00ebebe`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779280839ac6c6073401d79c852c9d696e3eace1c131d11108e53c493df947ab`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 105.2 KB (105242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:47328a35876e2dd7e853351f6352f66a75141ba91a935a0c3cbc331e91ef99d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc66bf80d0b2dda8634ee73d7770e19baf3a5feea2a59971ada23eb86492d478`

```dockerfile
```

-	Layers:
	-	`sha256:d332d6862683e5d1b3ab2a9b95808810e88d2ff242476a6404c0dba1e73252f4`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 2.0 MB (2002651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a09899de5c9a6030d4c0a7373ef9c207b4660e941a72ad0126b2268b979db356`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d037a60f85e3420771a09c5095426ed874d09300fbede4cb3573387b012275cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685e5e5da9030956235506036387fc62634485c42ed3aca5b1ae6bceba9b54a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5841415efed23c119a8469194131c18b87ee67753517a99d8fc01f06cf966fb8`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 5.3 MB (5340450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954c9f376345cca87bb2306dc082bd633d25c1c0b7a51281e45f302caa307554`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72af8df908af1001e54236b76d58c51b3eea7a5c7a3619097d305d4f775eac99`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c55ac7fc0e12deb1a3c7a55803df01877dbd826510bb33faf283e7a8300e28`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 105.3 KB (105291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f8f3f5dcdbb8d4a376f39a0a97981fabb7e6ba9a91bb9dab61851e0cfeb3aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbfc5c521f200740f1d1f0487bdb2674953bdd1ee81f47919ed971ca0ad86e5`

```dockerfile
```

-	Layers:
	-	`sha256:29772dc3da77b6599d1cbf04610642086bf317e3c95fe67f41ac60c212428c71`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 2.0 MB (2002879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a53c8b58100f31c59ec8233e0b9ba2b19ba33bc61cb1ea4e2294612be841cb1`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:a7973bf466790b8143043a176b3091e833236acf366247067448fe76903bc28d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6af11b8f91c1a72ab168ecc733cdf05682ec84fe424909677f7444517041cc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2773923a12eabf66248c89d3038c5f614157d96249c9515c71931da49b44c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e75c7a65b7f181c600367e7b795f2ec28ccac576cda7fb3aec11e9a2e86292`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 5.4 MB (5360302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e715970f91fb31540499b96725af5116ff4522ca91c5fa45aab0984fa63fbd`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012a6a853bcbc781468c32453ea7f08d0cbf446b023487c8a755e36c2e614afe`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54deb2d52bb8bdab1846b4807802dd24c6f5ff2919e2c4a348f443a82593ec07`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 105.3 KB (105257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693067606a22cfad4fd9f685006963d17c5ee91ec5bc8876a72eb23105e11040`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:eed7c7d0767f4c9c7379afb4406bfdf0e112d2f11af2856e01407139922f4b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f877252e27fa23a05113835795f85e3ef88fa5655ef443533c839c7bdedca7`

```dockerfile
```

-	Layers:
	-	`sha256:ac5945033dc85752c1e4c94b04d2a3ec607a05fb2e3c1229393bd4df8283b354`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 2.0 MB (2002687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3ef73ab5b3c258347d3cd74684999217465ffcfa8275049c86c9935596271ad`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:286183413af81badc42fff3f1c2c214b8e8380bc918faf10b56c7c7cfe3fb2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695fac297d77ea2b21f8c7b53fbbea39564422ecba2f82c08c2686b366931d5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5841415efed23c119a8469194131c18b87ee67753517a99d8fc01f06cf966fb8`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 5.3 MB (5340450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954c9f376345cca87bb2306dc082bd633d25c1c0b7a51281e45f302caa307554`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72af8df908af1001e54236b76d58c51b3eea7a5c7a3619097d305d4f775eac99`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c55ac7fc0e12deb1a3c7a55803df01877dbd826510bb33faf283e7a8300e28`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 105.3 KB (105291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e2477417bfa5f2fc5d0d63f9edff178409808de0c35bc34a1a757cfd524b4b`  
		Last Modified: Wed, 02 Oct 2024 03:26:53 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:493435274faa21682794a4be271b392285df984c551ddf0ef2741788492ede79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733485ab064e66c3a9f58370711f69892507e10abaf72855a6398b005916abaf`

```dockerfile
```

-	Layers:
	-	`sha256:a91ff4a74015d47addfa03915b086097cd2d93574003f5e670f729a8a494f445`  
		Last Modified: Wed, 02 Oct 2024 03:26:53 GMT  
		Size: 2.0 MB (2002915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b91e53da7f867d443449320933fcf94640d01084aaa5509e655b8ba07395ff`  
		Last Modified: Wed, 02 Oct 2024 03:26:52 GMT  
		Size: 15.8 KB (15775 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:8cd25968c7a8dda57e86f5f31179a392780c365d049c245f1563df254a345b6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:b5e2ad2679d21dfb98319132904ff13815643d741d29c2cbd61f795d2cfce2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03035b5fafec30a11ccaf9e676191d30bf2a93a2c961ae50bcdeae21ecee68c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e5fc20939f49ca46aaa63fda94b740a46522034dd33a99dc846c2ab47da385`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 3.6 MB (3622683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d7c12d3dff8024cc7a65a06760eefef7523e92d4ab01561da2876474be6e25`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257f9b0966cd5484318ba1e2300bcf4102ad856d15cf79307d6575cb919be75d`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25429882efb06104ffa477fe41e22a29ad87a1b8b5a97eddc221fb3cfb85bc29`  
		Last Modified: Tue, 17 Sep 2024 00:58:50 GMT  
		Size: 110.0 KB (110041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d732e29d091ef7f0e630eef553f727bdf00995f77c7dcc07b0561d4792f4341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb4b42740c8b876bb56d509444cd2d22fd632ea9c6254cf4af8ef60cb72b5aa`

```dockerfile
```

-	Layers:
	-	`sha256:46449a2a17035de35151d0f04752a18008bd77cdb9bd76b7f1465ab848857267`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 2.0 MB (2041055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229f62c1b512cec8166de552b1e0085eb7526f3474781a15c9cfadf62c2436da`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2e8ddba19dffa270b72c0c17efca5bea22c862945352f06ad9391ca69ae180ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e64399ffc86a2a302a5f8b07efe84fa560a195e25878c4a52e8f5d97367769e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ce4fcc7ac84933f63a18dcc1f51edb6a54d593241a9ad9eda2da49c4a0a93`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 3.6 MB (3594202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420d28ea54fd4f14398ac3479d15abc9d09b6fdfd86904d39445315fa9ccd4a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89798e75750754cd749a20391aabd4a2982ab8ea03464d1069af684488290b27`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a706a92656db8d1c42d48439ae56eb9ef232cfcd87be0f53362d7da0045c9f6`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 110.2 KB (110158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:769792b0a9ae99abbe1b81296f09e1e53c2e662643848544f1a641d54f8b29bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ab15b050723ad8ecd0ff560efdd18d3d1451cbd92375f54cf16c418e647366`

```dockerfile
```

-	Layers:
	-	`sha256:2a92568efc9bccb357a48dc2f8cc5ef4f0d34112762744fc1408de6d45f8e34a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 2.0 MB (2041314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783fe908caebc3d7a05968a298b4c97dd56aff0cc5841272d2f31f8d0eac4efd`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:c35390a21d7dcdaa5248caedb0c2d1d3f2b9a31a1ccc6a5fd082bc8262ef35a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e45ad58f9dc146f7c58fee7c828c3c6831e76bdb9cf7020f9f7c9448d53671ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4ea79fb23e81c99deef7e3da0330d8995389a5ed5528314613545bbc38a650`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e444df7ecce18d9b6a39b30f8f893e46de9a6c8393753ceb73f80be5147d5e`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 3.6 MB (3622684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eb688a315dc9dc281db41ae45a5e1651f96d5b6b93100b8f6b3604a1b7be90`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18efaf2abf8b145da9341e025a8599685148d724adf71187513efcefdc1eb92b`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c03e7463fe28779caf76a60210e080067f4e00e4a28d1ef22b5f71aab3511f`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 110.0 KB (110044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a748ff3cbe6a5eed1e2b979d6648c667fb7a29be6b3e2bc14ea06d88519a0592`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:49d3a7c89f96056348bc2f29c7aaab1b27bde7d7755e5cea5fe7102dbc63a96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0141b248fd4a83635efee725ebffc6599bb6e48aedbb01287016be2df2e9e29d`

```dockerfile
```

-	Layers:
	-	`sha256:2aa3ae2b7c2d8c84a96d9dfae22e8bdbef344f1dea22754309dafd7d8ba3fa7f`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 2.0 MB (2041091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48b6d14af7ecf44b9066d810db720df1078da0e69b612cc31771ef41b2957b4a`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4a2bedc35b23fd303d37b492a4dcd265b749cc561bed81266ef4fd4f072ca3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cc596bfd27c527f722fd0f60344b7c29c0ede0e0215ca28663dd6f7b11334d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ce4fcc7ac84933f63a18dcc1f51edb6a54d593241a9ad9eda2da49c4a0a93`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 3.6 MB (3594202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420d28ea54fd4f14398ac3479d15abc9d09b6fdfd86904d39445315fa9ccd4a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89798e75750754cd749a20391aabd4a2982ab8ea03464d1069af684488290b27`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a706a92656db8d1c42d48439ae56eb9ef232cfcd87be0f53362d7da0045c9f6`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 110.2 KB (110158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0571d1820815c6ffe6445310d6d56c0904985a7a40ce55ea60111c7ab14c14af`  
		Last Modified: Tue, 17 Sep 2024 02:37:09 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15e423dc66f68b2fd18342bafd40c16c24df1ff2d5a105e3d23fe7a7b66e4859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae14030ec66c96db8f89c291fc02780ff4e9dd29fbe18b7deeb19f1a70811d83`

```dockerfile
```

-	Layers:
	-	`sha256:b8a537c7762547e63f17b420cb0912f491db0829af8089494798ac00e311b1a7`  
		Last Modified: Tue, 17 Sep 2024 02:37:09 GMT  
		Size: 2.0 MB (2041350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab7d3d2aaba018f1a288d03ac3c709c72564deb83d89ee6d4197767b31a448c9`  
		Last Modified: Tue, 17 Sep 2024 02:37:08 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:8bac7605cb4e07975ae616c6bc573d5504ebb9e0fd4a658c7523008554f1bbfd
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
$ docker pull neurodebian@sha256:c8664a96795b166095b204fa54dbf0f48b5e6e4978643e8b763bb7c05b2dae1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb0c3b1ce774b89533bd30de564feff9ba4dc520f740d46ae423bc2653ea8f0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffec6389bcbf6537d5f6a384d29b76f4fcfd4cc7522491bbc0e1e95e5c3eb722`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 11.3 MB (11266554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc93f4d62109e8a5d2f564ccd69d7bef7d80a32aa7a410bc6363888daa816a5`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d017be4b2180bbb56d6789d0382e398768bd1b3e8f19973efa1578db0296c75`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9ced1a1a098fd13cc5a63fe69b80bbeb7435fa6bbdc8331b130d68a6b87ba8`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 93.1 KB (93127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9f8466efd911fc1b98e6f430f3b1aab449dad4490a17f294deec380b6afab020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78075cb443a7999c807e8fb4699f6f1c0086f081b30c2d93be94680e05390300`

```dockerfile
```

-	Layers:
	-	`sha256:f1b4f0b3cc2badb64712a79a6915ffb632e856347854c52ff14ad2fe57846900`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 3.9 MB (3924252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69c5d58fafb7ead8986e2f8e1a098fcb901d06df3df04978588846236a6382f`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4fdd7ad22ad58df80dd10606683277af81322d374dbe350d38dbce0bfaa51734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6e1d9ae380cac43aaec2a703a38e8ca2e44cdcd644eb36255f1f87d3bc82da`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18398593d4c19c61fc775e0592d0d8a432ee6462e9a8f7b8810a361333b485d`  
		Last Modified: Fri, 27 Sep 2024 15:28:29 GMT  
		Size: 11.2 MB (11232110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621de790ca72d0c42672a6a2ac731249ca406772328f8c3edd3d594f1f53f616`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b740e3d498ccc528d88bab38ee97183e394cdd50200b197502891dfb79ad4d1`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d5924f9901e2c8fcebcabc13a32cffd7e420213b1cf345f0e63ad1b70c157a`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 93.4 KB (93387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f6ddc4bef2a814ec4ed7ce137104c95355755aac94051ed2584e34c15d404348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec69833b161c4bfa7f5aae8110f38fd2534d0eb4d60817d5964fba9c789e44fe`

```dockerfile
```

-	Layers:
	-	`sha256:87a491eec926a01d51a0debed8c655c03fb443b6f954214fb0edf652bbdc5aa2`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 3.9 MB (3924505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be7392fcbd46d7179e2d77dd05520aba986c86d512f530902813ccf43c8a0fc0`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:6f06396dc77df5aac7320e6bbcf41a9994b200af40152dc6f2b1beb413f4da7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62360889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b454d9deddbaabc3b5e02402eaa5f36a6be6259d44d6f8f72b5635b284103c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b1802271ac5d573454388f4b70f4fbf4c217201a945a93e0682016e0b72363`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 11.7 MB (11689049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf63c47b065cbd544258be1ebb9c5677961a78ea9665467b070dd9e49b0a84`  
		Last Modified: Fri, 27 Sep 2024 09:04:13 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb09482f4c8db1430432478c291d716f8650fcca2c06c1617dff7feed224325`  
		Last Modified: Fri, 27 Sep 2024 09:04:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8069bf4bd59ce87b9f7bddcc213dee0cc9fab0c5b2fe2d66a271fea87b0a7ff`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 93.2 KB (93214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c53a5d4284554f73cee25e179165b4524528fc92fe1463caeb2763650227007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e75c7c021c242c4245bbbc2862e7a9c31a87afb3a2c0c6aa8d03f52be423472`

```dockerfile
```

-	Layers:
	-	`sha256:f3893b520c615b816af2a0700758df15452667d74c4ffe1ba97bc012e3f200fd`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 3.9 MB (3922169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c45cdb3c5a2d2164a75474bb428b49b69c600c314b0d44c6e356ffeb5d3dfe1`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:2fddaff134d7ca3561871178fb51109683144c5ab6714a910003a8e6d0529a74
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
$ docker pull neurodebian@sha256:b386e80e587d4c20ecf466054c921cfdc72aeb7e5502867ccdd6bac2d19048a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59631144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd3b8259795f4e2160852925aa7fbb7231a7e252c92696a27950f0303853dce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f475f97deaabc6193a3fa858337fe06184e11ad6b13315ab6c7f971b66a9bafc`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 6.3 MB (6287931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd7fed0f8636459064f9f964188e4826469f925ed396341fb68ce62fb315377`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9fec776045441161388c757e0ad726b5ab7fbd3548e03d22fa42b727e9b782`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e369688a9f2e20897b0342be14d8b6941a03ccb9fe3bb98dd6ddcfe4445ba29e`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 91.2 KB (91192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:822f4de5100bb1994064afb1cdd414af5247d0e87c51bb88c46ca6bed2dc05f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a37cb43875ddc7aa01e78a71637c84ed0a436c94162a5790e7bea0b07cc237`

```dockerfile
```

-	Layers:
	-	`sha256:8c16a39d93e2e784f37f3cbea84302594e573b2693f64b8b370f24ccf9d50237`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 3.5 MB (3542033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:503cf70ae76d49b40790396ff4fbdf7b5f3daaf8b7ca72be3e759ad8e79bcacb`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 13.4 KB (13396 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:58bfc8026888335070afa0f72044cdd664f87cf4b9aa4f26c46385c610885f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59958772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c27c5792cf7ac400d363febafbd72ae89764d94df31e0957faa9b3e6c9d75a0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1707618fa9372fa7563234001ca06291da815e7c963e11719d290dcc36218024`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 6.3 MB (6270740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f92dac85afbe3987da72fdcff7499ef9a4bef39d0ea83f70ad579e421b2b1`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560ef25c1ef36b5b05dc1fd297de1698589349e5c080811754da6ab61635771b`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c67a14658f20791e7bebae65768af2451f13d17e95b1fa2ffbcd886802abb3b`  
		Last Modified: Fri, 27 Sep 2024 15:30:29 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7c1a8705a3413350f04f5a1d739bcdaf9577a3dcaba3ae5e1fa73e801f1f3060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53c580a80c3d5c1142885b2d547f026e496f73afa9516d55b492a1fd6e19aa3`

```dockerfile
```

-	Layers:
	-	`sha256:1236d910e711e1eb3ba937faaabef1ecbb76904d2147d9e237f9088e67d19501`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 3.5 MB (3543075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:383b288126aa4491dde9bca5f83e6279bfed5b9378f20d43c6e8ce721a75e949`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 13.7 KB (13671 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:8b1dc1ce8b5e8c3c34ccce9276cae70f96439f7a251b57b0d867562e4bb61c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60787262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb7e7e400856419fe6dcfba9476730e473001cdb7071f69bc5b2c70f24a3407`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7024eca1d35e4bf56690a81c3c1da49afee7ee27f30584fad073bcbea685f1d6`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 6.6 MB (6616326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e114f1c83df29eedcbf0676bad5078aa0615db7e6590d793bba0242195937669`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af5f6f47b991c182b45b50e4e4234c3e05547782c074a70ce4b5357d5c65900`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4229c9987c9434cde75f4619617a1b7d0b032708a7e4e5b415357838601309c`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 91.1 KB (91141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a1f9b369fb100fe194ca9bc43464f41bd1a6938a0a4815da6d5bc7a3189579ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d5866efd6fe0420224e5d5b639885adf9285db5a32cdaf1e966cba25ac2ebb`

```dockerfile
```

-	Layers:
	-	`sha256:a01afa53c29c892db3413fbdcc505cb39abe7e98a9a4ae0aa52c992c8d222303`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 3.5 MB (3539125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825884d205bb9ee0ceca812d5351085152132f2aa40ac72738cb9389bc0280d2`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 13.4 KB (13371 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:ba48eba3960765f9ccfea266dbdcdd86d7969d5deed37f153a35fb3c3222ec48
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
$ docker pull neurodebian@sha256:d6385e1c5bb68d77f40e026ed12ce430380e0e470b79c3f5ccfcaefc931a7b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59631607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e776c45bc6971cf609f11e7627976f0cfe662728ec87d1d886c00188c57a3a0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9932c03d465e07be767be6c6546a5fed0a8b713450009a5ae5548c52bc48a318`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 6.3 MB (6287955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa69fe5d2dbb347bcff9484d062465fb6e89f3a62b98b0ff196ed4d6799f673`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a23af6f8797bbef0455d9cd57276520bb04a5171c6203bc5a5ab3d4c88811a`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7138d16f6eeae6939426514f30129bb8016e17c4b9a24883b9440e1353b605`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 91.2 KB (91238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7203ca1b15919f54f52922c71b014e2624ac6f086d13bc8f501cb8858bbd344d`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:465aeca1f63b6dc525b5632ac6eea79aab7b6e34c2630a00249831526eda91d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4661d626714f88f865b4ae67b6b9f36d1602de01880fa1be9dfbfbd03c8d6cd`

```dockerfile
```

-	Layers:
	-	`sha256:e3e8d0820b5babfaf76c87b38d941bf58eb80d5250a65992b20ba00063fb637b`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 3.5 MB (3542069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65c24b8306901ac0ef9a25e84ad3f7abf256dc28c444897f5eea6145f6e792b`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8405eb81d4fb50f2e0ca8052e64751a2166bc5f44bd91dfd5f8364928076fca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59959165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b6fc36a6afd9830924df899db96464eff91a08d2fd009cb9b3d1088a5325f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1707618fa9372fa7563234001ca06291da815e7c963e11719d290dcc36218024`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 6.3 MB (6270740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f92dac85afbe3987da72fdcff7499ef9a4bef39d0ea83f70ad579e421b2b1`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560ef25c1ef36b5b05dc1fd297de1698589349e5c080811754da6ab61635771b`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c67a14658f20791e7bebae65768af2451f13d17e95b1fa2ffbcd886802abb3b`  
		Last Modified: Fri, 27 Sep 2024 15:30:29 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed1a0ff889a3d19ad950be2e4cb5a585ad9f69009887c6d58da8a5f7bfb5ed`  
		Last Modified: Fri, 27 Sep 2024 15:30:50 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0a0fb2b4c94881a145a88d8cc5d383cc5abffb8759ae1bbce2a56aa27dcc36e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fea4b5d7ea7ed8b0f6ce474f3f3263dd4b2b04738558dccdd3a704db4e1b350`

```dockerfile
```

-	Layers:
	-	`sha256:0b580fb68668f72246a5b77f9ceab789100d2ab9171a59039e674ffc2dafe1b0`  
		Last Modified: Fri, 27 Sep 2024 15:30:51 GMT  
		Size: 3.5 MB (3543111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ccb2a5d05b136f255c231e5f7370718d916c8cee58b2a409d354d4a1fc598a`  
		Last Modified: Fri, 27 Sep 2024 15:30:50 GMT  
		Size: 15.7 KB (15703 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6bf4e8373e3f6f87febe8b3d0319f5eae2cbcf139f17280c044d49b1e17ee457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60787647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9459a6b567f0d06c3aea1dd09d4385c4b2baaa27e9efbf9cf5d9c421d9fc8f84`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143cefad1d4d9c4b8fd3771c226b9090a09e67f6afcd789097a49ddb1f5932ba`  
		Last Modified: Fri, 27 Sep 2024 09:04:36 GMT  
		Size: 6.6 MB (6616300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977207288632e8201bfaa72034a65eb6f6ec8e61ff6b653d4fb73cf84ccc1d1`  
		Last Modified: Fri, 27 Sep 2024 09:04:35 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105d3548d214af15c097f1d54ad01ceb9ede39ebdea69818d3e71bc47b2839f7`  
		Last Modified: Fri, 27 Sep 2024 09:04:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5769ecbf94961298ff7e98bf0aa70190a17384c3bb8a9f690579e7c6fb520481`  
		Last Modified: Fri, 27 Sep 2024 09:04:36 GMT  
		Size: 91.2 KB (91162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9019696d4316f86af9fd804eb7624e648250c6fa998fed26656d8c9a25ff33`  
		Last Modified: Fri, 27 Sep 2024 09:04:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0f672898bb01b946177bbaccbffa0299ab4816defdfd5e2b5087ac9572102657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32aad4c936608553494658612be8bda4f99b108cea7bf09723c1e5efa39b98e6`

```dockerfile
```

-	Layers:
	-	`sha256:838300a747539cfb1dbc0eff0c046248c8620cf10416eaed02824c77f7b7cf3e`  
		Last Modified: Fri, 27 Sep 2024 09:04:36 GMT  
		Size: 3.5 MB (3539161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0678c291feb069de787e1099a828f38de4639e00c1c427de8e71d86ea3d06b98`  
		Last Modified: Fri, 27 Sep 2024 09:04:35 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:a17b10e295be5c5b338b4b17803adbddd3acf9afac4e31acb5f095fba51d5866
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
$ docker pull neurodebian@sha256:74236c937c5b037ad60fc432ebc254c1e580993ab29f478a9b300daa626bb915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3adae40b3c213aa1ae0712e9060a41aaf499df6ccdbd746f19223f35ec6827e4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfb0a6060b8b0998db2e10892443ef142934b0ef2830beee3e3e7cfe4514bd9`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 11.1 MB (11104992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd7fed0f8636459064f9f964188e4826469f925ed396341fb68ce62fb315377`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d5910828d32d02f070dba4e7945868769def79e0f9902c66830608d68aa481`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be85d64ab216d005b467f6308b5615d673e978f19c236082f992bdaf4ad93bc8`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 101.2 KB (101161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0bc6eb256921208f76e8b28589cf11cc18adca9cfe24fed607071a4661686462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c56e3b7a65d4bc869c344278645e4b1720f997dbd966ddf3e536b74e2805f59`

```dockerfile
```

-	Layers:
	-	`sha256:29d56d4669ef53c2f9a8c6678f2b9a0ae5aca6a32c1944ff8aec60b1b297320a`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 4.2 MB (4223717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2583fb1f95ef1984a58e4586f792e94a80ff50ed736cd3b33c28bfd5be697f3f`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c1b307e80b0cca5d827f4fabca1b7fa68b2b5355d5eb816307e602219abbe3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64942766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501b37618933e9a7aa46b7820cff2e1cf2ee72529381c2b78215280f7c3c780a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fa9c49640a7a5333f3fea4cc6c5d10542a152ab8c5aa29cf3ce4e3238ef84`  
		Last Modified: Fri, 27 Sep 2024 15:27:29 GMT  
		Size: 11.1 MB (11105819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378f59383dbb4959374257665f63dc2bbb1a4b567e04ad57c7117f913c3b10ff`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e727a822f540249948c259f1aa14d33f2495d123ea9d71a46ae031dad3f2dfa`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605ac67eae58773d4ea2de3dbfe0fcd786ceb75b482cf2659454fc879955761a`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7496f749100a45e28a3cdf8b2c59c5ad5939df1baa7881b1e7db4809f87848af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a7e6672fbfd29db7a51de1d8a00b2c6c2945bee3352f8756d399494e8cf9b1`

```dockerfile
```

-	Layers:
	-	`sha256:f876fc9bb684c370d22243f71b7ab52c17c25168ec40a4e9baa82d45f345d9b3`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 4.2 MB (4223322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9967484c6a14ab3b598f1bd55d7bcb3796edf2c9752a473fc9b46a4c7375920`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 13.8 KB (13758 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:a0c3413d700fac3c2e42b3f3fb0a8094e86e55c396b294d4ef45cd257bf8017f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67679625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3913d138958cf56a3033fa33d1450a349acb1c26ffa3932174a0318873c12c24`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318fc0dffd0bbcbfbc3e8d1d7f4d6def79401d87b65941185a17d9d1621c4d51`  
		Last Modified: Fri, 27 Sep 2024 09:03:34 GMT  
		Size: 11.5 MB (11500045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e44d55f6736d033b09c6de41794ac0876512c0254e0a7cf845c02611523d3c`  
		Last Modified: Fri, 27 Sep 2024 09:03:34 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608e2076f93b2b34b8ddf699dc8a3daba615a06aa6d734ba3626867ae98b79ae`  
		Last Modified: Fri, 27 Sep 2024 09:03:34 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dbe956af8ef5282640aadbcb531f993aaa65aa2e8435fdbddbb51a6e2d06d0`  
		Last Modified: Fri, 27 Sep 2024 09:03:34 GMT  
		Size: 101.1 KB (101088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7b541d7d372bff707cee02bc3310942652abaabf7ebe5e122303bc7d905eb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4233629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c40a7055f6236b69bbb7bf4f19b33a2076cfe8f5e18477da2785386a059de7`

```dockerfile
```

-	Layers:
	-	`sha256:4c19184f99cc6404558624d58879f7507e207ce417c6a94e67504645b15ab9af`  
		Last Modified: Fri, 27 Sep 2024 09:03:34 GMT  
		Size: 4.2 MB (4220177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecaccf43adcb981ab7c46da53e39947d5b9f1db41289ffadab1f6e97e1bea1c4`  
		Last Modified: Fri, 27 Sep 2024 09:03:34 GMT  
		Size: 13.5 KB (13452 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:dd06c71912068499b62ddd2f8d1c48c8aa05aec07878fb276f79252feba79ac2
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
$ docker pull neurodebian@sha256:7f5088398c7f011e8097a29cd701f675a1080cc500196391c4b6794022b8a9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdfcd7ff9d894bb20277f777c30089d05e6bee15278a392b84be6561a744ef7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781057eafc4c33d419ac01788ae0f4708e6c8b9b42b4c0efa58265084ba5c337`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 11.1 MB (11105021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca9f0b8cb73e5762cef8aad324e1ee6e0a020348d975fcf9a1b709b4c3fe925`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297557466a2385d9af17a8e5e0acc6b5876c310f8717e40aa3661b00dcd1149`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0755dc4a01fa569e141b166f027a20446a1bbb2e769b0548ef4ddb92083bae`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 101.2 KB (101182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a4483fab3e6ba8071f141c5125469123ab6dcbd2c5b2d7d419005489a71053`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2af657dc55a7ddc9f14035295ebd2f147736d2fb0fab02638830682adf4479ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc49ad2aa5db65dc48910c228539fe3ce366263eeafc62176ba3c49fa58b7e06`

```dockerfile
```

-	Layers:
	-	`sha256:1c2d01c9aa9c1e38c274b4f75b13960fb53e6223ec48d13adfc84fb8419989a8`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 4.2 MB (4223753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad25678c39510df32b23c842ca8358063f7fc4eb6fc0befe7ae6135f725771ce`  
		Last Modified: Fri, 27 Sep 2024 06:02:00 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cc787f8d6b0791659d572b06a5fa980290626e3bc3a421b9acb3f75d23234707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64943125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cccdc0177ad7abcdb5602cd2d8f3a5013b464ca19336c1f0bfa4ba7e2c0bf60`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fa9c49640a7a5333f3fea4cc6c5d10542a152ab8c5aa29cf3ce4e3238ef84`  
		Last Modified: Fri, 27 Sep 2024 15:27:29 GMT  
		Size: 11.1 MB (11105819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378f59383dbb4959374257665f63dc2bbb1a4b567e04ad57c7117f913c3b10ff`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e727a822f540249948c259f1aa14d33f2495d123ea9d71a46ae031dad3f2dfa`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605ac67eae58773d4ea2de3dbfe0fcd786ceb75b482cf2659454fc879955761a`  
		Last Modified: Fri, 27 Sep 2024 15:27:28 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b2d89999965d2abe6c3956d01d734a83db7ed22ad6c44fca949da5078f4f62`  
		Last Modified: Fri, 27 Sep 2024 15:27:50 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:21e3436984d7178e7def5e7e4340ac7bd783a5bb22e2932260859cfb022df1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01956dd7fe8e6a0fa7565f0faeb9c3a9e40c6dedb154aff74302501140fee8f`

```dockerfile
```

-	Layers:
	-	`sha256:739059f3f6be9798d36c6fb5e157680422f75fadd6056dda7b1d8c65264fe269`  
		Last Modified: Fri, 27 Sep 2024 15:27:51 GMT  
		Size: 4.2 MB (4223358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d13d210d4aedef2e5938d87c57ae119eea6ea34c896e00f27667ae499ba66f8d`  
		Last Modified: Fri, 27 Sep 2024 15:27:50 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:a847974e93e911586570ee1d7e8f6254ae6933e4ff60a5a4eafc0a59e752e40f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67680032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76250fa78ef11613685bfbfcd9362128fbf96968b7ef1346163d86c43dba7967`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9ca90aeebcd7771a308666e5154ca8307d717696c46983eb0669169bfed216e3 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bullseye main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a35b2c2d5fcba94057a1442288fbd23a6f80e5473970de13afb9ad2f096240c9`  
		Last Modified: Fri, 27 Sep 2024 07:27:26 GMT  
		Size: 56.1 MB (56076503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef6e128fe253e9e92df878bdf6679d19c4c795a0ad5b4e2763d98dc38d52397`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 11.5 MB (11500106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ec30e15c8071ee1dd2c285d9e9180cbd765125f72712cde12b1e30609cd7d`  
		Last Modified: Fri, 27 Sep 2024 09:03:39 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3df436804194d27d1205da4b1b5b92b11b5e9dd37789901d1bb7054b49941e`  
		Last Modified: Fri, 27 Sep 2024 09:03:39 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec155c5566b8bfd54cb4ff20ed3df4ebe932bc0414cdb7a5a1686c9f2943d4c4`  
		Last Modified: Fri, 27 Sep 2024 09:03:39 GMT  
		Size: 101.1 KB (101076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f013ea1ffa93929d5f3fc804f87adaa36164ab369bb17de0daf168773747c7e`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0b8a94eaa507d01e918eb51c1691cc17c03ac6f5f39042bdd87316f86c7f4526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f97f8b8941aa00985d47d71e1ca26088ec2cf233814c1fcca8257344690427`

```dockerfile
```

-	Layers:
	-	`sha256:c13ac2c7f8d63495afdaca68139efd3b9e9e5363a3043024ca9ad151326111ac`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 4.2 MB (4220213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44468e83d9ce5d88b4eb7b5dc138e35d4e8586e0dddd16c82cdd5f9c45b443fb`  
		Last Modified: Fri, 27 Sep 2024 09:03:40 GMT  
		Size: 15.5 KB (15484 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:8bac7605cb4e07975ae616c6bc573d5504ebb9e0fd4a658c7523008554f1bbfd
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
$ docker pull neurodebian@sha256:c8664a96795b166095b204fa54dbf0f48b5e6e4978643e8b763bb7c05b2dae1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60916721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb0c3b1ce774b89533bd30de564feff9ba4dc520f740d46ae423bc2653ea8f0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffec6389bcbf6537d5f6a384d29b76f4fcfd4cc7522491bbc0e1e95e5c3eb722`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 11.3 MB (11266554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc93f4d62109e8a5d2f564ccd69d7bef7d80a32aa7a410bc6363888daa816a5`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d017be4b2180bbb56d6789d0382e398768bd1b3e8f19973efa1578db0296c75`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9ced1a1a098fd13cc5a63fe69b80bbeb7435fa6bbdc8331b130d68a6b87ba8`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 93.1 KB (93127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9f8466efd911fc1b98e6f430f3b1aab449dad4490a17f294deec380b6afab020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78075cb443a7999c807e8fb4699f6f1c0086f081b30c2d93be94680e05390300`

```dockerfile
```

-	Layers:
	-	`sha256:f1b4f0b3cc2badb64712a79a6915ffb632e856347854c52ff14ad2fe57846900`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 3.9 MB (3924252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69c5d58fafb7ead8986e2f8e1a098fcb901d06df3df04978588846236a6382f`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4fdd7ad22ad58df80dd10606683277af81322d374dbe350d38dbce0bfaa51734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6e1d9ae380cac43aaec2a703a38e8ca2e44cdcd644eb36255f1f87d3bc82da`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18398593d4c19c61fc775e0592d0d8a432ee6462e9a8f7b8810a361333b485d`  
		Last Modified: Fri, 27 Sep 2024 15:28:29 GMT  
		Size: 11.2 MB (11232110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621de790ca72d0c42672a6a2ac731249ca406772328f8c3edd3d594f1f53f616`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b740e3d498ccc528d88bab38ee97183e394cdd50200b197502891dfb79ad4d1`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d5924f9901e2c8fcebcabc13a32cffd7e420213b1cf345f0e63ad1b70c157a`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 93.4 KB (93387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f6ddc4bef2a814ec4ed7ce137104c95355755aac94051ed2584e34c15d404348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec69833b161c4bfa7f5aae8110f38fd2534d0eb4d60817d5964fba9c789e44fe`

```dockerfile
```

-	Layers:
	-	`sha256:87a491eec926a01d51a0debed8c655c03fb443b6f954214fb0edf652bbdc5aa2`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 3.9 MB (3924505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be7392fcbd46d7179e2d77dd05520aba986c86d512f530902813ccf43c8a0fc0`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:6f06396dc77df5aac7320e6bbcf41a9994b200af40152dc6f2b1beb413f4da7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62360889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b454d9deddbaabc3b5e02402eaa5f36a6be6259d44d6f8f72b5635b284103c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b1802271ac5d573454388f4b70f4fbf4c217201a945a93e0682016e0b72363`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 11.7 MB (11689049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf63c47b065cbd544258be1ebb9c5677961a78ea9665467b070dd9e49b0a84`  
		Last Modified: Fri, 27 Sep 2024 09:04:13 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb09482f4c8db1430432478c291d716f8650fcca2c06c1617dff7feed224325`  
		Last Modified: Fri, 27 Sep 2024 09:04:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8069bf4bd59ce87b9f7bddcc213dee0cc9fab0c5b2fe2d66a271fea87b0a7ff`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 93.2 KB (93214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c53a5d4284554f73cee25e179165b4524528fc92fe1463caeb2763650227007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e75c7c021c242c4245bbbc2862e7a9c31a87afb3a2c0c6aa8d03f52be423472`

```dockerfile
```

-	Layers:
	-	`sha256:f3893b520c615b816af2a0700758df15452667d74c4ffe1ba97bc012e3f200fd`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 3.9 MB (3922169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c45cdb3c5a2d2164a75474bb428b49b69c600c314b0d44c6e356ffeb5d3dfe1`  
		Last Modified: Fri, 27 Sep 2024 09:04:14 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:4c31540c4a47420fa5e9600cc5da4d3453175aa5a25a37860129f18bb5876da6
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
$ docker pull neurodebian@sha256:b48d6272400457ab71668d983cf66e3677f8df417b405a16646a77398ba08d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60917184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f348d52d0a30c0875589c2a9119a552d0157a52592558ed41ab0bfd3e3c77a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9051ff7592ebdf57081bea4813d054f179c10baf88e8edb1b1eb0503dc57a398`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 11.3 MB (11266587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b7d938f0d1f711b7744833ba75d25ef22f306b38fed3f791d43c283332c29d`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d8d64e9f86a243cadef1fab89c4bc283c6ab4b4d7acd3c713da0063cfbc7f8`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45240937643905b587fa479f7122727e4da480a63dc938c4d4e680049d4fd520`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 93.1 KB (93133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca5c0ab742bba3e582138550e8f5870657e878200808229861aaeff5b17eddd`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8be6a251f01d60f7c79d8354d52a880631b39d9b5e7686fa2e26ec2df80aeac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcc537a8cec282d091e002e6f0a1e677c36051a6c61478e3e8eb0454c94a884`

```dockerfile
```

-	Layers:
	-	`sha256:11250ff6b4c7bc963acdf419c612cf7ee613254e2246c5b3d2a533583138de69`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 3.9 MB (3924292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50bdef147161d65fa6df17b8f42d4d1bc566bd2ca0efeceae14bea0caf771bed`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1bf2ad888a05ef807d67508a9f6926ad1786f54786c4acea708e393305d3e908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f9c69de5373e2c9f69164910ff1d44257dc2596d2f0d7d3cfc67a0c584d68c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18398593d4c19c61fc775e0592d0d8a432ee6462e9a8f7b8810a361333b485d`  
		Last Modified: Fri, 27 Sep 2024 15:28:29 GMT  
		Size: 11.2 MB (11232110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621de790ca72d0c42672a6a2ac731249ca406772328f8c3edd3d594f1f53f616`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b740e3d498ccc528d88bab38ee97183e394cdd50200b197502891dfb79ad4d1`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d5924f9901e2c8fcebcabc13a32cffd7e420213b1cf345f0e63ad1b70c157a`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 93.4 KB (93387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c007be9f3baa091742dc1aebd0ae0a6e3cea7a4b810f0b8e43f15eb877896e70`  
		Last Modified: Fri, 27 Sep 2024 15:28:52 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a5037ed0757501393c215f764e0ae006eb95c5b18a1b83e29856a21a86f904f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a21e19ca8c5ff905338308a88e40f5a3e1df607f032725531e296e5de2077dd`

```dockerfile
```

-	Layers:
	-	`sha256:b824964735f0d18f63657b8d91305ccedf77807feae3a5161f131d57be3295f5`  
		Last Modified: Fri, 27 Sep 2024 15:28:52 GMT  
		Size: 3.9 MB (3924545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c864375c20088fe814094af1263b5d464fc676e095599494c207463caa2967`  
		Last Modified: Fri, 27 Sep 2024 15:28:51 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bee081949cf57ceaecb3135aafb92afa4570a49981637c3417a17b32403c4a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57394c8777f825902239d56e9004bd008fafe81bc34862a6a73b3642af4eb655`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ab7367486539cc2d6c35ad3018714f9ff4f1c097f65527882cda7ba2c4c48b`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 11.7 MB (11689049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47dd5e31a5ba70c7cbc3d81c9ac82a70b05d13aa142f333016a30c7c728d6fa`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92a1687c24021dd12f46d38e9eefe255336343473332498d5da65afd4da1a80`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109102859cc8b950870f53e366f28846943d199769ba5a2dd573058136b2dfa4`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 93.2 KB (93204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d3b5d7d64269625fae11e5e669b00c675b3beec6db5b29738bc55b876f48a9`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8125292b6b7515ef1a26096899be0b264288a183078b74c5c9be5b43c677a730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c852d546e62718c86e124fd2031e53b49ffc7e18124bd0ea1aa2c86f1c2c99`

```dockerfile
```

-	Layers:
	-	`sha256:5c1069382d1d1988c0a11261be34df46f7f5c1a229c8c1b93d7cc8711f94f922`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 3.9 MB (3922209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724f78771fbec7e294d02422660c6c79e3db21f706773c18f10c9c77d42bb59b`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:2ae61745c247d4a8c99d7c354b96029634ef5bdc33733e5b2da4bda458519e67
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
$ docker pull neurodebian@sha256:95b63a109fc48f08237b877fb7cffa77d61e8df22bf5a4d7791c6efd09c4ef8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59551601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe81e410768586b5492844badee22adc900027cdac5b1acf7b379c3a674edf9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267a7066a313165935bf4eaaa8b9aae312287191547d2809b4ad34773e828a5`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 6.3 MB (6280356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aafa6a0b3025fd4652316fc5e3fe6ea05e11344376a905017040b9b985cbf99`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5cb880e6abea22dd0197684015c78086ca2948c36925678e0bfe28e3465c00`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04bfec15b0903df67fad5cf467dc6eb0ca7d397677702389607bc4733e4fd4b`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 91.2 KB (91221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3320834de6354f493c1d82186351c117223665c2f4ead32bb77e28427b89eee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f4e2f5a80b3b29afc74f04e8902b4b3c96a67b973d863de928e9726e32f9c8`

```dockerfile
```

-	Layers:
	-	`sha256:a20598f20436ee588f58c36585795a38adaac735394605a913cfb849c611cdeb`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 3.5 MB (3542857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1088db98014479771d8f0b3f7e94eab159c63f2a9e60f1ec223437d6c43cde04`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 13.4 KB (13445 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e045c8722a0d09fb924908b53557b97d64b916b1e5f7034d0d5f9fae67d5424a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59971880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00daadd7fcf3264abc9af0febccd9a59cf1e87e61f9c621afb2b7d106794a72`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23f6352824fd96c8c6b9838bfb904e1d7622f6bfe55b4c553cbf57ff483a36`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 6.3 MB (6261488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c0a4b3a15644d2d672fb44fb7ef754851b4b999ae2449d908d2bcb61514ef9`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620d3e5d3b378b7be79ad19c20bfcdc40531f8bf0971a901824a5e8be8263f1`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dce128f9ff7538248e2b5e2edcd6ca43e5feea1880d5b8a5290a08534c4e63`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 91.8 KB (91807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e2a4489f748889ef85e038e010495eefa34e6dca07c0894d71860b17f81eb310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626360cf88fe014495b6a029a63b3915e45368305e7c9a89bb1cb126907c91e9`

```dockerfile
```

-	Layers:
	-	`sha256:542bbb008b88b55265ccbbf2227938f846127e85ae4c7737802a2427e4e3107e`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 3.5 MB (3543899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2b4a94f394589d2ff4a612422d51f4eb84d2ddbc340e5d3f3f6fe458774f1c`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:98a7bcbd0f48607aba203c188fc584d3eb2eb44a7972910a22aab506ba373691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60755232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c978744990dfb8d2fefe9889d4703ac1fd7df41317879cb1f5a804f0ebbeaf7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d66646f8689060ae7f27f71816fcf459f852eb6ffd38e84da1a7977af7339f`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 6.6 MB (6602168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499956c24221d0887f18337dfa8a40a66ef78ea9e5070296934feb3bfd7d4a5d`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7116eda93782aaaf1afc07d9a8ba9c05b4a670e4895f060a253a01309244cbc`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0378a4a334d3b4cffb9cab48b3af6ec246e132da90a1800995016cf0bf3589c2`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 91.1 KB (91113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5361635eb47ff0c54139fb8d6f735ec9beb3988828092dd2fc5d3822db6a20eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749228d8c97e77fd9c454b59dade707186a17580df86a112f59d4294c25e7bb8`

```dockerfile
```

-	Layers:
	-	`sha256:d2d9148adae996142f2c520e17f483fbdc69659298daa1f02d4de07c78624137`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 3.5 MB (3539948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca28f4c520dba6f7987ca6746a6762200a61a360201024c7e94e22a89fda061f`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 13.4 KB (13420 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:ac61648e2563a3882383fad081f7de6996fe8f0fa8f9627a7e6bb0ba22288aa4
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
$ docker pull neurodebian@sha256:b1f199d03815d48bab11ecaeeacd81e4b2ac39a65aec462dfe763fb7529d3789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59551988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2893f89434279438492df27d6533582a320166e62af2248cf9c6b82914766bad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b19379603d098a671eb23697522873f6e76947ab42375d6822c5b0a4b6e809`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 6.3 MB (6280319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d0c24d6a8e14e4685405a8aaf43a7ab30aa29e0e1f283aa98a3d7449868222`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b7a35dec8f5dd32abe5be6043a56585b31eede2c1645904e76cc3a0482af1a`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d57f109b0de41f938f7878759736faec767e84dac89736dbe1be92533a9acae`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 91.2 KB (91225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e14b1c01ac31d1c91fa43ae686e8efeb1145d926c79601a652e7726aae0434b`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15c88b06753416b8a2d15c8ec809ecbdb6754fdf950e7164e5fecc310c199b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d92db2beeb0a5cd44fee711408904a5286a853e7f5a750d1ad67c91a5b7482a`

```dockerfile
```

-	Layers:
	-	`sha256:413a52dce277246c096155463956e28af6833eaec6061b111fe35a78cd5126dc`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 3.5 MB (3542893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b06258c0c750ae4d23c85317f3cf98f715296d195230122d9ca927b48c27b20`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:de9deb09a9c4a574733d8bf0ee9a8435ca602569681432e0e590c0293bd56639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59972303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd450a6e5b8e10e76c6e84376a6dabc34200b6d18baa5cf78ed1fe5c5eb2ea4b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23f6352824fd96c8c6b9838bfb904e1d7622f6bfe55b4c553cbf57ff483a36`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 6.3 MB (6261488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c0a4b3a15644d2d672fb44fb7ef754851b4b999ae2449d908d2bcb61514ef9`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620d3e5d3b378b7be79ad19c20bfcdc40531f8bf0971a901824a5e8be8263f1`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dce128f9ff7538248e2b5e2edcd6ca43e5feea1880d5b8a5290a08534c4e63`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 91.8 KB (91807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcc1f5af84d08060d7baeab3587692d4e1469721eaf97086e62e8a08e46bffe`  
		Last Modified: Fri, 27 Sep 2024 15:29:50 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c889b01f93a511698d8f75dec67873b2853e860e6b4fe77a705985d114ee6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75670270a37805095bebb659f19bb51c4a240cc626b2d8de23d774dac2059c63`

```dockerfile
```

-	Layers:
	-	`sha256:3d01e9874db9175f10aac3e72aa9bbdb68bc9c22142cafda74af046e7cc9999b`  
		Last Modified: Fri, 27 Sep 2024 15:29:50 GMT  
		Size: 3.5 MB (3543935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11aab390c169d17bca4c29d127707bcd1072e69e4adf4beabeea95ad9335d9b6`  
		Last Modified: Fri, 27 Sep 2024 15:29:50 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:610d5a9fef431c9ba267348b518a43342679baf184d01ae3eb14666c2fc7d82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60755744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93978382e36acf60763014fe3bc88c467988d32325425aa648e2f8ff7bc56eca`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545000064ec8779f4364fc92c0c7f98105d8982df43953655f08d4136f0e059b`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 6.6 MB (6602251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b55a0ccc129180a73ace1423e5308abbb3f503a80e321fcdae582bcf6b65cd8`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03864c9590de88a98994e47c33acbd627c63c0f22b16caa991fa0d1b5f19e0af`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb66e8b891d253efd6cd929a90458ed0cd16376b0b3103ede91076cf1103e725`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 91.1 KB (91119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36db8fa03bfe1f6530a046c2ec1ac031c176b6bd18cb0c66c4fd002c6e47509d`  
		Last Modified: Fri, 27 Sep 2024 09:04:32 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2211dc7a785298dbf7d13565928c5611cd0a036d5582f40f6ce83bc822c5dd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5812a43efc0046dcba6e30c345df85cb1f3ff2eee19c2bab712b3796cef8d678`

```dockerfile
```

-	Layers:
	-	`sha256:ac1c2998bceeff2c57dec6d686342a5fb51826e29f47d9118e161c0512cf2793`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 3.5 MB (3539984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c98fbc9db7ddf44a5051ac50bf1efac038624ab56321f3e8bb393c605105d8`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:bccb027a7ee6016c0a98560e51caf98f68f947b948222c7bbcf90884f08a2f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:33321bd67f5c4092724b3cd7c84390a44effe62f516fa528cf835068466ea750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7712d68e6912e2dadede90156365035ed83ba26b955c56a9b6743bb689ebb8d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930f573b2289c54f50a7b09f6d9445bd27f0cb1a48348833d5e6e0986d46da3f`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 5.4 MB (5360160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c56884c4edd0cbca3617ec0ab7f4eb2f2db8594b9b0cac16d907a38c0fc6c5a`  
		Last Modified: Wed, 02 Oct 2024 01:58:10 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73dfcba298667a425ac0464a6b4a731a25e47be2f31f0a80c882d1cca00ebebe`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779280839ac6c6073401d79c852c9d696e3eace1c131d11108e53c493df947ab`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 105.2 KB (105242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:47328a35876e2dd7e853351f6352f66a75141ba91a935a0c3cbc331e91ef99d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc66bf80d0b2dda8634ee73d7770e19baf3a5feea2a59971ada23eb86492d478`

```dockerfile
```

-	Layers:
	-	`sha256:d332d6862683e5d1b3ab2a9b95808810e88d2ff242476a6404c0dba1e73252f4`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 2.0 MB (2002651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a09899de5c9a6030d4c0a7373ef9c207b4660e941a72ad0126b2268b979db356`  
		Last Modified: Wed, 02 Oct 2024 01:58:11 GMT  
		Size: 13.4 KB (13411 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d037a60f85e3420771a09c5095426ed874d09300fbede4cb3573387b012275cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685e5e5da9030956235506036387fc62634485c42ed3aca5b1ae6bceba9b54a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5841415efed23c119a8469194131c18b87ee67753517a99d8fc01f06cf966fb8`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 5.3 MB (5340450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954c9f376345cca87bb2306dc082bd633d25c1c0b7a51281e45f302caa307554`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72af8df908af1001e54236b76d58c51b3eea7a5c7a3619097d305d4f775eac99`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c55ac7fc0e12deb1a3c7a55803df01877dbd826510bb33faf283e7a8300e28`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 105.3 KB (105291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f8f3f5dcdbb8d4a376f39a0a97981fabb7e6ba9a91bb9dab61851e0cfeb3aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbfc5c521f200740f1d1f0487bdb2674953bdd1ee81f47919ed971ca0ad86e5`

```dockerfile
```

-	Layers:
	-	`sha256:29772dc3da77b6599d1cbf04610642086bf317e3c95fe67f41ac60c212428c71`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 2.0 MB (2002879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a53c8b58100f31c59ec8233e0b9ba2b19ba33bc61cb1ea4e2294612be841cb1`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:a7973bf466790b8143043a176b3091e833236acf366247067448fe76903bc28d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6af11b8f91c1a72ab168ecc733cdf05682ec84fe424909677f7444517041cc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2773923a12eabf66248c89d3038c5f614157d96249c9515c71931da49b44c5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e75c7a65b7f181c600367e7b795f2ec28ccac576cda7fb3aec11e9a2e86292`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 5.4 MB (5360302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e715970f91fb31540499b96725af5116ff4522ca91c5fa45aab0984fa63fbd`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012a6a853bcbc781468c32453ea7f08d0cbf446b023487c8a755e36c2e614afe`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54deb2d52bb8bdab1846b4807802dd24c6f5ff2919e2c4a348f443a82593ec07`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 105.3 KB (105257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693067606a22cfad4fd9f685006963d17c5ee91ec5bc8876a72eb23105e11040`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:eed7c7d0767f4c9c7379afb4406bfdf0e112d2f11af2856e01407139922f4b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f877252e27fa23a05113835795f85e3ef88fa5655ef443533c839c7bdedca7`

```dockerfile
```

-	Layers:
	-	`sha256:ac5945033dc85752c1e4c94b04d2a3ec607a05fb2e3c1229393bd4df8283b354`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 2.0 MB (2002687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3ef73ab5b3c258347d3cd74684999217465ffcfa8275049c86c9935596271ad`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:286183413af81badc42fff3f1c2c214b8e8380bc918faf10b56c7c7cfe3fb2b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695fac297d77ea2b21f8c7b53fbbea39564422ecba2f82c08c2686b366931d5c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5841415efed23c119a8469194131c18b87ee67753517a99d8fc01f06cf966fb8`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 5.3 MB (5340450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954c9f376345cca87bb2306dc082bd633d25c1c0b7a51281e45f302caa307554`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72af8df908af1001e54236b76d58c51b3eea7a5c7a3619097d305d4f775eac99`  
		Last Modified: Wed, 02 Oct 2024 03:26:34 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c55ac7fc0e12deb1a3c7a55803df01877dbd826510bb33faf283e7a8300e28`  
		Last Modified: Wed, 02 Oct 2024 03:26:35 GMT  
		Size: 105.3 KB (105291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e2477417bfa5f2fc5d0d63f9edff178409808de0c35bc34a1a757cfd524b4b`  
		Last Modified: Wed, 02 Oct 2024 03:26:53 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:493435274faa21682794a4be271b392285df984c551ddf0ef2741788492ede79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733485ab064e66c3a9f58370711f69892507e10abaf72855a6398b005916abaf`

```dockerfile
```

-	Layers:
	-	`sha256:a91ff4a74015d47addfa03915b086097cd2d93574003f5e670f729a8a494f445`  
		Last Modified: Wed, 02 Oct 2024 03:26:53 GMT  
		Size: 2.0 MB (2002915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b91e53da7f867d443449320933fcf94640d01084aaa5509e655b8ba07395ff`  
		Last Modified: Wed, 02 Oct 2024 03:26:52 GMT  
		Size: 15.8 KB (15775 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:8cd25968c7a8dda57e86f5f31179a392780c365d049c245f1563df254a345b6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:b5e2ad2679d21dfb98319132904ff13815643d741d29c2cbd61f795d2cfce2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03035b5fafec30a11ccaf9e676191d30bf2a93a2c961ae50bcdeae21ecee68c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e5fc20939f49ca46aaa63fda94b740a46522034dd33a99dc846c2ab47da385`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 3.6 MB (3622683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d7c12d3dff8024cc7a65a06760eefef7523e92d4ab01561da2876474be6e25`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257f9b0966cd5484318ba1e2300bcf4102ad856d15cf79307d6575cb919be75d`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25429882efb06104ffa477fe41e22a29ad87a1b8b5a97eddc221fb3cfb85bc29`  
		Last Modified: Tue, 17 Sep 2024 00:58:50 GMT  
		Size: 110.0 KB (110041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d732e29d091ef7f0e630eef553f727bdf00995f77c7dcc07b0561d4792f4341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb4b42740c8b876bb56d509444cd2d22fd632ea9c6254cf4af8ef60cb72b5aa`

```dockerfile
```

-	Layers:
	-	`sha256:46449a2a17035de35151d0f04752a18008bd77cdb9bd76b7f1465ab848857267`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 2.0 MB (2041055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229f62c1b512cec8166de552b1e0085eb7526f3474781a15c9cfadf62c2436da`  
		Last Modified: Tue, 17 Sep 2024 00:58:49 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2e8ddba19dffa270b72c0c17efca5bea22c862945352f06ad9391ca69ae180ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e64399ffc86a2a302a5f8b07efe84fa560a195e25878c4a52e8f5d97367769e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ce4fcc7ac84933f63a18dcc1f51edb6a54d593241a9ad9eda2da49c4a0a93`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 3.6 MB (3594202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420d28ea54fd4f14398ac3479d15abc9d09b6fdfd86904d39445315fa9ccd4a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89798e75750754cd749a20391aabd4a2982ab8ea03464d1069af684488290b27`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a706a92656db8d1c42d48439ae56eb9ef232cfcd87be0f53362d7da0045c9f6`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 110.2 KB (110158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:769792b0a9ae99abbe1b81296f09e1e53c2e662643848544f1a641d54f8b29bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ab15b050723ad8ecd0ff560efdd18d3d1451cbd92375f54cf16c418e647366`

```dockerfile
```

-	Layers:
	-	`sha256:2a92568efc9bccb357a48dc2f8cc5ef4f0d34112762744fc1408de6d45f8e34a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 2.0 MB (2041314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783fe908caebc3d7a05968a298b4c97dd56aff0cc5841272d2f31f8d0eac4efd`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:c35390a21d7dcdaa5248caedb0c2d1d3f2b9a31a1ccc6a5fd082bc8262ef35a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e45ad58f9dc146f7c58fee7c828c3c6831e76bdb9cf7020f9f7c9448d53671ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33270667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4ea79fb23e81c99deef7e3da0330d8995389a5ed5528314613545bbc38a650`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e444df7ecce18d9b6a39b30f8f893e46de9a6c8393753ceb73f80be5147d5e`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 3.6 MB (3622684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eb688a315dc9dc281db41ae45a5e1651f96d5b6b93100b8f6b3604a1b7be90`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18efaf2abf8b145da9341e025a8599685148d724adf71187513efcefdc1eb92b`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c03e7463fe28779caf76a60210e080067f4e00e4a28d1ef22b5f71aab3511f`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 110.0 KB (110044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a748ff3cbe6a5eed1e2b979d6648c667fb7a29be6b3e2bc14ea06d88519a0592`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:49d3a7c89f96056348bc2f29c7aaab1b27bde7d7755e5cea5fe7102dbc63a96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2056727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0141b248fd4a83635efee725ebffc6599bb6e48aedbb01287016be2df2e9e29d`

```dockerfile
```

-	Layers:
	-	`sha256:2aa3ae2b7c2d8c84a96d9dfae22e8bdbef344f1dea22754309dafd7d8ba3fa7f`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 2.0 MB (2041091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48b6d14af7ecf44b9066d810db720df1078da0e69b612cc31771ef41b2957b4a`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 15.6 KB (15636 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4a2bedc35b23fd303d37b492a4dcd265b749cc561bed81266ef4fd4f072ca3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cc596bfd27c527f722fd0f60344b7c29c0ede0e0215ca28663dd6f7b11334d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8ce4fcc7ac84933f63a18dcc1f51edb6a54d593241a9ad9eda2da49c4a0a93`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 3.6 MB (3594202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420d28ea54fd4f14398ac3479d15abc9d09b6fdfd86904d39445315fa9ccd4a`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89798e75750754cd749a20391aabd4a2982ab8ea03464d1069af684488290b27`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a706a92656db8d1c42d48439ae56eb9ef232cfcd87be0f53362d7da0045c9f6`  
		Last Modified: Tue, 17 Sep 2024 02:36:52 GMT  
		Size: 110.2 KB (110158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0571d1820815c6ffe6445310d6d56c0904985a7a40ce55ea60111c7ab14c14af`  
		Last Modified: Tue, 17 Sep 2024 02:37:09 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15e423dc66f68b2fd18342bafd40c16c24df1ff2d5a105e3d23fe7a7b66e4859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae14030ec66c96db8f89c291fc02780ff4e9dd29fbe18b7deeb19f1a70811d83`

```dockerfile
```

-	Layers:
	-	`sha256:b8a537c7762547e63f17b420cb0912f491db0829af8089494798ac00e311b1a7`  
		Last Modified: Tue, 17 Sep 2024 02:37:09 GMT  
		Size: 2.0 MB (2041350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab7d3d2aaba018f1a288d03ac3c709c72564deb83d89ee6d4197767b31a448c9`  
		Last Modified: Tue, 17 Sep 2024 02:37:08 GMT  
		Size: 15.9 KB (15912 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:be2f3716a4cec9a306cbd8d426117f8aab8727d6c0e9c200476a875338d9d419
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:ba3a22d89a7a32732bfabedb6f8b97f74f7bf663d7bfd10ee35e90a14d2a5a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33410513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e4911df4af3c3f01073a17ce1734d817aa7226671d53511d1849774a4d52c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657f2a0c259ff376993610ba80c419c5073712870b3c4102fc3fdc47621052e7`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 3.6 MB (3557869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f17957c9ae33ba95b7c1ae44535c130d7e8a9162b4c30ca673dff0bc86daa99`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d862893fb97f214fe809b8a564f061db2026ae314f8528202042c8db3129ea`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2243d0bd10d8e5d8d8b1fd7b85071b0e2e33209c7516489aa762758e173a6f`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 100.8 KB (100790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ede965cd728e5c520133c9d29a298e463b405f1db483e381f6cf039e20b40e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1985847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5691abb4119b847b8f00db93ef20163cc6264a958f96d64d276c39424ec3522e`

```dockerfile
```

-	Layers:
	-	`sha256:5d62bb1da4f37e3074d7ac217fac968beddcbc678b35366d4f7a76312ec7f33c`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 2.0 MB (1972437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd2751407fb0c291db83cf3d75ddf8cbde3b70fc70869d8e91bc616ea92f5503`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 13.4 KB (13410 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4981901a57f223c1b9c8891c69885caee2fd40918860bb6ba85cca873a53a0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32545805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b59b6aff1df9ce330d718830cddac2344afbfd17f2d9bb3388ec169422c2da6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d97f4c88babffcaa2541504a32c0a03166773de0a08bf0c98636dc16613977`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 3.6 MB (3556989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ac16409873f9bdc1698e67b746242ec770699376195c1c3ed68f171168f3aa`  
		Last Modified: Wed, 02 Oct 2024 03:27:22 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316fe113f82a4d8a693191a9c1a292b0fb3d412c356c88cb147e63b90264753f`  
		Last Modified: Wed, 02 Oct 2024 03:27:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03520ce4621ce6480c2bc6e4b7308731f458a108efd055cdd6deed3bb77b727e`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 101.4 KB (101390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bf9021c868e6d98d032cc69d7693491d1fe3023ff5fa80663af9dce9b5741802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb8d4ae921713e80f86d7d927cf18d51deb01d257a38ea865052b5f73c297a`

```dockerfile
```

-	Layers:
	-	`sha256:82f370cf47cfb6114fa6a88a78795e7ff6f2559c5c3305a72fbfba6aa9050207`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 2.0 MB (1973482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53fa90318a31deac3447b6fa554bcbed7d3186b765b2ccc8ecf219c00c76b6e3`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:03305ed9c497b5b5e36b5c12bb2b23db476790a959d91582c24d9e8818170623
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:23494218fcf4af676400f730f260d3496e45abeebb3643d4f2f6814e18804b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33410906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d7fab169b5c9cd9a6d29fd161d4333ea8b73868f7121cb26047d66a19f567f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c912f4f015c2c89eee9af3171573f750d3dc9de8e739f9252b3eb317387983`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 3.6 MB (3557868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8c30851e6913a144d98698c661b2fec79c5b55153c2a7a9390eca093ac6f50`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b0875bf1f60a4462947264348c9dfe2c2f1e578d1a51e0986a1ea56fda4c5a`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8874b45bac9e590e59a39707917cd81534064618fa99b1d4a6831dc368f91958`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 100.8 KB (100783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1e41da67b4900e7f74072bebda6ad867d9a766ab22e16f0e7d6e74fcb7427b`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:487bbe2da69bd02307432a0294d70892a959eceb03e0a0870e6017fa3ca9b5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c7e2f11b539c1c880472ecb2113456958831d10e99a7db75e13458d8d64834`

```dockerfile
```

-	Layers:
	-	`sha256:7eea4b77cc0770574c9a48f2e102d138a8e32a2ee294f610f29b3bd66d90daee`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 2.0 MB (1972473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02f4c475e61277a148d2dc8f0843497b857e7d8ba0561c7e9012723fb526a07d`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 15.6 KB (15640 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ab3af29777ef1e96c62a7f1c5c48287289866e342e0139a1b0ea7be19f88ca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1baa7bd0f8dd8adf7384b291d433c613c2ba1658faad4edfa857f9679e20dd77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d97f4c88babffcaa2541504a32c0a03166773de0a08bf0c98636dc16613977`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 3.6 MB (3556989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ac16409873f9bdc1698e67b746242ec770699376195c1c3ed68f171168f3aa`  
		Last Modified: Wed, 02 Oct 2024 03:27:22 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316fe113f82a4d8a693191a9c1a292b0fb3d412c356c88cb147e63b90264753f`  
		Last Modified: Wed, 02 Oct 2024 03:27:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03520ce4621ce6480c2bc6e4b7308731f458a108efd055cdd6deed3bb77b727e`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 101.4 KB (101390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c28804c3b527be89fe221d3e09ca03700fd3fba94da56e76fe5d02d64ef9b6d`  
		Last Modified: Wed, 02 Oct 2024 03:27:43 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ebe493caf95092645cbfe8f3f25c5a1a57cfba49a7a112c8c97e2bc3e4f2d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4238e49806212dc77601150e439864a64cb14c0fa77766ceadc11de27c1cd8`

```dockerfile
```

-	Layers:
	-	`sha256:0f2cb71ca13f4d8e2beba383fc3930a094dcfbbf13b05afd6ad32de5caebea3a`  
		Last Modified: Wed, 02 Oct 2024 03:27:43 GMT  
		Size: 2.0 MB (1973518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0caa6ec96e5d43f849399feb7117544fe5c636d6cc9c19ea5799a5d99925d0b8`  
		Last Modified: Wed, 02 Oct 2024 03:27:43 GMT  
		Size: 15.8 KB (15775 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:be2f3716a4cec9a306cbd8d426117f8aab8727d6c0e9c200476a875338d9d419
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:ba3a22d89a7a32732bfabedb6f8b97f74f7bf663d7bfd10ee35e90a14d2a5a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33410513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e4911df4af3c3f01073a17ce1734d817aa7226671d53511d1849774a4d52c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657f2a0c259ff376993610ba80c419c5073712870b3c4102fc3fdc47621052e7`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 3.6 MB (3557869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f17957c9ae33ba95b7c1ae44535c130d7e8a9162b4c30ca673dff0bc86daa99`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d862893fb97f214fe809b8a564f061db2026ae314f8528202042c8db3129ea`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2243d0bd10d8e5d8d8b1fd7b85071b0e2e33209c7516489aa762758e173a6f`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 100.8 KB (100790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ede965cd728e5c520133c9d29a298e463b405f1db483e381f6cf039e20b40e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1985847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5691abb4119b847b8f00db93ef20163cc6264a958f96d64d276c39424ec3522e`

```dockerfile
```

-	Layers:
	-	`sha256:5d62bb1da4f37e3074d7ac217fac968beddcbc678b35366d4f7a76312ec7f33c`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 2.0 MB (1972437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd2751407fb0c291db83cf3d75ddf8cbde3b70fc70869d8e91bc616ea92f5503`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 13.4 KB (13410 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4981901a57f223c1b9c8891c69885caee2fd40918860bb6ba85cca873a53a0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32545805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b59b6aff1df9ce330d718830cddac2344afbfd17f2d9bb3388ec169422c2da6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d97f4c88babffcaa2541504a32c0a03166773de0a08bf0c98636dc16613977`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 3.6 MB (3556989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ac16409873f9bdc1698e67b746242ec770699376195c1c3ed68f171168f3aa`  
		Last Modified: Wed, 02 Oct 2024 03:27:22 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316fe113f82a4d8a693191a9c1a292b0fb3d412c356c88cb147e63b90264753f`  
		Last Modified: Wed, 02 Oct 2024 03:27:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03520ce4621ce6480c2bc6e4b7308731f458a108efd055cdd6deed3bb77b727e`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 101.4 KB (101390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bf9021c868e6d98d032cc69d7693491d1fe3023ff5fa80663af9dce9b5741802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0cb8d4ae921713e80f86d7d927cf18d51deb01d257a38ea865052b5f73c297a`

```dockerfile
```

-	Layers:
	-	`sha256:82f370cf47cfb6114fa6a88a78795e7ff6f2559c5c3305a72fbfba6aa9050207`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 2.0 MB (1973482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53fa90318a31deac3447b6fa554bcbed7d3186b765b2ccc8ecf219c00c76b6e3`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 13.5 KB (13530 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:03305ed9c497b5b5e36b5c12bb2b23db476790a959d91582c24d9e8818170623
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:23494218fcf4af676400f730f260d3496e45abeebb3643d4f2f6814e18804b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33410906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d7fab169b5c9cd9a6d29fd161d4333ea8b73868f7121cb26047d66a19f567f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c912f4f015c2c89eee9af3171573f750d3dc9de8e739f9252b3eb317387983`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 3.6 MB (3557868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8c30851e6913a144d98698c661b2fec79c5b55153c2a7a9390eca093ac6f50`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b0875bf1f60a4462947264348c9dfe2c2f1e578d1a51e0986a1ea56fda4c5a`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8874b45bac9e590e59a39707917cd81534064618fa99b1d4a6831dc368f91958`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 100.8 KB (100783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1e41da67b4900e7f74072bebda6ad867d9a766ab22e16f0e7d6e74fcb7427b`  
		Last Modified: Wed, 02 Oct 2024 01:58:13 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:487bbe2da69bd02307432a0294d70892a959eceb03e0a0870e6017fa3ca9b5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c7e2f11b539c1c880472ecb2113456958831d10e99a7db75e13458d8d64834`

```dockerfile
```

-	Layers:
	-	`sha256:7eea4b77cc0770574c9a48f2e102d138a8e32a2ee294f610f29b3bd66d90daee`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 2.0 MB (1972473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02f4c475e61277a148d2dc8f0843497b857e7d8ba0561c7e9012723fb526a07d`  
		Last Modified: Wed, 02 Oct 2024 01:58:12 GMT  
		Size: 15.6 KB (15640 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ab3af29777ef1e96c62a7f1c5c48287289866e342e0139a1b0ea7be19f88ca24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1baa7bd0f8dd8adf7384b291d433c613c2ba1658faad4edfa857f9679e20dd77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d97f4c88babffcaa2541504a32c0a03166773de0a08bf0c98636dc16613977`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 3.6 MB (3556989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ac16409873f9bdc1698e67b746242ec770699376195c1c3ed68f171168f3aa`  
		Last Modified: Wed, 02 Oct 2024 03:27:22 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316fe113f82a4d8a693191a9c1a292b0fb3d412c356c88cb147e63b90264753f`  
		Last Modified: Wed, 02 Oct 2024 03:27:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03520ce4621ce6480c2bc6e4b7308731f458a108efd055cdd6deed3bb77b727e`  
		Last Modified: Wed, 02 Oct 2024 03:27:23 GMT  
		Size: 101.4 KB (101390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c28804c3b527be89fe221d3e09ca03700fd3fba94da56e76fe5d02d64ef9b6d`  
		Last Modified: Wed, 02 Oct 2024 03:27:43 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3ebe493caf95092645cbfe8f3f25c5a1a57cfba49a7a112c8c97e2bc3e4f2d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4238e49806212dc77601150e439864a64cb14c0fa77766ceadc11de27c1cd8`

```dockerfile
```

-	Layers:
	-	`sha256:0f2cb71ca13f4d8e2beba383fc3930a094dcfbbf13b05afd6ad32de5caebea3a`  
		Last Modified: Wed, 02 Oct 2024 03:27:43 GMT  
		Size: 2.0 MB (1973518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0caa6ec96e5d43f849399feb7117544fe5c636d6cc9c19ea5799a5d99925d0b8`  
		Last Modified: Wed, 02 Oct 2024 03:27:43 GMT  
		Size: 15.8 KB (15775 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:4c31540c4a47420fa5e9600cc5da4d3453175aa5a25a37860129f18bb5876da6
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
$ docker pull neurodebian@sha256:b48d6272400457ab71668d983cf66e3677f8df417b405a16646a77398ba08d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60917184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f348d52d0a30c0875589c2a9119a552d0157a52592558ed41ab0bfd3e3c77a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9051ff7592ebdf57081bea4813d054f179c10baf88e8edb1b1eb0503dc57a398`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 11.3 MB (11266587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b7d938f0d1f711b7744833ba75d25ef22f306b38fed3f791d43c283332c29d`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d8d64e9f86a243cadef1fab89c4bc283c6ab4b4d7acd3c713da0063cfbc7f8`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45240937643905b587fa479f7122727e4da480a63dc938c4d4e680049d4fd520`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 93.1 KB (93133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca5c0ab742bba3e582138550e8f5870657e878200808229861aaeff5b17eddd`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8be6a251f01d60f7c79d8354d52a880631b39d9b5e7686fa2e26ec2df80aeac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcc537a8cec282d091e002e6f0a1e677c36051a6c61478e3e8eb0454c94a884`

```dockerfile
```

-	Layers:
	-	`sha256:11250ff6b4c7bc963acdf419c612cf7ee613254e2246c5b3d2a533583138de69`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 3.9 MB (3924292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50bdef147161d65fa6df17b8f42d4d1bc566bd2ca0efeceae14bea0caf771bed`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1bf2ad888a05ef807d67508a9f6926ad1786f54786c4acea708e393305d3e908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60912794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f9c69de5373e2c9f69164910ff1d44257dc2596d2f0d7d3cfc67a0c584d68c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18398593d4c19c61fc775e0592d0d8a432ee6462e9a8f7b8810a361333b485d`  
		Last Modified: Fri, 27 Sep 2024 15:28:29 GMT  
		Size: 11.2 MB (11232110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621de790ca72d0c42672a6a2ac731249ca406772328f8c3edd3d594f1f53f616`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b740e3d498ccc528d88bab38ee97183e394cdd50200b197502891dfb79ad4d1`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d5924f9901e2c8fcebcabc13a32cffd7e420213b1cf345f0e63ad1b70c157a`  
		Last Modified: Fri, 27 Sep 2024 15:28:28 GMT  
		Size: 93.4 KB (93387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c007be9f3baa091742dc1aebd0ae0a6e3cea7a4b810f0b8e43f15eb877896e70`  
		Last Modified: Fri, 27 Sep 2024 15:28:52 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a5037ed0757501393c215f764e0ae006eb95c5b18a1b83e29856a21a86f904f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a21e19ca8c5ff905338308a88e40f5a3e1df607f032725531e296e5de2077dd`

```dockerfile
```

-	Layers:
	-	`sha256:b824964735f0d18f63657b8d91305ccedf77807feae3a5161f131d57be3295f5`  
		Last Modified: Fri, 27 Sep 2024 15:28:52 GMT  
		Size: 3.9 MB (3924545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c864375c20088fe814094af1263b5d464fc676e095599494c207463caa2967`  
		Last Modified: Fri, 27 Sep 2024 15:28:51 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bee081949cf57ceaecb3135aafb92afa4570a49981637c3417a17b32403c4a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57394c8777f825902239d56e9004bd008fafe81bc34862a6a73b3642af4eb655`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:2132367ce6b27831b6a98307337ab5a07127c389e0f77af1b73c2de06c847c1a in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c15b2f7ffe203e6872d10b7436380c84e07676a218e14df64bff6eb7961b9487`  
		Last Modified: Fri, 27 Sep 2024 07:26:35 GMT  
		Size: 50.6 MB (50576641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ab7367486539cc2d6c35ad3018714f9ff4f1c097f65527882cda7ba2c4c48b`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 11.7 MB (11689049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47dd5e31a5ba70c7cbc3d81c9ac82a70b05d13aa142f333016a30c7c728d6fa`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92a1687c24021dd12f46d38e9eefe255336343473332498d5da65afd4da1a80`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109102859cc8b950870f53e366f28846943d199769ba5a2dd573058136b2dfa4`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 93.2 KB (93204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d3b5d7d64269625fae11e5e669b00c675b3beec6db5b29738bc55b876f48a9`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8125292b6b7515ef1a26096899be0b264288a183078b74c5c9be5b43c677a730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c852d546e62718c86e124fd2031e53b49ffc7e18124bd0ea1aa2c86f1c2c99`

```dockerfile
```

-	Layers:
	-	`sha256:5c1069382d1d1988c0a11261be34df46f7f5c1a229c8c1b93d7cc8711f94f922`  
		Last Modified: Fri, 27 Sep 2024 09:03:59 GMT  
		Size: 3.9 MB (3922209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724f78771fbec7e294d02422660c6c79e3db21f706773c18f10c9c77d42bb59b`  
		Last Modified: Fri, 27 Sep 2024 09:03:58 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:2fddaff134d7ca3561871178fb51109683144c5ab6714a910003a8e6d0529a74
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
$ docker pull neurodebian@sha256:b386e80e587d4c20ecf466054c921cfdc72aeb7e5502867ccdd6bac2d19048a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59631144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd3b8259795f4e2160852925aa7fbb7231a7e252c92696a27950f0303853dce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f475f97deaabc6193a3fa858337fe06184e11ad6b13315ab6c7f971b66a9bafc`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 6.3 MB (6287931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd7fed0f8636459064f9f964188e4826469f925ed396341fb68ce62fb315377`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9fec776045441161388c757e0ad726b5ab7fbd3548e03d22fa42b727e9b782`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e369688a9f2e20897b0342be14d8b6941a03ccb9fe3bb98dd6ddcfe4445ba29e`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 91.2 KB (91192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:822f4de5100bb1994064afb1cdd414af5247d0e87c51bb88c46ca6bed2dc05f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a37cb43875ddc7aa01e78a71637c84ed0a436c94162a5790e7bea0b07cc237`

```dockerfile
```

-	Layers:
	-	`sha256:8c16a39d93e2e784f37f3cbea84302594e573b2693f64b8b370f24ccf9d50237`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 3.5 MB (3542033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:503cf70ae76d49b40790396ff4fbdf7b5f3daaf8b7ca72be3e759ad8e79bcacb`  
		Last Modified: Fri, 27 Sep 2024 06:02:01 GMT  
		Size: 13.4 KB (13396 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:58bfc8026888335070afa0f72044cdd664f87cf4b9aa4f26c46385c610885f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59958772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c27c5792cf7ac400d363febafbd72ae89764d94df31e0957faa9b3e6c9d75a0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1707618fa9372fa7563234001ca06291da815e7c963e11719d290dcc36218024`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 6.3 MB (6270740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f92dac85afbe3987da72fdcff7499ef9a4bef39d0ea83f70ad579e421b2b1`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560ef25c1ef36b5b05dc1fd297de1698589349e5c080811754da6ab61635771b`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c67a14658f20791e7bebae65768af2451f13d17e95b1fa2ffbcd886802abb3b`  
		Last Modified: Fri, 27 Sep 2024 15:30:29 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7c1a8705a3413350f04f5a1d739bcdaf9577a3dcaba3ae5e1fa73e801f1f3060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53c580a80c3d5c1142885b2d547f026e496f73afa9516d55b492a1fd6e19aa3`

```dockerfile
```

-	Layers:
	-	`sha256:1236d910e711e1eb3ba937faaabef1ecbb76904d2147d9e237f9088e67d19501`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 3.5 MB (3543075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:383b288126aa4491dde9bca5f83e6279bfed5b9378f20d43c6e8ce721a75e949`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 13.7 KB (13671 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:8b1dc1ce8b5e8c3c34ccce9276cae70f96439f7a251b57b0d867562e4bb61c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60787262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb7e7e400856419fe6dcfba9476730e473001cdb7071f69bc5b2c70f24a3407`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7024eca1d35e4bf56690a81c3c1da49afee7ee27f30584fad073bcbea685f1d6`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 6.6 MB (6616326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e114f1c83df29eedcbf0676bad5078aa0615db7e6590d793bba0242195937669`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af5f6f47b991c182b45b50e4e4234c3e05547782c074a70ce4b5357d5c65900`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4229c9987c9434cde75f4619617a1b7d0b032708a7e4e5b415357838601309c`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 91.1 KB (91141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a1f9b369fb100fe194ca9bc43464f41bd1a6938a0a4815da6d5bc7a3189579ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3552496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d5866efd6fe0420224e5d5b639885adf9285db5a32cdaf1e966cba25ac2ebb`

```dockerfile
```

-	Layers:
	-	`sha256:a01afa53c29c892db3413fbdcc505cb39abe7e98a9a4ae0aa52c992c8d222303`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 3.5 MB (3539125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:825884d205bb9ee0ceca812d5351085152132f2aa40ac72738cb9389bc0280d2`  
		Last Modified: Fri, 27 Sep 2024 09:04:51 GMT  
		Size: 13.4 KB (13371 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:ba48eba3960765f9ccfea266dbdcdd86d7969d5deed37f153a35fb3c3222ec48
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
$ docker pull neurodebian@sha256:d6385e1c5bb68d77f40e026ed12ce430380e0e470b79c3f5ccfcaefc931a7b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59631607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e776c45bc6971cf609f11e7627976f0cfe662728ec87d1d886c00188c57a3a0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9932c03d465e07be767be6c6546a5fed0a8b713450009a5ae5548c52bc48a318`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 6.3 MB (6287955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa69fe5d2dbb347bcff9484d062465fb6e89f3a62b98b0ff196ed4d6799f673`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a23af6f8797bbef0455d9cd57276520bb04a5171c6203bc5a5ab3d4c88811a`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7138d16f6eeae6939426514f30129bb8016e17c4b9a24883b9440e1353b605`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 91.2 KB (91238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7203ca1b15919f54f52922c71b014e2624ac6f086d13bc8f501cb8858bbd344d`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:465aeca1f63b6dc525b5632ac6eea79aab7b6e34c2630a00249831526eda91d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4661d626714f88f865b4ae67b6b9f36d1602de01880fa1be9dfbfbd03c8d6cd`

```dockerfile
```

-	Layers:
	-	`sha256:e3e8d0820b5babfaf76c87b38d941bf58eb80d5250a65992b20ba00063fb637b`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 3.5 MB (3542069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65c24b8306901ac0ef9a25e84ad3f7abf256dc28c444897f5eea6145f6e792b`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8405eb81d4fb50f2e0ca8052e64751a2166bc5f44bd91dfd5f8364928076fca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59959165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b6fc36a6afd9830924df899db96464eff91a08d2fd009cb9b3d1088a5325f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1707618fa9372fa7563234001ca06291da815e7c963e11719d290dcc36218024`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 6.3 MB (6270740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f92dac85afbe3987da72fdcff7499ef9a4bef39d0ea83f70ad579e421b2b1`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560ef25c1ef36b5b05dc1fd297de1698589349e5c080811754da6ab61635771b`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c67a14658f20791e7bebae65768af2451f13d17e95b1fa2ffbcd886802abb3b`  
		Last Modified: Fri, 27 Sep 2024 15:30:29 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed1a0ff889a3d19ad950be2e4cb5a585ad9f69009887c6d58da8a5f7bfb5ed`  
		Last Modified: Fri, 27 Sep 2024 15:30:50 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0a0fb2b4c94881a145a88d8cc5d383cc5abffb8759ae1bbce2a56aa27dcc36e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fea4b5d7ea7ed8b0f6ce474f3f3263dd4b2b04738558dccdd3a704db4e1b350`

```dockerfile
```

-	Layers:
	-	`sha256:0b580fb68668f72246a5b77f9ceab789100d2ab9171a59039e674ffc2dafe1b0`  
		Last Modified: Fri, 27 Sep 2024 15:30:51 GMT  
		Size: 3.5 MB (3543111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ccb2a5d05b136f255c231e5f7370718d916c8cee58b2a409d354d4a1fc598a`  
		Last Modified: Fri, 27 Sep 2024 15:30:50 GMT  
		Size: 15.7 KB (15703 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6bf4e8373e3f6f87febe8b3d0319f5eae2cbcf139f17280c044d49b1e17ee457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60787647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9459a6b567f0d06c3aea1dd09d4385c4b2baaa27e9efbf9cf5d9c421d9fc8f84`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143cefad1d4d9c4b8fd3771c226b9090a09e67f6afcd789097a49ddb1f5932ba`  
		Last Modified: Fri, 27 Sep 2024 09:04:36 GMT  
		Size: 6.6 MB (6616300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977207288632e8201bfaa72034a65eb6f6ec8e61ff6b653d4fb73cf84ccc1d1`  
		Last Modified: Fri, 27 Sep 2024 09:04:35 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105d3548d214af15c097f1d54ad01ceb9ede39ebdea69818d3e71bc47b2839f7`  
		Last Modified: Fri, 27 Sep 2024 09:04:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5769ecbf94961298ff7e98bf0aa70190a17384c3bb8a9f690579e7c6fb520481`  
		Last Modified: Fri, 27 Sep 2024 09:04:36 GMT  
		Size: 91.2 KB (91162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9019696d4316f86af9fd804eb7624e648250c6fa998fed26656d8c9a25ff33`  
		Last Modified: Fri, 27 Sep 2024 09:04:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0f672898bb01b946177bbaccbffa0299ab4816defdfd5e2b5087ac9572102657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32aad4c936608553494658612be8bda4f99b108cea7bf09723c1e5efa39b98e6`

```dockerfile
```

-	Layers:
	-	`sha256:838300a747539cfb1dbc0eff0c046248c8620cf10416eaed02824c77f7b7cf3e`  
		Last Modified: Fri, 27 Sep 2024 09:04:36 GMT  
		Size: 3.5 MB (3539161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0678c291feb069de787e1099a828f38de4639e00c1c427de8e71d86ea3d06b98`  
		Last Modified: Fri, 27 Sep 2024 09:04:35 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:2ae61745c247d4a8c99d7c354b96029634ef5bdc33733e5b2da4bda458519e67
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
$ docker pull neurodebian@sha256:95b63a109fc48f08237b877fb7cffa77d61e8df22bf5a4d7791c6efd09c4ef8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59551601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe81e410768586b5492844badee22adc900027cdac5b1acf7b379c3a674edf9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267a7066a313165935bf4eaaa8b9aae312287191547d2809b4ad34773e828a5`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 6.3 MB (6280356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aafa6a0b3025fd4652316fc5e3fe6ea05e11344376a905017040b9b985cbf99`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5cb880e6abea22dd0197684015c78086ca2948c36925678e0bfe28e3465c00`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04bfec15b0903df67fad5cf467dc6eb0ca7d397677702389607bc4733e4fd4b`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 91.2 KB (91221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3320834de6354f493c1d82186351c117223665c2f4ead32bb77e28427b89eee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f4e2f5a80b3b29afc74f04e8902b4b3c96a67b973d863de928e9726e32f9c8`

```dockerfile
```

-	Layers:
	-	`sha256:a20598f20436ee588f58c36585795a38adaac735394605a913cfb849c611cdeb`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 3.5 MB (3542857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1088db98014479771d8f0b3f7e94eab159c63f2a9e60f1ec223437d6c43cde04`  
		Last Modified: Fri, 27 Sep 2024 06:02:09 GMT  
		Size: 13.4 KB (13445 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e045c8722a0d09fb924908b53557b97d64b916b1e5f7034d0d5f9fae67d5424a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59971880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00daadd7fcf3264abc9af0febccd9a59cf1e87e61f9c621afb2b7d106794a72`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23f6352824fd96c8c6b9838bfb904e1d7622f6bfe55b4c553cbf57ff483a36`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 6.3 MB (6261488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c0a4b3a15644d2d672fb44fb7ef754851b4b999ae2449d908d2bcb61514ef9`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620d3e5d3b378b7be79ad19c20bfcdc40531f8bf0971a901824a5e8be8263f1`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dce128f9ff7538248e2b5e2edcd6ca43e5feea1880d5b8a5290a08534c4e63`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 91.8 KB (91807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e2a4489f748889ef85e038e010495eefa34e6dca07c0894d71860b17f81eb310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626360cf88fe014495b6a029a63b3915e45368305e7c9a89bb1cb126907c91e9`

```dockerfile
```

-	Layers:
	-	`sha256:542bbb008b88b55265ccbbf2227938f846127e85ae4c7737802a2427e4e3107e`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 3.5 MB (3543899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b2b4a94f394589d2ff4a612422d51f4eb84d2ddbc340e5d3f3f6fe458774f1c`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:98a7bcbd0f48607aba203c188fc584d3eb2eb44a7972910a22aab506ba373691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60755232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c978744990dfb8d2fefe9889d4703ac1fd7df41317879cb1f5a804f0ebbeaf7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d66646f8689060ae7f27f71816fcf459f852eb6ffd38e84da1a7977af7339f`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 6.6 MB (6602168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499956c24221d0887f18337dfa8a40a66ef78ea9e5070296934feb3bfd7d4a5d`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7116eda93782aaaf1afc07d9a8ba9c05b4a670e4895f060a253a01309244cbc`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0378a4a334d3b4cffb9cab48b3af6ec246e132da90a1800995016cf0bf3589c2`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 91.1 KB (91113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5361635eb47ff0c54139fb8d6f735ec9beb3988828092dd2fc5d3822db6a20eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3553368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749228d8c97e77fd9c454b59dade707186a17580df86a112f59d4294c25e7bb8`

```dockerfile
```

-	Layers:
	-	`sha256:d2d9148adae996142f2c520e17f483fbdc69659298daa1f02d4de07c78624137`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 3.5 MB (3539948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca28f4c520dba6f7987ca6746a6762200a61a360201024c7e94e22a89fda061f`  
		Last Modified: Fri, 27 Sep 2024 09:03:55 GMT  
		Size: 13.4 KB (13420 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:ac61648e2563a3882383fad081f7de6996fe8f0fa8f9627a7e6bb0ba22288aa4
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
$ docker pull neurodebian@sha256:b1f199d03815d48bab11ecaeeacd81e4b2ac39a65aec462dfe763fb7529d3789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59551988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2893f89434279438492df27d6533582a320166e62af2248cf9c6b82914766bad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:c2e548cee70ab5a71ba4d165e822331b99bfac5828c9967b54be455f74f37cb5 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:cef23d1777526a612ddd7b1a451e2d6b9f5841ab0d62aedf20e185729a23a02a`  
		Last Modified: Fri, 27 Sep 2024 04:36:02 GMT  
		Size: 53.2 MB (53178037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b19379603d098a671eb23697522873f6e76947ab42375d6822c5b0a4b6e809`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 6.3 MB (6280319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d0c24d6a8e14e4685405a8aaf43a7ab30aa29e0e1f283aa98a3d7449868222`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b7a35dec8f5dd32abe5be6043a56585b31eede2c1645904e76cc3a0482af1a`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d57f109b0de41f938f7878759736faec767e84dac89736dbe1be92533a9acae`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 91.2 KB (91225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e14b1c01ac31d1c91fa43ae686e8efeb1145d926c79601a652e7726aae0434b`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15c88b06753416b8a2d15c8ec809ecbdb6754fdf950e7164e5fecc310c199b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d92db2beeb0a5cd44fee711408904a5286a853e7f5a750d1ad67c91a5b7482a`

```dockerfile
```

-	Layers:
	-	`sha256:413a52dce277246c096155463956e28af6833eaec6061b111fe35a78cd5126dc`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 3.5 MB (3542893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b06258c0c750ae4d23c85317f3cf98f715296d195230122d9ca927b48c27b20`  
		Last Modified: Fri, 27 Sep 2024 06:01:58 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:de9deb09a9c4a574733d8bf0ee9a8435ca602569681432e0e590c0293bd56639
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59972303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd450a6e5b8e10e76c6e84376a6dabc34200b6d18baa5cf78ed1fe5c5eb2ea4b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6e593c1f521506b0f2af9a3f995a4a4355898a8de85014ead699072096977336 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:789b7eaf9779c1b4818e6bfd3f071ee22446dc33481efffa3036978d098e31d7`  
		Last Modified: Fri, 27 Sep 2024 04:43:31 GMT  
		Size: 53.6 MB (53616601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c23f6352824fd96c8c6b9838bfb904e1d7622f6bfe55b4c553cbf57ff483a36`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 6.3 MB (6261488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c0a4b3a15644d2d672fb44fb7ef754851b4b999ae2449d908d2bcb61514ef9`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b620d3e5d3b378b7be79ad19c20bfcdc40531f8bf0971a901824a5e8be8263f1`  
		Last Modified: Fri, 27 Sep 2024 15:29:28 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27dce128f9ff7538248e2b5e2edcd6ca43e5feea1880d5b8a5290a08534c4e63`  
		Last Modified: Fri, 27 Sep 2024 15:29:29 GMT  
		Size: 91.8 KB (91807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcc1f5af84d08060d7baeab3587692d4e1469721eaf97086e62e8a08e46bffe`  
		Last Modified: Fri, 27 Sep 2024 15:29:50 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c889b01f93a511698d8f75dec67873b2853e860e6b4fe77a705985d114ee6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75670270a37805095bebb659f19bb51c4a240cc626b2d8de23d774dac2059c63`

```dockerfile
```

-	Layers:
	-	`sha256:3d01e9874db9175f10aac3e72aa9bbdb68bc9c22142cafda74af046e7cc9999b`  
		Last Modified: Fri, 27 Sep 2024 15:29:50 GMT  
		Size: 3.5 MB (3543935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11aab390c169d17bca4c29d127707bcd1072e69e4adf4beabeea95ad9335d9b6`  
		Last Modified: Fri, 27 Sep 2024 15:29:50 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:610d5a9fef431c9ba267348b518a43342679baf184d01ae3eb14666c2fc7d82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60755744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93978382e36acf60763014fe3bc88c467988d32325425aa648e2f8ff7bc56eca`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ed6c137f2444326ea2aab7c98ae002052b2a872d9931a0de81cfd9212f14f4fc in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
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
	-	`sha256:a2ccf63332f54ffbc2e94366ea06b762b69ecfb3e405c902e5a835b8aa2dce0a`  
		Last Modified: Fri, 27 Sep 2024 07:30:29 GMT  
		Size: 54.1 MB (54059963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545000064ec8779f4364fc92c0c7f98105d8982df43953655f08d4136f0e059b`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 6.6 MB (6602251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b55a0ccc129180a73ace1423e5308abbb3f503a80e321fcdae582bcf6b65cd8`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03864c9590de88a98994e47c33acbd627c63c0f22b16caa991fa0d1b5f19e0af`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb66e8b891d253efd6cd929a90458ed0cd16376b0b3103ede91076cf1103e725`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 91.1 KB (91119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36db8fa03bfe1f6530a046c2ec1ac031c176b6bd18cb0c66c4fd002c6e47509d`  
		Last Modified: Fri, 27 Sep 2024 09:04:32 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2211dc7a785298dbf7d13565928c5611cd0a036d5582f40f6ce83bc822c5dd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5812a43efc0046dcba6e30c345df85cb1f3ff2eee19c2bab712b3796cef8d678`

```dockerfile
```

-	Layers:
	-	`sha256:ac1c2998bceeff2c57dec6d686342a5fb51826e29f47d9118e161c0512cf2793`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 3.5 MB (3539984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c98fbc9db7ddf44a5051ac50bf1efac038624ab56321f3e8bb393c605105d8`  
		Last Modified: Fri, 27 Sep 2024 09:04:31 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json
