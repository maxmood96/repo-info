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
$ docker pull neurodebian@sha256:305a959a60ae161fd1e2f8b9d126acb78f47303f5b2dd360f2aa4e99d8116d8d
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
$ docker pull neurodebian@sha256:62882ad0f33cbdd9eafb7c6e9b5eb8ae372a25a3c0f21f62d0acdf1497333dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fead143accff411376d04d2bb8b320457f355d17d0d27de94083e816f8f3a0f6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d842fdeb916ebdf94d0bbf538179616ad81e7f1dedc4ed501023f251d18357`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 11.3 MB (11266589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b6525920c59417749f5f5ed2a2b63bf70e4372d1ad1e43940269f4e46a6a39`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe030c3262712f09530bec25a14ab3358602038a50cd68318f64e517a0d7106d`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e7a9c054202f338852b4263dacb6b225a16d4950ae6bb727864599c43ac5f4`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 92.8 KB (92805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c08007fdc95a1b89e9bd08160fd1ac6c3b8fa0f7b865ca9831db8c621d10d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea68d861f08bf1d925c0f249e39c42140b65d239b0cb8609a37c5443bbe64b8f`

```dockerfile
```

-	Layers:
	-	`sha256:564761329007c6319eda102596fe80eafa8f03a704f8c8df0d8850da67515ce5`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 3.9 MB (3924239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff9da6553a56e9140cd5c7d5f7c5f801677dc978c7cc89afb8cca432ddd6512`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b71cd83d5bd8b0be36b87ea3e0563cab2fd7fdc8fda441dfca994c724878c959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2a5069168923cdc4f70896cc2dcaf93a70115c7d82eaec01f4a07b469d6ef2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0c4964b2c74b33113f4f9253f8fdbd6f9effb7070fabfe7998ec7f9f71a68c`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 11.2 MB (11231990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a84d3037e0ebe02d7b2e60abbfa3c50ab185daf05e3e55e3f8ff6cf96a45b2`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784313ea4757f773fd668b9d92e36d3061207f4d5f2fc7c75d857979e14d6f21`  
		Last Modified: Tue, 23 Jul 2024 18:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f51ef3b42547d51fc5c3da2f3e174e60effa7629f2f7e46098c454225497cd1`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 93.1 KB (93109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:757c7bd29e99f08e021102ec7bab71368c08fc5b8dedd1b342098d8ce5324fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd73107a0a9709640c47c4e4f59fa6ca1ebabf8a0658aa9381cbf4bde03a849`

```dockerfile
```

-	Layers:
	-	`sha256:862421904df231d53bf60f81099184d7c0682e30c697de8f23794783ed2daf08`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 3.9 MB (3924492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d478e353d009dfe08925d196921f6845eb6fe158e70304bc9b9b2fb952370c9`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:1184adc545dd3b80508bd0adcd117196187c4825b29ff153899089f4501c8684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e38664e416dbd750fcbef2b2c721aca187d947d630ebc182b261ae0f21b3e8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
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
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e04896951f4797da44433346ff837b12526b15ede28ac1391f6f529b8a5bb46`  
		Last Modified: Tue, 23 Jul 2024 06:16:19 GMT  
		Size: 11.7 MB (11688963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939e2e66405723c6e381754628c666f4480cd54ce632d36b4f31128c4bf6cb9`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee6af13f2ad58d368e1f54c9833e5d7b1093fb8e67d2d693018268220dee32e`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a61af3afc6a59b3caf11dff00dba8ac19254f62101f1ffa96f3e06b7bbf3d`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 92.9 KB (92903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:32dcd4adceddf5965142735cf711565c4d71d2fd65c46f638f6c2c88d2c5cdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6868034e60a48e100990f215ad44d0f7f612693e50d7973457c7d63a8f1103dc`

```dockerfile
```

-	Layers:
	-	`sha256:6e83eb80c81718b0e2802438a860455d9406d77c8fba4eb3a087230ca32834f1`  
		Last Modified: Tue, 23 Jul 2024 06:16:19 GMT  
		Size: 3.9 MB (3922156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:576ab878aa57f1bc0e41b7c88c53498ab35e8d1d7807748675a2d1541b7a17ba`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:9934738130c0d0eac989ad9387f991401146190767c418b84da3c5b4473606e5
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
$ docker pull neurodebian@sha256:fabd233511b29371372f9c089fd4b683864f679d1d252216ef8eea4864ca2c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe07a5b4c9c1ea95f2170b1a0087e99a61040d0d41574896c04818aa8b9015e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3ec0f21348ab8b97e349a1a230224eab2abaa91a9bc15ec1756ec679881613`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 11.3 MB (11266567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b6525920c59417749f5f5ed2a2b63bf70e4372d1ad1e43940269f4e46a6a39`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d510146f760f735becbde5f61ec22ff8776568601bab5334c20503e95b76a154`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b114ecc986793dc815210203aae62abfa08219b0f843467dbc1eeec64b622d3`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 92.8 KB (92781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5408265a03e3fc2f5df205622d83f4dccb742f73006527dd9e1a4ffb01eac9c`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:580991d536d1bc4083e536e117f083c498d841a0f9d1f6cd22c6f20ce261626d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9974c18c88586a5a7e0be07f0b836711a742452a233bb0f02ed0035a72456b`

```dockerfile
```

-	Layers:
	-	`sha256:37efcafc97e143a00d67dfcc8a8cce6afb3fd0ee1a47ad53c1283a640f457d55`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 3.9 MB (3924279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a29a33d0193d9594976606f3cbea45d1c7997a112205fda7d13587bf33e8faa5`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8ad50c552d2d9ba9971607e3e25fcff5e656fe578bc84e4ebd7fb18738512adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b4c5c48066c6bab18c83db1004c63f2276ce263810a3b47cd0e67ca0e5d0be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0c4964b2c74b33113f4f9253f8fdbd6f9effb7070fabfe7998ec7f9f71a68c`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 11.2 MB (11231990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a84d3037e0ebe02d7b2e60abbfa3c50ab185daf05e3e55e3f8ff6cf96a45b2`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784313ea4757f773fd668b9d92e36d3061207f4d5f2fc7c75d857979e14d6f21`  
		Last Modified: Tue, 23 Jul 2024 18:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f51ef3b42547d51fc5c3da2f3e174e60effa7629f2f7e46098c454225497cd1`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 93.1 KB (93109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a89e8d1db6d68a3f2363d7ce074b5496e4fa63f099ca409686e3f84f30ebda5`  
		Last Modified: Tue, 23 Jul 2024 18:36:05 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2d20471e880f9bbd6c72aae7179ae7d0d26c0ea16bbfc67999f481fe78ad46d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08416b7a7fa5ef781f905251ee5d1a660baae6bfaf1e10c86a265115cf1660ef`

```dockerfile
```

-	Layers:
	-	`sha256:01968acc1d8a7282a89c4b803ed512cd39f8497d1768e0cf330e008a56dfdad1`  
		Last Modified: Tue, 23 Jul 2024 18:36:06 GMT  
		Size: 3.9 MB (3924532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c13697cc7290159bcf6b045e62a67f922b62336ce65509f7615633065b67364b`  
		Last Modified: Tue, 23 Jul 2024 18:36:05 GMT  
		Size: 16.1 KB (16113 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ca14280056db89cfb3698b0f5ed6f7f98c228f7b413c045d84ba87127e8c13e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50812a4495199c3e047fae3ed8ad96942ce0584681f827fed5d49c763caa0d6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
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
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c2009cb5fa8b7669e4a2ddc7fe615fd9380d7fa24095ac161b734c176809b`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 11.7 MB (11689019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581009e1a3eab679cc96f1a56f84957915a31999300ee01d3b0eb71c1a4c9bc`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fe1928d3b2e8e4b5cd4c4b503be928244764ffb7b11b74acb72b734dd9f208`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfed7927d4c9944bfa51451f9fd78ccf4f2fec34f40ef194178d40a8c4bae9c`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 92.9 KB (92902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3ea134dabf34c21bb382a7c8d3557c91f40f18a3d35d74d32798fe37081a31`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:585b7f303597ee97acc8e1fd4412bdee58c4ae5d0eb0e80b2a2df82125aa3cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d25650556ecf8f5da6c003c46848f43f3fc156dd14b89a1d52b24f3e9e829db`

```dockerfile
```

-	Layers:
	-	`sha256:788b93f4232871e16b9893be5e8b6cde56c93769029ffa2a5cd71dee99730b96`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 3.9 MB (3922196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f697f0775bb09d617db679f5fa2ad36451d8af809edc427f8cfc7a07c8b1e80c`  
		Last Modified: Tue, 23 Jul 2024 06:16:19 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:d666b7dfd1e2c733118b91bd9d2e28456600cf9fd6f39d432996c331ed871fb3
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
$ docker pull neurodebian@sha256:3a3dacd8dc96c4600157ef1952dd2e5e4fe982d2dad7431358d7c27e4c2757f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66292272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8d90ef9e063476eb296f568d628c75554d9d83100f01bafafdad95e9cf216e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
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
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95209e4966d531d5c931399542274b21d850060079423c08a1878a68833aec55`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 11.1 MB (11104986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfcc9d547b28c0197ff7a323d9b22b76f47e15814975d67dbbb97e53ebafc35`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b41d188bccfa3b45960a95c278f8c902024914b7b05ed0d0e79cdb870715e05`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f638952d08e98890b62f809755d2c9ad0a07dc8fe6504baba832485584467aca`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 100.7 KB (100721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46d70ce8dd8d99e9ce02056cb1ad5d54d105614367bd5c1f56262b4a2bd5ea0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5efa4a7f679eeef05b95a9a80a10f17e7415178c98a306cb70a4fbaf47d51d`

```dockerfile
```

-	Layers:
	-	`sha256:cee9eddc17c2655dfb9abaf0cdf71d375aada9bcaf16023262c5a0035da85efe`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 4.2 MB (4223704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4501df5eb6df5c5c2f4feff8ebd1f42e47607ab814df96b3e3c861aa70e2c7b`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cde9c5093d7919668908f2795c05bc199d0c432638f67e9d14b309ab2edb8eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64938431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befb656edf4b25ace9183765b76423f2197e84039d81357e21cf823f3bfde5e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
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
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748620df5e1335ff4d2a1ff3d6b29fdcadb199a1da1c0f954ee400b0987da57`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 11.1 MB (11105782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28772ec05400cd0f7075f13813c452cc315f7c87a3370a48753a5530b8c202b2`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74765cc784e39ab51976cb4f82860a87708d3a5f7bba696c461c07136ec85c5`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c36deb65a886758fde62b0455cb2efcf0eba23ed9c43693d1ed048665413046`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 100.7 KB (100677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b631b50282e273242ea8ec4651730804f5e39c293de9e9c41e6d2059aa6f5952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e537dc44a9bf7b9bb9cfe463e69b23d635f05116354a8724e9eb267376818e0`

```dockerfile
```

-	Layers:
	-	`sha256:6a24eb35e9e307896a7530df9b7ec113f39630d9ca0832ba730d924cdb69fcdc`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 4.2 MB (4223309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea98358f3ad2b7c9a87381e505c068f04bc1c3c1c5f79192474dcaefe75ce9b0`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 13.8 KB (13758 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:fcd74b1122a78f38941aac24e98412a3c60225d7c351aa383651d3632af8fb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67676913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8053a7cf2f0a6835bd493e840cfa717c0b20a139e03a14b39749a75e8e7c7da6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
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
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c77211f128141a673636e216cc4d5f3e6fa8674bc357847ff9eb04f1b427a2`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 11.5 MB (11500120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e587578fa6285bc49b36daeed4fa6c88fc37fb4c9e75f0fc67ceb57495b4f223`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282d3333d81cb4ad90ea1458f97a73a58b780683b18204825ed5e7ed457efa`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5fa6aee575f2dd024b3e4d2792dc08580763adb69fa8f7ff39380585d9dd4f`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 100.6 KB (100635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7547f244373eefa4aa1f16d59e722f06a5d7d6465966dbfee113d03bd019446b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4233617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e67b4e71e1ea5cb009225bb500ed01fb2710613c394548c4a620d11dd208708`

```dockerfile
```

-	Layers:
	-	`sha256:3da418a9915b7fdac6c23aff7728473a3d24a8dcdf0ae64515ea57c160a5a113`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 4.2 MB (4220164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab295110c910721b348bcfb4aef1dd38b7f2520b28cedfb80c870d2460c72d2`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:6eb7047131d18122f0e2d754480629d1d823a544092c832286f32f954c70bfa2
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
$ docker pull neurodebian@sha256:9169aca8765b26832244003e164111bddf36e9000b1216f8e7a03c7f96c4fe7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66292710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86de54931fdb819e97959ffdc98c5b1d5c1d95609b179fc3ac1fc802d33a8945`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
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
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4203d3e26932e117e5a08d861f59e1899dce1c005702276450b904177c19cb2a`  
		Last Modified: Tue, 23 Jul 2024 07:14:51 GMT  
		Size: 11.1 MB (11105032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3355d9bc6ce568013c3b0db91282f933798aa18867ab4c1c817007bb650d6eab`  
		Last Modified: Tue, 23 Jul 2024 07:14:50 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8ac34ee9820db6d31a67aa65ff870c61daea5034053781f925a4158b91ad4d`  
		Last Modified: Tue, 23 Jul 2024 07:14:50 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3a4495a6fb1dd49d4a821cf3976220e6395a9e8439809d8cbf021e645ce2f9`  
		Last Modified: Tue, 23 Jul 2024 07:14:51 GMT  
		Size: 100.8 KB (100750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449f168b0c554b07cab2523e57a84d5385be3575dc1e6276859b3ed58065d1df`  
		Last Modified: Tue, 23 Jul 2024 07:14:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a26ac99eecf184cfe3431360a0cd033220f702ca73fa56dfd59d33e0d3a50266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82637fa1391447c6d0544d010aeaa356a69a64427c058a9707be2176451d39e`

```dockerfile
```

-	Layers:
	-	`sha256:a4ab3b457787b5e3126ec0fac5720bf2c186fa30a8f8d0e6b17e5b1a3ce030fa`  
		Last Modified: Tue, 23 Jul 2024 07:14:51 GMT  
		Size: 4.2 MB (4223740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:943ae89fbf22535224d00ebcdef1727f67a52537b65d0abafa7a4070e6d3cf3a`  
		Last Modified: Tue, 23 Jul 2024 07:14:50 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:82bf4e5ed94becd63bc80613bbbfcab1117f3531cb3e6bdc4de8b91584390bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64938791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4fd46d859c6c291dfcc03a794a375e2419819290d85a5ac3be035574f3acee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
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
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748620df5e1335ff4d2a1ff3d6b29fdcadb199a1da1c0f954ee400b0987da57`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 11.1 MB (11105782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28772ec05400cd0f7075f13813c452cc315f7c87a3370a48753a5530b8c202b2`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74765cc784e39ab51976cb4f82860a87708d3a5f7bba696c461c07136ec85c5`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c36deb65a886758fde62b0455cb2efcf0eba23ed9c43693d1ed048665413046`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 100.7 KB (100677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb59aa94f3e9a771660b397dd7d1d9b5696b3825b0a79e545024cd1d2a0849d`  
		Last Modified: Tue, 23 Jul 2024 18:35:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f14d63d20d8059739706c1703eb4b34926365cd9a6f1cc608f90d03aa733da22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668b5b5bd362e873dd3e0d4f8760bc5294fcdd2aab0ed043728a78c754145f9b`

```dockerfile
```

-	Layers:
	-	`sha256:e0a878916f8e961699113fb67ad468aea57e710c163490714237c67b508d9d2d`  
		Last Modified: Tue, 23 Jul 2024 18:35:12 GMT  
		Size: 4.2 MB (4223345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5642cb35f6a21f1a43ec2b4c604519bb2ce12aca7fa740d57a0f0170b0ce26d`  
		Last Modified: Tue, 23 Jul 2024 18:35:12 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f3bbd6cb40a972adad281c251a26b3849256f1d5e23eb4e46cf24bac38710bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8c3d85fb9747aab0f870841c258a2de0195db99c08ada430dff64008a85062`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
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
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6fbe20aa5b4a62df6fddf9098e73fcd193053f19ec4b96dcfc3980ed765b16`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 11.5 MB (11500131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939e2e66405723c6e381754628c666f4480cd54ce632d36b4f31128c4bf6cb9`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75cdda278d30c01a386f46a7403ae0ecf5bc79ede317554522d0468911dad85`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9347731466fa755649ac3f9513a02e4212f1ee9d62296c50f43a8ad484c73bc1`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 100.6 KB (100647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e0e622a2c8fffcc48a2e8ef53ef03849e5267ecfda9859881263db6951d853`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:09ea5537d94e7fc078811fd6a01bf389a0aa6cd17f4046584b89cfe35bb65dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e13baaa881b84dc52642d868a8eeb129e242389e8bab71d8314fb60db018700`

```dockerfile
```

-	Layers:
	-	`sha256:8d3ad12904a82508081c67419c32149f22aaf2a3f750bb2caeae9248f030cc27`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 4.2 MB (4220200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69a91c6d7601c8ea9fdca46d69836734a4129a6c0d0471974d6b9221047fab40`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 15.5 KB (15485 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:35696f693b6ef96260422b9091c766188a7983d82eb58b1eb04f6bd7b58ce84a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:8436872dff585d3f4fd9ba47de2a0c07d2c9601ea7683cd5d98156073fb3e61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69c59f4bc1665f4125a9108a35f53ff8fd3c0f0db4bea3086ff4c0cb4117d2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aadfed4b17ce30257b1e83849176e62dda5f82aa6e95a8478f76eec14d065d`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 5.4 MB (5360246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ad67a268cae8111d8fe8b7df873538bdf930ee3af83bddeae455228cf4b12a`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d727c6072b0d91a97e0e503910ae3a3875e0eb0f330dad37430449c5d538f6f1`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a1cbd18209d18420e1b340bb0af4bf1810b5523ee10e459833effca52500e`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 105.2 KB (105213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af0c65cce1965a1a6b3c2b2975e967c195bd2eba5a033dfefc365029b377dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45da22baf7d2b89589eaf2d5f3e761d81c297d1c7034615e130e5031d2b182c1`

```dockerfile
```

-	Layers:
	-	`sha256:b358a4f2b71ae1fc1b775755876a2990c2755cb455ca4551f7204050603fd0fb`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 2.0 MB (1977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:543ad7176c91bae6840122d5e6913e1dabd6c77bfd53962ded0190dfc7eaffd4`  
		Last Modified: Wed, 05 Jun 2024 02:20:28 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0f5b1443b574b5ace2b0987cd1977e8210613ba725ed472573cfbe9c5cfe23ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b273064c8a6c81f5cacbef5005cb8661311bf23c477bd55a7c401646da2abe1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cef2030478aeb05027ae08e0f6b777479bcfbf91a27f17361fc0b0e8736b09`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 5.3 MB (5340340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84221cff6256e155e65ee5ee2cf1b79bc4f716f5f843f95d834bc0ab9cef7d97`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cf015f90c17438e9ab1dffee54454fd740a774dbcb9498497fa9f358af8672`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad32ddb7c055110e7c49a0cd0fd2fda98f4276a618d67f805938519e1998cf6`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 105.3 KB (105272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:284dd670c2b0916e7375fa296cc94b380cd5d78ea887f00690b52596df26c8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c3a8fbbf35052ef29f84d07daf978d8d877ce6f9fcacb449acf1ffd0144aba`

```dockerfile
```

-	Layers:
	-	`sha256:813766013ab606a80d4443383a3397da61d8900db25f42772d29d6cf04b2bce7`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 2.0 MB (1978184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1bf415abcaaa1e6c9340665180fe32490ac956e54c13e38d2b031ff973533bb`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 13.6 KB (13634 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:69eea5eee69951a81433ff44e3a76d25374f43b5ede7e2be7991cafbb9ab8480
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2614cd1459a929df672f30c4de3ff5f4f423b10d0204439ea00b153fb35a4ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ba3c03399056b312baca33d2bef793afd92675c192b7d90af7db16bd0fe08b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab32168f62b0a56e9d1738ba27dd0e7b6b3b7c2e892a19527bf5495039d950`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 5.4 MB (5360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c5f6a989efa6cf7d58ae9018a40243e81a4b1bdcb7a242de74e77d92f945db`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfefe3835ca69f4b947ebba8fa742346a61ebab4361ca98d383e7ba7489fb004`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdc23cea86c9950d617b60a8e9e162dfa93280986c8e4ea3c9efc6450810bbd`  
		Last Modified: Wed, 05 Jun 2024 02:20:11 GMT  
		Size: 105.2 KB (105229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026d40b80d1375c0c978e08b9ee3768e5635a011dcf98d75ec8a728fea6461cb`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8052d782c0e8c3437bea67acf4b2a22d79a7dffa5297317f4776bdc773d0701a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1993579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b545e88e893b1df4e4133705e4b3af666a09fa688c52562b97322c9c6d4c0099`

```dockerfile
```

-	Layers:
	-	`sha256:fa21014e2151b093cd2b0f181163b6be1985c8371a5cc2d7e52e4613433f80bb`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 2.0 MB (1977992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15b3763a1a7a0714189ffe6046baae58c42e3ed9f083352e41a11ca77cd14e5`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 15.6 KB (15587 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a765833d6e8524c6babfed520f054ff84a6adea03bbc27c95574cb07aa8fa14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10519d9344ce22cf8b6dffbe4a09a105acf140f518107098b2c66a242582141f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cef2030478aeb05027ae08e0f6b777479bcfbf91a27f17361fc0b0e8736b09`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 5.3 MB (5340340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84221cff6256e155e65ee5ee2cf1b79bc4f716f5f843f95d834bc0ab9cef7d97`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cf015f90c17438e9ab1dffee54454fd740a774dbcb9498497fa9f358af8672`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad32ddb7c055110e7c49a0cd0fd2fda98f4276a618d67f805938519e1998cf6`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 105.3 KB (105272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5151156e9cc1c424bbecfc412c4effcbd14bdcecf53693bab61b678ae9ed5fd9`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d450bd9f532b807f700d228fe37fceb706c7960f3b87d06090658a57978a3d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1994083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e25fe54f10b92c153df2cdadaa8eb3efa03f0dee4e099174db24e3ac65946`

```dockerfile
```

-	Layers:
	-	`sha256:ed1c978d1833cda54dd5250213c0833f524702bb98f9f00a81505d89c5d1b173`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 2.0 MB (1978220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b63cad0b9de5d2bb91de6e7fb6616926fabbf2094cb6ffb471176092d3df97e`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 15.9 KB (15863 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:ec0ea51809c4a7caf3e84ace97c51774a2c4a8a756870b79c371406dbd1b71ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:50332ada0faa254b85fa3c99a2fb1022451d84260772392e0e6ae137e1769632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33268848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324940094fa472191de171a4ba863183350cf4d1a1e43ccc421a71b66e094cf8`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d862268cca33b20dc33b79c6e362573fb742dcd42a2c8a20009493450369ddc5`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 3.6 MB (3622702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7004f9084ccb849430b7c98f8ef2eb567e8caa461377671d0ac1aba06db6d2`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f70324bbe5ab5ca9fd0e2cf5ea3b95c81703e6cd98a5b415809ceb4638987c`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ced8e730e6d5dd8769cd1bdbbdeb4d189659f419d807c42534b5d3654f8c48`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 110.1 KB (110097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f4826a37a310d849e4c83b7f084dee6af9a823f43d94d62ac6a708b6ec638e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f326f94e3b16867754bfd251636fdec9ac49e83e1e1cb329c204511c7e7ae1dc`

```dockerfile
```

-	Layers:
	-	`sha256:7246425b0d75d34d4e317919e463322149ad3be8c5ef7e9c58c8dc4712ece091`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 2.0 MB (2015659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ed2ec0795d1e6759f5395fa3f89dc5ecae1e9b4c754824dab0613aa1226807`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9bcf1392985d3afd0ecbc668940d0456f696bcdf4730bbe47f0cd4fa295bfaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31066446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d877dec38ef78dcb8000403d7491c4618ddf3d900efc02d7a784d5c1185d7e6c`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dc16b23ee00d53f4adf324698b87c709e486e05c5b634739181bbce1d56c82`  
		Last Modified: Tue, 02 Jul 2024 15:59:21 GMT  
		Size: 3.6 MB (3594186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f31c419c5921eb500e6bb4d1394cbc4cce89c991aa6ea0cb14769a2e4ceff8b`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e4d5b48676456aba5e60bf7d682a9253b4301c3e43347c5f6b707ffe70669e`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d807b10b523db43ea06a66dc581da167eaaa97bc25dc203e08be033b9c646`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 110.2 KB (110240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14e7e743ccaae8dbbd8443016ed72061835e4425f075357bd75167779976b156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8170de6e72729ed20e70e4dc912f16558b929bdbc526e2c6a9fe606c149a8e1`

```dockerfile
```

-	Layers:
	-	`sha256:6a6fe57d1a82e58c192048c7cb131fdabb2a4364f02324a8fa100b681aa8356a`  
		Last Modified: Tue, 02 Jul 2024 15:59:21 GMT  
		Size: 2.0 MB (2015918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5262a37a6988f6c82d7bcf44109f408b46c5d30de14569ccb3690d44371739`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 13.7 KB (13682 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:97f3c220574924fe964fa06d61fc892692bb1a6b009a039df7d5e66c78d35239
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2623a7c28522a7b25eb3fe44172632fc2b1c20a3ac1433aac85570c3d5a894af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69650e35f150a56a819ebf3c57f2723e3327461a3975bd8a64633add1bb9b27d`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c600cd6d952702399348890ccb963cad1adb5d6098ffb092caec1a36545b59`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 3.6 MB (3622723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ba852eb2127a816ea9594d23647541e8598c273234f40d074e70f717f2b363`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb0f24912426a9bcca1a5e3ee9b310973b13df995b7565182f492ab021df7e2`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263c87d1b026352611e6b8267a292c541a135e3842177e774f5f9d5b91f64ef5`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 110.1 KB (110118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8772a37561b5fd83f6ab10e0506ed41d8922a4fd314dce23f19451b55a5d37ea`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dd1b06de41553a1c77638c8b54f222974b849d784be607edd211468735b0c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612275f45e18d0d569032ec2fc8952576023e24a60c792c2616ffa5aad12d4f1`

```dockerfile
```

-	Layers:
	-	`sha256:3447301f1f169b1f3acdd1f023f78fe04e8dd87a9de8dc89f3ef9b82fc18a35a`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 2.0 MB (2015695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7244937c2399932fdc4026b34ea0785d361e1562807e9a3c5a205419dd4a72a`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 15.6 KB (15635 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1933b2f19205647fc57be0a0ce1f60390d0ca130346609824d899c010635ee7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31066708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d41beebcdb80261bc322b441a2586ca83ceb3ebba450083e4795434e7bc28c5`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dc16b23ee00d53f4adf324698b87c709e486e05c5b634739181bbce1d56c82`  
		Last Modified: Tue, 02 Jul 2024 15:59:21 GMT  
		Size: 3.6 MB (3594186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f31c419c5921eb500e6bb4d1394cbc4cce89c991aa6ea0cb14769a2e4ceff8b`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e4d5b48676456aba5e60bf7d682a9253b4301c3e43347c5f6b707ffe70669e`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d807b10b523db43ea06a66dc581da167eaaa97bc25dc203e08be033b9c646`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 110.2 KB (110240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ad070ba592bf4d760b4956a98ae70ec4651c7f5db0f4e2aabf5ac2bfe3b2c1`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:13f5ac4a8e9c0cef26a3377cc0f187b30ff2d40b24c8960944ec77b804232628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2acc579da0541db5b1806051198453ff0806569e736508bcf7c0c8876c064c5`

```dockerfile
```

-	Layers:
	-	`sha256:4fea70f73d3b08b467c57896ed29255771bb9295dba7ed13d1e55b6054cfb260`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 2.0 MB (2015954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b174930aea8ca924db6c39b0b1980d1d11b0b31e5eb7814b33f219112f583424`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:305a959a60ae161fd1e2f8b9d126acb78f47303f5b2dd360f2aa4e99d8116d8d
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
$ docker pull neurodebian@sha256:62882ad0f33cbdd9eafb7c6e9b5eb8ae372a25a3c0f21f62d0acdf1497333dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fead143accff411376d04d2bb8b320457f355d17d0d27de94083e816f8f3a0f6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d842fdeb916ebdf94d0bbf538179616ad81e7f1dedc4ed501023f251d18357`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 11.3 MB (11266589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b6525920c59417749f5f5ed2a2b63bf70e4372d1ad1e43940269f4e46a6a39`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe030c3262712f09530bec25a14ab3358602038a50cd68318f64e517a0d7106d`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e7a9c054202f338852b4263dacb6b225a16d4950ae6bb727864599c43ac5f4`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 92.8 KB (92805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c08007fdc95a1b89e9bd08160fd1ac6c3b8fa0f7b865ca9831db8c621d10d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea68d861f08bf1d925c0f249e39c42140b65d239b0cb8609a37c5443bbe64b8f`

```dockerfile
```

-	Layers:
	-	`sha256:564761329007c6319eda102596fe80eafa8f03a704f8c8df0d8850da67515ce5`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 3.9 MB (3924239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff9da6553a56e9140cd5c7d5f7c5f801677dc978c7cc89afb8cca432ddd6512`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b71cd83d5bd8b0be36b87ea3e0563cab2fd7fdc8fda441dfca994c724878c959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2a5069168923cdc4f70896cc2dcaf93a70115c7d82eaec01f4a07b469d6ef2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0c4964b2c74b33113f4f9253f8fdbd6f9effb7070fabfe7998ec7f9f71a68c`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 11.2 MB (11231990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a84d3037e0ebe02d7b2e60abbfa3c50ab185daf05e3e55e3f8ff6cf96a45b2`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784313ea4757f773fd668b9d92e36d3061207f4d5f2fc7c75d857979e14d6f21`  
		Last Modified: Tue, 23 Jul 2024 18:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f51ef3b42547d51fc5c3da2f3e174e60effa7629f2f7e46098c454225497cd1`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 93.1 KB (93109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:757c7bd29e99f08e021102ec7bab71368c08fc5b8dedd1b342098d8ce5324fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd73107a0a9709640c47c4e4f59fa6ca1ebabf8a0658aa9381cbf4bde03a849`

```dockerfile
```

-	Layers:
	-	`sha256:862421904df231d53bf60f81099184d7c0682e30c697de8f23794783ed2daf08`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 3.9 MB (3924492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d478e353d009dfe08925d196921f6845eb6fe158e70304bc9b9b2fb952370c9`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:1184adc545dd3b80508bd0adcd117196187c4825b29ff153899089f4501c8684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e38664e416dbd750fcbef2b2c721aca187d947d630ebc182b261ae0f21b3e8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
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
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e04896951f4797da44433346ff837b12526b15ede28ac1391f6f529b8a5bb46`  
		Last Modified: Tue, 23 Jul 2024 06:16:19 GMT  
		Size: 11.7 MB (11688963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939e2e66405723c6e381754628c666f4480cd54ce632d36b4f31128c4bf6cb9`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee6af13f2ad58d368e1f54c9833e5d7b1093fb8e67d2d693018268220dee32e`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a61af3afc6a59b3caf11dff00dba8ac19254f62101f1ffa96f3e06b7bbf3d`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 92.9 KB (92903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:32dcd4adceddf5965142735cf711565c4d71d2fd65c46f638f6c2c88d2c5cdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6868034e60a48e100990f215ad44d0f7f612693e50d7973457c7d63a8f1103dc`

```dockerfile
```

-	Layers:
	-	`sha256:6e83eb80c81718b0e2802438a860455d9406d77c8fba4eb3a087230ca32834f1`  
		Last Modified: Tue, 23 Jul 2024 06:16:19 GMT  
		Size: 3.9 MB (3922156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:576ab878aa57f1bc0e41b7c88c53498ab35e8d1d7807748675a2d1541b7a17ba`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:ee6e57e8f69661aa0376f17ea69c259624a498970172f61a4db5ebcd9c29fdaf
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
$ docker pull neurodebian@sha256:8df25b7381b56e0c058ce85c9a33f671c6e1daf7f46efbcf14fd5528b3202b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59098051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246cb0db993b407cffde6493e242d3de06ae128cf87b2267b22a47439c4af6ed`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:119c9b007e2126bffd87612039b5305513fe8cedcb052cb679094aa5c0182fe8 in / 
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
	-	`sha256:66b1db94c2eed297b9f748a1ebf50a98574aafe88f8cfc08d94ad3f35d83c48a`  
		Last Modified: Tue, 23 Jul 2024 05:29:19 GMT  
		Size: 52.8 MB (52781957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebedff2812269508116bdc4cfef008441e28a0371783e5d7858c4781c1feb07d`  
		Last Modified: Tue, 23 Jul 2024 06:16:50 GMT  
		Size: 6.2 MB (6224015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7a97239599a4e60b31be674f713a6b1e22c175b2c02845b61568d1db2fca0e`  
		Last Modified: Tue, 23 Jul 2024 06:16:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a545f13c4b3248136207595b0479eabda06be2625497db2580a1d192d0fb472`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5226c81f305bd3e0c716692aecb129ea31b38f0a17252ed8ce8074fdb8890d3`  
		Last Modified: Tue, 23 Jul 2024 06:16:49 GMT  
		Size: 90.1 KB (90093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:44d15eaf8b16820042eb3da978d2cdae7052cb71a741d96ffe135242c6671f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc7595d4909f057493250e003bc9e2c5f3afa421c262c0372e83e6592bd1755`

```dockerfile
```

-	Layers:
	-	`sha256:2660976885a91f1b983c76bf298e1b3850a460a9a8529833488f454f140d5528`  
		Last Modified: Tue, 23 Jul 2024 06:16:50 GMT  
		Size: 3.6 MB (3560484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:542975e582d79cf3bd0666b614e52805ade397c7a5c3985cc1d0f1b0e27c7f6e`  
		Last Modified: Tue, 23 Jul 2024 06:16:49 GMT  
		Size: 13.4 KB (13395 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8c95c9493701e6ce942dc6bd4246781a631d9b5197e631b6ae293949023ccd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59372464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695e6cfe4adc6f346d5c84bbf1bc7154bcd6669f2a0d083c38ea98d34cdd67`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:368e6d1d2999bc62054217cfec29bdcf59fe672d1d5db07c2f2c2939222c4a42 in / 
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
	-	`sha256:88161cad314c45536b001a7558a18c0a54c991650605a6212e9720f7ac3bbc4a`  
		Last Modified: Tue, 23 Jul 2024 04:21:45 GMT  
		Size: 53.1 MB (53060158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c5e22eab6bfb0637511700afc2f7acd0c3fce57b42bad64a4534c5c34f2b23`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 6.2 MB (6219604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88300873cb59f94a9b5b736e89bc5fdec8a6c027a5aa343e28fe5596a82a1177`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9261c28300bccbc9dc3a8f5e25c8ec61266871386ae0bf74f7f95402d20b353a`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a368fbf666afd365681e06a696c68bc93362d632f6326c8caead3c876de84885`  
		Last Modified: Tue, 23 Jul 2024 18:37:43 GMT  
		Size: 90.7 KB (90721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:af51a66c271250ae8a200c0aacf5743141c34b74875ed711b01d39de1fd3d171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d942133d8a2c4c5122c1362446eb9237ac2b26dcd3dbc033c75e5120c0ff5049`

```dockerfile
```

-	Layers:
	-	`sha256:dad4a51b19f92441f221131eabd713c323dd07f9199d2cc5407851b23d413a20`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 3.6 MB (3561526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2161ab33b33d74b6035e8bc891ad6b32b14e53933ea34e9b1c0c298e9b95d0fb`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 13.7 KB (13670 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:3b372a54e1ce429917523e9c2859fb6720877ec0f30be7ed8ce8d07abe5109fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60347544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f950c70258e58d2a04cbaa96072681433773c05ea1973cfa4e9bdd4d5c609e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:934dcd467a296b55e9373c03c1e502c3a9f186f9c1e08b54e88bb5c0bf30fd70 in / 
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
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82bec79dff3a3ed87ff22e886c5aafea0a550f124ca9f5991042ef6cc4c99aa`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 6.6 MB (6554808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd40d97447dd271777a17658fddd6e0adb18cb96c4c55d60d7b164ef5cf4fb8`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ed2f5ee74e882fbfb7a7ab0794df8358d83de25f763a8e085fc0ecabe76d2f`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f41dfdfe44562c08bf96630bed334529c1ebf002d479fc1d5930fb70cfe0859`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 90.0 KB (90008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb83ef00b339426a4d143411d85fa66511dcdc042a56a33803050d28f153a258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2b7a38b2f8a331c5bc8798fc52439dfc30869aa43d893ab5362e307440aad2`

```dockerfile
```

-	Layers:
	-	`sha256:f3e38412e47a224b162530825ddb5c0174967d282cb6b3bf7598e1ae9e09b248`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 3.6 MB (3557577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74437b60de29329d791d3af9660d31ba10f449b2fbb525da0626d417e2e6ccfd`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:26583651880b747302b934d5a887f572a8b61dce1871f7eedbfe85a7f57e9dfc
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
$ docker pull neurodebian@sha256:fe00f914907411d2718c1090b33671bd938acc75d18f6e9bd33915ae25007622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59098491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3329beaad1b7df1a274c23c124cf41b240f4974f192876230d1a238a6723945`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:119c9b007e2126bffd87612039b5305513fe8cedcb052cb679094aa5c0182fe8 in / 
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
	-	`sha256:66b1db94c2eed297b9f748a1ebf50a98574aafe88f8cfc08d94ad3f35d83c48a`  
		Last Modified: Tue, 23 Jul 2024 05:29:19 GMT  
		Size: 52.8 MB (52781957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba78cc727fb8c4d6be3b81320c6cad029de3e21545cbd6ff7f5d3e24101f151a`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 6.2 MB (6224024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2d81607b27beb9a44d5a4417a9a035589e70b3b1ec2100391a8b57208c416f`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a545f13c4b3248136207595b0479eabda06be2625497db2580a1d192d0fb472`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca6000aeeffffc4a99aa4b2a506c1c37b60feaba0f4abbb0b0df48d71c168b3`  
		Last Modified: Tue, 23 Jul 2024 06:16:48 GMT  
		Size: 90.1 KB (90134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73252cba8a182a2d4e3711e7b3ca228fe88fc064566e9fca00041e6169eac54`  
		Last Modified: Tue, 23 Jul 2024 06:16:48 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1f17ba763e3de97abf585a033972887d9566a765283b42b13e76d63a07fb6c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab996e76af23a9465feb34e25cf43c601f80837b9cb33fc4c9a699029842601b`

```dockerfile
```

-	Layers:
	-	`sha256:029906b62d9492d3fd7fcc7f30c42d40dbca591a8e4f4625452a132c7bb16237`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 3.6 MB (3560520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed57b663d769dc87ecba0f0d26f41a9774ef1d870b398bf12f681312a26ccec`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bf133873c23d03980c9d3b650b754fd4f358e3e0e352eb32c15ff2f0f71a4c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59372858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b36d5dd60acbe2494379448b88f3860f372c0fb76e1fd36bfb41f506c36333`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:368e6d1d2999bc62054217cfec29bdcf59fe672d1d5db07c2f2c2939222c4a42 in / 
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
	-	`sha256:88161cad314c45536b001a7558a18c0a54c991650605a6212e9720f7ac3bbc4a`  
		Last Modified: Tue, 23 Jul 2024 04:21:45 GMT  
		Size: 53.1 MB (53060158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c5e22eab6bfb0637511700afc2f7acd0c3fce57b42bad64a4534c5c34f2b23`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 6.2 MB (6219604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88300873cb59f94a9b5b736e89bc5fdec8a6c027a5aa343e28fe5596a82a1177`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9261c28300bccbc9dc3a8f5e25c8ec61266871386ae0bf74f7f95402d20b353a`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a368fbf666afd365681e06a696c68bc93362d632f6326c8caead3c876de84885`  
		Last Modified: Tue, 23 Jul 2024 18:37:43 GMT  
		Size: 90.7 KB (90721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02deda8175a76811cbe2e5cd721980efdbc7a9d4ad836f3a0f7d07ac36ce51a2`  
		Last Modified: Tue, 23 Jul 2024 18:38:00 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:16c1f738d55249a635030e91f4ea08ba5bf2b58aac18867449d4056178dae3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e658cbf98e35d798d073a33235d32b9ea30ccd99ff3aa192c0c0e51ce3555df9`

```dockerfile
```

-	Layers:
	-	`sha256:04b19be0c9e27b3babc5ab6687d6d64e862a4b989d3feb1d0d1f1aa812493051`  
		Last Modified: Tue, 23 Jul 2024 18:38:00 GMT  
		Size: 3.6 MB (3561562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f305496ab906cad0f4da0b7b7b5a7c6e3a2f1140d9dbd2afd4fed76ff1a231e`  
		Last Modified: Tue, 23 Jul 2024 18:38:00 GMT  
		Size: 15.7 KB (15703 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:573427ab2013d8649e8c77e0c43bc3c7b5b5f4fcde037e6c85a054575958da8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60347600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087f6bb71890c249e63439d7a260d4d4ff8b25d84f6ff76e84993a8400a9217c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:934dcd467a296b55e9373c03c1e502c3a9f186f9c1e08b54e88bb5c0bf30fd70 in / 
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
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5853df0c476cb6b47074aecdc44c8989de1742ae9f80314550a5b130cbd8cc93`  
		Last Modified: Tue, 23 Jul 2024 06:16:45 GMT  
		Size: 6.6 MB (6554507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ea7f033db96bdba75250d4e1d338c9d502f3041c12b5d849f4b056c52135b1`  
		Last Modified: Tue, 23 Jul 2024 06:16:44 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2c54943a31f955045ec02343ddd94eac368955c1adf7e5c49bf9d15b245dcf`  
		Last Modified: Tue, 23 Jul 2024 06:16:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46257428d44167f3bc35b5e28d989e657f3ba1561445dc6279343bfbd3d6e182`  
		Last Modified: Tue, 23 Jul 2024 06:16:45 GMT  
		Size: 90.0 KB (89966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325034bc80906c9ecd3452f092b7378c6ea12b3e022d1839bc4e2580c8ebed12`  
		Last Modified: Tue, 23 Jul 2024 06:16:45 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:04eb5e30a4c547f455df66af4e1bdd2a670958758479b28c99da857edad49e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae053737de19f1e726412e8398493852de05747ad7b20e98595017394c240a00`

```dockerfile
```

-	Layers:
	-	`sha256:1c58c3cfa44d3b57862b1ac055d5022d978d6d2bd6781ffd4800c75fc04921d1`  
		Last Modified: Tue, 23 Jul 2024 06:16:45 GMT  
		Size: 3.6 MB (3557613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c52f4ebd0b2d5e69e3a5681d4454b99743cca8d75a57d5175f3edb59fa3cf83e`  
		Last Modified: Tue, 23 Jul 2024 06:16:44 GMT  
		Size: 15.4 KB (15400 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:d666b7dfd1e2c733118b91bd9d2e28456600cf9fd6f39d432996c331ed871fb3
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
$ docker pull neurodebian@sha256:3a3dacd8dc96c4600157ef1952dd2e5e4fe982d2dad7431358d7c27e4c2757f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66292272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8d90ef9e063476eb296f568d628c75554d9d83100f01bafafdad95e9cf216e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
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
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95209e4966d531d5c931399542274b21d850060079423c08a1878a68833aec55`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 11.1 MB (11104986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfcc9d547b28c0197ff7a323d9b22b76f47e15814975d67dbbb97e53ebafc35`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b41d188bccfa3b45960a95c278f8c902024914b7b05ed0d0e79cdb870715e05`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f638952d08e98890b62f809755d2c9ad0a07dc8fe6504baba832485584467aca`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 100.7 KB (100721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46d70ce8dd8d99e9ce02056cb1ad5d54d105614367bd5c1f56262b4a2bd5ea0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d5efa4a7f679eeef05b95a9a80a10f17e7415178c98a306cb70a4fbaf47d51d`

```dockerfile
```

-	Layers:
	-	`sha256:cee9eddc17c2655dfb9abaf0cdf71d375aada9bcaf16023262c5a0035da85efe`  
		Last Modified: Tue, 23 Jul 2024 07:14:43 GMT  
		Size: 4.2 MB (4223704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4501df5eb6df5c5c2f4feff8ebd1f42e47607ab814df96b3e3c861aa70e2c7b`  
		Last Modified: Tue, 23 Jul 2024 07:14:42 GMT  
		Size: 13.5 KB (13478 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:cde9c5093d7919668908f2795c05bc199d0c432638f67e9d14b309ab2edb8eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64938431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befb656edf4b25ace9183765b76423f2197e84039d81357e21cf823f3bfde5e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
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
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748620df5e1335ff4d2a1ff3d6b29fdcadb199a1da1c0f954ee400b0987da57`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 11.1 MB (11105782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28772ec05400cd0f7075f13813c452cc315f7c87a3370a48753a5530b8c202b2`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74765cc784e39ab51976cb4f82860a87708d3a5f7bba696c461c07136ec85c5`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c36deb65a886758fde62b0455cb2efcf0eba23ed9c43693d1ed048665413046`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 100.7 KB (100677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b631b50282e273242ea8ec4651730804f5e39c293de9e9c41e6d2059aa6f5952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4237067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e537dc44a9bf7b9bb9cfe463e69b23d635f05116354a8724e9eb267376818e0`

```dockerfile
```

-	Layers:
	-	`sha256:6a24eb35e9e307896a7530df9b7ec113f39630d9ca0832ba730d924cdb69fcdc`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 4.2 MB (4223309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea98358f3ad2b7c9a87381e505c068f04bc1c3c1c5f79192474dcaefe75ce9b0`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 13.8 KB (13758 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:fcd74b1122a78f38941aac24e98412a3c60225d7c351aa383651d3632af8fb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67676913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8053a7cf2f0a6835bd493e840cfa717c0b20a139e03a14b39749a75e8e7c7da6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
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
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c77211f128141a673636e216cc4d5f3e6fa8674bc357847ff9eb04f1b427a2`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 11.5 MB (11500120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e587578fa6285bc49b36daeed4fa6c88fc37fb4c9e75f0fc67ceb57495b4f223`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282d3333d81cb4ad90ea1458f97a73a58b780683b18204825ed5e7ed457efa`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a5fa6aee575f2dd024b3e4d2792dc08580763adb69fa8f7ff39380585d9dd4f`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 100.6 KB (100635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7547f244373eefa4aa1f16d59e722f06a5d7d6465966dbfee113d03bd019446b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4233617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e67b4e71e1ea5cb009225bb500ed01fb2710613c394548c4a620d11dd208708`

```dockerfile
```

-	Layers:
	-	`sha256:3da418a9915b7fdac6c23aff7728473a3d24a8dcdf0ae64515ea57c160a5a113`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 4.2 MB (4220164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ab295110c910721b348bcfb4aef1dd38b7f2520b28cedfb80c870d2460c72d2`  
		Last Modified: Tue, 23 Jul 2024 06:16:02 GMT  
		Size: 13.5 KB (13453 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:6eb7047131d18122f0e2d754480629d1d823a544092c832286f32f954c70bfa2
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
$ docker pull neurodebian@sha256:9169aca8765b26832244003e164111bddf36e9000b1216f8e7a03c7f96c4fe7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66292710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86de54931fdb819e97959ffdc98c5b1d5c1d95609b179fc3ac1fc802d33a8945`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
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
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4203d3e26932e117e5a08d861f59e1899dce1c005702276450b904177c19cb2a`  
		Last Modified: Tue, 23 Jul 2024 07:14:51 GMT  
		Size: 11.1 MB (11105032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3355d9bc6ce568013c3b0db91282f933798aa18867ab4c1c817007bb650d6eab`  
		Last Modified: Tue, 23 Jul 2024 07:14:50 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8ac34ee9820db6d31a67aa65ff870c61daea5034053781f925a4158b91ad4d`  
		Last Modified: Tue, 23 Jul 2024 07:14:50 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3a4495a6fb1dd49d4a821cf3976220e6395a9e8439809d8cbf021e645ce2f9`  
		Last Modified: Tue, 23 Jul 2024 07:14:51 GMT  
		Size: 100.8 KB (100750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449f168b0c554b07cab2523e57a84d5385be3575dc1e6276859b3ed58065d1df`  
		Last Modified: Tue, 23 Jul 2024 07:14:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a26ac99eecf184cfe3431360a0cd033220f702ca73fa56dfd59d33e0d3a50266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82637fa1391447c6d0544d010aeaa356a69a64427c058a9707be2176451d39e`

```dockerfile
```

-	Layers:
	-	`sha256:a4ab3b457787b5e3126ec0fac5720bf2c186fa30a8f8d0e6b17e5b1a3ce030fa`  
		Last Modified: Tue, 23 Jul 2024 07:14:51 GMT  
		Size: 4.2 MB (4223740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:943ae89fbf22535224d00ebcdef1727f67a52537b65d0abafa7a4070e6d3cf3a`  
		Last Modified: Tue, 23 Jul 2024 07:14:50 GMT  
		Size: 15.5 KB (15512 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:82bf4e5ed94becd63bc80613bbbfcab1117f3531cb3e6bdc4de8b91584390bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64938791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4fd46d859c6c291dfcc03a794a375e2419819290d85a5ac3be035574f3acee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
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
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2748620df5e1335ff4d2a1ff3d6b29fdcadb199a1da1c0f954ee400b0987da57`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 11.1 MB (11105782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28772ec05400cd0f7075f13813c452cc315f7c87a3370a48753a5530b8c202b2`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74765cc784e39ab51976cb4f82860a87708d3a5f7bba696c461c07136ec85c5`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c36deb65a886758fde62b0455cb2efcf0eba23ed9c43693d1ed048665413046`  
		Last Modified: Tue, 23 Jul 2024 18:34:49 GMT  
		Size: 100.7 KB (100677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb59aa94f3e9a771660b397dd7d1d9b5696b3825b0a79e545024cd1d2a0849d`  
		Last Modified: Tue, 23 Jul 2024 18:35:12 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f14d63d20d8059739706c1703eb4b34926365cd9a6f1cc608f90d03aa733da22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4239137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668b5b5bd362e873dd3e0d4f8760bc5294fcdd2aab0ed043728a78c754145f9b`

```dockerfile
```

-	Layers:
	-	`sha256:e0a878916f8e961699113fb67ad468aea57e710c163490714237c67b508d9d2d`  
		Last Modified: Tue, 23 Jul 2024 18:35:12 GMT  
		Size: 4.2 MB (4223345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5642cb35f6a21f1a43ec2b4c604519bb2ce12aca7fa740d57a0f0170b0ce26d`  
		Last Modified: Tue, 23 Jul 2024 18:35:12 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f3bbd6cb40a972adad281c251a26b3849256f1d5e23eb4e46cf24bac38710bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67677294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8c3d85fb9747aab0f870841c258a2de0195db99c08ada430dff64008a85062`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:d1f79afb47e16fbf87d0a90342c567c752e14b1bf325fa45d6de69ea871b26df in / 
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
	-	`sha256:35a8dcedb97fd8133fbcd18694f30c60eebc7e4f268630ab7b35eefe40254457`  
		Last Modified: Tue, 23 Jul 2024 03:58:11 GMT  
		Size: 56.1 MB (56074170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6fbe20aa5b4a62df6fddf9098e73fcd193053f19ec4b96dcfc3980ed765b16`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 11.5 MB (11500131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939e2e66405723c6e381754628c666f4480cd54ce632d36b4f31128c4bf6cb9`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75cdda278d30c01a386f46a7403ae0ecf5bc79ede317554522d0468911dad85`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9347731466fa755649ac3f9513a02e4212f1ee9d62296c50f43a8ad484c73bc1`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 100.6 KB (100647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e0e622a2c8fffcc48a2e8ef53ef03849e5267ecfda9859881263db6951d853`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:09ea5537d94e7fc078811fd6a01bf389a0aa6cd17f4046584b89cfe35bb65dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e13baaa881b84dc52642d868a8eeb129e242389e8bab71d8314fb60db018700`

```dockerfile
```

-	Layers:
	-	`sha256:8d3ad12904a82508081c67419c32149f22aaf2a3f750bb2caeae9248f030cc27`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 4.2 MB (4220200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69a91c6d7601c8ea9fdca46d69836734a4129a6c0d0471974d6b9221047fab40`  
		Last Modified: Tue, 23 Jul 2024 06:16:21 GMT  
		Size: 15.5 KB (15485 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:305a959a60ae161fd1e2f8b9d126acb78f47303f5b2dd360f2aa4e99d8116d8d
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
$ docker pull neurodebian@sha256:62882ad0f33cbdd9eafb7c6e9b5eb8ae372a25a3c0f21f62d0acdf1497333dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fead143accff411376d04d2bb8b320457f355d17d0d27de94083e816f8f3a0f6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d842fdeb916ebdf94d0bbf538179616ad81e7f1dedc4ed501023f251d18357`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 11.3 MB (11266589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b6525920c59417749f5f5ed2a2b63bf70e4372d1ad1e43940269f4e46a6a39`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe030c3262712f09530bec25a14ab3358602038a50cd68318f64e517a0d7106d`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e7a9c054202f338852b4263dacb6b225a16d4950ae6bb727864599c43ac5f4`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 92.8 KB (92805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c08007fdc95a1b89e9bd08160fd1ac6c3b8fa0f7b865ca9831db8c621d10d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea68d861f08bf1d925c0f249e39c42140b65d239b0cb8609a37c5443bbe64b8f`

```dockerfile
```

-	Layers:
	-	`sha256:564761329007c6319eda102596fe80eafa8f03a704f8c8df0d8850da67515ce5`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 3.9 MB (3924239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff9da6553a56e9140cd5c7d5f7c5f801677dc978c7cc89afb8cca432ddd6512`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b71cd83d5bd8b0be36b87ea3e0563cab2fd7fdc8fda441dfca994c724878c959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2a5069168923cdc4f70896cc2dcaf93a70115c7d82eaec01f4a07b469d6ef2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0c4964b2c74b33113f4f9253f8fdbd6f9effb7070fabfe7998ec7f9f71a68c`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 11.2 MB (11231990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a84d3037e0ebe02d7b2e60abbfa3c50ab185daf05e3e55e3f8ff6cf96a45b2`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784313ea4757f773fd668b9d92e36d3061207f4d5f2fc7c75d857979e14d6f21`  
		Last Modified: Tue, 23 Jul 2024 18:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f51ef3b42547d51fc5c3da2f3e174e60effa7629f2f7e46098c454225497cd1`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 93.1 KB (93109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:757c7bd29e99f08e021102ec7bab71368c08fc5b8dedd1b342098d8ce5324fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3938569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd73107a0a9709640c47c4e4f59fa6ca1ebabf8a0658aa9381cbf4bde03a849`

```dockerfile
```

-	Layers:
	-	`sha256:862421904df231d53bf60f81099184d7c0682e30c697de8f23794783ed2daf08`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 3.9 MB (3924492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d478e353d009dfe08925d196921f6845eb6fe158e70304bc9b9b2fb952370c9`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 14.1 KB (14077 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:1184adc545dd3b80508bd0adcd117196187c4825b29ff153899089f4501c8684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71e38664e416dbd750fcbef2b2c721aca187d947d630ebc182b261ae0f21b3e8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
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
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e04896951f4797da44433346ff837b12526b15ede28ac1391f6f529b8a5bb46`  
		Last Modified: Tue, 23 Jul 2024 06:16:19 GMT  
		Size: 11.7 MB (11688963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b939e2e66405723c6e381754628c666f4480cd54ce632d36b4f31128c4bf6cb9`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee6af13f2ad58d368e1f54c9833e5d7b1093fb8e67d2d693018268220dee32e`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a61af3afc6a59b3caf11dff00dba8ac19254f62101f1ffa96f3e06b7bbf3d`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 92.9 KB (92903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:32dcd4adceddf5965142735cf711565c4d71d2fd65c46f638f6c2c88d2c5cdeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6868034e60a48e100990f215ad44d0f7f612693e50d7973457c7d63a8f1103dc`

```dockerfile
```

-	Layers:
	-	`sha256:6e83eb80c81718b0e2802438a860455d9406d77c8fba4eb3a087230ca32834f1`  
		Last Modified: Tue, 23 Jul 2024 06:16:19 GMT  
		Size: 3.9 MB (3922156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:576ab878aa57f1bc0e41b7c88c53498ab35e8d1d7807748675a2d1541b7a17ba`  
		Last Modified: Tue, 23 Jul 2024 06:16:18 GMT  
		Size: 13.8 KB (13755 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:9934738130c0d0eac989ad9387f991401146190767c418b84da3c5b4473606e5
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
$ docker pull neurodebian@sha256:fabd233511b29371372f9c089fd4b683864f679d1d252216ef8eea4864ca2c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe07a5b4c9c1ea95f2170b1a0087e99a61040d0d41574896c04818aa8b9015e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3ec0f21348ab8b97e349a1a230224eab2abaa91a9bc15ec1756ec679881613`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 11.3 MB (11266567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b6525920c59417749f5f5ed2a2b63bf70e4372d1ad1e43940269f4e46a6a39`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d510146f760f735becbde5f61ec22ff8776568601bab5334c20503e95b76a154`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b114ecc986793dc815210203aae62abfa08219b0f843467dbc1eeec64b622d3`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 92.8 KB (92781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5408265a03e3fc2f5df205622d83f4dccb742f73006527dd9e1a4ffb01eac9c`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:580991d536d1bc4083e536e117f083c498d841a0f9d1f6cd22c6f20ce261626d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9974c18c88586a5a7e0be07f0b836711a742452a233bb0f02ed0035a72456b`

```dockerfile
```

-	Layers:
	-	`sha256:37efcafc97e143a00d67dfcc8a8cce6afb3fd0ee1a47ad53c1283a640f457d55`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 3.9 MB (3924279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a29a33d0193d9594976606f3cbea45d1c7997a112205fda7d13587bf33e8faa5`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8ad50c552d2d9ba9971607e3e25fcff5e656fe578bc84e4ebd7fb18738512adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b4c5c48066c6bab18c83db1004c63f2276ce263810a3b47cd0e67ca0e5d0be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0c4964b2c74b33113f4f9253f8fdbd6f9effb7070fabfe7998ec7f9f71a68c`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 11.2 MB (11231990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a84d3037e0ebe02d7b2e60abbfa3c50ab185daf05e3e55e3f8ff6cf96a45b2`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784313ea4757f773fd668b9d92e36d3061207f4d5f2fc7c75d857979e14d6f21`  
		Last Modified: Tue, 23 Jul 2024 18:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f51ef3b42547d51fc5c3da2f3e174e60effa7629f2f7e46098c454225497cd1`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 93.1 KB (93109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a89e8d1db6d68a3f2363d7ce074b5496e4fa63f099ca409686e3f84f30ebda5`  
		Last Modified: Tue, 23 Jul 2024 18:36:05 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2d20471e880f9bbd6c72aae7179ae7d0d26c0ea16bbfc67999f481fe78ad46d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08416b7a7fa5ef781f905251ee5d1a660baae6bfaf1e10c86a265115cf1660ef`

```dockerfile
```

-	Layers:
	-	`sha256:01968acc1d8a7282a89c4b803ed512cd39f8497d1768e0cf330e008a56dfdad1`  
		Last Modified: Tue, 23 Jul 2024 18:36:06 GMT  
		Size: 3.9 MB (3924532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c13697cc7290159bcf6b045e62a67f922b62336ce65509f7615633065b67364b`  
		Last Modified: Tue, 23 Jul 2024 18:36:05 GMT  
		Size: 16.1 KB (16113 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ca14280056db89cfb3698b0f5ed6f7f98c228f7b413c045d84ba87127e8c13e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50812a4495199c3e047fae3ed8ad96942ce0584681f827fed5d49c763caa0d6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
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
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c2009cb5fa8b7669e4a2ddc7fe615fd9380d7fa24095ac161b734c176809b`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 11.7 MB (11689019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581009e1a3eab679cc96f1a56f84957915a31999300ee01d3b0eb71c1a4c9bc`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fe1928d3b2e8e4b5cd4c4b503be928244764ffb7b11b74acb72b734dd9f208`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfed7927d4c9944bfa51451f9fd78ccf4f2fec34f40ef194178d40a8c4bae9c`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 92.9 KB (92902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3ea134dabf34c21bb382a7c8d3557c91f40f18a3d35d74d32798fe37081a31`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:585b7f303597ee97acc8e1fd4412bdee58c4ae5d0eb0e80b2a2df82125aa3cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d25650556ecf8f5da6c003c46848f43f3fc156dd14b89a1d52b24f3e9e829db`

```dockerfile
```

-	Layers:
	-	`sha256:788b93f4232871e16b9893be5e8b6cde56c93769029ffa2a5cd71dee99730b96`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 3.9 MB (3922196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f697f0775bb09d617db679f5fa2ad36451d8af809edc427f8cfc7a07c8b1e80c`  
		Last Modified: Tue, 23 Jul 2024 06:16:19 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:111066afff1cf55b71fc11820e1bf70e832c06db19b663e65946879d1a20c4ae
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
$ docker pull neurodebian@sha256:c4b81779c10398e7fe06a035dca38cd224ac16e3645a01acd85db78649dbb786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59137257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3678be57aa9d30360d8695e003711a4c831053fc502f54e607ba8149a51abf11`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
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
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca506ff4506aafde8da4f21eb9a2f615611948d193d55f477560e72e88a04a4`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 6.2 MB (6223958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a501c5b0743ce37ee8f6bd0c5a7f3bbd2851b958fbac6133c82cfa57902b10`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a00bf503c4fa80a04227f2ed1c6dffcb56daf70572e1e4743abf42476c4d44`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544162e28a198dad4dfc9abc136e6b1c32aa8b6c688bb942bbdce3c8e6359ed6`  
		Last Modified: Tue, 23 Jul 2024 07:14:56 GMT  
		Size: 90.1 KB (90104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0974df9b32ace9cd20072bb6d5a8e1e3e761d9fec7e1630c5ffb71acfa8396b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381571328f9c493079d456cecadf9934520da72a9dc06b4e1711040b0447b482`

```dockerfile
```

-	Layers:
	-	`sha256:2dc16c93ac20b71df6dad38c59949baee0a48aa143ef11aa088ae6a7f852a0d5`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 3.6 MB (3560542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2276638b179367c1cd2cf60c2dfef8230023447c2b757f248985a62e839486`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 13.4 KB (13445 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:45bc1b5e04ca256a3094c23858b20fdce1c507bd1b29b0b8e5824c98f79901cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59338780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a457663f11cf1f18f4dfb55e7e6d29e9a7b19cc52067423fca67f1e7b7eb19`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:36c12887052d1b06bbaec01740a2cd1b9dab4bc7827e406c3311158554478418 in / 
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
	-	`sha256:493524e4a43f41421b39cb784ceebfde54145b94187eac6910c35f8178b410da`  
		Last Modified: Tue, 23 Jul 2024 04:23:05 GMT  
		Size: 53.0 MB (53026321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ddcf50fbfd15049ddbcb10dc63259476763e98b097bffa8a32df909bad91f0`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 6.2 MB (6219715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3483aa0e91299a8856a36b0b796da1e56032f6bf6264a46bc561cc2396e5bb6`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a293bdf5fe3adfbdf9fc137d610631e39fb5217f0ae782744d49b0ecb810a71a`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00033a80d29cf074dbb5224456ccd6939491504875f91ecc06de897b8c7e05c2`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 90.8 KB (90756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:376e6b8ebc08c698f9070bccffa5dbaae910eb06f287c399f0a66a1e603bc2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b582f3f8a0b06db108a39a5b9dd097dbe5c2564d4a5be963ff8d41dc10e545`

```dockerfile
```

-	Layers:
	-	`sha256:e1342257e0b7816ef7e7148994cb9dfc3cea41fd489f7e6208d4cc70d1b49c20`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 3.6 MB (3561584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63601a096d77be57ad1fa6b9007d197b4192f066d720aa3377deb800e33ce73a`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:b8766a69e3f032dc2f6b2cbe4d089960517e300fa667303031b1ca347e0530cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60327871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dd7d012d4427fdc78cc3d99925a826d93f30b2af108e1ff2259cc078e4d7a3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
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
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe93559091ca5d3ea9a2404a6a0041392e2d6a77c8c2175fb2fcf6d43b1a5dc7`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 6.6 MB (6554634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e5ddc09f8fa7a074698278a93f275d8f43471e76f728d5565fd5208e6bf60`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e6c08312333a956a5d07c8006e3363f7c3602a92e9e7ae72ef8021a657d03c`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb757c0ceb60c7b92a16ddc5e134af72f24cc17185d5faed73fda17ed6438733`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 90.0 KB (90003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2c1eeb9815e16c9aa307b7a53c9ac453f52d051282d5ef3d74cf0329510c75c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1e7c9987235a5add1af665720bd726dbdb11d83f43866c2688489e7809478a`

```dockerfile
```

-	Layers:
	-	`sha256:77423ed85dee033a7d2148fb492b023f86649bb56b475ff1fc1f5dec2126ae64`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 3.6 MB (3557635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954999e20fe2243cce79ddf1335de6381ab8bd1e102c7b7e5974800aad37ad99`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 13.4 KB (13420 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:43f5c9c760ec3a6d80953769f7257365dcc98f921d3b3c1337ec0020432b17f5
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
$ docker pull neurodebian@sha256:06213ad735cb9a6dec843dd46a756e6b61a15922bf5c448f0afd3a59c6803ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59137682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5959f881ab5a82c005d28359bf56c196d165f5b86c9d6578553f207513293437`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
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
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f76dce71e1cdaf2f5fbbd8321fb590faf24afaaf4a1e757a396ba83dc03427`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 6.2 MB (6223956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ef9a74a7171a057b6e8682fe8283d6c99f2e2795d1231f741add8be82d21f2`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a00bf503c4fa80a04227f2ed1c6dffcb56daf70572e1e4743abf42476c4d44`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d563d6355bc3eaf1edef92c45806cb76accd4674904436e2654218c5eb40a5fe`  
		Last Modified: Tue, 23 Jul 2024 07:14:56 GMT  
		Size: 90.1 KB (90111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee3021a05c47fd41365f8421cc847881c408b070780e17c45432ec1ed6f8249`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d761f467d9a341847f66b8b2f1033031bfb02af2db2c217c0f6cc074253e30c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acd0f860e0b9b1c93d7fe9bae5ffb7c454e2d1ac0dce37eca140e0f3bc1c717`

```dockerfile
```

-	Layers:
	-	`sha256:6e58ebed64a728619313a89cac46d38167884ac8c427705b67f3aa3d6a26aa91`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 3.6 MB (3560578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80a7b1e282aa3abb11bda3c500a34f80575dd2a0db3198ccd4f136261b220252`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ae227e01cf2cf4676e0dad06a85f444edf7110c3308e37dca9ab2a8a0ef9b53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59339204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66aec19c986d35008e382bc76893b6503d2a27ce5bbfda0ec9285be568b9e2f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:36c12887052d1b06bbaec01740a2cd1b9dab4bc7827e406c3311158554478418 in / 
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
	-	`sha256:493524e4a43f41421b39cb784ceebfde54145b94187eac6910c35f8178b410da`  
		Last Modified: Tue, 23 Jul 2024 04:23:05 GMT  
		Size: 53.0 MB (53026321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ddcf50fbfd15049ddbcb10dc63259476763e98b097bffa8a32df909bad91f0`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 6.2 MB (6219715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3483aa0e91299a8856a36b0b796da1e56032f6bf6264a46bc561cc2396e5bb6`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a293bdf5fe3adfbdf9fc137d610631e39fb5217f0ae782744d49b0ecb810a71a`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00033a80d29cf074dbb5224456ccd6939491504875f91ecc06de897b8c7e05c2`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 90.8 KB (90756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba27a9cd424832252c3bc77be2ceaf9ec1bfa8b7d89b6d274efafd9c44229fa`  
		Last Modified: Tue, 23 Jul 2024 18:37:06 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3a7a5d1d9aa5d38f7b816188f0bbb15d7b8afdddeb3c696a0cbd7475cb4fa9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8c10ab083598a842ccbc3dcb4c849e36d85315aec9293da11de467620a3c21`

```dockerfile
```

-	Layers:
	-	`sha256:2f0eb7be74e008400584761b42470fbf19c4facfec49d94fab3b40dd02da6921`  
		Last Modified: Tue, 23 Jul 2024 18:37:06 GMT  
		Size: 3.6 MB (3561620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad58bd9e9493475fe159f6f233256b3f58f8f9bea08a050d53f7ba19cb479e5a`  
		Last Modified: Tue, 23 Jul 2024 18:37:06 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b515e0fe0aa2ee64f2f6717bfc7f14e39916427324c828605ac1c54aa47ecbb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60328513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687dbf3f13e8f713e239fb916d5bf5b193e2ac5a6901c46bc11ee7c7d8d804a0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
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
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e24e2f4d3a2116efacc50f90bbb107706948c81dc9a0d5fe2ddcdd54751244`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 6.6 MB (6554835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9da4a0f05951e430e555d94186fdbe3cbe71c5ddee0192d4561e6819b593ae1`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cbcd981bac49fe2c027662d6e6abd44f42fcf467e76250be3030a7b0661073`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c94e30e865fcd72a4d1fc4ba4efecba64573c63dc4e4783c2b3595e28d6fafa`  
		Last Modified: Tue, 23 Jul 2024 06:16:25 GMT  
		Size: 90.0 KB (90019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacdc2bb43e1590673d770ada6aa1acc80a042cdf346ba2cdafdedde940d7984`  
		Last Modified: Tue, 23 Jul 2024 06:16:25 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:26fd30457b2ed02bedb0ea1dda2b4dcf2241fdeee25266e834fd89e44207228c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ee93264ade3b9c117f66523d30697b1a90cd364bb14f33f78236dc70a7bfd`

```dockerfile
```

-	Layers:
	-	`sha256:0f2c2bde88471d36a43b3754cebf04d9bcc4b9d8a92de54dfcefa4fe969a1fcd`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 3.6 MB (3557671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:050ed7c66b436ec6430ef1671e8ffc4626cddabb29ae26a072df54302fdaaa1b`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:35696f693b6ef96260422b9091c766188a7983d82eb58b1eb04f6bd7b58ce84a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:8436872dff585d3f4fd9ba47de2a0c07d2c9601ea7683cd5d98156073fb3e61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69c59f4bc1665f4125a9108a35f53ff8fd3c0f0db4bea3086ff4c0cb4117d2c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8aadfed4b17ce30257b1e83849176e62dda5f82aa6e95a8478f76eec14d065d`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 5.4 MB (5360246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ad67a268cae8111d8fe8b7df873538bdf930ee3af83bddeae455228cf4b12a`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d727c6072b0d91a97e0e503910ae3a3875e0eb0f330dad37430449c5d538f6f1`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1a1cbd18209d18420e1b340bb0af4bf1810b5523ee10e459833effca52500e`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 105.2 KB (105213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af0c65cce1965a1a6b3c2b2975e967c195bd2eba5a033dfefc365029b377dd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45da22baf7d2b89589eaf2d5f3e761d81c297d1c7034615e130e5031d2b182c1`

```dockerfile
```

-	Layers:
	-	`sha256:b358a4f2b71ae1fc1b775755876a2990c2755cb455ca4551f7204050603fd0fb`  
		Last Modified: Wed, 05 Jun 2024 02:20:29 GMT  
		Size: 2.0 MB (1977956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:543ad7176c91bae6840122d5e6913e1dabd6c77bfd53962ded0190dfc7eaffd4`  
		Last Modified: Wed, 05 Jun 2024 02:20:28 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0f5b1443b574b5ace2b0987cd1977e8210613ba725ed472573cfbe9c5cfe23ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b273064c8a6c81f5cacbef5005cb8661311bf23c477bd55a7c401646da2abe1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cef2030478aeb05027ae08e0f6b777479bcfbf91a27f17361fc0b0e8736b09`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 5.3 MB (5340340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84221cff6256e155e65ee5ee2cf1b79bc4f716f5f843f95d834bc0ab9cef7d97`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cf015f90c17438e9ab1dffee54454fd740a774dbcb9498497fa9f358af8672`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad32ddb7c055110e7c49a0cd0fd2fda98f4276a618d67f805938519e1998cf6`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 105.3 KB (105272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:284dd670c2b0916e7375fa296cc94b380cd5d78ea887f00690b52596df26c8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1991818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c3a8fbbf35052ef29f84d07daf978d8d877ce6f9fcacb449acf1ffd0144aba`

```dockerfile
```

-	Layers:
	-	`sha256:813766013ab606a80d4443383a3397da61d8900db25f42772d29d6cf04b2bce7`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 2.0 MB (1978184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1bf415abcaaa1e6c9340665180fe32490ac956e54c13e38d2b031ff973533bb`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 13.6 KB (13634 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:69eea5eee69951a81433ff44e3a76d25374f43b5ede7e2be7991cafbb9ab8480
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2614cd1459a929df672f30c4de3ff5f4f423b10d0204439ea00b153fb35a4ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ba3c03399056b312baca33d2bef793afd92675c192b7d90af7db16bd0fe08b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddab32168f62b0a56e9d1738ba27dd0e7b6b3b7c2e892a19527bf5495039d950`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 5.4 MB (5360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c5f6a989efa6cf7d58ae9018a40243e81a4b1bdcb7a242de74e77d92f945db`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfefe3835ca69f4b947ebba8fa742346a61ebab4361ca98d383e7ba7489fb004`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdc23cea86c9950d617b60a8e9e162dfa93280986c8e4ea3c9efc6450810bbd`  
		Last Modified: Wed, 05 Jun 2024 02:20:11 GMT  
		Size: 105.2 KB (105229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026d40b80d1375c0c978e08b9ee3768e5635a011dcf98d75ec8a728fea6461cb`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8052d782c0e8c3437bea67acf4b2a22d79a7dffa5297317f4776bdc773d0701a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1993579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b545e88e893b1df4e4133705e4b3af666a09fa688c52562b97322c9c6d4c0099`

```dockerfile
```

-	Layers:
	-	`sha256:fa21014e2151b093cd2b0f181163b6be1985c8371a5cc2d7e52e4613433f80bb`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 2.0 MB (1977992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15b3763a1a7a0714189ffe6046baae58c42e3ed9f083352e41a11ca77cd14e5`  
		Last Modified: Wed, 05 Jun 2024 02:20:10 GMT  
		Size: 15.6 KB (15587 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a765833d6e8524c6babfed520f054ff84a6adea03bbc27c95574cb07aa8fa14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10519d9344ce22cf8b6dffbe4a09a105acf140f518107098b2c66a242582141f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62cef2030478aeb05027ae08e0f6b777479bcfbf91a27f17361fc0b0e8736b09`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 5.3 MB (5340340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84221cff6256e155e65ee5ee2cf1b79bc4f716f5f843f95d834bc0ab9cef7d97`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cf015f90c17438e9ab1dffee54454fd740a774dbcb9498497fa9f358af8672`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad32ddb7c055110e7c49a0cd0fd2fda98f4276a618d67f805938519e1998cf6`  
		Last Modified: Wed, 05 Jun 2024 16:35:45 GMT  
		Size: 105.3 KB (105272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5151156e9cc1c424bbecfc412c4effcbd14bdcecf53693bab61b678ae9ed5fd9`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d450bd9f532b807f700d228fe37fceb706c7960f3b87d06090658a57978a3d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1994083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30e25fe54f10b92c153df2cdadaa8eb3efa03f0dee4e099174db24e3ac65946`

```dockerfile
```

-	Layers:
	-	`sha256:ed1c978d1833cda54dd5250213c0833f524702bb98f9f00a81505d89c5d1b173`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 2.0 MB (1978220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b63cad0b9de5d2bb91de6e7fb6616926fabbf2094cb6ffb471176092d3df97e`  
		Last Modified: Wed, 05 Jun 2024 16:36:03 GMT  
		Size: 15.9 KB (15863 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:ec0ea51809c4a7caf3e84ace97c51774a2c4a8a756870b79c371406dbd1b71ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:50332ada0faa254b85fa3c99a2fb1022451d84260772392e0e6ae137e1769632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33268848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324940094fa472191de171a4ba863183350cf4d1a1e43ccc421a71b66e094cf8`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d862268cca33b20dc33b79c6e362573fb742dcd42a2c8a20009493450369ddc5`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 3.6 MB (3622702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7004f9084ccb849430b7c98f8ef2eb567e8caa461377671d0ac1aba06db6d2`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f70324bbe5ab5ca9fd0e2cf5ea3b95c81703e6cd98a5b415809ceb4638987c`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ced8e730e6d5dd8769cd1bdbbdeb4d189659f419d807c42534b5d3654f8c48`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 110.1 KB (110097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f4826a37a310d849e4c83b7f084dee6af9a823f43d94d62ac6a708b6ec638e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f326f94e3b16867754bfd251636fdec9ac49e83e1e1cb329c204511c7e7ae1dc`

```dockerfile
```

-	Layers:
	-	`sha256:7246425b0d75d34d4e317919e463322149ad3be8c5ef7e9c58c8dc4712ece091`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 2.0 MB (2015659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ed2ec0795d1e6759f5395fa3f89dc5ecae1e9b4c754824dab0613aa1226807`  
		Last Modified: Tue, 02 Jul 2024 03:19:34 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9bcf1392985d3afd0ecbc668940d0456f696bcdf4730bbe47f0cd4fa295bfaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31066446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d877dec38ef78dcb8000403d7491c4618ddf3d900efc02d7a784d5c1185d7e6c`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dc16b23ee00d53f4adf324698b87c709e486e05c5b634739181bbce1d56c82`  
		Last Modified: Tue, 02 Jul 2024 15:59:21 GMT  
		Size: 3.6 MB (3594186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f31c419c5921eb500e6bb4d1394cbc4cce89c991aa6ea0cb14769a2e4ceff8b`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e4d5b48676456aba5e60bf7d682a9253b4301c3e43347c5f6b707ffe70669e`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d807b10b523db43ea06a66dc581da167eaaa97bc25dc203e08be033b9c646`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 110.2 KB (110240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:14e7e743ccaae8dbbd8443016ed72061835e4425f075357bd75167779976b156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8170de6e72729ed20e70e4dc912f16558b929bdbc526e2c6a9fe606c149a8e1`

```dockerfile
```

-	Layers:
	-	`sha256:6a6fe57d1a82e58c192048c7cb131fdabb2a4364f02324a8fa100b681aa8356a`  
		Last Modified: Tue, 02 Jul 2024 15:59:21 GMT  
		Size: 2.0 MB (2015918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5262a37a6988f6c82d7bcf44109f408b46c5d30de14569ccb3690d44371739`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 13.7 KB (13682 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:97f3c220574924fe964fa06d61fc892692bb1a6b009a039df7d5e66c78d35239
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2623a7c28522a7b25eb3fe44172632fc2b1c20a3ac1433aac85570c3d5a894af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33269150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69650e35f150a56a819ebf3c57f2723e3327461a3975bd8a64633add1bb9b27d`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c600cd6d952702399348890ccb963cad1adb5d6098ffb092caec1a36545b59`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 3.6 MB (3622723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ba852eb2127a816ea9594d23647541e8598c273234f40d074e70f717f2b363`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb0f24912426a9bcca1a5e3ee9b310973b13df995b7565182f492ab021df7e2`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263c87d1b026352611e6b8267a292c541a135e3842177e774f5f9d5b91f64ef5`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 110.1 KB (110118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8772a37561b5fd83f6ab10e0506ed41d8922a4fd314dce23f19451b55a5d37ea`  
		Last Modified: Tue, 02 Jul 2024 03:19:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5dd1b06de41553a1c77638c8b54f222974b849d784be607edd211468735b0c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612275f45e18d0d569032ec2fc8952576023e24a60c792c2616ffa5aad12d4f1`

```dockerfile
```

-	Layers:
	-	`sha256:3447301f1f169b1f3acdd1f023f78fe04e8dd87a9de8dc89f3ef9b82fc18a35a`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 2.0 MB (2015695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7244937c2399932fdc4026b34ea0785d361e1562807e9a3c5a205419dd4a72a`  
		Last Modified: Tue, 02 Jul 2024 03:19:21 GMT  
		Size: 15.6 KB (15635 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1933b2f19205647fc57be0a0ce1f60390d0ca130346609824d899c010635ee7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31066708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d41beebcdb80261bc322b441a2586ca83ceb3ebba450083e4795434e7bc28c5`
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
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
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
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dc16b23ee00d53f4adf324698b87c709e486e05c5b634739181bbce1d56c82`  
		Last Modified: Tue, 02 Jul 2024 15:59:21 GMT  
		Size: 3.6 MB (3594186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f31c419c5921eb500e6bb4d1394cbc4cce89c991aa6ea0cb14769a2e4ceff8b`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e4d5b48676456aba5e60bf7d682a9253b4301c3e43347c5f6b707ffe70669e`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d807b10b523db43ea06a66dc581da167eaaa97bc25dc203e08be033b9c646`  
		Last Modified: Tue, 02 Jul 2024 15:59:20 GMT  
		Size: 110.2 KB (110240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ad070ba592bf4d760b4956a98ae70ec4651c7f5db0f4e2aabf5ac2bfe3b2c1`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:13f5ac4a8e9c0cef26a3377cc0f187b30ff2d40b24c8960944ec77b804232628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2acc579da0541db5b1806051198453ff0806569e736508bcf7c0c8876c064c5`

```dockerfile
```

-	Layers:
	-	`sha256:4fea70f73d3b08b467c57896ed29255771bb9295dba7ed13d1e55b6054cfb260`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 2.0 MB (2015954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b174930aea8ca924db6c39b0b1980d1d11b0b31e5eb7814b33f219112f583424`  
		Last Modified: Tue, 02 Jul 2024 15:59:38 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:259b321a353852a396595fe3dccae3af14e80acea23b5fa253ccef9abe8d607f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:bc97960df24336fb9ab6ddba39cef28ad5b5981ee2a71c536fc3ecaa3c99c191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33362900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cd2f3d101d99b8267c310b3a0379c5bac16f919035486b3add1b7b5ed6ffe5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
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
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045c8cfbb245c130721a6cce4ebaedd89b348c2f379bf11bbfeb3454b2c2c334`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 3.6 MB (3556375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d2d8a2f97d35ad8bfefe9e419c256552b427d8b6fd56f66298e27c6cab496c`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b2c472b41de28eb92dabae81984e17e4a3b31534b465f808ff43b6fb7a46a2`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75198d942de23473eb6ea13cc2747a0e564e3f96fdc80ae20291fa9f47bb56b3`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 99.4 KB (99380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:99d8189e975305f1f07e17ecd824dbe2680c00952af5ed50226095ed6c8491e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1960446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9a27a6f5a2270e273af05a7f37c7dafca9bb07e0f08356da7c2b5740bf397e`

```dockerfile
```

-	Layers:
	-	`sha256:05ec958be125c66bf2f39d91bcb27965f188147d7402585e574602d6da467f81`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 1.9 MB (1947044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f13b86b37031b1394e9d8e7c0089f611cfc72d136367e630b15a1dce9e470bbf`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 13.4 KB (13402 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c28c5692fdd8cb6094cf16f901ff1bb8eee7e085a2ef7da969264001f4810927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32502115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6375e1dd2dfd99a6f8b88dc59bb53c6a03f5d7ea6d2dcd700b7f3c7d8246f52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107d59261961bebfec87d95f4e1e558ce8e42798b8d28a75edc34fef7bf4b89c`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 3.6 MB (3556246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26154957829f9bf3bb985a70068979a5c42aa97b39becd3512c54b7685a00f`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ab8b90a3fe15e463e6f48c57d92b4fcf48bc4fc24903cd114dd8401e1ba8e8`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2435f75ec9c31dcdc86d4ec5a5f303baf23cf77f8a231e7aae021ee70f35b47e`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 100.8 KB (100832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:71d5864e86f67f564aa0c3126aec7283f2e0f89a9e8ad42d6e31aa2ec7013e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1961771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b0f43f02531953bdb18ca8f475463223d5348b8f4e1feecd67d99f4e3bf3bf`

```dockerfile
```

-	Layers:
	-	`sha256:94eb2bd81873a92dec3252b19c382a0b2497df4ccf57fb01faecc941faed637d`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 1.9 MB (1948089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c43622364623d3bcb476f96cf74141e8cbaf957e54c79e57170d0097080807`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 13.7 KB (13682 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:b96be1088de53c9575d486ca8036410fca479c7e89c00858a8f591ce4fe833aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3e8781cda6623406f20d46b9691666b81659a4bb104f1933ae9486ac8f5ec208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33363306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090fe7ce2dee91c02bb8858a9424b7e8a64e040c1558a8c999386a1d694dce5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
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
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f5a806a7d10c69acfbf90844245f143b3482e6466c123a5c09da2efb8188a7`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 3.6 MB (3556384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60236668873eca6257c1fcfd556cab099eca2191d92cb29decd2e6ae3d9766ce`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1581a86dedda365c08b9c6cfd5bc95959519c98e884e1b639d663882c0146870`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b46e6f530a9a30413e06fa98a60210aaf8e3444d36977e30bcb74336afe08c7`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 99.4 KB (99378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2be2c0f2bb018655be9a1d817db1ab59cb62c114bc229a444090561cae35e6`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e8eb2d7d6c97d6b4322fb5ff411dbf16c74e1963e2e9460a14c46ef017fe2c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1962713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df8cccdcbb2218070b64b3b614767783aefb18cecf75a1baa7f1aaa113e3496`

```dockerfile
```

-	Layers:
	-	`sha256:1768075ff854355336a6a1efdf0e8f55279c7cbfe8476643fc4c349416b6b3ee`  
		Last Modified: Fri, 21 Jun 2024 22:54:25 GMT  
		Size: 1.9 MB (1947080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229f1583b6e8effb98ce4b38e5aa71246f3f7849c8a8438e75fe964b1e93ad6d`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7f00f5a48b9b4249d216d59daf7211df3b18af80811ae01887340122eefa8e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32502520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c71a47d0235e4dc26f3c57266e0e1d4b92587c896fd20699c4040556bae931`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107d59261961bebfec87d95f4e1e558ce8e42798b8d28a75edc34fef7bf4b89c`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 3.6 MB (3556246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26154957829f9bf3bb985a70068979a5c42aa97b39becd3512c54b7685a00f`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ab8b90a3fe15e463e6f48c57d92b4fcf48bc4fc24903cd114dd8401e1ba8e8`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2435f75ec9c31dcdc86d4ec5a5f303baf23cf77f8a231e7aae021ee70f35b47e`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 100.8 KB (100832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14adb417e445e782b6c6f4c031353ab60033f483e74163ccdfb6602d3234a0e`  
		Last Modified: Fri, 21 Jun 2024 22:54:45 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:abd941f9bb109976ae0f41cd5e1cce7c1c58d4cdf895851cbcba66a992e1df0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1964038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb75f98268d56b8ee8c7348c7cac0ff27ed25feb5634301eb1500990213c1b`

```dockerfile
```

-	Layers:
	-	`sha256:dc5a9652ff1195ae6074a02db46430f39cd20c384a53e978e8fee9fb923d411a`  
		Last Modified: Fri, 21 Jun 2024 22:54:45 GMT  
		Size: 1.9 MB (1948125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a8b3e52ef57e9ec95b816881052676acf6b01d9657ea900f954cf1c28c8a5a9`  
		Last Modified: Fri, 21 Jun 2024 22:54:45 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:259b321a353852a396595fe3dccae3af14e80acea23b5fa253ccef9abe8d607f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:bc97960df24336fb9ab6ddba39cef28ad5b5981ee2a71c536fc3ecaa3c99c191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33362900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5cd2f3d101d99b8267c310b3a0379c5bac16f919035486b3add1b7b5ed6ffe5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
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
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045c8cfbb245c130721a6cce4ebaedd89b348c2f379bf11bbfeb3454b2c2c334`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 3.6 MB (3556375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d2d8a2f97d35ad8bfefe9e419c256552b427d8b6fd56f66298e27c6cab496c`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b2c472b41de28eb92dabae81984e17e4a3b31534b465f808ff43b6fb7a46a2`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75198d942de23473eb6ea13cc2747a0e564e3f96fdc80ae20291fa9f47bb56b3`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 99.4 KB (99380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:99d8189e975305f1f07e17ecd824dbe2680c00952af5ed50226095ed6c8491e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1960446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b9a27a6f5a2270e273af05a7f37c7dafca9bb07e0f08356da7c2b5740bf397e`

```dockerfile
```

-	Layers:
	-	`sha256:05ec958be125c66bf2f39d91bcb27965f188147d7402585e574602d6da467f81`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 1.9 MB (1947044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f13b86b37031b1394e9d8e7c0089f611cfc72d136367e630b15a1dce9e470bbf`  
		Last Modified: Fri, 21 Jun 2024 22:54:21 GMT  
		Size: 13.4 KB (13402 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c28c5692fdd8cb6094cf16f901ff1bb8eee7e085a2ef7da969264001f4810927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32502115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6375e1dd2dfd99a6f8b88dc59bb53c6a03f5d7ea6d2dcd700b7f3c7d8246f52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107d59261961bebfec87d95f4e1e558ce8e42798b8d28a75edc34fef7bf4b89c`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 3.6 MB (3556246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26154957829f9bf3bb985a70068979a5c42aa97b39becd3512c54b7685a00f`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ab8b90a3fe15e463e6f48c57d92b4fcf48bc4fc24903cd114dd8401e1ba8e8`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2435f75ec9c31dcdc86d4ec5a5f303baf23cf77f8a231e7aae021ee70f35b47e`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 100.8 KB (100832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:71d5864e86f67f564aa0c3126aec7283f2e0f89a9e8ad42d6e31aa2ec7013e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1961771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b0f43f02531953bdb18ca8f475463223d5348b8f4e1feecd67d99f4e3bf3bf`

```dockerfile
```

-	Layers:
	-	`sha256:94eb2bd81873a92dec3252b19c382a0b2497df4ccf57fb01faecc941faed637d`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 1.9 MB (1948089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c43622364623d3bcb476f96cf74141e8cbaf957e54c79e57170d0097080807`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 13.7 KB (13682 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:b96be1088de53c9575d486ca8036410fca479c7e89c00858a8f591ce4fe833aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3e8781cda6623406f20d46b9691666b81659a4bb104f1933ae9486ac8f5ec208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33363306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090fe7ce2dee91c02bb8858a9424b7e8a64e040c1558a8c999386a1d694dce5d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
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
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f5a806a7d10c69acfbf90844245f143b3482e6466c123a5c09da2efb8188a7`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 3.6 MB (3556384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60236668873eca6257c1fcfd556cab099eca2191d92cb29decd2e6ae3d9766ce`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1581a86dedda365c08b9c6cfd5bc95959519c98e884e1b639d663882c0146870`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b46e6f530a9a30413e06fa98a60210aaf8e3444d36977e30bcb74336afe08c7`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 99.4 KB (99378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2be2c0f2bb018655be9a1d817db1ab59cb62c114bc229a444090561cae35e6`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e8eb2d7d6c97d6b4322fb5ff411dbf16c74e1963e2e9460a14c46ef017fe2c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1962713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df8cccdcbb2218070b64b3b614767783aefb18cecf75a1baa7f1aaa113e3496`

```dockerfile
```

-	Layers:
	-	`sha256:1768075ff854355336a6a1efdf0e8f55279c7cbfe8476643fc4c349416b6b3ee`  
		Last Modified: Fri, 21 Jun 2024 22:54:25 GMT  
		Size: 1.9 MB (1947080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229f1583b6e8effb98ce4b38e5aa71246f3f7849c8a8438e75fe964b1e93ad6d`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 15.6 KB (15633 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7f00f5a48b9b4249d216d59daf7211df3b18af80811ae01887340122eefa8e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32502520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c71a47d0235e4dc26f3c57266e0e1d4b92587c896fd20699c4040556bae931`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107d59261961bebfec87d95f4e1e558ce8e42798b8d28a75edc34fef7bf4b89c`  
		Last Modified: Fri, 21 Jun 2024 22:54:24 GMT  
		Size: 3.6 MB (3556246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26154957829f9bf3bb985a70068979a5c42aa97b39becd3512c54b7685a00f`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ab8b90a3fe15e463e6f48c57d92b4fcf48bc4fc24903cd114dd8401e1ba8e8`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2435f75ec9c31dcdc86d4ec5a5f303baf23cf77f8a231e7aae021ee70f35b47e`  
		Last Modified: Fri, 21 Jun 2024 22:54:23 GMT  
		Size: 100.8 KB (100832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14adb417e445e782b6c6f4c031353ab60033f483e74163ccdfb6602d3234a0e`  
		Last Modified: Fri, 21 Jun 2024 22:54:45 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:abd941f9bb109976ae0f41cd5e1cce7c1c58d4cdf895851cbcba66a992e1df0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1964038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eb75f98268d56b8ee8c7348c7cac0ff27ed25feb5634301eb1500990213c1b`

```dockerfile
```

-	Layers:
	-	`sha256:dc5a9652ff1195ae6074a02db46430f39cd20c384a53e978e8fee9fb923d411a`  
		Last Modified: Fri, 21 Jun 2024 22:54:45 GMT  
		Size: 1.9 MB (1948125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a8b3e52ef57e9ec95b816881052676acf6b01d9657ea900f954cf1c28c8a5a9`  
		Last Modified: Fri, 21 Jun 2024 22:54:45 GMT  
		Size: 15.9 KB (15913 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:9934738130c0d0eac989ad9387f991401146190767c418b84da3c5b4473606e5
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
$ docker pull neurodebian@sha256:fabd233511b29371372f9c089fd4b683864f679d1d252216ef8eea4864ca2c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe07a5b4c9c1ea95f2170b1a0087e99a61040d0d41574896c04818aa8b9015e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
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
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3ec0f21348ab8b97e349a1a230224eab2abaa91a9bc15ec1756ec679881613`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 11.3 MB (11266567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b6525920c59417749f5f5ed2a2b63bf70e4372d1ad1e43940269f4e46a6a39`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d510146f760f735becbde5f61ec22ff8776568601bab5334c20503e95b76a154`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b114ecc986793dc815210203aae62abfa08219b0f843467dbc1eeec64b622d3`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 92.8 KB (92781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5408265a03e3fc2f5df205622d83f4dccb742f73006527dd9e1a4ffb01eac9c`  
		Last Modified: Tue, 23 Jul 2024 07:14:41 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:580991d536d1bc4083e536e117f083c498d841a0f9d1f6cd22c6f20ce261626d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9974c18c88586a5a7e0be07f0b836711a742452a233bb0f02ed0035a72456b`

```dockerfile
```

-	Layers:
	-	`sha256:37efcafc97e143a00d67dfcc8a8cce6afb3fd0ee1a47ad53c1283a640f457d55`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 3.9 MB (3924279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a29a33d0193d9594976606f3cbea45d1c7997a112205fda7d13587bf33e8faa5`  
		Last Modified: Tue, 23 Jul 2024 07:14:40 GMT  
		Size: 15.8 KB (15822 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8ad50c552d2d9ba9971607e3e25fcff5e656fe578bc84e4ebd7fb18738512adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b4c5c48066c6bab18c83db1004c63f2276ce263810a3b47cd0e67ca0e5d0be`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
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
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0c4964b2c74b33113f4f9253f8fdbd6f9effb7070fabfe7998ec7f9f71a68c`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 11.2 MB (11231990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a84d3037e0ebe02d7b2e60abbfa3c50ab185daf05e3e55e3f8ff6cf96a45b2`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784313ea4757f773fd668b9d92e36d3061207f4d5f2fc7c75d857979e14d6f21`  
		Last Modified: Tue, 23 Jul 2024 18:35:45 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f51ef3b42547d51fc5c3da2f3e174e60effa7629f2f7e46098c454225497cd1`  
		Last Modified: Tue, 23 Jul 2024 18:35:46 GMT  
		Size: 93.1 KB (93109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a89e8d1db6d68a3f2363d7ce074b5496e4fa63f099ca409686e3f84f30ebda5`  
		Last Modified: Tue, 23 Jul 2024 18:36:05 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2d20471e880f9bbd6c72aae7179ae7d0d26c0ea16bbfc67999f481fe78ad46d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3940645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08416b7a7fa5ef781f905251ee5d1a660baae6bfaf1e10c86a265115cf1660ef`

```dockerfile
```

-	Layers:
	-	`sha256:01968acc1d8a7282a89c4b803ed512cd39f8497d1768e0cf330e008a56dfdad1`  
		Last Modified: Tue, 23 Jul 2024 18:36:06 GMT  
		Size: 3.9 MB (3924532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c13697cc7290159bcf6b045e62a67f922b62336ce65509f7615633065b67364b`  
		Last Modified: Tue, 23 Jul 2024 18:36:05 GMT  
		Size: 16.1 KB (16113 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ca14280056db89cfb3698b0f5ed6f7f98c228f7b413c045d84ba87127e8c13e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62363754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50812a4495199c3e047fae3ed8ad96942ce0584681f827fed5d49c763caa0d6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
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
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33c2009cb5fa8b7669e4a2ddc7fe615fd9380d7fa24095ac161b734c176809b`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 11.7 MB (11689019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e581009e1a3eab679cc96f1a56f84957915a31999300ee01d3b0eb71c1a4c9bc`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fe1928d3b2e8e4b5cd4c4b503be928244764ffb7b11b74acb72b734dd9f208`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfed7927d4c9944bfa51451f9fd78ccf4f2fec34f40ef194178d40a8c4bae9c`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 92.9 KB (92902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3ea134dabf34c21bb382a7c8d3557c91f40f18a3d35d74d32798fe37081a31`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:585b7f303597ee97acc8e1fd4412bdee58c4ae5d0eb0e80b2a2df82125aa3cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3937986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d25650556ecf8f5da6c003c46848f43f3fc156dd14b89a1d52b24f3e9e829db`

```dockerfile
```

-	Layers:
	-	`sha256:788b93f4232871e16b9893be5e8b6cde56c93769029ffa2a5cd71dee99730b96`  
		Last Modified: Tue, 23 Jul 2024 06:16:20 GMT  
		Size: 3.9 MB (3922196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f697f0775bb09d617db679f5fa2ad36451d8af809edc427f8cfc7a07c8b1e80c`  
		Last Modified: Tue, 23 Jul 2024 06:16:19 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:ee6e57e8f69661aa0376f17ea69c259624a498970172f61a4db5ebcd9c29fdaf
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
$ docker pull neurodebian@sha256:8df25b7381b56e0c058ce85c9a33f671c6e1daf7f46efbcf14fd5528b3202b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59098051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246cb0db993b407cffde6493e242d3de06ae128cf87b2267b22a47439c4af6ed`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:119c9b007e2126bffd87612039b5305513fe8cedcb052cb679094aa5c0182fe8 in / 
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
	-	`sha256:66b1db94c2eed297b9f748a1ebf50a98574aafe88f8cfc08d94ad3f35d83c48a`  
		Last Modified: Tue, 23 Jul 2024 05:29:19 GMT  
		Size: 52.8 MB (52781957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebedff2812269508116bdc4cfef008441e28a0371783e5d7858c4781c1feb07d`  
		Last Modified: Tue, 23 Jul 2024 06:16:50 GMT  
		Size: 6.2 MB (6224015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7a97239599a4e60b31be674f713a6b1e22c175b2c02845b61568d1db2fca0e`  
		Last Modified: Tue, 23 Jul 2024 06:16:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a545f13c4b3248136207595b0479eabda06be2625497db2580a1d192d0fb472`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5226c81f305bd3e0c716692aecb129ea31b38f0a17252ed8ce8074fdb8890d3`  
		Last Modified: Tue, 23 Jul 2024 06:16:49 GMT  
		Size: 90.1 KB (90093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:44d15eaf8b16820042eb3da978d2cdae7052cb71a741d96ffe135242c6671f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc7595d4909f057493250e003bc9e2c5f3afa421c262c0372e83e6592bd1755`

```dockerfile
```

-	Layers:
	-	`sha256:2660976885a91f1b983c76bf298e1b3850a460a9a8529833488f454f140d5528`  
		Last Modified: Tue, 23 Jul 2024 06:16:50 GMT  
		Size: 3.6 MB (3560484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:542975e582d79cf3bd0666b614e52805ade397c7a5c3985cc1d0f1b0e27c7f6e`  
		Last Modified: Tue, 23 Jul 2024 06:16:49 GMT  
		Size: 13.4 KB (13395 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8c95c9493701e6ce942dc6bd4246781a631d9b5197e631b6ae293949023ccd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59372464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695e6cfe4adc6f346d5c84bbf1bc7154bcd6669f2a0d083c38ea98d34cdd67`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:368e6d1d2999bc62054217cfec29bdcf59fe672d1d5db07c2f2c2939222c4a42 in / 
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
	-	`sha256:88161cad314c45536b001a7558a18c0a54c991650605a6212e9720f7ac3bbc4a`  
		Last Modified: Tue, 23 Jul 2024 04:21:45 GMT  
		Size: 53.1 MB (53060158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c5e22eab6bfb0637511700afc2f7acd0c3fce57b42bad64a4534c5c34f2b23`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 6.2 MB (6219604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88300873cb59f94a9b5b736e89bc5fdec8a6c027a5aa343e28fe5596a82a1177`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9261c28300bccbc9dc3a8f5e25c8ec61266871386ae0bf74f7f95402d20b353a`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a368fbf666afd365681e06a696c68bc93362d632f6326c8caead3c876de84885`  
		Last Modified: Tue, 23 Jul 2024 18:37:43 GMT  
		Size: 90.7 KB (90721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:af51a66c271250ae8a200c0aacf5743141c34b74875ed711b01d39de1fd3d171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d942133d8a2c4c5122c1362446eb9237ac2b26dcd3dbc033c75e5120c0ff5049`

```dockerfile
```

-	Layers:
	-	`sha256:dad4a51b19f92441f221131eabd713c323dd07f9199d2cc5407851b23d413a20`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 3.6 MB (3561526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2161ab33b33d74b6035e8bc891ad6b32b14e53933ea34e9b1c0c298e9b95d0fb`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 13.7 KB (13670 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:3b372a54e1ce429917523e9c2859fb6720877ec0f30be7ed8ce8d07abe5109fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60347544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f950c70258e58d2a04cbaa96072681433773c05ea1973cfa4e9bdd4d5c609e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:934dcd467a296b55e9373c03c1e502c3a9f186f9c1e08b54e88bb5c0bf30fd70 in / 
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
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82bec79dff3a3ed87ff22e886c5aafea0a550f124ca9f5991042ef6cc4c99aa`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 6.6 MB (6554808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd40d97447dd271777a17658fddd6e0adb18cb96c4c55d60d7b164ef5cf4fb8`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ed2f5ee74e882fbfb7a7ab0794df8358d83de25f763a8e085fc0ecabe76d2f`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f41dfdfe44562c08bf96630bed334529c1ebf002d479fc1d5930fb70cfe0859`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 90.0 KB (90008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb83ef00b339426a4d143411d85fa66511dcdc042a56a33803050d28f153a258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2b7a38b2f8a331c5bc8798fc52439dfc30869aa43d893ab5362e307440aad2`

```dockerfile
```

-	Layers:
	-	`sha256:f3e38412e47a224b162530825ddb5c0174967d282cb6b3bf7598e1ae9e09b248`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 3.6 MB (3557577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74437b60de29329d791d3af9660d31ba10f449b2fbb525da0626d417e2e6ccfd`  
		Last Modified: Tue, 23 Jul 2024 06:16:57 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:26583651880b747302b934d5a887f572a8b61dce1871f7eedbfe85a7f57e9dfc
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
$ docker pull neurodebian@sha256:fe00f914907411d2718c1090b33671bd938acc75d18f6e9bd33915ae25007622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59098491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3329beaad1b7df1a274c23c124cf41b240f4974f192876230d1a238a6723945`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:119c9b007e2126bffd87612039b5305513fe8cedcb052cb679094aa5c0182fe8 in / 
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
	-	`sha256:66b1db94c2eed297b9f748a1ebf50a98574aafe88f8cfc08d94ad3f35d83c48a`  
		Last Modified: Tue, 23 Jul 2024 05:29:19 GMT  
		Size: 52.8 MB (52781957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba78cc727fb8c4d6be3b81320c6cad029de3e21545cbd6ff7f5d3e24101f151a`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 6.2 MB (6224024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2d81607b27beb9a44d5a4417a9a035589e70b3b1ec2100391a8b57208c416f`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a545f13c4b3248136207595b0479eabda06be2625497db2580a1d192d0fb472`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca6000aeeffffc4a99aa4b2a506c1c37b60feaba0f4abbb0b0df48d71c168b3`  
		Last Modified: Tue, 23 Jul 2024 06:16:48 GMT  
		Size: 90.1 KB (90134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73252cba8a182a2d4e3711e7b3ca228fe88fc064566e9fca00041e6169eac54`  
		Last Modified: Tue, 23 Jul 2024 06:16:48 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1f17ba763e3de97abf585a033972887d9566a765283b42b13e76d63a07fb6c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab996e76af23a9465feb34e25cf43c601f80837b9cb33fc4c9a699029842601b`

```dockerfile
```

-	Layers:
	-	`sha256:029906b62d9492d3fd7fcc7f30c42d40dbca591a8e4f4625452a132c7bb16237`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 3.6 MB (3560520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ed57b663d769dc87ecba0f0d26f41a9774ef1d870b398bf12f681312a26ccec`  
		Last Modified: Tue, 23 Jul 2024 06:16:47 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bf133873c23d03980c9d3b650b754fd4f358e3e0e352eb32c15ff2f0f71a4c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59372858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b36d5dd60acbe2494379448b88f3860f372c0fb76e1fd36bfb41f506c36333`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:368e6d1d2999bc62054217cfec29bdcf59fe672d1d5db07c2f2c2939222c4a42 in / 
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
	-	`sha256:88161cad314c45536b001a7558a18c0a54c991650605a6212e9720f7ac3bbc4a`  
		Last Modified: Tue, 23 Jul 2024 04:21:45 GMT  
		Size: 53.1 MB (53060158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c5e22eab6bfb0637511700afc2f7acd0c3fce57b42bad64a4534c5c34f2b23`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 6.2 MB (6219604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88300873cb59f94a9b5b736e89bc5fdec8a6c027a5aa343e28fe5596a82a1177`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9261c28300bccbc9dc3a8f5e25c8ec61266871386ae0bf74f7f95402d20b353a`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a368fbf666afd365681e06a696c68bc93362d632f6326c8caead3c876de84885`  
		Last Modified: Tue, 23 Jul 2024 18:37:43 GMT  
		Size: 90.7 KB (90721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02deda8175a76811cbe2e5cd721980efdbc7a9d4ad836f3a0f7d07ac36ce51a2`  
		Last Modified: Tue, 23 Jul 2024 18:38:00 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:16c1f738d55249a635030e91f4ea08ba5bf2b58aac18867449d4056178dae3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e658cbf98e35d798d073a33235d32b9ea30ccd99ff3aa192c0c0e51ce3555df9`

```dockerfile
```

-	Layers:
	-	`sha256:04b19be0c9e27b3babc5ab6687d6d64e862a4b989d3feb1d0d1f1aa812493051`  
		Last Modified: Tue, 23 Jul 2024 18:38:00 GMT  
		Size: 3.6 MB (3561562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f305496ab906cad0f4da0b7b7b5a7c6e3a2f1140d9dbd2afd4fed76ff1a231e`  
		Last Modified: Tue, 23 Jul 2024 18:38:00 GMT  
		Size: 15.7 KB (15703 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:573427ab2013d8649e8c77e0c43bc3c7b5b5f4fcde037e6c85a054575958da8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60347600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087f6bb71890c249e63439d7a260d4d4ff8b25d84f6ff76e84993a8400a9217c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:934dcd467a296b55e9373c03c1e502c3a9f186f9c1e08b54e88bb5c0bf30fd70 in / 
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
	-	`sha256:16078dfedeec5d2bd03b072408fac505eccfab6bd3255afa70ae860262541f79`  
		Last Modified: Tue, 23 Jul 2024 03:59:31 GMT  
		Size: 53.7 MB (53700748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5853df0c476cb6b47074aecdc44c8989de1742ae9f80314550a5b130cbd8cc93`  
		Last Modified: Tue, 23 Jul 2024 06:16:45 GMT  
		Size: 6.6 MB (6554507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ea7f033db96bdba75250d4e1d338c9d502f3041c12b5d849f4b056c52135b1`  
		Last Modified: Tue, 23 Jul 2024 06:16:44 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2c54943a31f955045ec02343ddd94eac368955c1adf7e5c49bf9d15b245dcf`  
		Last Modified: Tue, 23 Jul 2024 06:16:44 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46257428d44167f3bc35b5e28d989e657f3ba1561445dc6279343bfbd3d6e182`  
		Last Modified: Tue, 23 Jul 2024 06:16:45 GMT  
		Size: 90.0 KB (89966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325034bc80906c9ecd3452f092b7378c6ea12b3e022d1839bc4e2580c8ebed12`  
		Last Modified: Tue, 23 Jul 2024 06:16:45 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:04eb5e30a4c547f455df66af4e1bdd2a670958758479b28c99da857edad49e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae053737de19f1e726412e8398493852de05747ad7b20e98595017394c240a00`

```dockerfile
```

-	Layers:
	-	`sha256:1c58c3cfa44d3b57862b1ac055d5022d978d6d2bd6781ffd4800c75fc04921d1`  
		Last Modified: Tue, 23 Jul 2024 06:16:45 GMT  
		Size: 3.6 MB (3557613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c52f4ebd0b2d5e69e3a5681d4454b99743cca8d75a57d5175f3edb59fa3cf83e`  
		Last Modified: Tue, 23 Jul 2024 06:16:44 GMT  
		Size: 15.4 KB (15400 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:111066afff1cf55b71fc11820e1bf70e832c06db19b663e65946879d1a20c4ae
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
$ docker pull neurodebian@sha256:c4b81779c10398e7fe06a035dca38cd224ac16e3645a01acd85db78649dbb786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59137257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3678be57aa9d30360d8695e003711a4c831053fc502f54e607ba8149a51abf11`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
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
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca506ff4506aafde8da4f21eb9a2f615611948d193d55f477560e72e88a04a4`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 6.2 MB (6223958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a501c5b0743ce37ee8f6bd0c5a7f3bbd2851b958fbac6133c82cfa57902b10`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a00bf503c4fa80a04227f2ed1c6dffcb56daf70572e1e4743abf42476c4d44`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544162e28a198dad4dfc9abc136e6b1c32aa8b6c688bb942bbdce3c8e6359ed6`  
		Last Modified: Tue, 23 Jul 2024 07:14:56 GMT  
		Size: 90.1 KB (90104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0974df9b32ace9cd20072bb6d5a8e1e3e761d9fec7e1630c5ffb71acfa8396b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381571328f9c493079d456cecadf9934520da72a9dc06b4e1711040b0447b482`

```dockerfile
```

-	Layers:
	-	`sha256:2dc16c93ac20b71df6dad38c59949baee0a48aa143ef11aa088ae6a7f852a0d5`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 3.6 MB (3560542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c2276638b179367c1cd2cf60c2dfef8230023447c2b757f248985a62e839486`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 13.4 KB (13445 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:45bc1b5e04ca256a3094c23858b20fdce1c507bd1b29b0b8e5824c98f79901cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59338780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a457663f11cf1f18f4dfb55e7e6d29e9a7b19cc52067423fca67f1e7b7eb19`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:36c12887052d1b06bbaec01740a2cd1b9dab4bc7827e406c3311158554478418 in / 
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
	-	`sha256:493524e4a43f41421b39cb784ceebfde54145b94187eac6910c35f8178b410da`  
		Last Modified: Tue, 23 Jul 2024 04:23:05 GMT  
		Size: 53.0 MB (53026321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ddcf50fbfd15049ddbcb10dc63259476763e98b097bffa8a32df909bad91f0`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 6.2 MB (6219715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3483aa0e91299a8856a36b0b796da1e56032f6bf6264a46bc561cc2396e5bb6`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a293bdf5fe3adfbdf9fc137d610631e39fb5217f0ae782744d49b0ecb810a71a`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00033a80d29cf074dbb5224456ccd6939491504875f91ecc06de897b8c7e05c2`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 90.8 KB (90756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:376e6b8ebc08c698f9070bccffa5dbaae910eb06f287c399f0a66a1e603bc2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b582f3f8a0b06db108a39a5b9dd097dbe5c2564d4a5be963ff8d41dc10e545`

```dockerfile
```

-	Layers:
	-	`sha256:e1342257e0b7816ef7e7148994cb9dfc3cea41fd489f7e6208d4cc70d1b49c20`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 3.6 MB (3561584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63601a096d77be57ad1fa6b9007d197b4192f066d720aa3377deb800e33ce73a`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 13.7 KB (13723 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:b8766a69e3f032dc2f6b2cbe4d089960517e300fa667303031b1ca347e0530cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60327871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dd7d012d4427fdc78cc3d99925a826d93f30b2af108e1ff2259cc078e4d7a3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
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
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe93559091ca5d3ea9a2404a6a0041392e2d6a77c8c2175fb2fcf6d43b1a5dc7`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 6.6 MB (6554634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620e5ddc09f8fa7a074698278a93f275d8f43471e76f728d5565fd5208e6bf60`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e6c08312333a956a5d07c8006e3363f7c3602a92e9e7ae72ef8021a657d03c`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb757c0ceb60c7b92a16ddc5e134af72f24cc17185d5faed73fda17ed6438733`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 90.0 KB (90003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2c1eeb9815e16c9aa307b7a53c9ac453f52d051282d5ef3d74cf0329510c75c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e1e7c9987235a5add1af665720bd726dbdb11d83f43866c2688489e7809478a`

```dockerfile
```

-	Layers:
	-	`sha256:77423ed85dee033a7d2148fb492b023f86649bb56b475ff1fc1f5dec2126ae64`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 3.6 MB (3557635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954999e20fe2243cce79ddf1335de6381ab8bd1e102c7b7e5974800aad37ad99`  
		Last Modified: Tue, 23 Jul 2024 06:16:35 GMT  
		Size: 13.4 KB (13420 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:43f5c9c760ec3a6d80953769f7257365dcc98f921d3b3c1337ec0020432b17f5
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
$ docker pull neurodebian@sha256:06213ad735cb9a6dec843dd46a756e6b61a15922bf5c448f0afd3a59c6803ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59137682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5959f881ab5a82c005d28359bf56c196d165f5b86c9d6578553f207513293437`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:aeee476035b2ce2f3c795377011e41eae116861792cc7c02090d8c6e0e5b40e9 in / 
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
	-	`sha256:2c622000fb34abccd4a19243f49979fc534d754c97f8e18457162c25dfabe489`  
		Last Modified: Tue, 23 Jul 2024 05:30:46 GMT  
		Size: 52.8 MB (52821206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f76dce71e1cdaf2f5fbbd8321fb590faf24afaaf4a1e757a396ba83dc03427`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 6.2 MB (6223956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ef9a74a7171a057b6e8682fe8283d6c99f2e2795d1231f741add8be82d21f2`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a00bf503c4fa80a04227f2ed1c6dffcb56daf70572e1e4743abf42476c4d44`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d563d6355bc3eaf1edef92c45806cb76accd4674904436e2654218c5eb40a5fe`  
		Last Modified: Tue, 23 Jul 2024 07:14:56 GMT  
		Size: 90.1 KB (90111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee3021a05c47fd41365f8421cc847881c408b070780e17c45432ec1ed6f8249`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 423.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d761f467d9a341847f66b8b2f1033031bfb02af2db2c217c0f6cc074253e30c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acd0f860e0b9b1c93d7fe9bae5ffb7c454e2d1ac0dce37eca140e0f3bc1c717`

```dockerfile
```

-	Layers:
	-	`sha256:6e58ebed64a728619313a89cac46d38167884ac8c427705b67f3aa3d6a26aa91`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 3.6 MB (3560578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80a7b1e282aa3abb11bda3c500a34f80575dd2a0db3198ccd4f136261b220252`  
		Last Modified: Tue, 23 Jul 2024 07:14:55 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ae227e01cf2cf4676e0dad06a85f444edf7110c3308e37dca9ab2a8a0ef9b53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59339204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66aec19c986d35008e382bc76893b6503d2a27ce5bbfda0ec9285be568b9e2f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:36c12887052d1b06bbaec01740a2cd1b9dab4bc7827e406c3311158554478418 in / 
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
	-	`sha256:493524e4a43f41421b39cb784ceebfde54145b94187eac6910c35f8178b410da`  
		Last Modified: Tue, 23 Jul 2024 04:23:05 GMT  
		Size: 53.0 MB (53026321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ddcf50fbfd15049ddbcb10dc63259476763e98b097bffa8a32df909bad91f0`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 6.2 MB (6219715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3483aa0e91299a8856a36b0b796da1e56032f6bf6264a46bc561cc2396e5bb6`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a293bdf5fe3adfbdf9fc137d610631e39fb5217f0ae782744d49b0ecb810a71a`  
		Last Modified: Tue, 23 Jul 2024 18:36:44 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00033a80d29cf074dbb5224456ccd6939491504875f91ecc06de897b8c7e05c2`  
		Last Modified: Tue, 23 Jul 2024 18:36:45 GMT  
		Size: 90.8 KB (90756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba27a9cd424832252c3bc77be2ceaf9ec1bfa8b7d89b6d274efafd9c44229fa`  
		Last Modified: Tue, 23 Jul 2024 18:37:06 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3a7a5d1d9aa5d38f7b816188f0bbb15d7b8afdddeb3c696a0cbd7475cb4fa9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8c10ab083598a842ccbc3dcb4c849e36d85315aec9293da11de467620a3c21`

```dockerfile
```

-	Layers:
	-	`sha256:2f0eb7be74e008400584761b42470fbf19c4facfec49d94fab3b40dd02da6921`  
		Last Modified: Tue, 23 Jul 2024 18:37:06 GMT  
		Size: 3.6 MB (3561620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad58bd9e9493475fe159f6f233256b3f58f8f9bea08a050d53f7ba19cb479e5a`  
		Last Modified: Tue, 23 Jul 2024 18:37:06 GMT  
		Size: 15.8 KB (15755 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b515e0fe0aa2ee64f2f6717bfc7f14e39916427324c828605ac1c54aa47ecbb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60328513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:687dbf3f13e8f713e239fb916d5bf5b193e2ac5a6901c46bc11ee7c7d8d804a0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:01a40f7b1e06135068b561ea73bceefb80384e78cf04f7afc30b29280b89be42 in / 
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
	-	`sha256:603ccf6e4399370cd3c9b421529967f58d124fe253b75b4d92b2e58cf112fdbb`  
		Last Modified: Tue, 23 Jul 2024 04:01:16 GMT  
		Size: 53.7 MB (53681250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e24e2f4d3a2116efacc50f90bbb107706948c81dc9a0d5fe2ddcdd54751244`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 6.6 MB (6554835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9da4a0f05951e430e555d94186fdbe3cbe71c5ddee0192d4561e6819b593ae1`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cbcd981bac49fe2c027662d6e6abd44f42fcf467e76250be3030a7b0661073`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c94e30e865fcd72a4d1fc4ba4efecba64573c63dc4e4783c2b3595e28d6fafa`  
		Last Modified: Tue, 23 Jul 2024 06:16:25 GMT  
		Size: 90.0 KB (90019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacdc2bb43e1590673d770ada6aa1acc80a042cdf346ba2cdafdedde940d7984`  
		Last Modified: Tue, 23 Jul 2024 06:16:25 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:26fd30457b2ed02bedb0ea1dda2b4dcf2241fdeee25266e834fd89e44207228c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d75ee93264ade3b9c117f66523d30697b1a90cd364bb14f33f78236dc70a7bfd`

```dockerfile
```

-	Layers:
	-	`sha256:0f2c2bde88471d36a43b3754cebf04d9bcc4b9d8a92de54dfcefa4fe969a1fcd`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 3.6 MB (3557671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:050ed7c66b436ec6430ef1671e8ffc4626cddabb29ae26a072df54302fdaaa1b`  
		Last Modified: Tue, 23 Jul 2024 06:16:24 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json
