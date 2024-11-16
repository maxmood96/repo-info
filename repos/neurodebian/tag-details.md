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
$ docker pull neurodebian@sha256:aacfdbb5899916ce6aff133d995785d867b2697513f51930626919df8816b52c
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
$ docker pull neurodebian@sha256:dc1103341f4ea2f25e0d9bd456c9a29d1ce3c89fc9fdf03ef9855b40020ce2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60937609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae651fbb06567e9d58779eb005a0d338e9fd6c3e9e2f94f104bc7cf56cf2d8e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f92fba1f2243260f740882b33bd65ce9be7c710ee5ab93f9c7b65c5657cfab`  
		Last Modified: Tue, 12 Nov 2024 02:14:48 GMT  
		Size: 11.3 MB (11266780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0dcde979a959198da9acd3e0363652603c29070808043e0f715abacc4cab3d`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca047e2ff6934fd61ea0fdd2bcfe2eb8c113d771ddf33cd7d69c8e029508bb`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9bc304a1bc3fe8ff0d4ba75eaa7938ce3de3002a43c18a34cbd5f436180128`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 93.1 KB (93143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fd1d034fa70625003727fedc26cc6409115c5ddcef4a034a2b4763cb77ecf1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb574390b66288dc89d92f025f7fbe7bdc29e2f6dfef2aca5cf5b04ed2269f5d`

```dockerfile
```

-	Layers:
	-	`sha256:716b9d855b2d05a308e0a2415f3fc35b67cac1d7d59a739292f73c7c76e4e054`  
		Last Modified: Tue, 12 Nov 2024 02:14:48 GMT  
		Size: 3.9 MB (3938479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b957b5cd62d235b91fff8c8a270d1fb78b3627590548e5fee46f029a6b756fa1`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 14.0 KB (13999 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1f36fdde405355c0bf1aa5e1d801e1ac091b9a13b79b5fdc64c67386e08c0e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971276f59476fb7abd2a062acfe28a943c1358d6e56974be08536e68e600e96f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e374b4f322cd89941e3a79c9bd26d1a5f1c6bc1cbada76ddcd1dc30f5e5cdba3`  
		Last Modified: Tue, 12 Nov 2024 13:32:21 GMT  
		Size: 11.2 MB (11232560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c07a4424e486742d8557f51e2d6ea83c25c81a3fe1083cdc92f2aaabe53972`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76a820ff7756abf0046ae961df3ad5d2f997f1277bdb445d4f9ce1e548f3cc`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89406019c22729ee9e55b00384b15954a2694a0806199b7273eb34553edfd429`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 93.4 KB (93378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:195fe9b7df249422f67b240aa86b08c2bf8393248857a29dc39df933cd31a46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fdf531367dece30285e6b03802b5dee15e61557eb51ef949d9d3d1fcaef099a`

```dockerfile
```

-	Layers:
	-	`sha256:d432ab8fb3e5457fa892a9a9d8693b0ebe28adbc5fa2a5dcd064d8d3244e1ff6`  
		Last Modified: Tue, 12 Nov 2024 13:32:21 GMT  
		Size: 3.9 MB (3938732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:475ed9a1ab4f5e86469908636c4524eadd55ea92f90cb3e7584a8c8bc22d5e85`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 14.1 KB (14137 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:4c58317ed937fc30fdccbfd6e609c1810573b9052f6937bea93c95eacf668e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436d8bc3e03a379a8d2b25a3b9fbeced8bdfc032e18b7bacf4ea206c9eed744e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cfb12e48f51f3be731070cc296a425d5d61dbb1fd547b84dfa0eadc63c471b`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 11.7 MB (11688927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b6e6861b0b6e94b6ba6dd87d46e8cf625779109eba1a6332bc56147d591897`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a4461e0d5e9d53b5bd20baaf7ce175126b90a0527a6d018f518ff1e8b492f5`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6a54db7525e753cb39845d57cb48831ef1d279a3b3314d566ef7df0cb9afea`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 93.2 KB (93209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3909c5a6bcd7ccb77cffd551f11881687911a606ce66ea956d9182ac8795e15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bd98ee86105104e646e2c3de982967161ba4b0854f37f59dfab18b0f08a312`

```dockerfile
```

-	Layers:
	-	`sha256:d9d58fdc2e7d7ce479676d3a6b83a4d215bf5d795015bff631faabc74c8acc24`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 3.9 MB (3936396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b0af7d2d2c98366f72972bf6bdf848dcde29818c43ba6666476d0b655fe602`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:a29ddff999331d8a84d57feb7604e07f98e15bb6d19fce6094e68a77bb3ec8f7
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
$ docker pull neurodebian@sha256:b8afb69da5b752b060806ec138fc3250abbedd6e6b123ec18579d284a0fa6498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60938060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e220ceb0b306f430cc776ed85f4e2a38f5b334e2fae14cce9cb5f8707630f5f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e875bcda0d24503a52645cf07fa8aa3dc1787e24f752990271aba967a9cfb2`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 11.3 MB (11266807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cca6a0f2fda1ef8ccfaeb511a82fcda80b6db7b91c345af7ea41dbe4f31e28`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6765a2eef3310ed643c9cbddd43e752a916e9ad1dcef70d89ef5dac93caba3f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f968c64ee180766d3e71944b655ff6d334e49b33b507c3daaccb449da7105`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 93.1 KB (93143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36ebc47b1d30568b2899589ba58430ac196cc8a733cfcbcb822f531251167de`  
		Last Modified: Tue, 12 Nov 2024 02:14:52 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6349e62c60180c5f04a0f88d011ad639c93e6ccecaea806de68713c6f69f1b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0450b5647d02f833f34a0f5672bfa7087713135811665f4bbd8444eb384d5347`

```dockerfile
```

-	Layers:
	-	`sha256:f5570f0790a0acacb7b300035ab5b7326e867a2ca3567c8e5523e787a4bfed04`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 3.9 MB (3938519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68a35dbd054a1e8d7907f5afc5da4b8de02e38190d41b7a811862d59a6edc98`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1de43f7b125dbbbfe5a310600098e8de1fbfd335184997e9cc609b4758231958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce5ba9d618002f94a38cff26b1170db170e99a36d546b12c1e2a5cc68717d50`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e374b4f322cd89941e3a79c9bd26d1a5f1c6bc1cbada76ddcd1dc30f5e5cdba3`  
		Last Modified: Tue, 12 Nov 2024 13:32:21 GMT  
		Size: 11.2 MB (11232560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c07a4424e486742d8557f51e2d6ea83c25c81a3fe1083cdc92f2aaabe53972`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76a820ff7756abf0046ae961df3ad5d2f997f1277bdb445d4f9ce1e548f3cc`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89406019c22729ee9e55b00384b15954a2694a0806199b7273eb34553edfd429`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 93.4 KB (93378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6918a4974dfa238bbfdcb88f3d3f3458661a13de3a8be18203eff7defe143`  
		Last Modified: Tue, 12 Nov 2024 13:32:51 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:454165faeccb15f4aa5f0a212fc5218e227aa920fc5efa71800221a7aa824d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a29833a80483958f799c7ad16899b52498cf4e2f87262d5bfc5275cbe29c1a7`

```dockerfile
```

-	Layers:
	-	`sha256:c1010f6fd3eee44d87ebb438d3b23434a45fa4899ff9a6ae85965ce06845eda6`  
		Last Modified: Tue, 12 Nov 2024 13:32:51 GMT  
		Size: 3.9 MB (3938772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd8b5199518f821a024f414a90c2b37720a635f8bb8c6cc3c6cf2d1a5cf0fc9`  
		Last Modified: Tue, 12 Nov 2024 13:32:50 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f13d92e5211f97d59e114b6436138348667d7cc56920e67c081e941416adb094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150d422afc9147c5b81e217636b9324ce038c190cd5403829a80f8f38fdb8aad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8b2bc7e2c4724e0d9cc99253b76322cead2324f1116c27c22e45882c20b73b`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 11.7 MB (11688981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66a8acf27bb69d2d3bbfbaa534d4977b944e9f27fbdbea8956f2bc958022dae`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0ba9db146b8f5a4270e9de5dd5552b75471e8b8b207fcc3ed7a5074dfecf8e`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebee1da5e8ebfd36eea82726d73c31e81d1bd572d464a7c2e1735488895c79fb`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 93.2 KB (93224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b8bcd17001bedce769ee0a613e4ff52e7a2324d77bef8e3ad6996ecd0f70ac`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:668fa7f722219a898de96bb7335edb634f3ae7fceb8edca2b504e43a6ab42ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84f4bff819dd2497c5fc6382cc7ed783a292326d68e126067bd7a6ee1db7a6c`

```dockerfile
```

-	Layers:
	-	`sha256:fdaa6a6a15e6b4d89406be98109008f643f841b097fb21432b53f7c7520fec64`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 3.9 MB (3936436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79e84acf401893a2bcccb52bef19425ff82fc1e6122b7a32860ca01d7c2a473`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:622bde4678ffeb69360f0f68d9606def240860d692ce8c738d05b887dcc04d89
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
$ docker pull neurodebian@sha256:2232750107c8bfc49bb93193550714a803da33eda58209d85a420673ac1c78f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66317020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48506232fa8180d8ecafd8f9ef54758c61b7ec5e58c2c808a3197123928de3df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfa11ef8c4aa3ade3aebc334b60d4d70e47c5dfb4df8cb3bb69af638f1012ed`  
		Last Modified: Tue, 12 Nov 2024 02:14:24 GMT  
		Size: 11.1 MB (11105060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e446eb6fa386c8e7218c2736b31102cbbed336088e6e52bb23b8ccbb00882`  
		Last Modified: Tue, 12 Nov 2024 02:14:23 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c1a5b6fc7731b200d91a9a3531098229dae00f840ba97fd9e461511fe7fdff`  
		Last Modified: Tue, 12 Nov 2024 02:14:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4fd44ed3bd40f10613a235d854263aad592ddd89228aa50676eb400c5d3f5a`  
		Last Modified: Tue, 12 Nov 2024 02:14:23 GMT  
		Size: 101.2 KB (101189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:13746c2aaa1494df83c9e70f7025af1d4e73cc7d12b41a0b64902d09bfaa9b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251fab2583de867838dabca119850e404fb6efcc5be78496bacf71f1d8dee8a`

```dockerfile
```

-	Layers:
	-	`sha256:4bb29fc5223c99961577083a12229edba4481bf7d5e9c8dd566141f0793f7db0`  
		Last Modified: Tue, 12 Nov 2024 02:14:24 GMT  
		Size: 4.2 MB (4238918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14f66a1d7edddb9f5b9c6e38d917e7a9f4f903085ea5aabe3251890a5ebd252`  
		Last Modified: Tue, 12 Nov 2024 02:14:23 GMT  
		Size: 13.7 KB (13692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6d6d0b65eaf825b60f7979095a157f818515bd9053f1e86d6d18dcf3de3d0030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64966120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539f6ed23a0cfff2ba047b745d08b0dccef7b9f7a6d036c24cc2a3f433f414cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b1aa34dae88839f31ee7186cfe6048acef4d263fa3b8b52b9d0c6053c909c7`  
		Last Modified: Tue, 12 Nov 2024 13:31:22 GMT  
		Size: 11.1 MB (11105942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f915087e901fc60bc7393af36830404c4a309df7569bde113df0428a4fbe925`  
		Last Modified: Tue, 12 Nov 2024 13:31:21 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cec66bba35fcec6dccf7caff91f7d960335174fb55f5892210df9808005acc`  
		Last Modified: Tue, 12 Nov 2024 13:31:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51635ed477ac459b18fbe60d935a5d12a047bb21c234e1972ad0ae06e4c41c2b`  
		Last Modified: Tue, 12 Nov 2024 13:31:22 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:390865aa2b88965c55b34bb827a635cfa45a3e6314e13016f830a75e8e7fa117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e5c732e6afd8ce4a15c8acdceefced9f07a367a36f967a7cc231f32fd7eff2`

```dockerfile
```

-	Layers:
	-	`sha256:fdf7a39b8db915a202944215a81d73f562c842d9c73e3d208f3e586e830ec589`  
		Last Modified: Tue, 12 Nov 2024 13:31:22 GMT  
		Size: 4.2 MB (4238523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dc963cc994593d6bf9078c5680f80a74241206e36f1c67160544d28c5146dd0`  
		Last Modified: Tue, 12 Nov 2024 13:31:21 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:f609c274c2618998d24c52a6df0441f5df0032e90e3f1a63b95b37ca6484704c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67697112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b76e2f6a3b11a04443a3080caae4e2c101b66dd1c25c336121874acfefabb07`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d073a1c601e48b16b6148c0f2b74b5addc1206092570714a5dc88b69e85c8511`  
		Last Modified: Tue, 12 Nov 2024 02:14:17 GMT  
		Size: 11.5 MB (11500364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1586fd7ccc89fe18e9b4f40b0b184b6ef9d9769d8bb35dd6ae4f5f7a8eddaef9`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f8fe0c7aedc2a709542bc16b130dacdcaba65a2a616ff1c1d36dabde3ec385`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331f23be06d960a18a04fb88ca8d5843394679c00ae5ddb89c916f593605fbf2`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 101.1 KB (101080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a70195da17d31b1ab2a452e2cdd149967b05b10539b68e17dfc5075f59572da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e9e768b155ef0d4ea448b5e5cc7a300921fe2ed660e78c818d1d8d6a9447a6`

```dockerfile
```

-	Layers:
	-	`sha256:e0be0e44bd613d4907a7a5e80e795b4892345264f77ee55efba29073fd90ff16`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 4.2 MB (4235378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:901e1ce288d57a3a9099616eabda5520b086aae1e6d09cc03c1c0f3c2234ffac`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 13.7 KB (13664 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:49808875f485729b5226827899e0b24e87b9c3db517c10cd04360c9237b2ebe2
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
$ docker pull neurodebian@sha256:02ce659bb167d59ab6ef1ce34e2ead94bdedf4d7d2033b0ff5abc0609d5965b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66317451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b02b0048fe7520afec08f7397d6ef93116f8d8185d2672bd0f86b8080801ee1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a37c6f541b5475a2edf1197b5c614e880e7198985a1b8ec0dea4b56d54df03`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 11.1 MB (11105106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c59917fd0abe12cd41ae981ceab5136df3b29e5524b77b56926cff5e7f2541`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c80ba689189a2ba5d02ff74c1ad6e9336099fe96cc77aa1f3edcdcde5b80310`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4f0dce01bd7f03f165e2a75abc50ba124834a23c6696acdc4c61062248dd6e`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 101.2 KB (101220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035b33d71c46650a25383fa983d31ee778f4369a986b057470f3f322c4cc4fe`  
		Last Modified: Tue, 12 Nov 2024 02:14:32 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0d7cafa1afbcc1c9daf9c5c396252a234ecebdf09a5aa8e65a391f0864429941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4254675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7eb0681a44503368077354fb1b000d8e000ffd8e2db6d9a37dae5837064b1d`

```dockerfile
```

-	Layers:
	-	`sha256:5029676a85e8ae6250c676c64cc90541923b66cba1bb3f9f266169b008bb4b3f`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 4.2 MB (4238954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6172bf8268b5a35eb36e648113a11d9b8a66cc27cbbacef84cc0e055c70a7b95`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:79d498377a625be39384077c7dad1a554b925638413a5e8775e4cdf1daa25f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64966480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b3c4044e621d2d723e8039316f26ec936252758eecbe55c68368d20b8f63d5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b1aa34dae88839f31ee7186cfe6048acef4d263fa3b8b52b9d0c6053c909c7`  
		Last Modified: Tue, 12 Nov 2024 13:31:22 GMT  
		Size: 11.1 MB (11105942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f915087e901fc60bc7393af36830404c4a309df7569bde113df0428a4fbe925`  
		Last Modified: Tue, 12 Nov 2024 13:31:21 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cec66bba35fcec6dccf7caff91f7d960335174fb55f5892210df9808005acc`  
		Last Modified: Tue, 12 Nov 2024 13:31:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51635ed477ac459b18fbe60d935a5d12a047bb21c234e1972ad0ae06e4c41c2b`  
		Last Modified: Tue, 12 Nov 2024 13:31:22 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636d6c91546d976a3f0b12348d0e11726f8e74587a3e2fcf8b877284c5d19124`  
		Last Modified: Tue, 12 Nov 2024 13:31:50 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8d1f9be6c2df006a3b9e16bde016c8aab8332bc8be8919bad237b7fe4d39d492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4254420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ac76b19108ef4b9d89c64f1cc09ea2711fc7e312b93dd3da5d9fca5dc087fd`

```dockerfile
```

-	Layers:
	-	`sha256:e238d020544911f296e9016c0f63aac044aafcfe8df6d1120549eba2d6a5a39a`  
		Last Modified: Tue, 12 Nov 2024 13:31:50 GMT  
		Size: 4.2 MB (4238559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75208d7e9d142a4971bcad16f1bf4a19b90a6c1b8d5de9bfe0619cfe62ab5dc`  
		Last Modified: Tue, 12 Nov 2024 13:31:49 GMT  
		Size: 15.9 KB (15861 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1d8853f7410229e33e0e1eb7d3c0f1c986d0956ac3667a4a00eee8502222ff88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67697344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506288179711128f76d5ddde51c19b0683b5e131733e5b78349c66e17b7e7eed`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852ae5e516fa02820da75a950a2294dc25d67da99c33d679ded811ab6c0d6089`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 11.5 MB (11500245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ff72eea72a6cd65b46ea3111a4a99ddfc564018dc4244298d84496d5c8b8ca`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d85b7909226fa80dcb04b965a3dffa806c46cb25fdf24c12ef6747b428cc641`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3532548a28e972d50b8e915b968250f536debd39f6faa3e4b28fb6d723f7639c`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 101.1 KB (101069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1b1adbd380455d0c77a203b2d2c09f432ef2a8a02241618dd006ccb95ba4e4`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:212079c516e0addb2743f2e8cc567cd40f8ffc7839b61ff48aae727858c94332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb6915bfe6b29bfd22f1abaa95f7e7e993a81dfb7bdabe9c3c8979f76ee9cf8`

```dockerfile
```

-	Layers:
	-	`sha256:a0bf5352d1cc80c064869854eaa71c8fff6141f9aab0ed63b2fd723a22d6c8a6`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 4.2 MB (4235414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f521ec6a86a2bb91bc017f685c79a6ed5e6ec6eae3ac01da89c7a1bc8c0546`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 15.7 KB (15691 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:8bcdb02c955c552289fb14468e3d0eccac712d0a170f1fff5601f3f3af9d8a49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:a0c6cb45ac1cfbe06c47f14d684929ff5f5907ef7f083c360195214c3ac6aca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1335fc867ea7b822d1b6882dc96ad365e5cc4643152d61c5fc8a7bc5f85a988`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49fa7316f784f5cf307546c8c97bd1b9f3a1fd2943c27fceb71ec2dd6409f48`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 5.4 MB (5360278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb7c65bbf482527df64ccec5d79c08cb11cf2d1f4054f4977e47dad48ff8435`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e678bedd7e50e1ba3e947302d4a3badb36d988b369aab4b47c1fa78259c23552`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9792897da4dcee6732822377f46272804fb1e9b7f31dd60d17894a127edb839`  
		Last Modified: Wed, 16 Oct 2024 16:13:43 GMT  
		Size: 105.3 KB (105327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:848d25161f517586e1457fc807e778d3305bad2daae744ec21fc37849f68173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820220dbbd11c6d8f3103b1a3ed83da871c77d7b02f18798badcf3237303dcae`

```dockerfile
```

-	Layers:
	-	`sha256:27970857ec501c025d084e20e5352a5d5ddc17824cc89a85f49e7025cdcb4a02`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 2.0 MB (2002651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:849d52e89f42eba3812416ede3dd4d1badb9a69a5a982f874e39c325041eb9a2`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 13.4 KB (13444 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1a3f2e41cb72abdd7dcab281d6513ce2dc547865fa3b4ba0776bd58ea8a5de97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2c98411bfbdccf11946d245a8061c56c6ce058ada6075d911256dd80fadff8`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6101036d9458690903008f9743d7d9982835f206b38bec0aee1147faccc7c0`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 5.3 MB (5340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a29390bcc04ab62cd8664a0c5eb9c2c8529bc1cf5a8fc1e442f9740f53d73`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a06a5898141ddee96056f1057c0595e290735b4831567d9e98c36af5687cba6`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead23b60010d07ced4212e4cf8a6c4f69eae17b7d32e4a35b7bf00c6df7eacd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 105.4 KB (105412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1f3f34f75e1a4bc32b849a9ffc880a30708443a7fdc0da8a50c2e90180094f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5772b0ce1260ce48effc24ad2f6bdefdb4674ee0d585774b4464dfdaa8df07f`

```dockerfile
```

-	Layers:
	-	`sha256:71ee94546588c20b92a492d129395aac336c0ae8677f9f8048b6890a1e640901`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 2.0 MB (2002879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa10decb4cbaa5f56d95540086539ce9a7bfee79f97ecf26a18eb6160c482bbd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 13.6 KB (13563 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:focal-non-free`

```console
$ docker pull neurodebian@sha256:e1b1eebaa7be7a7ae8986f10c005fbaacce6a33e73c7193cef12dee6f49b40b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2ddc9018acf97b1f5814caa6cde3c3d36dc386f558589639e00bd07b61c4ceed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02507bb93b25ace19e3dbcf9e5a746ee64169a6e6641918f946da8db0e4d17b`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f4005701787afe01df59207e8d67264732bba189629db1779b4ffa79571550`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 5.4 MB (5360288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6862ce93e83033ea4be1d4f8bd4ea70b498c761c3664782d446af47aa9926b`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce53e76a062f11aaecdb2eaab737adaf3dfe235440d4e34cfa7bd8bc8634e70`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f662144d756ef598c43631f18e5a5aa12b2a8e2c719e17635359530cbf9a9b`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 105.3 KB (105328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c113f4052eb4bc0e89d69bbfef200be8e9cc348104fc8ae5bc167ebdf6ac683`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fdd9dd95911aad8010d1bd7b668cfc9886a64e712c66aeab16529edd5642e84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419484197e2594f495dc65df02606517cfd33b3e8fb27db49620e293bfb8facc`

```dockerfile
```

-	Layers:
	-	`sha256:96b650f1cbef5c5dbf1b7069ca052e04734ab3f40d4e9ed771e9496d60fd999e`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 2.0 MB (2002687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdacbdc41b77b356c35fb81b7e0fcf121e4d6c1b38d2d913103141df6f522c9a`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b3f6acebf8e01d4ccb64904ddb4e553df094a7fb6223b50f683882a0756a284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9be140461e203793948a95c87503859fadcb667866ac155c79cf9aea88c1edf`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6101036d9458690903008f9743d7d9982835f206b38bec0aee1147faccc7c0`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 5.3 MB (5340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a29390bcc04ab62cd8664a0c5eb9c2c8529bc1cf5a8fc1e442f9740f53d73`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a06a5898141ddee96056f1057c0595e290735b4831567d9e98c36af5687cba6`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead23b60010d07ced4212e4cf8a6c4f69eae17b7d32e4a35b7bf00c6df7eacd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 105.4 KB (105412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4975400a8d7cbc9b67c0e50618fd95fa63506aa713da18a3da28accdeb57768`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b26186688e44f87210438ddae17d14c31f634b630c497d04013b36ec09d92089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b3564811c260795602aab1de18bc1a0e9abcc4a1a00d4aa08bf2c13102fd50`

```dockerfile
```

-	Layers:
	-	`sha256:5f09b22f2f9e9d8a1f0ccc85ccd622a779576a09f4ec13d286e85c8831be03eb`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 2.0 MB (2002915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc6326745662ee2e02b1d747a2d2ba13494721e28def82decf35cf47a1614ff`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 15.8 KB (15808 bytes)  
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
$ docker pull neurodebian@sha256:aacfdbb5899916ce6aff133d995785d867b2697513f51930626919df8816b52c
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
$ docker pull neurodebian@sha256:dc1103341f4ea2f25e0d9bd456c9a29d1ce3c89fc9fdf03ef9855b40020ce2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60937609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae651fbb06567e9d58779eb005a0d338e9fd6c3e9e2f94f104bc7cf56cf2d8e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f92fba1f2243260f740882b33bd65ce9be7c710ee5ab93f9c7b65c5657cfab`  
		Last Modified: Tue, 12 Nov 2024 02:14:48 GMT  
		Size: 11.3 MB (11266780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0dcde979a959198da9acd3e0363652603c29070808043e0f715abacc4cab3d`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca047e2ff6934fd61ea0fdd2bcfe2eb8c113d771ddf33cd7d69c8e029508bb`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9bc304a1bc3fe8ff0d4ba75eaa7938ce3de3002a43c18a34cbd5f436180128`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 93.1 KB (93143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fd1d034fa70625003727fedc26cc6409115c5ddcef4a034a2b4763cb77ecf1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb574390b66288dc89d92f025f7fbe7bdc29e2f6dfef2aca5cf5b04ed2269f5d`

```dockerfile
```

-	Layers:
	-	`sha256:716b9d855b2d05a308e0a2415f3fc35b67cac1d7d59a739292f73c7c76e4e054`  
		Last Modified: Tue, 12 Nov 2024 02:14:48 GMT  
		Size: 3.9 MB (3938479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b957b5cd62d235b91fff8c8a270d1fb78b3627590548e5fee46f029a6b756fa1`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 14.0 KB (13999 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1f36fdde405355c0bf1aa5e1d801e1ac091b9a13b79b5fdc64c67386e08c0e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971276f59476fb7abd2a062acfe28a943c1358d6e56974be08536e68e600e96f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e374b4f322cd89941e3a79c9bd26d1a5f1c6bc1cbada76ddcd1dc30f5e5cdba3`  
		Last Modified: Tue, 12 Nov 2024 13:32:21 GMT  
		Size: 11.2 MB (11232560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c07a4424e486742d8557f51e2d6ea83c25c81a3fe1083cdc92f2aaabe53972`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76a820ff7756abf0046ae961df3ad5d2f997f1277bdb445d4f9ce1e548f3cc`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89406019c22729ee9e55b00384b15954a2694a0806199b7273eb34553edfd429`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 93.4 KB (93378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:195fe9b7df249422f67b240aa86b08c2bf8393248857a29dc39df933cd31a46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fdf531367dece30285e6b03802b5dee15e61557eb51ef949d9d3d1fcaef099a`

```dockerfile
```

-	Layers:
	-	`sha256:d432ab8fb3e5457fa892a9a9d8693b0ebe28adbc5fa2a5dcd064d8d3244e1ff6`  
		Last Modified: Tue, 12 Nov 2024 13:32:21 GMT  
		Size: 3.9 MB (3938732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:475ed9a1ab4f5e86469908636c4524eadd55ea92f90cb3e7584a8c8bc22d5e85`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 14.1 KB (14137 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:4c58317ed937fc30fdccbfd6e609c1810573b9052f6937bea93c95eacf668e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436d8bc3e03a379a8d2b25a3b9fbeced8bdfc032e18b7bacf4ea206c9eed744e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cfb12e48f51f3be731070cc296a425d5d61dbb1fd547b84dfa0eadc63c471b`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 11.7 MB (11688927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b6e6861b0b6e94b6ba6dd87d46e8cf625779109eba1a6332bc56147d591897`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a4461e0d5e9d53b5bd20baaf7ce175126b90a0527a6d018f518ff1e8b492f5`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6a54db7525e753cb39845d57cb48831ef1d279a3b3314d566ef7df0cb9afea`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 93.2 KB (93209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3909c5a6bcd7ccb77cffd551f11881687911a606ce66ea956d9182ac8795e15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bd98ee86105104e646e2c3de982967161ba4b0854f37f59dfab18b0f08a312`

```dockerfile
```

-	Layers:
	-	`sha256:d9d58fdc2e7d7ce479676d3a6b83a4d215bf5d795015bff631faabc74c8acc24`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 3.9 MB (3936396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b0af7d2d2c98366f72972bf6bdf848dcde29818c43ba6666476d0b655fe602`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:671aebf4b5441b626f248d33d6000831bac3229c6b1da9adf42dbfc20177e97c
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
$ docker pull neurodebian@sha256:02341e7bf46103f4577ef0e2d745f58d05ae7bb047112c648ec906a889f1ca2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5725464d7419d0cbb29281a4b025c7edc770b315b07e2ab05bfa3cb835841155`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce556cde727d333e73847bbca3d36e434dfca710f1a863ee0439ab136253bf3`  
		Last Modified: Tue, 12 Nov 2024 02:39:28 GMT  
		Size: 6.3 MB (6309051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876190866705e261719a491e7f19b8aab0e39abad8ec417f1480956bd157bcc4`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c713715bdac20ad3f35c0c1187975b28de614033b14c0f83e294aa738eefc15`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e22ee5b8424b9b34d19b1a8282f540e71fe0c07b5d3e25e5263c3d62980313`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 91.4 KB (91428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8dd30245382f3d326108491d8c69fec58237345376554ebbc013cd05fe00c04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3580325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f08055e6c70bd7f3696bfdd302af032ff300de65230935ed0088fec46bf3bf`

```dockerfile
```

-	Layers:
	-	`sha256:554a9c326bb4d05222499547a3867292da16c8ae1ba2a279279cb1a564f974d8`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 3.6 MB (3566698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0fc255b6b0f15440f238e312105fdf72dbb54ab3cd63108a000ad188fa088eb`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 13.6 KB (13627 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9a863cbdfe04b91a740c54eeae31e5b9f35ab8716b8bdb46c0bf8b7aefbc62e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60142419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c186ca488265cebb588dfcd888c6005590ebebc506eb3f87ab8d396ffabf753`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:0c8e2196f060907b4d5381cc165d86913c4b9e9c632b3596563398b5e178a84a`  
		Last Modified: Tue, 12 Nov 2024 00:59:55 GMT  
		Size: 53.8 MB (53759747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3316ef29e88ef66b287f756afc754e9a91d063e4a929cc02b22ab796e4e934`  
		Last Modified: Tue, 12 Nov 2024 13:34:26 GMT  
		Size: 6.3 MB (6288501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3bc0e8335a41c803791dd9651d0311bde3d580b261d8a93b0d2f1416926347`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a48a1f73dd1e3427a91a00259b5902db95632d4bdde9a9c716599a82aaf95`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a65fde09dca43100cea07b77b49479f81cbd872ee34bb95d8182df9b774ef63`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 92.2 KB (92191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bd884045b322d450ab4a2830c115c78807eec2535170a42aeb0b1d9106b50c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43849ccb04e72ca000c433e3d0a58825ee093366ed8503f1085948b56a4097d5`

```dockerfile
```

-	Layers:
	-	`sha256:b1b4f3ff58c64efa2ed2dba778ae3ef6087651d32805951af58a4e828aaaa47f`  
		Last Modified: Tue, 12 Nov 2024 13:34:26 GMT  
		Size: 3.6 MB (3572216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac7c3c393176545af7583e84316b3211197c14053c26333b28edd1f4a769d141`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 13.8 KB (13752 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:8b53b7402bba2ecb131156dc19c095fa66b390c3e0543ba59bc34a2cf7628808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60921682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855f8cd464ac928372c09088f3336af43660b41eab691ba6369c7efc9a683b0a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a37078e7ce7126f34e971c8ebed2d9cd9e8ca7917e038a57cbf35f9aab06538`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 6.6 MB (6636005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4828555fa65d9b69815653e52d20d2148dabbc62c748edbecee8d58f2c468da7`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb3886367217864504c880e1e2576ab2ef75119eabeca72c6a29719a2b1af47`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04aafacf598e2fdf002ab8f6b212b056da94e49cc7e813a12c6db9710dfc037`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 91.6 KB (91649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4529d7359a60db5677161dfdac0eaaa2b16f04e52f36f1de8a9c06828760248e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc10daa577d6f41b82fb0a72c8adc673319b83887670bedad3d7f60f049d066`

```dockerfile
```

-	Layers:
	-	`sha256:8452ffb7e51105f9857d885c835b57c39d6ad8ddbf501edb1554680e707ccf1f`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 3.6 MB (3563934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f190e9516f9bca8b481a2ae742f3b3f5ec684d606f53be1fd37fba9ebd0ed36b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 13.6 KB (13599 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:5c04eb01918764be8c5eca3892cc52fd87d2b42b5bf519533ef1ae05d6031607
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
$ docker pull neurodebian@sha256:b16595e63ba04c7e0841c6967c6836bc323e3a4f5be5775016b435463d05f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3bcb7fbca38c758f45c29940aa0046dd2fb52c05d76557f8965ad6d75e7ec9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04acb53059fdb56a81917ae63844cdc7d1347befaf6268afc454c8f14eedbe1c`  
		Last Modified: Tue, 12 Nov 2024 02:39:32 GMT  
		Size: 6.3 MB (6308926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849966c7cdea3eccdafc1d6f151deceacbe76414ee9110113000a38ca53de21e`  
		Last Modified: Tue, 12 Nov 2024 02:39:31 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26889570a7c30127539f0f09b14a7a97160478527741986bb26dc5cbefe5d9ae`  
		Last Modified: Tue, 12 Nov 2024 02:39:31 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dca83d71667f3556e88dde7a6b401f7d3161e58440d39fe177b3e08f509230`  
		Last Modified: Tue, 12 Nov 2024 02:39:31 GMT  
		Size: 91.4 KB (91430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7adabfd3ac898c58a22effd512bc9f3414a90bc969291ac6bb76d624c77642`  
		Last Modified: Tue, 12 Nov 2024 02:39:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7bbb2d989aaa50bba0d13101afa86023116fc26198c91c5d7650b59a33f3483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3582387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5171bcb6e91aac1dbe42a490166691bded29cccec6ccc2b3411ad3adf080d95`

```dockerfile
```

-	Layers:
	-	`sha256:c8e7df85f0ba147ed47c2f2de77ce911bbb23317845db0121bebbc88b3b1a936`  
		Last Modified: Tue, 12 Nov 2024 02:39:32 GMT  
		Size: 3.6 MB (3566734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf55523d3adeb0ad34254cb09aeea051639378dc2450e32dfe5fe84e4a49b96e`  
		Last Modified: Tue, 12 Nov 2024 02:39:32 GMT  
		Size: 15.7 KB (15653 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:34b94a301382f06dfc59758c0b8aade252fca19793adb6da21122590e169d76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60142813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4fb85e87963f3ba0563c6f1c98c5ff68f1cd7241a52dcf0158cb02302232243`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:0c8e2196f060907b4d5381cc165d86913c4b9e9c632b3596563398b5e178a84a`  
		Last Modified: Tue, 12 Nov 2024 00:59:55 GMT  
		Size: 53.8 MB (53759747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3316ef29e88ef66b287f756afc754e9a91d063e4a929cc02b22ab796e4e934`  
		Last Modified: Tue, 12 Nov 2024 13:34:26 GMT  
		Size: 6.3 MB (6288501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3bc0e8335a41c803791dd9651d0311bde3d580b261d8a93b0d2f1416926347`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a48a1f73dd1e3427a91a00259b5902db95632d4bdde9a9c716599a82aaf95`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a65fde09dca43100cea07b77b49479f81cbd872ee34bb95d8182df9b774ef63`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 92.2 KB (92191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978c8532dd250bc4d8c593bae3aa7a48deed54dc049a69324ded8323eb365e6b`  
		Last Modified: Tue, 12 Nov 2024 13:34:56 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1391cd91f179eb0fc12367937c798e664a4d66f393f5fdd76ad47e4996b242ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3588045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de476c105279f5cdc19c81a0329788dc243862903ef318d9527be09a1198bd63`

```dockerfile
```

-	Layers:
	-	`sha256:4d76b589fe27bbb689e38881f8daee613334cbcf3512d66f4c94dde88b212243`  
		Last Modified: Tue, 12 Nov 2024 13:34:57 GMT  
		Size: 3.6 MB (3572252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:584b98384b9ab548d7c8a7a9e02b47900e3a3318ea9cfc62927caacb08e041d7`  
		Last Modified: Tue, 12 Nov 2024 13:34:56 GMT  
		Size: 15.8 KB (15793 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:8845c7ed5b6d8416f9855b7bfe27a19c7d30aa28d292315ceed1208b3ba010be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60922100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2cac8eb5ab9ea391b78bf58b3009c37226156e61983dfa3bd713767973d918`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f05d044e3c2e56e20b7d8664005a131b7f0db158a0815b6ce0e963cd6fc766`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 6.6 MB (6636013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86351738a6ffd8a98282b090108718fd6e1ae2e9844a2af0c0b0b965a02b723`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ebda76b66a81c0a7173531a24d7eec966e7980ae07fe7c2a526d7a84a9f4e`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8339bbf5071f7546c5f224a122b1523ae558568d2167e052f3abc925bee431b2`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 91.7 KB (91668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413c486f7d7508fe28152d1b0353e06c91d1945ce06dbc30755b3ed9bd998394`  
		Last Modified: Tue, 12 Nov 2024 02:39:21 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed502b06a74350a876c7e6c61711adf51a489f6579f09b02125da12abe3671dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efff5e3a11aa6528b0e441f116da4e6a7ea7cfa2b827b2ee6bf07ee16edd5c2e`

```dockerfile
```

-	Layers:
	-	`sha256:4cfa1d9dd39b3ed912815c7fab75213e74f763e42cfa2c1a7046c7eee356f07b`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 3.6 MB (3563970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16276af2d35957766d2b5863e3a7e6f54e9ff3d186ef0347471d7e811660d184`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 15.6 KB (15622 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:622bde4678ffeb69360f0f68d9606def240860d692ce8c738d05b887dcc04d89
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
$ docker pull neurodebian@sha256:2232750107c8bfc49bb93193550714a803da33eda58209d85a420673ac1c78f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66317020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48506232fa8180d8ecafd8f9ef54758c61b7ec5e58c2c808a3197123928de3df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfa11ef8c4aa3ade3aebc334b60d4d70e47c5dfb4df8cb3bb69af638f1012ed`  
		Last Modified: Tue, 12 Nov 2024 02:14:24 GMT  
		Size: 11.1 MB (11105060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0e446eb6fa386c8e7218c2736b31102cbbed336088e6e52bb23b8ccbb00882`  
		Last Modified: Tue, 12 Nov 2024 02:14:23 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c1a5b6fc7731b200d91a9a3531098229dae00f840ba97fd9e461511fe7fdff`  
		Last Modified: Tue, 12 Nov 2024 02:14:23 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4fd44ed3bd40f10613a235d854263aad592ddd89228aa50676eb400c5d3f5a`  
		Last Modified: Tue, 12 Nov 2024 02:14:23 GMT  
		Size: 101.2 KB (101189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:13746c2aaa1494df83c9e70f7025af1d4e73cc7d12b41a0b64902d09bfaa9b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8251fab2583de867838dabca119850e404fb6efcc5be78496bacf71f1d8dee8a`

```dockerfile
```

-	Layers:
	-	`sha256:4bb29fc5223c99961577083a12229edba4481bf7d5e9c8dd566141f0793f7db0`  
		Last Modified: Tue, 12 Nov 2024 02:14:24 GMT  
		Size: 4.2 MB (4238918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14f66a1d7edddb9f5b9c6e38d917e7a9f4f903085ea5aabe3251890a5ebd252`  
		Last Modified: Tue, 12 Nov 2024 02:14:23 GMT  
		Size: 13.7 KB (13692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6d6d0b65eaf825b60f7979095a157f818515bd9053f1e86d6d18dcf3de3d0030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64966120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539f6ed23a0cfff2ba047b745d08b0dccef7b9f7a6d036c24cc2a3f433f414cb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b1aa34dae88839f31ee7186cfe6048acef4d263fa3b8b52b9d0c6053c909c7`  
		Last Modified: Tue, 12 Nov 2024 13:31:22 GMT  
		Size: 11.1 MB (11105942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f915087e901fc60bc7393af36830404c4a309df7569bde113df0428a4fbe925`  
		Last Modified: Tue, 12 Nov 2024 13:31:21 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cec66bba35fcec6dccf7caff91f7d960335174fb55f5892210df9808005acc`  
		Last Modified: Tue, 12 Nov 2024 13:31:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51635ed477ac459b18fbe60d935a5d12a047bb21c234e1972ad0ae06e4c41c2b`  
		Last Modified: Tue, 12 Nov 2024 13:31:22 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:390865aa2b88965c55b34bb827a635cfa45a3e6314e13016f830a75e8e7fa117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e5c732e6afd8ce4a15c8acdceefced9f07a367a36f967a7cc231f32fd7eff2`

```dockerfile
```

-	Layers:
	-	`sha256:fdf7a39b8db915a202944215a81d73f562c842d9c73e3d208f3e586e830ec589`  
		Last Modified: Tue, 12 Nov 2024 13:31:22 GMT  
		Size: 4.2 MB (4238523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dc963cc994593d6bf9078c5680f80a74241206e36f1c67160544d28c5146dd0`  
		Last Modified: Tue, 12 Nov 2024 13:31:21 GMT  
		Size: 13.8 KB (13818 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:f609c274c2618998d24c52a6df0441f5df0032e90e3f1a63b95b37ca6484704c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67697112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b76e2f6a3b11a04443a3080caae4e2c101b66dd1c25c336121874acfefabb07`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d073a1c601e48b16b6148c0f2b74b5addc1206092570714a5dc88b69e85c8511`  
		Last Modified: Tue, 12 Nov 2024 02:14:17 GMT  
		Size: 11.5 MB (11500364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1586fd7ccc89fe18e9b4f40b0b184b6ef9d9769d8bb35dd6ae4f5f7a8eddaef9`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f8fe0c7aedc2a709542bc16b130dacdcaba65a2a616ff1c1d36dabde3ec385`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331f23be06d960a18a04fb88ca8d5843394679c00ae5ddb89c916f593605fbf2`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 101.1 KB (101080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a70195da17d31b1ab2a452e2cdd149967b05b10539b68e17dfc5075f59572da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4249042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e9e768b155ef0d4ea448b5e5cc7a300921fe2ed660e78c818d1d8d6a9447a6`

```dockerfile
```

-	Layers:
	-	`sha256:e0be0e44bd613d4907a7a5e80e795b4892345264f77ee55efba29073fd90ff16`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 4.2 MB (4235378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:901e1ce288d57a3a9099616eabda5520b086aae1e6d09cc03c1c0f3c2234ffac`  
		Last Modified: Tue, 12 Nov 2024 02:14:16 GMT  
		Size: 13.7 KB (13664 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:49808875f485729b5226827899e0b24e87b9c3db517c10cd04360c9237b2ebe2
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
$ docker pull neurodebian@sha256:02ce659bb167d59ab6ef1ce34e2ead94bdedf4d7d2033b0ff5abc0609d5965b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66317451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b02b0048fe7520afec08f7397d6ef93116f8d8185d2672bd0f86b8080801ee1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a37c6f541b5475a2edf1197b5c614e880e7198985a1b8ec0dea4b56d54df03`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 11.1 MB (11105106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c59917fd0abe12cd41ae981ceab5136df3b29e5524b77b56926cff5e7f2541`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c80ba689189a2ba5d02ff74c1ad6e9336099fe96cc77aa1f3edcdcde5b80310`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4f0dce01bd7f03f165e2a75abc50ba124834a23c6696acdc4c61062248dd6e`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 101.2 KB (101220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f035b33d71c46650a25383fa983d31ee778f4369a986b057470f3f322c4cc4fe`  
		Last Modified: Tue, 12 Nov 2024 02:14:32 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0d7cafa1afbcc1c9daf9c5c396252a234ecebdf09a5aa8e65a391f0864429941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4254675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7eb0681a44503368077354fb1b000d8e000ffd8e2db6d9a37dae5837064b1d`

```dockerfile
```

-	Layers:
	-	`sha256:5029676a85e8ae6250c676c64cc90541923b66cba1bb3f9f266169b008bb4b3f`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 4.2 MB (4238954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6172bf8268b5a35eb36e648113a11d9b8a66cc27cbbacef84cc0e055c70a7b95`  
		Last Modified: Tue, 12 Nov 2024 02:14:31 GMT  
		Size: 15.7 KB (15721 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:79d498377a625be39384077c7dad1a554b925638413a5e8775e4cdf1daa25f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64966480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b3c4044e621d2d723e8039316f26ec936252758eecbe55c68368d20b8f63d5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b1aa34dae88839f31ee7186cfe6048acef4d263fa3b8b52b9d0c6053c909c7`  
		Last Modified: Tue, 12 Nov 2024 13:31:22 GMT  
		Size: 11.1 MB (11105942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f915087e901fc60bc7393af36830404c4a309df7569bde113df0428a4fbe925`  
		Last Modified: Tue, 12 Nov 2024 13:31:21 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cec66bba35fcec6dccf7caff91f7d960335174fb55f5892210df9808005acc`  
		Last Modified: Tue, 12 Nov 2024 13:31:21 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51635ed477ac459b18fbe60d935a5d12a047bb21c234e1972ad0ae06e4c41c2b`  
		Last Modified: Tue, 12 Nov 2024 13:31:22 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636d6c91546d976a3f0b12348d0e11726f8e74587a3e2fcf8b877284c5d19124`  
		Last Modified: Tue, 12 Nov 2024 13:31:50 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8d1f9be6c2df006a3b9e16bde016c8aab8332bc8be8919bad237b7fe4d39d492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4254420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ac76b19108ef4b9d89c64f1cc09ea2711fc7e312b93dd3da5d9fca5dc087fd`

```dockerfile
```

-	Layers:
	-	`sha256:e238d020544911f296e9016c0f63aac044aafcfe8df6d1120549eba2d6a5a39a`  
		Last Modified: Tue, 12 Nov 2024 13:31:50 GMT  
		Size: 4.2 MB (4238559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75208d7e9d142a4971bcad16f1bf4a19b90a6c1b8d5de9bfe0619cfe62ab5dc`  
		Last Modified: Tue, 12 Nov 2024 13:31:49 GMT  
		Size: 15.9 KB (15861 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:1d8853f7410229e33e0e1eb7d3c0f1c986d0956ac3667a4a00eee8502222ff88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67697344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506288179711128f76d5ddde51c19b0683b5e131733e5b78349c66e17b7e7eed`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852ae5e516fa02820da75a950a2294dc25d67da99c33d679ded811ab6c0d6089`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 11.5 MB (11500245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ff72eea72a6cd65b46ea3111a4a99ddfc564018dc4244298d84496d5c8b8ca`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d85b7909226fa80dcb04b965a3dffa806c46cb25fdf24c12ef6747b428cc641`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3532548a28e972d50b8e915b968250f536debd39f6faa3e4b28fb6d723f7639c`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 101.1 KB (101069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1b1adbd380455d0c77a203b2d2c09f432ef2a8a02241618dd006ccb95ba4e4`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:212079c516e0addb2743f2e8cc567cd40f8ffc7839b61ff48aae727858c94332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb6915bfe6b29bfd22f1abaa95f7e7e993a81dfb7bdabe9c3c8979f76ee9cf8`

```dockerfile
```

-	Layers:
	-	`sha256:a0bf5352d1cc80c064869854eaa71c8fff6141f9aab0ed63b2fd723a22d6c8a6`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 4.2 MB (4235414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f521ec6a86a2bb91bc017f685c79a6ed5e6ec6eae3ac01da89c7a1bc8c0546`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 15.7 KB (15691 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:aacfdbb5899916ce6aff133d995785d867b2697513f51930626919df8816b52c
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
$ docker pull neurodebian@sha256:dc1103341f4ea2f25e0d9bd456c9a29d1ce3c89fc9fdf03ef9855b40020ce2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60937609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae651fbb06567e9d58779eb005a0d338e9fd6c3e9e2f94f104bc7cf56cf2d8e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f92fba1f2243260f740882b33bd65ce9be7c710ee5ab93f9c7b65c5657cfab`  
		Last Modified: Tue, 12 Nov 2024 02:14:48 GMT  
		Size: 11.3 MB (11266780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0dcde979a959198da9acd3e0363652603c29070808043e0f715abacc4cab3d`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ca047e2ff6934fd61ea0fdd2bcfe2eb8c113d771ddf33cd7d69c8e029508bb`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9bc304a1bc3fe8ff0d4ba75eaa7938ce3de3002a43c18a34cbd5f436180128`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 93.1 KB (93143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fd1d034fa70625003727fedc26cc6409115c5ddcef4a034a2b4763cb77ecf1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb574390b66288dc89d92f025f7fbe7bdc29e2f6dfef2aca5cf5b04ed2269f5d`

```dockerfile
```

-	Layers:
	-	`sha256:716b9d855b2d05a308e0a2415f3fc35b67cac1d7d59a739292f73c7c76e4e054`  
		Last Modified: Tue, 12 Nov 2024 02:14:48 GMT  
		Size: 3.9 MB (3938479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b957b5cd62d235b91fff8c8a270d1fb78b3627590548e5fee46f029a6b756fa1`  
		Last Modified: Tue, 12 Nov 2024 02:14:47 GMT  
		Size: 14.0 KB (13999 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1f36fdde405355c0bf1aa5e1d801e1ac091b9a13b79b5fdc64c67386e08c0e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971276f59476fb7abd2a062acfe28a943c1358d6e56974be08536e68e600e96f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e374b4f322cd89941e3a79c9bd26d1a5f1c6bc1cbada76ddcd1dc30f5e5cdba3`  
		Last Modified: Tue, 12 Nov 2024 13:32:21 GMT  
		Size: 11.2 MB (11232560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c07a4424e486742d8557f51e2d6ea83c25c81a3fe1083cdc92f2aaabe53972`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76a820ff7756abf0046ae961df3ad5d2f997f1277bdb445d4f9ce1e548f3cc`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89406019c22729ee9e55b00384b15954a2694a0806199b7273eb34553edfd429`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 93.4 KB (93378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:195fe9b7df249422f67b240aa86b08c2bf8393248857a29dc39df933cd31a46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fdf531367dece30285e6b03802b5dee15e61557eb51ef949d9d3d1fcaef099a`

```dockerfile
```

-	Layers:
	-	`sha256:d432ab8fb3e5457fa892a9a9d8693b0ebe28adbc5fa2a5dcd064d8d3244e1ff6`  
		Last Modified: Tue, 12 Nov 2024 13:32:21 GMT  
		Size: 3.9 MB (3938732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:475ed9a1ab4f5e86469908636c4524eadd55ea92f90cb3e7584a8c8bc22d5e85`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 14.1 KB (14137 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:4c58317ed937fc30fdccbfd6e609c1810573b9052f6937bea93c95eacf668e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436d8bc3e03a379a8d2b25a3b9fbeced8bdfc032e18b7bacf4ea206c9eed744e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cfb12e48f51f3be731070cc296a425d5d61dbb1fd547b84dfa0eadc63c471b`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 11.7 MB (11688927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b6e6861b0b6e94b6ba6dd87d46e8cf625779109eba1a6332bc56147d591897`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a4461e0d5e9d53b5bd20baaf7ce175126b90a0527a6d018f518ff1e8b492f5`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6a54db7525e753cb39845d57cb48831ef1d279a3b3314d566ef7df0cb9afea`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 93.2 KB (93209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3909c5a6bcd7ccb77cffd551f11881687911a606ce66ea956d9182ac8795e15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bd98ee86105104e646e2c3de982967161ba4b0854f37f59dfab18b0f08a312`

```dockerfile
```

-	Layers:
	-	`sha256:d9d58fdc2e7d7ce479676d3a6b83a4d215bf5d795015bff631faabc74c8acc24`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 3.9 MB (3936396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1b0af7d2d2c98366f72972bf6bdf848dcde29818c43ba6666476d0b655fe602`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:a29ddff999331d8a84d57feb7604e07f98e15bb6d19fce6094e68a77bb3ec8f7
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
$ docker pull neurodebian@sha256:b8afb69da5b752b060806ec138fc3250abbedd6e6b123ec18579d284a0fa6498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60938060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e220ceb0b306f430cc776ed85f4e2a38f5b334e2fae14cce9cb5f8707630f5f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e875bcda0d24503a52645cf07fa8aa3dc1787e24f752990271aba967a9cfb2`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 11.3 MB (11266807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cca6a0f2fda1ef8ccfaeb511a82fcda80b6db7b91c345af7ea41dbe4f31e28`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6765a2eef3310ed643c9cbddd43e752a916e9ad1dcef70d89ef5dac93caba3f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f968c64ee180766d3e71944b655ff6d334e49b33b507c3daaccb449da7105`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 93.1 KB (93143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36ebc47b1d30568b2899589ba58430ac196cc8a733cfcbcb822f531251167de`  
		Last Modified: Tue, 12 Nov 2024 02:14:52 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6349e62c60180c5f04a0f88d011ad639c93e6ccecaea806de68713c6f69f1b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0450b5647d02f833f34a0f5672bfa7087713135811665f4bbd8444eb384d5347`

```dockerfile
```

-	Layers:
	-	`sha256:f5570f0790a0acacb7b300035ab5b7326e867a2ca3567c8e5523e787a4bfed04`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 3.9 MB (3938519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68a35dbd054a1e8d7907f5afc5da4b8de02e38190d41b7a811862d59a6edc98`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1de43f7b125dbbbfe5a310600098e8de1fbfd335184997e9cc609b4758231958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce5ba9d618002f94a38cff26b1170db170e99a36d546b12c1e2a5cc68717d50`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e374b4f322cd89941e3a79c9bd26d1a5f1c6bc1cbada76ddcd1dc30f5e5cdba3`  
		Last Modified: Tue, 12 Nov 2024 13:32:21 GMT  
		Size: 11.2 MB (11232560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c07a4424e486742d8557f51e2d6ea83c25c81a3fe1083cdc92f2aaabe53972`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76a820ff7756abf0046ae961df3ad5d2f997f1277bdb445d4f9ce1e548f3cc`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89406019c22729ee9e55b00384b15954a2694a0806199b7273eb34553edfd429`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 93.4 KB (93378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6918a4974dfa238bbfdcb88f3d3f3458661a13de3a8be18203eff7defe143`  
		Last Modified: Tue, 12 Nov 2024 13:32:51 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:454165faeccb15f4aa5f0a212fc5218e227aa920fc5efa71800221a7aa824d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a29833a80483958f799c7ad16899b52498cf4e2f87262d5bfc5275cbe29c1a7`

```dockerfile
```

-	Layers:
	-	`sha256:c1010f6fd3eee44d87ebb438d3b23434a45fa4899ff9a6ae85965ce06845eda6`  
		Last Modified: Tue, 12 Nov 2024 13:32:51 GMT  
		Size: 3.9 MB (3938772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd8b5199518f821a024f414a90c2b37720a635f8bb8c6cc3c6cf2d1a5cf0fc9`  
		Last Modified: Tue, 12 Nov 2024 13:32:50 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f13d92e5211f97d59e114b6436138348667d7cc56920e67c081e941416adb094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150d422afc9147c5b81e217636b9324ce038c190cd5403829a80f8f38fdb8aad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8b2bc7e2c4724e0d9cc99253b76322cead2324f1116c27c22e45882c20b73b`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 11.7 MB (11688981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66a8acf27bb69d2d3bbfbaa534d4977b944e9f27fbdbea8956f2bc958022dae`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0ba9db146b8f5a4270e9de5dd5552b75471e8b8b207fcc3ed7a5074dfecf8e`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebee1da5e8ebfd36eea82726d73c31e81d1bd572d464a7c2e1735488895c79fb`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 93.2 KB (93224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b8bcd17001bedce769ee0a613e4ff52e7a2324d77bef8e3ad6996ecd0f70ac`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:668fa7f722219a898de96bb7335edb634f3ae7fceb8edca2b504e43a6ab42ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84f4bff819dd2497c5fc6382cc7ed783a292326d68e126067bd7a6ee1db7a6c`

```dockerfile
```

-	Layers:
	-	`sha256:fdaa6a6a15e6b4d89406be98109008f643f841b097fb21432b53f7c7520fec64`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 3.9 MB (3936436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79e84acf401893a2bcccb52bef19425ff82fc1e6122b7a32860ca01d7c2a473`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:f6c1ccdcb97d58199a4fe9b6997f978983843482b34c5babe4a38d2cf176c9eb
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
$ docker pull neurodebian@sha256:72c7fb2bb9af69e070b5390bcb374f2f175fd2e73b8daafec61e08d6c5bbd253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59629163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ca9503f4aa83cfe919dacf2b290a7d13bbf3ddc3864519a46f07712b9c2a86`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b66215324468b304d65417422182e741faf08e579711cc5b611bff87de60658`  
		Last Modified: Tue, 12 Nov 2024 02:14:53 GMT  
		Size: 6.3 MB (6309001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd86868e3d1348edde63aacd3f2cd52c81b86c5cae97904fd2d6b659fb34f542`  
		Last Modified: Tue, 12 Nov 2024 02:14:53 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30be10f95fcad90b450b563ca25b5b28cc758633cd781903543304c02e2fd5be`  
		Last Modified: Tue, 12 Nov 2024 02:14:53 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182b9b4748f6b00a4f0c10446f160c1db72c8f307cf1555591e7e4b75e26780f`  
		Last Modified: Tue, 12 Nov 2024 02:14:53 GMT  
		Size: 91.4 KB (91416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:619f2dfff60b15946f03b5bdbb43fddec04e24e1f1abc7b3e626ddd15de4e33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9fe63e7e734efcb915916efe66fd39947b563fe11012b1723a406068bca8e9`

```dockerfile
```

-	Layers:
	-	`sha256:113c08f2c118c359d3eb34f45411012fe14f4a21a7273d2861fd818562dc6d3d`  
		Last Modified: Tue, 12 Nov 2024 02:14:53 GMT  
		Size: 3.6 MB (3568293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8fc47140b7d97dad4226626ad55056597ff8625fd30bb01a2f9ecc113cff8ae`  
		Last Modified: Tue, 12 Nov 2024 02:14:53 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:77a48b74180ed9debd079eba0e2e1e17caea4266541bfa0ca3fb4f61185e8f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60052495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a21c587a7c0def54d24960091ec58c697dbd157813eae767ce541a46d0305c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:4de57c6718ff0fb4c76cd3ff1a33db2bde24e482395a89d0d4f6c7e6b3c20f53`  
		Last Modified: Tue, 12 Nov 2024 01:03:14 GMT  
		Size: 53.7 MB (53669977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae23bf76a989ff5e6f76f330379b3e989793687ed133de3ac5410064a9c771a9`  
		Last Modified: Tue, 12 Nov 2024 13:33:25 GMT  
		Size: 6.3 MB (6288346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7120c2a86c21de9f38d4094726b8a00af5f3789a15c63dc031095f5280692244`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79269e860b98db1f347c42152747f764202ed57267f8615d3fce3fb871305cb9`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c82a537cb0fa455330670123eb470dd2cc9577f0075c1e0248d0d011a21835`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 92.2 KB (92189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2544ef8e974d4d3f0b0d695a620edbeb67f9bb9dc198a317f5e4ecbf110cde56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e41c3e4fea4a1621ba76e72312ddde54b8adc7f971b1ebd4298235b6198d2c7`

```dockerfile
```

-	Layers:
	-	`sha256:4786e059f82385d56b3a97a5ad00a568fb9ae05f47efcd1918a1892988c7fcfa`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 3.6 MB (3573811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fdfaa5b7d702f4e84eed71cc37bc2225cc2b5550e54b5cbd726b01f72faea4b`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 13.8 KB (13791 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:16fd11b6cfdb9fa690598b6dae7f84931f21bf7666cde4285e93fb1a9eb35697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60824771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a2fbf3810c021671c9ae29eb911fd97e9c8a43986eeed40b0846901330c025`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba5659d64325588b4a84d3c1b8c517318a047ef2e09978658a022f97d67f3b7`  
		Last Modified: Tue, 12 Nov 2024 02:15:16 GMT  
		Size: 6.6 MB (6635985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf8e3cf3654b722eeb19e2d68c89a05d0f97a1144fd06f65efea22e1f283ea3`  
		Last Modified: Tue, 12 Nov 2024 02:15:15 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f592776bdbe4553329727b8e38657f07591c55566c55cff9ff1ca0ebbdbf7e6e`  
		Last Modified: Tue, 12 Nov 2024 02:15:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c8ff2773363fcdca8df14781ca836f475929f2a2c5d159651acc6905cedfec`  
		Last Modified: Tue, 12 Nov 2024 02:15:16 GMT  
		Size: 91.6 KB (91641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e6b6eb09ec7e80f9d593216e59327ecf2d068b7b34ef798fcaf13768ba326984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6033d4d50453458b36fbc73be878f522ef78525f73e6e13cceb51c69d8fd041d`

```dockerfile
```

-	Layers:
	-	`sha256:a311239e72e2d48545cb84e404204f7a4d243d35c055ee422cd0ee090b62d662`  
		Last Modified: Tue, 12 Nov 2024 02:15:16 GMT  
		Size: 3.6 MB (3565527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:791b8e79009489fb6f95b5fa305a489b6ee848a70702723036023b374e2378aa`  
		Last Modified: Tue, 12 Nov 2024 02:15:15 GMT  
		Size: 13.6 KB (13638 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:81e8dd0a9e0b26661c24f769c2b9f490280388e12cd8b34a10892163f013c33c
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
$ docker pull neurodebian@sha256:fefe8fa828fed725f0862bb1e17640968cdbb6217136386f9afa4c217dcaba03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59629598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0886cde28c0abe347d5b9297675537483f8b89adfa3614f1f7b3b6d24b3b6362`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12105003f4e642f6b650661aac893181b1d5a223522c4ea9707f4c49c1c21146`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 6.3 MB (6309012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b019d15d3ab6709e952717fee2030801d3a2e7b48627e0495968e6a3dddc82f7`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5031ae0507f16d4327df45397b64a44524f00f43ce0a3c4b92d1841d4d4894`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb0be616ed4754fd8aaae15a80e494a5b232e34566aa75406ff523bfaa076b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 91.4 KB (91413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c93fc498acc8bd76e7c80e33b3fc67fe2b87d972f2a10e421cc3f9c28b1c75`  
		Last Modified: Tue, 12 Nov 2024 02:39:13 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2777c05f8a9537fbd757ed82f1648ad91528d8a7b1d708eea6dea994aecc9129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3584021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a94faceb0ba666bfbb25c7f7d11c1da2069fb19c2835549905ecae4eee59b39`

```dockerfile
```

-	Layers:
	-	`sha256:c57d732a8ed4c5dbaadccf163569842c875c0401b711a18a1bc6cd10670536c3`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 3.6 MB (3568329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fbd41c2b70b3c5115f92fcb0c70f179193c0b3d101a2e9b6a17c436584ae60`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 15.7 KB (15692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2124810c59c2070507d08e02b39e70ec6c559ef9db627160ac466ad8e024b528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60052919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d4cf3027ffd02a3b90835d95098378de393c5f8c1f0fceed499f13fa28e7a9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:4de57c6718ff0fb4c76cd3ff1a33db2bde24e482395a89d0d4f6c7e6b3c20f53`  
		Last Modified: Tue, 12 Nov 2024 01:03:14 GMT  
		Size: 53.7 MB (53669977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae23bf76a989ff5e6f76f330379b3e989793687ed133de3ac5410064a9c771a9`  
		Last Modified: Tue, 12 Nov 2024 13:33:25 GMT  
		Size: 6.3 MB (6288346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7120c2a86c21de9f38d4094726b8a00af5f3789a15c63dc031095f5280692244`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79269e860b98db1f347c42152747f764202ed57267f8615d3fce3fb871305cb9`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c82a537cb0fa455330670123eb470dd2cc9577f0075c1e0248d0d011a21835`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 92.2 KB (92189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a3fee26e316a8996c2e950f1ad5e0b6fe7c4021ecf5dd1d81ea3cbf9cf28ec`  
		Last Modified: Tue, 12 Nov 2024 13:33:54 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e988c7c55ce2dec9c07a22613faae849c9174ff303d408c0da6e69dcb31b4196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f11d4d0641ffbe565e4c011a9c392802ea9a92d0c210137a8730c01fc6ba4b`

```dockerfile
```

-	Layers:
	-	`sha256:4fa1271a0a18eebf089f507b19592bdb596a03efa9809236fd734eed8add7f39`  
		Last Modified: Tue, 12 Nov 2024 13:33:55 GMT  
		Size: 3.6 MB (3573847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:784bc588fdda505cd76103136b7bb9470a0ddc64a3ea6d7b531cd79f5bea34fa`  
		Last Modified: Tue, 12 Nov 2024 13:33:54 GMT  
		Size: 15.8 KB (15832 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:534dce1a3347a1871c4179745706a330c6b415fa9fd8eda2f32b41251d970ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60825149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a57bbdf189d2c4ec8efaa71b304424be58a2d1e58cd22074929fe6c196ca00`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea0ffbd19363ce5a9fc6e9f7187c63b2555049a39825812a94c390e6d270d52`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 6.6 MB (6635929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172f7e731b0de0a50742f1afcbacaebdf9c053a18fe4aa63b34f108143ce784f`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a4148e81020142fc4c880700a5d8912a5ba1357a3e86a38dbfdf1421011cfa`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cebeba3a77966586091e95bab2b4a598231d8c300e6551fd937ddbd75a7d9b`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 91.7 KB (91650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80068347cef0c5223d5f71e7dc0d64b732ec48e36d6055338c7f363bc46f3a23`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:50deb3e18194c5d466b1b6686d20d650631d5abb9211cc67f1275a9f18c945dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fc10c3e19ac99eb4c385e5f1d514019783499f18773f359e61963a5cf47327`

```dockerfile
```

-	Layers:
	-	`sha256:5827057745618179658ddb32068a4bb10e525186aed20b21cd4ce612b5e0268e`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 3.6 MB (3565563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dd822b3c8e11b3af5d8111e0582dee4147705a9e8c8e9f967578b5d00b5d286`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 15.7 KB (15662 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04`

```console
$ docker pull neurodebian@sha256:8bcdb02c955c552289fb14468e3d0eccac712d0a170f1fff5601f3f3af9d8a49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:a0c6cb45ac1cfbe06c47f14d684929ff5f5907ef7f083c360195214c3ac6aca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1335fc867ea7b822d1b6882dc96ad365e5cc4643152d61c5fc8a7bc5f85a988`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49fa7316f784f5cf307546c8c97bd1b9f3a1fd2943c27fceb71ec2dd6409f48`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 5.4 MB (5360278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb7c65bbf482527df64ccec5d79c08cb11cf2d1f4054f4977e47dad48ff8435`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e678bedd7e50e1ba3e947302d4a3badb36d988b369aab4b47c1fa78259c23552`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9792897da4dcee6732822377f46272804fb1e9b7f31dd60d17894a127edb839`  
		Last Modified: Wed, 16 Oct 2024 16:13:43 GMT  
		Size: 105.3 KB (105327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:848d25161f517586e1457fc807e778d3305bad2daae744ec21fc37849f68173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820220dbbd11c6d8f3103b1a3ed83da871c77d7b02f18798badcf3237303dcae`

```dockerfile
```

-	Layers:
	-	`sha256:27970857ec501c025d084e20e5352a5d5ddc17824cc89a85f49e7025cdcb4a02`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 2.0 MB (2002651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:849d52e89f42eba3812416ede3dd4d1badb9a69a5a982f874e39c325041eb9a2`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 13.4 KB (13444 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1a3f2e41cb72abdd7dcab281d6513ce2dc547865fa3b4ba0776bd58ea8a5de97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2c98411bfbdccf11946d245a8061c56c6ce058ada6075d911256dd80fadff8`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6101036d9458690903008f9743d7d9982835f206b38bec0aee1147faccc7c0`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 5.3 MB (5340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a29390bcc04ab62cd8664a0c5eb9c2c8529bc1cf5a8fc1e442f9740f53d73`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a06a5898141ddee96056f1057c0595e290735b4831567d9e98c36af5687cba6`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead23b60010d07ced4212e4cf8a6c4f69eae17b7d32e4a35b7bf00c6df7eacd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 105.4 KB (105412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1f3f34f75e1a4bc32b849a9ffc880a30708443a7fdc0da8a50c2e90180094f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5772b0ce1260ce48effc24ad2f6bdefdb4674ee0d585774b4464dfdaa8df07f`

```dockerfile
```

-	Layers:
	-	`sha256:71ee94546588c20b92a492d129395aac336c0ae8677f9f8048b6890a1e640901`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 2.0 MB (2002879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa10decb4cbaa5f56d95540086539ce9a7bfee79f97ecf26a18eb6160c482bbd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 13.6 KB (13563 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd20.04-non-free`

```console
$ docker pull neurodebian@sha256:e1b1eebaa7be7a7ae8986f10c005fbaacce6a33e73c7193cef12dee6f49b40b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd20.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2ddc9018acf97b1f5814caa6cde3c3d36dc386f558589639e00bd07b61c4ceed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02507bb93b25ace19e3dbcf9e5a746ee64169a6e6641918f946da8db0e4d17b`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f4005701787afe01df59207e8d67264732bba189629db1779b4ffa79571550`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 5.4 MB (5360288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6862ce93e83033ea4be1d4f8bd4ea70b498c761c3664782d446af47aa9926b`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce53e76a062f11aaecdb2eaab737adaf3dfe235440d4e34cfa7bd8bc8634e70`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f662144d756ef598c43631f18e5a5aa12b2a8e2c719e17635359530cbf9a9b`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 105.3 KB (105328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c113f4052eb4bc0e89d69bbfef200be8e9cc348104fc8ae5bc167ebdf6ac683`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fdd9dd95911aad8010d1bd7b668cfc9886a64e712c66aeab16529edd5642e84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419484197e2594f495dc65df02606517cfd33b3e8fb27db49620e293bfb8facc`

```dockerfile
```

-	Layers:
	-	`sha256:96b650f1cbef5c5dbf1b7069ca052e04734ab3f40d4e9ed771e9496d60fd999e`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 2.0 MB (2002687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdacbdc41b77b356c35fb81b7e0fcf121e4d6c1b38d2d913103141df6f522c9a`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd20.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b3f6acebf8e01d4ccb64904ddb4e553df094a7fb6223b50f683882a0756a284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31422067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9be140461e203793948a95c87503859fadcb667866ac155c79cf9aea88c1edf`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6101036d9458690903008f9743d7d9982835f206b38bec0aee1147faccc7c0`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 5.3 MB (5340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a29390bcc04ab62cd8664a0c5eb9c2c8529bc1cf5a8fc1e442f9740f53d73`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a06a5898141ddee96056f1057c0595e290735b4831567d9e98c36af5687cba6`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead23b60010d07ced4212e4cf8a6c4f69eae17b7d32e4a35b7bf00c6df7eacd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 105.4 KB (105412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4975400a8d7cbc9b67c0e50618fd95fa63506aa713da18a3da28accdeb57768`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 260.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd20.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b26186688e44f87210438ddae17d14c31f634b630c497d04013b36ec09d92089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2018723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b3564811c260795602aab1de18bc1a0e9abcc4a1a00d4aa08bf2c13102fd50`

```dockerfile
```

-	Layers:
	-	`sha256:5f09b22f2f9e9d8a1f0ccc85ccd622a779576a09f4ec13d286e85c8831be03eb`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 2.0 MB (2002915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cc6326745662ee2e02b1d747a2d2ba13494721e28def82decf35cf47a1614ff`  
		Last Modified: Wed, 16 Oct 2024 03:53:11 GMT  
		Size: 15.8 KB (15808 bytes)  
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
$ docker pull neurodebian@sha256:f2a303058812cfb9b283a3d77fb18a12de025f1c677735b76d734567e7f27b00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:49f743b3961c80ab758f749dfda65a7c5d8c41d677ddaa3eae3a0284acf5ff2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e3f60dd83e8b03b5a5aee878747e102f5a869c4a631e01590996cec149c5c1`
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
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
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
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1104a9f772d1b9535fd5ae89076e8c021d8b00ec27869c31d709faf2d09a1b54`  
		Last Modified: Sat, 16 Nov 2024 02:56:41 GMT  
		Size: 3.6 MB (3558732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8053e09f2f92c8fd8da8188698ea06040479c6bb40ba472ca9652909a71d0a16`  
		Last Modified: Sat, 16 Nov 2024 02:56:41 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06948c37d1e043df6082973324afc6b36168f415f7a5c5cfcf4194007d32b7a`  
		Last Modified: Sat, 16 Nov 2024 02:56:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33eea4e80e0244f99ab6c911b77148cfc85d3fc1c777bedbaf3d42942084fe7`  
		Last Modified: Sat, 16 Nov 2024 02:56:41 GMT  
		Size: 101.5 KB (101491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c3d81bb65ec247bf82874a72308817f2c2ac7eb45d68aebbf2e35f06c2d1cedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2000837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec51786455eba5c34b7d57636b240503c73d34ad45719117c9c9ec99fcd1d596`

```dockerfile
```

-	Layers:
	-	`sha256:3382b7400c53515a18f1fc7650b531204ce629ef25f9818affccc7fe7999e338`  
		Last Modified: Sat, 16 Nov 2024 02:56:41 GMT  
		Size: 2.0 MB (1987177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0ed112ea6d6bbfa9ec3928669668b74ff8edcfcacbb6fe100ce925aefa2591`  
		Last Modified: Sat, 16 Nov 2024 02:56:41 GMT  
		Size: 13.7 KB (13660 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a10e72d6a81812ae2222eeccfb64929c3d72226c89a7ed3856bde0d97c1185be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd56122b0c56b1f31ad10b071f4e3d181f366049656adc0a516df241eb5ad9b9`
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
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2730281b7aa2afc6f5415359b1e75ab20ffd63a9aeb9a6434ee4dd72ca91fa9`  
		Last Modified: Sat, 16 Nov 2024 03:19:07 GMT  
		Size: 3.6 MB (3557696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf185d2700eb1e11f3b9a77be6f31690a23dbb1d5a78b27b69393023b1abbb3`  
		Last Modified: Sat, 16 Nov 2024 03:19:06 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bcc50f4e7e6bd421fe9ce745bcba73eee74e2e7816a4c1934614f7868a964f`  
		Last Modified: Sat, 16 Nov 2024 03:19:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cb1aacd27b7dfc27830b6eeea54c14aceb3cba8d0e34c28d0c74b6b0c472c0`  
		Last Modified: Sat, 16 Nov 2024 03:19:07 GMT  
		Size: 102.0 KB (101983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb9ca8ce8ba0ae877f8fcf2e9f3ccca655f03f86441eb66487d254750e0219d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2002007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c5a4dc81e242dc2fdddd9b03e395be1dc0694686c0da784ad845cab12d6e97`

```dockerfile
```

-	Layers:
	-	`sha256:e783213e7062fb42e4f5f24908e6b54d667bc6d61e5639f17efe022a160d2b26`  
		Last Modified: Sat, 16 Nov 2024 03:19:07 GMT  
		Size: 2.0 MB (1988222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bef98e677abc343410bdc53477c7ea59919dabd87904f98d7c2c1a0e8f616b7`  
		Last Modified: Sat, 16 Nov 2024 03:19:06 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:7e1437687865294520ccdbd7c5c463babea5d73652986c21f575d20cb5f98225
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fecbf737e69bb6a7280a580f4a39f0893fb62f333727951d4366d1bb91d76367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a3f74a76e86e43681715ae7139cfc226f3642dd2d9a65306bbe3b8d9432f0b`
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
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
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
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d38b8e8aef4d64c7ae344914f29a40650790b36ca4af904e3f9ed2de985476`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 3.6 MB (3558751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d16b35ef360fa2983c365ebf28fe3e4d6dea08b178e8050b4a46f478a44f87f`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e88aade09779dfa4c13efaaf96275542949d9c6540340a0b01dd9d671a8b919`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95da935f4fb7e0e90557addc25a2ddad11daec76acb4a6d5d696659b0586ee6`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 101.5 KB (101484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17149c52c7bb0f4b4d6dafd08d3cb8ff441b98ec1b97e5b86ce2d422a493f481`  
		Last Modified: Sat, 16 Nov 2024 02:57:01 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b3146e161f3ce19f6e07ce945ebc7a43c30f49761e7fb6c57f819bd3e750dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100dbace151c02e6f4a60ce451a34763bf3ecd57bb4abc64d578aa922af3ffc`

```dockerfile
```

-	Layers:
	-	`sha256:9b01392fdf284c1a62db9958a609cc4a560d35ecf7f78ba48af30ff812066ce1`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 2.0 MB (1987213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df126d1669c6415286cc56056524dcd7e479d578a1c11f4c9d807f801a2bde79`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:53cac0b1df1cae57e55ac370115f26068e80c52188f8ce50be5ed3d844c4fa96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb969f64ea5c3d014d044f4992c56012a9b8a0356e7c8ca8ca2ccbd1bed4f30`
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
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2730281b7aa2afc6f5415359b1e75ab20ffd63a9aeb9a6434ee4dd72ca91fa9`  
		Last Modified: Sat, 16 Nov 2024 03:19:07 GMT  
		Size: 3.6 MB (3557696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf185d2700eb1e11f3b9a77be6f31690a23dbb1d5a78b27b69393023b1abbb3`  
		Last Modified: Sat, 16 Nov 2024 03:19:06 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bcc50f4e7e6bd421fe9ce745bcba73eee74e2e7816a4c1934614f7868a964f`  
		Last Modified: Sat, 16 Nov 2024 03:19:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cb1aacd27b7dfc27830b6eeea54c14aceb3cba8d0e34c28d0c74b6b0c472c0`  
		Last Modified: Sat, 16 Nov 2024 03:19:07 GMT  
		Size: 102.0 KB (101983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee28ffbafa489ac28fd8e18ea35adcb543ad84ee357a75f80ac8ef7aaa69eea`  
		Last Modified: Sat, 16 Nov 2024 03:19:25 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a1cf199eb2c3f73236eab154bf58c1e4bff9c5ac8c29cf77537d9dff4f6640ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ea1a0acbe9b173e127aea0f1504fb82854416e150246da15f0b6f53b6fb9dc`

```dockerfile
```

-	Layers:
	-	`sha256:4f591be482f23eebd2a681515139b503c698cb622ac37af35d8c69430cb98f32`  
		Last Modified: Sat, 16 Nov 2024 03:19:26 GMT  
		Size: 2.0 MB (1988258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a703cabb485d5e6cdbc0cf01bfbf655d0df04e4718faf6a7d729c55597a294`  
		Last Modified: Sat, 16 Nov 2024 03:19:25 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:f2a303058812cfb9b283a3d77fb18a12de025f1c677735b76d734567e7f27b00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:49f743b3961c80ab758f749dfda65a7c5d8c41d677ddaa3eae3a0284acf5ff2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e3f60dd83e8b03b5a5aee878747e102f5a869c4a631e01590996cec149c5c1`
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
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
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
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1104a9f772d1b9535fd5ae89076e8c021d8b00ec27869c31d709faf2d09a1b54`  
		Last Modified: Sat, 16 Nov 2024 02:56:41 GMT  
		Size: 3.6 MB (3558732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8053e09f2f92c8fd8da8188698ea06040479c6bb40ba472ca9652909a71d0a16`  
		Last Modified: Sat, 16 Nov 2024 02:56:41 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06948c37d1e043df6082973324afc6b36168f415f7a5c5cfcf4194007d32b7a`  
		Last Modified: Sat, 16 Nov 2024 02:56:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33eea4e80e0244f99ab6c911b77148cfc85d3fc1c777bedbaf3d42942084fe7`  
		Last Modified: Sat, 16 Nov 2024 02:56:41 GMT  
		Size: 101.5 KB (101491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c3d81bb65ec247bf82874a72308817f2c2ac7eb45d68aebbf2e35f06c2d1cedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2000837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec51786455eba5c34b7d57636b240503c73d34ad45719117c9c9ec99fcd1d596`

```dockerfile
```

-	Layers:
	-	`sha256:3382b7400c53515a18f1fc7650b531204ce629ef25f9818affccc7fe7999e338`  
		Last Modified: Sat, 16 Nov 2024 02:56:41 GMT  
		Size: 2.0 MB (1987177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0ed112ea6d6bbfa9ec3928669668b74ff8edcfcacbb6fe100ce925aefa2591`  
		Last Modified: Sat, 16 Nov 2024 02:56:41 GMT  
		Size: 13.7 KB (13660 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a10e72d6a81812ae2222eeccfb64929c3d72226c89a7ed3856bde0d97c1185be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd56122b0c56b1f31ad10b071f4e3d181f366049656adc0a516df241eb5ad9b9`
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
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2730281b7aa2afc6f5415359b1e75ab20ffd63a9aeb9a6434ee4dd72ca91fa9`  
		Last Modified: Sat, 16 Nov 2024 03:19:07 GMT  
		Size: 3.6 MB (3557696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf185d2700eb1e11f3b9a77be6f31690a23dbb1d5a78b27b69393023b1abbb3`  
		Last Modified: Sat, 16 Nov 2024 03:19:06 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bcc50f4e7e6bd421fe9ce745bcba73eee74e2e7816a4c1934614f7868a964f`  
		Last Modified: Sat, 16 Nov 2024 03:19:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cb1aacd27b7dfc27830b6eeea54c14aceb3cba8d0e34c28d0c74b6b0c472c0`  
		Last Modified: Sat, 16 Nov 2024 03:19:07 GMT  
		Size: 102.0 KB (101983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb9ca8ce8ba0ae877f8fcf2e9f3ccca655f03f86441eb66487d254750e0219d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2002007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c5a4dc81e242dc2fdddd9b03e395be1dc0694686c0da784ad845cab12d6e97`

```dockerfile
```

-	Layers:
	-	`sha256:e783213e7062fb42e4f5f24908e6b54d667bc6d61e5639f17efe022a160d2b26`  
		Last Modified: Sat, 16 Nov 2024 03:19:07 GMT  
		Size: 2.0 MB (1988222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bef98e677abc343410bdc53477c7ea59919dabd87904f98d7c2c1a0e8f616b7`  
		Last Modified: Sat, 16 Nov 2024 03:19:06 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:7e1437687865294520ccdbd7c5c463babea5d73652986c21f575d20cb5f98225
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:fecbf737e69bb6a7280a580f4a39f0893fb62f333727951d4366d1bb91d76367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33414411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a3f74a76e86e43681715ae7139cfc226f3642dd2d9a65306bbe3b8d9432f0b`
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
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
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
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d38b8e8aef4d64c7ae344914f29a40650790b36ca4af904e3f9ed2de985476`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 3.6 MB (3558751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d16b35ef360fa2983c365ebf28fe3e4d6dea08b178e8050b4a46f478a44f87f`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e88aade09779dfa4c13efaaf96275542949d9c6540340a0b01dd9d671a8b919`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95da935f4fb7e0e90557addc25a2ddad11daec76acb4a6d5d696659b0586ee6`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 101.5 KB (101484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17149c52c7bb0f4b4d6dafd08d3cb8ff441b98ec1b97e5b86ce2d422a493f481`  
		Last Modified: Sat, 16 Nov 2024 02:57:01 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9b3146e161f3ce19f6e07ce945ebc7a43c30f49761e7fb6c57f819bd3e750dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2003103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100dbace151c02e6f4a60ce451a34763bf3ecd57bb4abc64d578aa922af3ffc`

```dockerfile
```

-	Layers:
	-	`sha256:9b01392fdf284c1a62db9958a609cc4a560d35ecf7f78ba48af30ff812066ce1`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 2.0 MB (1987213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df126d1669c6415286cc56056524dcd7e479d578a1c11f4c9d807f801a2bde79`  
		Last Modified: Sat, 16 Nov 2024 02:57:00 GMT  
		Size: 15.9 KB (15890 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:53cac0b1df1cae57e55ac370115f26068e80c52188f8ce50be5ed3d844c4fa96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32554504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb969f64ea5c3d014d044f4992c56012a9b8a0356e7c8ca8ca2ccbd1bed4f30`
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
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
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
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2730281b7aa2afc6f5415359b1e75ab20ffd63a9aeb9a6434ee4dd72ca91fa9`  
		Last Modified: Sat, 16 Nov 2024 03:19:07 GMT  
		Size: 3.6 MB (3557696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf185d2700eb1e11f3b9a77be6f31690a23dbb1d5a78b27b69393023b1abbb3`  
		Last Modified: Sat, 16 Nov 2024 03:19:06 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bcc50f4e7e6bd421fe9ce745bcba73eee74e2e7816a4c1934614f7868a964f`  
		Last Modified: Sat, 16 Nov 2024 03:19:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cb1aacd27b7dfc27830b6eeea54c14aceb3cba8d0e34c28d0c74b6b0c472c0`  
		Last Modified: Sat, 16 Nov 2024 03:19:07 GMT  
		Size: 102.0 KB (101983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee28ffbafa489ac28fd8e18ea35adcb543ad84ee357a75f80ac8ef7aaa69eea`  
		Last Modified: Sat, 16 Nov 2024 03:19:25 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a1cf199eb2c3f73236eab154bf58c1e4bff9c5ac8c29cf77537d9dff4f6640ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2004288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ea1a0acbe9b173e127aea0f1504fb82854416e150246da15f0b6f53b6fb9dc`

```dockerfile
```

-	Layers:
	-	`sha256:4f591be482f23eebd2a681515139b503c698cb622ac37af35d8c69430cb98f32`  
		Last Modified: Sat, 16 Nov 2024 03:19:26 GMT  
		Size: 2.0 MB (1988258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a703cabb485d5e6cdbc0cf01bfbf655d0df04e4718faf6a7d729c55597a294`  
		Last Modified: Sat, 16 Nov 2024 03:19:25 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:a29ddff999331d8a84d57feb7604e07f98e15bb6d19fce6094e68a77bb3ec8f7
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
$ docker pull neurodebian@sha256:b8afb69da5b752b060806ec138fc3250abbedd6e6b123ec18579d284a0fa6498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60938060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e220ceb0b306f430cc776ed85f4e2a38f5b334e2fae14cce9cb5f8707630f5f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e875bcda0d24503a52645cf07fa8aa3dc1787e24f752990271aba967a9cfb2`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 11.3 MB (11266807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cca6a0f2fda1ef8ccfaeb511a82fcda80b6db7b91c345af7ea41dbe4f31e28`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6765a2eef3310ed643c9cbddd43e752a916e9ad1dcef70d89ef5dac93caba3f6`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f968c64ee180766d3e71944b655ff6d334e49b33b507c3daaccb449da7105`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 93.1 KB (93143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36ebc47b1d30568b2899589ba58430ac196cc8a733cfcbcb822f531251167de`  
		Last Modified: Tue, 12 Nov 2024 02:14:52 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6349e62c60180c5f04a0f88d011ad639c93e6ccecaea806de68713c6f69f1b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0450b5647d02f833f34a0f5672bfa7087713135811665f4bbd8444eb384d5347`

```dockerfile
```

-	Layers:
	-	`sha256:f5570f0790a0acacb7b300035ab5b7326e867a2ca3567c8e5523e787a4bfed04`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 3.9 MB (3938519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68a35dbd054a1e8d7907f5afc5da4b8de02e38190d41b7a811862d59a6edc98`  
		Last Modified: Tue, 12 Nov 2024 02:14:51 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1de43f7b125dbbbfe5a310600098e8de1fbfd335184997e9cc609b4758231958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60915558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce5ba9d618002f94a38cff26b1170db170e99a36d546b12c1e2a5cc68717d50`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e374b4f322cd89941e3a79c9bd26d1a5f1c6bc1cbada76ddcd1dc30f5e5cdba3`  
		Last Modified: Tue, 12 Nov 2024 13:32:21 GMT  
		Size: 11.2 MB (11232560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c07a4424e486742d8557f51e2d6ea83c25c81a3fe1083cdc92f2aaabe53972`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb76a820ff7756abf0046ae961df3ad5d2f997f1277bdb445d4f9ce1e548f3cc`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89406019c22729ee9e55b00384b15954a2694a0806199b7273eb34553edfd429`  
		Last Modified: Tue, 12 Nov 2024 13:32:20 GMT  
		Size: 93.4 KB (93378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6918a4974dfa238bbfdcb88f3d3f3458661a13de3a8be18203eff7defe143`  
		Last Modified: Tue, 12 Nov 2024 13:32:51 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:454165faeccb15f4aa5f0a212fc5218e227aa920fc5efa71800221a7aa824d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a29833a80483958f799c7ad16899b52498cf4e2f87262d5bfc5275cbe29c1a7`

```dockerfile
```

-	Layers:
	-	`sha256:c1010f6fd3eee44d87ebb438d3b23434a45fa4899ff9a6ae85965ce06845eda6`  
		Last Modified: Tue, 12 Nov 2024 13:32:51 GMT  
		Size: 3.9 MB (3938772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd8b5199518f821a024f414a90c2b37720a635f8bb8c6cc3c6cf2d1a5cf0fc9`  
		Last Modified: Tue, 12 Nov 2024 13:32:50 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f13d92e5211f97d59e114b6436138348667d7cc56920e67c081e941416adb094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62361668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150d422afc9147c5b81e217636b9324ce038c190cd5403829a80f8f38fdb8aad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:832e5094f1d1a0806638216e108f8c5f304112749840ba33b550928d48d45f1f`  
		Last Modified: Tue, 12 Nov 2024 00:55:00 GMT  
		Size: 50.6 MB (50577048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8b2bc7e2c4724e0d9cc99253b76322cead2324f1116c27c22e45882c20b73b`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 11.7 MB (11688981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66a8acf27bb69d2d3bbfbaa534d4977b944e9f27fbdbea8956f2bc958022dae`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0ba9db146b8f5a4270e9de5dd5552b75471e8b8b207fcc3ed7a5074dfecf8e`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebee1da5e8ebfd36eea82726d73c31e81d1bd572d464a7c2e1735488895c79fb`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 93.2 KB (93224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b8bcd17001bedce769ee0a613e4ff52e7a2324d77bef8e3ad6996ecd0f70ac`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:668fa7f722219a898de96bb7335edb634f3ae7fceb8edca2b504e43a6ab42ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84f4bff819dd2497c5fc6382cc7ed783a292326d68e126067bd7a6ee1db7a6c`

```dockerfile
```

-	Layers:
	-	`sha256:fdaa6a6a15e6b4d89406be98109008f643f841b097fb21432b53f7c7520fec64`  
		Last Modified: Tue, 12 Nov 2024 02:14:57 GMT  
		Size: 3.9 MB (3936436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79e84acf401893a2bcccb52bef19425ff82fc1e6122b7a32860ca01d7c2a473`  
		Last Modified: Tue, 12 Nov 2024 02:14:56 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:671aebf4b5441b626f248d33d6000831bac3229c6b1da9adf42dbfc20177e97c
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
$ docker pull neurodebian@sha256:02341e7bf46103f4577ef0e2d745f58d05ae7bb047112c648ec906a889f1ca2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5725464d7419d0cbb29281a4b025c7edc770b315b07e2ab05bfa3cb835841155`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce556cde727d333e73847bbca3d36e434dfca710f1a863ee0439ab136253bf3`  
		Last Modified: Tue, 12 Nov 2024 02:39:28 GMT  
		Size: 6.3 MB (6309051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876190866705e261719a491e7f19b8aab0e39abad8ec417f1480956bd157bcc4`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c713715bdac20ad3f35c0c1187975b28de614033b14c0f83e294aa738eefc15`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e22ee5b8424b9b34d19b1a8282f540e71fe0c07b5d3e25e5263c3d62980313`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 91.4 KB (91428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8dd30245382f3d326108491d8c69fec58237345376554ebbc013cd05fe00c04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3580325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f08055e6c70bd7f3696bfdd302af032ff300de65230935ed0088fec46bf3bf`

```dockerfile
```

-	Layers:
	-	`sha256:554a9c326bb4d05222499547a3867292da16c8ae1ba2a279279cb1a564f974d8`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 3.6 MB (3566698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0fc255b6b0f15440f238e312105fdf72dbb54ab3cd63108a000ad188fa088eb`  
		Last Modified: Tue, 12 Nov 2024 02:39:27 GMT  
		Size: 13.6 KB (13627 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9a863cbdfe04b91a740c54eeae31e5b9f35ab8716b8bdb46c0bf8b7aefbc62e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60142419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c186ca488265cebb588dfcd888c6005590ebebc506eb3f87ab8d396ffabf753`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:0c8e2196f060907b4d5381cc165d86913c4b9e9c632b3596563398b5e178a84a`  
		Last Modified: Tue, 12 Nov 2024 00:59:55 GMT  
		Size: 53.8 MB (53759747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3316ef29e88ef66b287f756afc754e9a91d063e4a929cc02b22ab796e4e934`  
		Last Modified: Tue, 12 Nov 2024 13:34:26 GMT  
		Size: 6.3 MB (6288501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3bc0e8335a41c803791dd9651d0311bde3d580b261d8a93b0d2f1416926347`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a48a1f73dd1e3427a91a00259b5902db95632d4bdde9a9c716599a82aaf95`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a65fde09dca43100cea07b77b49479f81cbd872ee34bb95d8182df9b774ef63`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 92.2 KB (92191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bd884045b322d450ab4a2830c115c78807eec2535170a42aeb0b1d9106b50c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43849ccb04e72ca000c433e3d0a58825ee093366ed8503f1085948b56a4097d5`

```dockerfile
```

-	Layers:
	-	`sha256:b1b4f3ff58c64efa2ed2dba778ae3ef6087651d32805951af58a4e828aaaa47f`  
		Last Modified: Tue, 12 Nov 2024 13:34:26 GMT  
		Size: 3.6 MB (3572216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac7c3c393176545af7583e84316b3211197c14053c26333b28edd1f4a769d141`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 13.8 KB (13752 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:8b53b7402bba2ecb131156dc19c095fa66b390c3e0543ba59bc34a2cf7628808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60921682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855f8cd464ac928372c09088f3336af43660b41eab691ba6369c7efc9a683b0a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a37078e7ce7126f34e971c8ebed2d9cd9e8ca7917e038a57cbf35f9aab06538`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 6.6 MB (6636005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4828555fa65d9b69815653e52d20d2148dabbc62c748edbecee8d58f2c468da7`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb3886367217864504c880e1e2576ab2ef75119eabeca72c6a29719a2b1af47`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04aafacf598e2fdf002ab8f6b212b056da94e49cc7e813a12c6db9710dfc037`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 91.6 KB (91649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4529d7359a60db5677161dfdac0eaaa2b16f04e52f36f1de8a9c06828760248e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc10daa577d6f41b82fb0a72c8adc673319b83887670bedad3d7f60f049d066`

```dockerfile
```

-	Layers:
	-	`sha256:8452ffb7e51105f9857d885c835b57c39d6ad8ddbf501edb1554680e707ccf1f`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 3.6 MB (3563934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f190e9516f9bca8b481a2ae742f3b3f5ec684d606f53be1fd37fba9ebd0ed36b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 13.6 KB (13599 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:5c04eb01918764be8c5eca3892cc52fd87d2b42b5bf519533ef1ae05d6031607
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
$ docker pull neurodebian@sha256:b16595e63ba04c7e0841c6967c6836bc323e3a4f5be5775016b435463d05f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3bcb7fbca38c758f45c29940aa0046dd2fb52c05d76557f8965ad6d75e7ec9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04acb53059fdb56a81917ae63844cdc7d1347befaf6268afc454c8f14eedbe1c`  
		Last Modified: Tue, 12 Nov 2024 02:39:32 GMT  
		Size: 6.3 MB (6308926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849966c7cdea3eccdafc1d6f151deceacbe76414ee9110113000a38ca53de21e`  
		Last Modified: Tue, 12 Nov 2024 02:39:31 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26889570a7c30127539f0f09b14a7a97160478527741986bb26dc5cbefe5d9ae`  
		Last Modified: Tue, 12 Nov 2024 02:39:31 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dca83d71667f3556e88dde7a6b401f7d3161e58440d39fe177b3e08f509230`  
		Last Modified: Tue, 12 Nov 2024 02:39:31 GMT  
		Size: 91.4 KB (91430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7adabfd3ac898c58a22effd512bc9f3414a90bc969291ac6bb76d624c77642`  
		Last Modified: Tue, 12 Nov 2024 02:39:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7bbb2d989aaa50bba0d13101afa86023116fc26198c91c5d7650b59a33f3483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3582387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5171bcb6e91aac1dbe42a490166691bded29cccec6ccc2b3411ad3adf080d95`

```dockerfile
```

-	Layers:
	-	`sha256:c8e7df85f0ba147ed47c2f2de77ce911bbb23317845db0121bebbc88b3b1a936`  
		Last Modified: Tue, 12 Nov 2024 02:39:32 GMT  
		Size: 3.6 MB (3566734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf55523d3adeb0ad34254cb09aeea051639378dc2450e32dfe5fe84e4a49b96e`  
		Last Modified: Tue, 12 Nov 2024 02:39:32 GMT  
		Size: 15.7 KB (15653 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:34b94a301382f06dfc59758c0b8aade252fca19793adb6da21122590e169d76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60142813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4fb85e87963f3ba0563c6f1c98c5ff68f1cd7241a52dcf0158cb02302232243`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:0c8e2196f060907b4d5381cc165d86913c4b9e9c632b3596563398b5e178a84a`  
		Last Modified: Tue, 12 Nov 2024 00:59:55 GMT  
		Size: 53.8 MB (53759747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3316ef29e88ef66b287f756afc754e9a91d063e4a929cc02b22ab796e4e934`  
		Last Modified: Tue, 12 Nov 2024 13:34:26 GMT  
		Size: 6.3 MB (6288501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3bc0e8335a41c803791dd9651d0311bde3d580b261d8a93b0d2f1416926347`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093a48a1f73dd1e3427a91a00259b5902db95632d4bdde9a9c716599a82aaf95`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a65fde09dca43100cea07b77b49479f81cbd872ee34bb95d8182df9b774ef63`  
		Last Modified: Tue, 12 Nov 2024 13:34:25 GMT  
		Size: 92.2 KB (92191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978c8532dd250bc4d8c593bae3aa7a48deed54dc049a69324ded8323eb365e6b`  
		Last Modified: Tue, 12 Nov 2024 13:34:56 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1391cd91f179eb0fc12367937c798e664a4d66f393f5fdd76ad47e4996b242ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3588045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de476c105279f5cdc19c81a0329788dc243862903ef318d9527be09a1198bd63`

```dockerfile
```

-	Layers:
	-	`sha256:4d76b589fe27bbb689e38881f8daee613334cbcf3512d66f4c94dde88b212243`  
		Last Modified: Tue, 12 Nov 2024 13:34:57 GMT  
		Size: 3.6 MB (3572252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:584b98384b9ab548d7c8a7a9e02b47900e3a3318ea9cfc62927caacb08e041d7`  
		Last Modified: Tue, 12 Nov 2024 13:34:56 GMT  
		Size: 15.8 KB (15793 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:8845c7ed5b6d8416f9855b7bfe27a19c7d30aa28d292315ceed1208b3ba010be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60922100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2cac8eb5ab9ea391b78bf58b3009c37226156e61983dfa3bd713767973d918`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f05d044e3c2e56e20b7d8664005a131b7f0db158a0815b6ce0e963cd6fc766`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 6.6 MB (6636013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86351738a6ffd8a98282b090108718fd6e1ae2e9844a2af0c0b0b965a02b723`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ebda76b66a81c0a7173531a24d7eec966e7980ae07fe7c2a526d7a84a9f4e`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8339bbf5071f7546c5f224a122b1523ae558568d2167e052f3abc925bee431b2`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 91.7 KB (91668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413c486f7d7508fe28152d1b0353e06c91d1945ce06dbc30755b3ed9bd998394`  
		Last Modified: Tue, 12 Nov 2024 02:39:21 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed502b06a74350a876c7e6c61711adf51a489f6579f09b02125da12abe3671dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efff5e3a11aa6528b0e441f116da4e6a7ea7cfa2b827b2ee6bf07ee16edd5c2e`

```dockerfile
```

-	Layers:
	-	`sha256:4cfa1d9dd39b3ed912815c7fab75213e74f763e42cfa2c1a7046c7eee356f07b`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 3.6 MB (3563970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16276af2d35957766d2b5863e3a7e6f54e9ff3d186ef0347471d7e811660d184`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 15.6 KB (15622 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:f6c1ccdcb97d58199a4fe9b6997f978983843482b34c5babe4a38d2cf176c9eb
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
$ docker pull neurodebian@sha256:72c7fb2bb9af69e070b5390bcb374f2f175fd2e73b8daafec61e08d6c5bbd253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59629163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ca9503f4aa83cfe919dacf2b290a7d13bbf3ddc3864519a46f07712b9c2a86`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b66215324468b304d65417422182e741faf08e579711cc5b611bff87de60658`  
		Last Modified: Tue, 12 Nov 2024 02:14:53 GMT  
		Size: 6.3 MB (6309001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd86868e3d1348edde63aacd3f2cd52c81b86c5cae97904fd2d6b659fb34f542`  
		Last Modified: Tue, 12 Nov 2024 02:14:53 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30be10f95fcad90b450b563ca25b5b28cc758633cd781903543304c02e2fd5be`  
		Last Modified: Tue, 12 Nov 2024 02:14:53 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182b9b4748f6b00a4f0c10446f160c1db72c8f307cf1555591e7e4b75e26780f`  
		Last Modified: Tue, 12 Nov 2024 02:14:53 GMT  
		Size: 91.4 KB (91416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:619f2dfff60b15946f03b5bdbb43fddec04e24e1f1abc7b3e626ddd15de4e33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9fe63e7e734efcb915916efe66fd39947b563fe11012b1723a406068bca8e9`

```dockerfile
```

-	Layers:
	-	`sha256:113c08f2c118c359d3eb34f45411012fe14f4a21a7273d2861fd818562dc6d3d`  
		Last Modified: Tue, 12 Nov 2024 02:14:53 GMT  
		Size: 3.6 MB (3568293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8fc47140b7d97dad4226626ad55056597ff8625fd30bb01a2f9ecc113cff8ae`  
		Last Modified: Tue, 12 Nov 2024 02:14:53 GMT  
		Size: 13.7 KB (13666 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:77a48b74180ed9debd079eba0e2e1e17caea4266541bfa0ca3fb4f61185e8f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60052495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a21c587a7c0def54d24960091ec58c697dbd157813eae767ce541a46d0305c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:4de57c6718ff0fb4c76cd3ff1a33db2bde24e482395a89d0d4f6c7e6b3c20f53`  
		Last Modified: Tue, 12 Nov 2024 01:03:14 GMT  
		Size: 53.7 MB (53669977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae23bf76a989ff5e6f76f330379b3e989793687ed133de3ac5410064a9c771a9`  
		Last Modified: Tue, 12 Nov 2024 13:33:25 GMT  
		Size: 6.3 MB (6288346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7120c2a86c21de9f38d4094726b8a00af5f3789a15c63dc031095f5280692244`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79269e860b98db1f347c42152747f764202ed57267f8615d3fce3fb871305cb9`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c82a537cb0fa455330670123eb470dd2cc9577f0075c1e0248d0d011a21835`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 92.2 KB (92189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2544ef8e974d4d3f0b0d695a620edbeb67f9bb9dc198a317f5e4ecbf110cde56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e41c3e4fea4a1621ba76e72312ddde54b8adc7f971b1ebd4298235b6198d2c7`

```dockerfile
```

-	Layers:
	-	`sha256:4786e059f82385d56b3a97a5ad00a568fb9ae05f47efcd1918a1892988c7fcfa`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 3.6 MB (3573811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fdfaa5b7d702f4e84eed71cc37bc2225cc2b5550e54b5cbd726b01f72faea4b`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 13.8 KB (13791 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:16fd11b6cfdb9fa690598b6dae7f84931f21bf7666cde4285e93fb1a9eb35697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60824771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a2fbf3810c021671c9ae29eb911fd97e9c8a43986eeed40b0846901330c025`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba5659d64325588b4a84d3c1b8c517318a047ef2e09978658a022f97d67f3b7`  
		Last Modified: Tue, 12 Nov 2024 02:15:16 GMT  
		Size: 6.6 MB (6635985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf8e3cf3654b722eeb19e2d68c89a05d0f97a1144fd06f65efea22e1f283ea3`  
		Last Modified: Tue, 12 Nov 2024 02:15:15 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f592776bdbe4553329727b8e38657f07591c55566c55cff9ff1ca0ebbdbf7e6e`  
		Last Modified: Tue, 12 Nov 2024 02:15:15 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c8ff2773363fcdca8df14781ca836f475929f2a2c5d159651acc6905cedfec`  
		Last Modified: Tue, 12 Nov 2024 02:15:16 GMT  
		Size: 91.6 KB (91641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e6b6eb09ec7e80f9d593216e59327ecf2d068b7b34ef798fcaf13768ba326984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6033d4d50453458b36fbc73be878f522ef78525f73e6e13cceb51c69d8fd041d`

```dockerfile
```

-	Layers:
	-	`sha256:a311239e72e2d48545cb84e404204f7a4d243d35c055ee422cd0ee090b62d662`  
		Last Modified: Tue, 12 Nov 2024 02:15:16 GMT  
		Size: 3.6 MB (3565527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:791b8e79009489fb6f95b5fa305a489b6ee848a70702723036023b374e2378aa`  
		Last Modified: Tue, 12 Nov 2024 02:15:15 GMT  
		Size: 13.6 KB (13638 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:81e8dd0a9e0b26661c24f769c2b9f490280388e12cd8b34a10892163f013c33c
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
$ docker pull neurodebian@sha256:fefe8fa828fed725f0862bb1e17640968cdbb6217136386f9afa4c217dcaba03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59629598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0886cde28c0abe347d5b9297675537483f8b89adfa3614f1f7b3b6d24b3b6362`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12105003f4e642f6b650661aac893181b1d5a223522c4ea9707f4c49c1c21146`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 6.3 MB (6309012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b019d15d3ab6709e952717fee2030801d3a2e7b48627e0495968e6a3dddc82f7`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5031ae0507f16d4327df45397b64a44524f00f43ce0a3c4b92d1841d4d4894`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb0be616ed4754fd8aaae15a80e494a5b232e34566aa75406ff523bfaa076b`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 91.4 KB (91413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c93fc498acc8bd76e7c80e33b3fc67fe2b87d972f2a10e421cc3f9c28b1c75`  
		Last Modified: Tue, 12 Nov 2024 02:39:13 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2777c05f8a9537fbd757ed82f1648ad91528d8a7b1d708eea6dea994aecc9129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3584021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a94faceb0ba666bfbb25c7f7d11c1da2069fb19c2835549905ecae4eee59b39`

```dockerfile
```

-	Layers:
	-	`sha256:c57d732a8ed4c5dbaadccf163569842c875c0401b711a18a1bc6cd10670536c3`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 3.6 MB (3568329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16fbd41c2b70b3c5115f92fcb0c70f179193c0b3d101a2e9b6a17c436584ae60`  
		Last Modified: Tue, 12 Nov 2024 02:39:12 GMT  
		Size: 15.7 KB (15692 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2124810c59c2070507d08e02b39e70ec6c559ef9db627160ac466ad8e024b528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60052919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d4cf3027ffd02a3b90835d95098378de393c5f8c1f0fceed499f13fa28e7a9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:4de57c6718ff0fb4c76cd3ff1a33db2bde24e482395a89d0d4f6c7e6b3c20f53`  
		Last Modified: Tue, 12 Nov 2024 01:03:14 GMT  
		Size: 53.7 MB (53669977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae23bf76a989ff5e6f76f330379b3e989793687ed133de3ac5410064a9c771a9`  
		Last Modified: Tue, 12 Nov 2024 13:33:25 GMT  
		Size: 6.3 MB (6288346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7120c2a86c21de9f38d4094726b8a00af5f3789a15c63dc031095f5280692244`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79269e860b98db1f347c42152747f764202ed57267f8615d3fce3fb871305cb9`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c82a537cb0fa455330670123eb470dd2cc9577f0075c1e0248d0d011a21835`  
		Last Modified: Tue, 12 Nov 2024 13:33:24 GMT  
		Size: 92.2 KB (92189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a3fee26e316a8996c2e950f1ad5e0b6fe7c4021ecf5dd1d81ea3cbf9cf28ec`  
		Last Modified: Tue, 12 Nov 2024 13:33:54 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e988c7c55ce2dec9c07a22613faae849c9174ff303d408c0da6e69dcb31b4196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f11d4d0641ffbe565e4c011a9c392802ea9a92d0c210137a8730c01fc6ba4b`

```dockerfile
```

-	Layers:
	-	`sha256:4fa1271a0a18eebf089f507b19592bdb596a03efa9809236fd734eed8add7f39`  
		Last Modified: Tue, 12 Nov 2024 13:33:55 GMT  
		Size: 3.6 MB (3573847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:784bc588fdda505cd76103136b7bb9470a0ddc64a3ea6d7b531cd79f5bea34fa`  
		Last Modified: Tue, 12 Nov 2024 13:33:54 GMT  
		Size: 15.8 KB (15832 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:534dce1a3347a1871c4179745706a330c6b415fa9fd8eda2f32b41251d970ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60825149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a57bbdf189d2c4ec8efaa71b304424be58a2d1e58cd22074929fe6c196ca00`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea0ffbd19363ce5a9fc6e9f7187c63b2555049a39825812a94c390e6d270d52`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 6.6 MB (6635929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172f7e731b0de0a50742f1afcbacaebdf9c053a18fe4aa63b34f108143ce784f`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a4148e81020142fc4c880700a5d8912a5ba1357a3e86a38dbfdf1421011cfa`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cebeba3a77966586091e95bab2b4a598231d8c300e6551fd937ddbd75a7d9b`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 91.7 KB (91650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80068347cef0c5223d5f71e7dc0d64b732ec48e36d6055338c7f363bc46f3a23`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 424.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:50deb3e18194c5d466b1b6686d20d650631d5abb9211cc67f1275a9f18c945dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fc10c3e19ac99eb4c385e5f1d514019783499f18773f359e61963a5cf47327`

```dockerfile
```

-	Layers:
	-	`sha256:5827057745618179658ddb32068a4bb10e525186aed20b21cd4ce612b5e0268e`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 3.6 MB (3565563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dd822b3c8e11b3af5d8111e0582dee4147705a9e8c8e9f967578b5d00b5d286`  
		Last Modified: Tue, 12 Nov 2024 02:39:19 GMT  
		Size: 15.7 KB (15662 bytes)  
		MIME: application/vnd.in-toto+json
