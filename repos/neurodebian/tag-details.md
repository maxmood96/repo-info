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
-	[`neurodebian:nd25.04`](#neurodebiannd2504)
-	[`neurodebian:nd25.04-non-free`](#neurodebiannd2504-non-free)
-	[`neurodebian:noble`](#neurodebiannoble)
-	[`neurodebian:noble-non-free`](#neurodebiannoble-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:plucky`](#neurodebianplucky)
-	[`neurodebian:plucky-non-free`](#neurodebianplucky-non-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:trixie`](#neurodebiantrixie)
-	[`neurodebian:trixie-non-free`](#neurodebiantrixie-non-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:82f76b53bbe4befe34c1cd8c837004b33cc081f9258b3376a8ee0f3463b3ac7f
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
$ docker pull neurodebian@sha256:9df40b0ea9c95868d65e0d4230bc6cf3af140542662751ad4858fc2818faad93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a2827ed3ae4e6c34042eead78d08bf2cbd5ca365feda35134f83f64d5a78fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:00:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:00:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:00:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360a3db99ecdb732a16f1f126976d4207aa9d983372d036f2b27c3fe152fcb7d`  
		Last Modified: Tue, 30 Dec 2025 00:00:54 GMT  
		Size: 11.3 MB (11269725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d2f319fdaefa9ea946357280ed31787a8424d1c2fb90c5c04233a3421762b2`  
		Last Modified: Tue, 30 Dec 2025 00:00:53 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b35ba6c19f111c946178b9e375dadc3d8f1ae76f9a5eae2ff0ae89ae98090a6`  
		Last Modified: Tue, 30 Dec 2025 00:00:53 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a28bdb6feee559d1cd4dfcb333fa279e90a66e33e29f8ded0cc4d368faad44`  
		Last Modified: Tue, 30 Dec 2025 00:00:53 GMT  
		Size: 93.4 KB (93362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:32a86f15faa5dcc16bf6c784d55a31b761c66ab7c8529554d1657d0458cef74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5312d8239141252c42ebf8df81bc38e3b7cffbc8a79c6beb0c2a61fb1aca054f`

```dockerfile
```

-	Layers:
	-	`sha256:47bf88e7f96240e091e5766b95388b68ff7beed8b87d60f0b4fc52a3a2dd6b44`  
		Last Modified: Tue, 30 Dec 2025 02:08:04 GMT  
		Size: 4.1 MB (4075236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bed509e4049d93b04efaaf9a8cea41fe2da5b01edcea80dc537c82f331659f`  
		Last Modified: Tue, 30 Dec 2025 02:08:05 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6833c0bd4b9f3b8516fff1dabd1be547a6755435608d0c7d5bfb73bbe5896b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac88fb8f2f18c14f33633d001057ccd8332f2b7e183bcfb88b19303409bd080`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:00:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:01:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:01:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76de6c96e27597369b524e7338a949708ab094acfce0ab9acf41063372d76b11`  
		Last Modified: Tue, 30 Dec 2025 00:01:21 GMT  
		Size: 11.3 MB (11253479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cb27afeb28fbf93480fe947d17b3bbc43b3b8413a6e64f2718c9eb6798bbbd`  
		Last Modified: Tue, 30 Dec 2025 00:01:20 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01298f07bbc2cddc4313c6e7a20c79eb3b315e8de19434e19c11f9b8060cf534`  
		Last Modified: Tue, 30 Dec 2025 00:01:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267428ab28b53f5994fcac1d5a6d79dd9b2e94492fee8c05b7d29f5c115377e`  
		Last Modified: Tue, 30 Dec 2025 00:01:20 GMT  
		Size: 93.5 KB (93507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6f2599c0efdadf08ab22a3d433cf5372b7aa1621c29b1a9da6a236725c60046a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7e3b4ad787579bf2b2289c8d421f4fa997cdef176d24b19bd2425ac6d8feeb`

```dockerfile
```

-	Layers:
	-	`sha256:34f8520afdf262ef9c568b886a0ed65c06d34bf6c59174fd757244317d01bc25`  
		Last Modified: Tue, 30 Dec 2025 02:08:09 GMT  
		Size: 4.1 MB (4075478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d952abe5c366f262ecf4300fd673502af65a4e9c98038025db08ffad9834a4`  
		Last Modified: Tue, 30 Dec 2025 02:08:10 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:e541bd3d6e8c2e350585ff969178f5b1eb50d8c9ba616b7bdbf2f8399c5f14aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7d620a96142dcd3f186a6fe338504785161072efe1e215f5852fcfc5f84864`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:15:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f52798efde006ed1cd5f8b1568731b4e192bb8d42469448e91e101a0db4474`  
		Last Modified: Mon, 08 Dec 2025 23:15:29 GMT  
		Size: 11.7 MB (11690144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab9b17f9e8302b4007852306001a4fec79b4040b0206f90e41917f36c14aaf`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80fb5d370b48a0007fee996c5762d278fe813640bb9c94a63fb41e8d8b2e096`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b644a9afbba75e07f7cce8cdc7ddff087b8ce4f882d4922da7656fe6eae3e1cf`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 93.4 KB (93393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:682023088122f95448d674072ec064ed9c5f200510c386b7da9b9572a60dcf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb59ba0285827e553a3b085b7aa8dcc0cb47e214ae0b993a08817c9ad3cfb10`

```dockerfile
```

-	Layers:
	-	`sha256:ee7b2db1f021c38b521cae01de099d8549088a69985b97fdf1eae25474abc095`  
		Last Modified: Tue, 09 Dec 2025 02:07:38 GMT  
		Size: 4.1 MB (4073204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a489f0243008eccca8a2550085e9994ad5c7db757f3065e9cbac12ae22242e1d`  
		Last Modified: Tue, 09 Dec 2025 02:07:39 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:1df3d441b412b21428738a991ef82ec761861eece4e78a72435307753613749e
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
$ docker pull neurodebian@sha256:abd11df33ce94245c5b308a02ac07a8a0db9d3ba22e30bf2ba86b8e53105a48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd504540067624ec06b2c5272b16151d76e122ffa720c3875f296e98a8ba9713`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:01:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:01:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:01:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9219b618e4e6182d17706ece800345bbb50e09f73c77956af27105335ff597f5`  
		Last Modified: Tue, 30 Dec 2025 00:01:25 GMT  
		Size: 11.3 MB (11269781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13e191d6357ce5e635c96f1043c54d607e416a6266aa6d684bed72db3a5f010`  
		Last Modified: Tue, 30 Dec 2025 00:01:24 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6854b4553261e47e94358955f111b2475846ef1c8a4dab48857bb9f1a27e410`  
		Last Modified: Tue, 30 Dec 2025 00:01:24 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da4d2477a14e4cb069f0a2140cc894b75cd66ad7b520df1deed197c3530388a`  
		Last Modified: Tue, 30 Dec 2025 00:01:24 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ff8688eea57caa57840fef43d615760ba7ce668911891c755024d88ed3e7d8`  
		Last Modified: Tue, 30 Dec 2025 00:01:24 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2cddb674f7050215234bc8be391bca98e2b8d08870fa1d3f4d46b017e1cb39c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caec4de3b585e2c59818c179bff8a44609e5c58a301c70740835e9fc19e0714b`

```dockerfile
```

-	Layers:
	-	`sha256:7e55eee76bcffd1b4113daa63da2b2545d8f22a76ff8fabf8dfe0fcfbcf62e79`  
		Last Modified: Tue, 30 Dec 2025 02:08:14 GMT  
		Size: 4.1 MB (4075272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6521059055acdbe9eb6d741b62ff7e9c9d935dd808f3f6a5f29606ff245f7f43`  
		Last Modified: Tue, 30 Dec 2025 02:08:15 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:16b167b5084868ee4438b040d0e853f0983d1dbe370ecd6afc27b0cab1dd553e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544fa085ce3c72e8d91d7823155b0f299415f72adca3cf4159d4e6c780d05d8d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:01:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:01:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:01:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9572c2275cab572abb5887a4d4189ac1d16a900d802307d56f56d04e6ffc7dec`  
		Last Modified: Tue, 30 Dec 2025 00:01:39 GMT  
		Size: 11.3 MB (11253500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344bd7ca3dca19b442c7c96748dd10cee6b42422065e4b78e1c1e0d0c3eb1fc9`  
		Last Modified: Tue, 30 Dec 2025 00:01:38 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70da94820edfa3b121d63698dbf16aa22dd1b90df6bf21411a9dee8ad9e8c199`  
		Last Modified: Tue, 30 Dec 2025 00:01:38 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4555cee033ceaef40afc778e219498e0cbeaf00aa94df88e40ddf1ebc1ce47`  
		Last Modified: Tue, 30 Dec 2025 00:01:38 GMT  
		Size: 93.5 KB (93530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62a2808c0e83420cf223b94befb2e48d1db29559e1a334c89e015733151897e`  
		Last Modified: Tue, 30 Dec 2025 00:01:38 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8ca76a295a3584e1bba1a47d6224e58411fa0045cddfc42c11a2ed387162ff3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401e8b75ebeac47608271b90d088a56c0313183c4d4f84a5ca3293b0c2e19e49`

```dockerfile
```

-	Layers:
	-	`sha256:2aa7cfce6cff107c6e71a07fa4f85fc560fdfc5532c1e67d4016539deacdd99a`  
		Last Modified: Tue, 30 Dec 2025 02:08:20 GMT  
		Size: 4.1 MB (4075514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20b0b3436e8d94f4f58c2bc0b789bbb969fae42b5437cbd6c8860d487d798f33`  
		Last Modified: Tue, 30 Dec 2025 02:08:21 GMT  
		Size: 16.1 KB (16131 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:9a32e796340a46ccaa79995c6356a8ee8907a0384617d3ca1d62bc7abbc519dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a7cf4fb69ad656303e0cbb42407cb0e78b11763a461bc4b707dc5d83aa0cf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:15:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:15 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfea0d8e4e48d2ed88857fa647a44ad0812430118aaf423ca71393709f1e738`  
		Last Modified: Mon, 08 Dec 2025 23:15:33 GMT  
		Size: 11.7 MB (11690094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9eb22c650699e169eb028f46c41221994a2556ec3bd4be0d2559aeb1d5fe1b`  
		Last Modified: Mon, 08 Dec 2025 23:15:32 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b82668d4fe89353db6e2d50cb43e936051f8ebc7377922145ef6e183043053d`  
		Last Modified: Mon, 08 Dec 2025 23:15:32 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c5501984a937c9a1905dfe66b2ebd4e0cbd9fe1232880dc1e283b1a8d0a14b`  
		Last Modified: Mon, 08 Dec 2025 23:15:32 GMT  
		Size: 93.4 KB (93374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61f029ba16f9cf3b81359ae9885b6449a1378e50b4f21041be43a2208e75f04`  
		Last Modified: Mon, 08 Dec 2025 23:15:32 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8d24dd4a17c911e8f6b1d6df7fdd2a5884a56ddacd395ba9fe61b20d9b737d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914ea91f455df92d0644bf85fad635d2b920cfbc7b9cbd368e7c5abbbd7539f9`

```dockerfile
```

-	Layers:
	-	`sha256:ea5f6d542df3b6cf1041a0765816de213980e146ac726111d73f5413e827ca07`  
		Last Modified: Tue, 09 Dec 2025 02:07:46 GMT  
		Size: 4.1 MB (4073240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83b94969bb82f97c4f66bf4ec317e7ef048252032a76a327ede5483777308620`  
		Last Modified: Tue, 09 Dec 2025 02:07:47 GMT  
		Size: 16.0 KB (15961 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:95ecbfbba64f882290ff4041ece04640458dc215ea8ff57d98776a94fd938281
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
$ docker pull neurodebian@sha256:afc13bda090ecaf3ac1b2accfc3afec40dcd0f9ad3fe289f5460eae326c5aa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73432b2122fde979a52ac102b60e572c641f4abd553df8e3d3130625749eb7c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:59:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:59:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:59:27 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 29 Dec 2025 23:59:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6feac15215b04fe6ff00ecee76eec1a10d916db11898f37c6ac0f23b40bf85be`  
		Last Modified: Mon, 29 Dec 2025 23:59:47 GMT  
		Size: 11.1 MB (11105092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe720542ed12f17dabcec33ece34d4425ef6060a620d8f6076cd5360bad8491`  
		Last Modified: Mon, 29 Dec 2025 23:59:45 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dce16499536d9b4a500d06ddeacce19bfff247e2d69c5e1aac845a43cf0462`  
		Last Modified: Mon, 29 Dec 2025 23:59:45 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e6fcbf8e20ee654c131fc8c2c917a84faca170627a725144121717c2e29e43`  
		Last Modified: Mon, 29 Dec 2025 23:59:45 GMT  
		Size: 101.4 KB (101395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cdc2f9b9381ab35b4af1725acc1b2ab5e85c6a8b51c0743c28e8ebfb35d14ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac52ebb6f9269638c430bb740475207451ef51c58e47db307c2df6b26cf5119`

```dockerfile
```

-	Layers:
	-	`sha256:ee7697754ee9aa54b472c49c0551b5f949e4095b5060d42305ec024331b4db7a`  
		Last Modified: Tue, 30 Dec 2025 02:08:22 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44bd6525a484172404af1b711d90625f9803ed33211001ea7c4c432aff8c1271`  
		Last Modified: Tue, 30 Dec 2025 02:08:22 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a4b2366a3c691cb717ef4ff43ae49d946de113f2d8007f327ac12bb51dbccc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0e3fc101445c459501393620d0073207fa2601be082724778db9d4e557aba0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:16:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:16:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:16:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:16:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3200e0d5217bd158af22bf7ef8ed42551b408a2592587e3f13308a82d31e96bb`  
		Last Modified: Mon, 08 Dec 2025 23:16:26 GMT  
		Size: 11.1 MB (11106123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c04fc2ea5f436bb3af900d47add9f023d50b01ab6d46415ee6905fdf161698d`  
		Last Modified: Mon, 08 Dec 2025 23:16:25 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50327f1c81ee220fcd0a86f8a92dba7686da3b498d6854d43c0adee0f4e7829b`  
		Last Modified: Mon, 08 Dec 2025 23:16:25 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15161a0070f04ad6a72ee2dbb340ca37f9ee72a97f08db1080e7f4a2d90e620d`  
		Last Modified: Mon, 08 Dec 2025 23:16:25 GMT  
		Size: 101.1 KB (101140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e13c5a1ea24826dd934a8b3455f5111d94040c18e27fbb1c75b053be81694290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04453afce7d3d3215429a6ca2c9c0926d2a85e1b4042694534a4e731b76bb16`

```dockerfile
```

-	Layers:
	-	`sha256:d0879d24ea82e9a10230652eb00867d502c71d0c868c6df7864e3b0e7a1a3eb8`  
		Last Modified: Tue, 09 Dec 2025 05:07:46 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9524159d356d35efeb1eecd138dbffde6b122798fabcc42a773925344e9a3f8`  
		Last Modified: Tue, 09 Dec 2025 05:07:47 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:741d48dae2883591009a5600aea62044c2b47fafc5a28f8df720255339da78bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b054b6156dcfd6ad85f044d2a3d936e2cbeb800ff1f62b1e0c51ee9f56d58a70`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:14:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:14:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:14:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:14:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20381eeb836e270b6cf9dd675babbdf823eb79206c868ce7f8ae8aa6250aa68b`  
		Last Modified: Mon, 08 Dec 2025 22:16:45 GMT  
		Size: 54.7 MB (54699532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fae04539f9499024dbfb30db944df534e7fc1d3089e4943a312e38b4a69fd`  
		Last Modified: Mon, 08 Dec 2025 23:15:12 GMT  
		Size: 11.5 MB (11500429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bde3f6ae3038114a37d889b3c291f70c9e4c6d29295cd9bb68bfb568819f3a`  
		Last Modified: Mon, 08 Dec 2025 23:15:11 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c97b5d3dc87e66b87ca24b0f615f0c6ac445df09a319a951094c0c2ea7221b`  
		Last Modified: Mon, 08 Dec 2025 23:15:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b8827f711faca9a8f1e805dab780dc41cff831485a86f3394c60a2c253ea30`  
		Last Modified: Mon, 08 Dec 2025 23:15:11 GMT  
		Size: 101.2 KB (101246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9fbf1005be46d348fd4575f1b72606610689969d6dba2495e7b642ea7ebffe47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b4bb56f70f428aed7e4e5c892de59dc3151f40220d177495002677e361c169`

```dockerfile
```

-	Layers:
	-	`sha256:ce48fb6b0ec255fb67170a8f79e4a5e0e7621d0b672e562ab0f6c0591a2f47d6`  
		Last Modified: Tue, 09 Dec 2025 02:08:02 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe103c3872070089f9b9327238a702c20145a8365c9719ec3027749e37d1b6a`  
		Last Modified: Tue, 09 Dec 2025 02:08:03 GMT  
		Size: 13.9 KB (13936 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:e3d76255c0105123c24c4f1777801836a8f765b8f223611b4671a46af438b488
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
$ docker pull neurodebian@sha256:6499766008cc053ec0b912ab66f23ce159e90bc18dabcb983bea84e09bfb4d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2604b1395cdb6aeee4e5890085b8fb3d04329bba19f625732b834e8729482f69`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:00:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:00:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:00:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da2c912bbc072214889aeea785d93b1fd8aa6ac61f78f85b74b1a2c7bfcc997`  
		Last Modified: Tue, 30 Dec 2025 00:00:33 GMT  
		Size: 11.1 MB (11105115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ff0255c58351a2bdba00dd012ac2e5cade79fbaf9d1df40944d6c30c6a501e`  
		Last Modified: Tue, 30 Dec 2025 00:00:31 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435192cbd31c304b5fbac1df842572bae61d4fd458e10413c8141aa34964cb6d`  
		Last Modified: Tue, 30 Dec 2025 00:00:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29481e40463e9c197f580cd03ddc64c30c46fa1ba531cf4869bebd8d7d0200b6`  
		Last Modified: Tue, 30 Dec 2025 00:00:31 GMT  
		Size: 101.4 KB (101396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0121127037c15088a06f5d4cc6665309b3f83687431cc5142ec69c3c16e9318a`  
		Last Modified: Tue, 30 Dec 2025 00:00:31 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f83b90058f681f5053a1593fc0a12f4856716795661306bfbc724002d56aa874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46354a8d2d79693e43d1445e84737548a1c54070368dac19159b6f8a606c3a57`

```dockerfile
```

-	Layers:
	-	`sha256:d6ca80cab20a5068344a3e2cc4f3a9d28ce32bb29b29ae87e3fa44e15d05fa59`  
		Last Modified: Tue, 30 Dec 2025 02:08:32 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e34a7b7174f53501b30b764d19c594a3452293501cb17a2c945c2de3051d4852`  
		Last Modified: Tue, 30 Dec 2025 02:08:33 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:539dd8660e2085bb168825edb74d4ed15382a70e2c498682da2b9efc8749db51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282bd03ed2f4cb666de301ace1692498c449a676a3e2c09c050d43280b7a47d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:00:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:00:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:00:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4150bee3f59a90f4911382dc6222dd13cc4f90ea24737fa822fd838c5c900b89`  
		Last Modified: Tue, 30 Dec 2025 00:00:52 GMT  
		Size: 11.1 MB (11106058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328a05363145dda7feeed31d22415cd120633e3b81ff7951c64a84ae766a7911`  
		Last Modified: Tue, 30 Dec 2025 00:00:51 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1befde1ef3c3cb2133d055bf2666550d14799515f1d229a8dd35bb2678a0198`  
		Last Modified: Tue, 30 Dec 2025 00:00:51 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8894397cad319a6153574c231eca833c7decca9aad1ff7f76c04e4aa734ce365`  
		Last Modified: Tue, 30 Dec 2025 00:00:51 GMT  
		Size: 101.1 KB (101115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f061a44f9b67b704e57c1c4022f0f59aa038e70373c788ac3694c4b6a50689`  
		Last Modified: Tue, 30 Dec 2025 00:00:51 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9689afe7068ec77cd86564703ac070ca70b7920e316aadcbfed21cf14199e90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc0372e30b2dc423cbce0c822c721a46631073ab465a819eaad98fcc76bb19a`

```dockerfile
```

-	Layers:
	-	`sha256:48e4ce2a888502ee2eb216d44b41e5d56c20fc09581f399712611354271eb53d`  
		Last Modified: Tue, 30 Dec 2025 02:08:37 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e192cf3fb3f567c3f4bffa267e219ff497105ed5a570a9011162858883b82d5`  
		Last Modified: Tue, 30 Dec 2025 02:08:38 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b412ef6ea141b35d048e28eeff4fe19392ec52c81625d8a03f10763bc8381a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998a4ceda4a3ee98bc31128d7e959463d63b1bab6339855f76e607d7b810ac60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:15:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:20381eeb836e270b6cf9dd675babbdf823eb79206c868ce7f8ae8aa6250aa68b`  
		Last Modified: Mon, 08 Dec 2025 22:16:45 GMT  
		Size: 54.7 MB (54699532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c030937cbbfb99adaf86783a860ed5d3cebcd1379d49c4e97853f3c1275263`  
		Last Modified: Mon, 08 Dec 2025 23:15:28 GMT  
		Size: 11.5 MB (11500413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805690f6ca6c5f3b783b7101716247b76abb6269b102b76142bbdd7f30da9a05`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46f35f9e3e3ad94601a7da1c16987fdc97b474cc01eeff25d712e4981dcbadb`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6664cf221203a95a3f5caa3fcee991c45d0adbfec5746b52600794de16127980`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 101.3 KB (101264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc295741e813d317bb24d92ab162ac433d018b9c312da7351fd0fe4910911596`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73f0a417e354d3934993bd9981e3ff5ab5cdab551b690bd1a8b8cc43a5d7eecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c9c13fb82aa274bc9b1f02e17f76cbefb5e69a02c99312ab68bbc3d1962f1e`

```dockerfile
```

-	Layers:
	-	`sha256:d8676d57bfa7ce1d1ca06c7ce2221855bc19fc07d1a4c49ce60f6d934b9e718c`  
		Last Modified: Tue, 09 Dec 2025 02:08:06 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:481798e95db057aa84ef00b287c2a69c2566950f493f9240abfff8a2e6a73c5d`  
		Last Modified: Tue, 09 Dec 2025 02:08:07 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:150bf0efbc0cf3e71c4e917e1365f4ce12f068b52f78b4b3ad7edf35b51bac84
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
$ docker pull neurodebian@sha256:2302018712146863aeb4690550a5b76df8b7df13e0d802be71a0c3c38149a135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60548458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec708323e8e211beffa0a80ae7bba5f384b434ce88123b60733a0d195d8aa7b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:03:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e1869079ab5cc3b00301445717c112f3ddb9424b5d7b2a41713bc70d9482ee85`  
		Last Modified: Mon, 29 Dec 2025 22:28:05 GMT  
		Size: 48.8 MB (48830058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4e5a600b42af7e7249a38577cc844cd06b82d1f22fca446507bc4d97304e37`  
		Last Modified: Tue, 30 Dec 2025 00:03:22 GMT  
		Size: 11.6 MB (11625089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24bf27c0bb0ed449a81b5fa6ada1e384d2e5ab45f9922c801299bb91e5dab52`  
		Last Modified: Tue, 30 Dec 2025 00:03:21 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e586810401da99692985a5491071e4faf2cbeba2c773b81a6c74603b1ef3e30d`  
		Last Modified: Tue, 30 Dec 2025 00:03:21 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fe4dcbbac465ccc98a30e7771909d8458a9f36baedec710f84603defa1dcba`  
		Last Modified: Tue, 30 Dec 2025 00:03:21 GMT  
		Size: 90.4 KB (90408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f519e2e0c5660ae6c3b23a247879ae3da45a30261b90d6a9e855c44ab69afa65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf20aec7ddfa5fede50a25e0ed3e08a788b1e122a1f045868785e829dd18b35`

```dockerfile
```

-	Layers:
	-	`sha256:5a0737d7a8f7467ed51fc907ab110086336b2a8248f44a46f1cf3e860d5b3651`  
		Last Modified: Tue, 30 Dec 2025 02:08:39 GMT  
		Size: 3.6 MB (3592069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba3fc4fd325b4e974cb70b4248875c0c5cd5f6d01a0aa49b27aeda7b7ea9fa01`  
		Last Modified: Tue, 30 Dec 2025 02:08:40 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7cb33f542c2b2416b8360d80bf270f017394a8248f5547bd25b910d362907e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60209869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d523ae26b69c0e69f59c722a906ef5e749bc1b0072a349d4b47e66752980ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:03:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6ed83950a3f675536ad8634cde3cf4c241d5faea11ae3192ff5909f826256f2`  
		Last Modified: Mon, 29 Dec 2025 22:27:42 GMT  
		Size: 48.8 MB (48831993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2c77bf93408787969c8c3f6ff7213d99a7e697e69620cca332ac58446528bf`  
		Last Modified: Tue, 30 Dec 2025 00:03:43 GMT  
		Size: 11.3 MB (11283854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffa76c7561f8431bcf2d9458d0b5122c83188cb1a0af66ba63739670f119ad8`  
		Last Modified: Tue, 30 Dec 2025 00:03:42 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f90c9596551e2e36dca68165bdffea5d2e3885d8c814d8ec39b6430e18051a`  
		Last Modified: Tue, 30 Dec 2025 00:03:42 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8891a2507db7acd33db08d268da2d5cfe43517b88b3c5e4d64e7746d884a2120`  
		Last Modified: Tue, 30 Dec 2025 00:03:42 GMT  
		Size: 91.1 KB (91115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:677e960c2528d3f9423b79824ad6bd592c57b82a587b2e13c10fe717f1ced255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec4e91d533b3762f44007169dfd298ae15029e6c51d8049c5674a2410e24c89`

```dockerfile
```

-	Layers:
	-	`sha256:bbd84bbc74533abe8bf8740104e0d06c186ae3cff091c08be59b46b536a3e3ec`  
		Last Modified: Tue, 30 Dec 2025 02:08:44 GMT  
		Size: 3.6 MB (3592945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c39f6fcbfd1dc80794642dc576dfd48079c6de50372df3ff1ac44eef02c17cc3`  
		Last Modified: Tue, 30 Dec 2025 02:08:45 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:ed17bf7744b05e17a7f5a07512b499f7853d80ca2634d1b3091f724ec12704c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61720534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4a7e442293c27bab1441b206d263cbbfda95db72021a246e34633483d87277`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:15:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a5d3e60f8c1eac1ccb5aac1ab5735dd586fe448287d7c7d1d7f59a687bd9b9b1`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 49.9 MB (49874580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cee8645950fcb2cac8e786ded94810e24e89ade2e4f5cc4099b37f01809d5`  
		Last Modified: Mon, 08 Dec 2025 23:16:12 GMT  
		Size: 11.8 MB (11752135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b16c5bf742f0f200c67b5041f2cf3e97f655ef571b984e5b607960988763c66`  
		Last Modified: Mon, 08 Dec 2025 23:16:07 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec3e51522085c44202103858e4b4bc149caf3ac8be3196028e5327cc90b577e`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a58fde9f6b48ef00bb0ab006f68aaa17d9c356d37254ac44110fe0f3dadc452`  
		Last Modified: Mon, 08 Dec 2025 23:16:07 GMT  
		Size: 90.9 KB (90913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ade3efb3c881d0f2aebde1a8dfd977b7cec6e59eadd851d32e96d5442cdd4c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac31d7558920461a59e82693d3c70a6a3ec175dbf6017f477e182186218a2197`

```dockerfile
```

-	Layers:
	-	`sha256:16859a3d98038419a32fbc0eb7b4a65dfc2adab665a924d9bb3ff4e6dfb608c8`  
		Last Modified: Tue, 09 Dec 2025 02:08:11 GMT  
		Size: 3.6 MB (3583531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104b1ce751d490df8412608415756e6158e3a99cfc6d9d66a088c869af428201`  
		Last Modified: Tue, 09 Dec 2025 02:08:12 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:d635200f4e3f15d9c13d3bc4c8a68ef05d2a992afddd547ca59eb2450c05994d
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
$ docker pull neurodebian@sha256:56ea8c0eba2929e786fc26a4b61337bbcd45c6602c0e633949dd1a233d86d173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60548879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa82304520ea72936c1f1be9740090de2d22dd3eeb4175e3f9f0d6287e2765c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:03:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e1869079ab5cc3b00301445717c112f3ddb9424b5d7b2a41713bc70d9482ee85`  
		Last Modified: Mon, 29 Dec 2025 22:28:05 GMT  
		Size: 48.8 MB (48830058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaf0ac99f659bb6461220191a78a66c276d9816bf54d5b7182576ada79daa7`  
		Last Modified: Tue, 30 Dec 2025 00:03:39 GMT  
		Size: 11.6 MB (11625073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f62653a9582b12b399b318130654cb00f1e7633a7dee96cbd1cbdb492a173b`  
		Last Modified: Tue, 30 Dec 2025 00:03:38 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fbae46621e155e25e4836a84dd7ca71e6e4f31f86ddb9924239ceefb1fcc0c`  
		Last Modified: Tue, 30 Dec 2025 00:05:14 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5677abe2abd0ea16c83243a95dfa4d82828123fe243948ebecaf73a1a2137`  
		Last Modified: Tue, 30 Dec 2025 00:03:38 GMT  
		Size: 90.4 KB (90394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6c1cf3b8f91aa7794755a003db44fc5c2f67b48acf65c7a0b9c8a7e7b4fa93`  
		Last Modified: Tue, 30 Dec 2025 00:03:38 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0d38eca5c86573632d19313a058b0ecbc0e568e302f0426ebe28033b93e719d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e043b1451aeae3d0b9327ad512efe6438e8f08fadd4e6cc75b4d8880a188dca`

```dockerfile
```

-	Layers:
	-	`sha256:b9e68dda9c60e65ccae7d20c80d1f74a3829b61170430a31144926ffacba2427`  
		Last Modified: Tue, 30 Dec 2025 02:08:48 GMT  
		Size: 3.6 MB (3592105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd14da38b318103abc72d4da22409c4d400f464e564ab525e1d80436718605ba`  
		Last Modified: Tue, 30 Dec 2025 02:08:49 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e3f88edb3744a1481d41725b392334f62ffe29db0291e3c93b61dd2df66c9a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60210263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ec30ac7f439988b4368dfd9dfa11d36be4411c8128c0f32ec915cb65d02c20`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:04:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:11 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d6ed83950a3f675536ad8634cde3cf4c241d5faea11ae3192ff5909f826256f2`  
		Last Modified: Mon, 29 Dec 2025 22:27:42 GMT  
		Size: 48.8 MB (48831993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278e9ed2ac59aa8e052b8c075a014ec12973527aa13dcfc47386b5fc849d09dc`  
		Last Modified: Tue, 30 Dec 2025 00:04:30 GMT  
		Size: 11.3 MB (11283833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e5e80e4b2f6c88528a91fe91f2b355ed86bbfb9e96088827682cf0dd2fe3f0`  
		Last Modified: Tue, 30 Dec 2025 00:04:29 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28c95221e4cea56d32ff27ac8a53bb48fe70456cc900191a16be091be283769`  
		Last Modified: Tue, 30 Dec 2025 00:04:29 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f473be47c5749d5d961e89ec52f21d33af161fbde6fa39bf270b3682b3906d`  
		Last Modified: Tue, 30 Dec 2025 00:04:29 GMT  
		Size: 91.1 KB (91085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ec3638ca167076fc05df171bfda204d00eb1f3ea1d007ef3b85db710e0582d`  
		Last Modified: Tue, 30 Dec 2025 00:04:29 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef6bb4894931f521530b7db4fd13f66c4226fe5bf1425c4d024c2f567edd946f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3609079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0b389ba0fe727bd64ef60b5007f1271d09508c42e0364b7dc035f445ca4e7b`

```dockerfile
```

-	Layers:
	-	`sha256:5f14d023f73b435b23489a0d89f2a5bad5a57d6efc8da662e4abbb50418a0fa2`  
		Last Modified: Tue, 30 Dec 2025 02:08:54 GMT  
		Size: 3.6 MB (3592981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad81100e36b669c78cf4ab2bf837b7bcafd554fe4f55a126cc3bf816defae711`  
		Last Modified: Tue, 30 Dec 2025 02:08:54 GMT  
		Size: 16.1 KB (16098 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:310986ea6782ef724d41e8f67240e005c3c0fbfe36d6e9779c703452978b2061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61721053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75690de1cdcfaaa39c9be4ef65273d76e990e6fab068d68efa4f94bb0ba85995`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:15:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a5d3e60f8c1eac1ccb5aac1ab5735dd586fe448287d7c7d1d7f59a687bd9b9b1`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 49.9 MB (49874580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae4cf933beea0d74190c5108f5592160b361455d8d0aca4852d56b28f1816ec`  
		Last Modified: Mon, 08 Dec 2025 23:16:08 GMT  
		Size: 11.8 MB (11752199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69195fca673288bc2be238012fb534a989339e533d6a8f67d5d4ee43d28117d5`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3571e3ea3babea5298321571e0ecff849e4104964f3e97b88921df3717d1aa`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d10761b27d78d3cab80c345eade32d07c1317137a5ae92a9998e523977655ab`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 90.9 KB (90921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6e1907cacf4ae722d1b080f12e49ca31d368e482e1835e219185719e6c1090`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3638e2924b6b21634a03c10613ef941641ea6b6d835763bb584846dbb4776e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9d1adf120a2f484750d4044e9113b7a12ad4287c721ee006427934f80f2ef3`

```dockerfile
```

-	Layers:
	-	`sha256:536b0ea1c809e7d334f738198e24640d9fdcc2284f7ea5394d9ac75a89aa1e12`  
		Last Modified: Tue, 09 Dec 2025 02:08:21 GMT  
		Size: 3.6 MB (3583567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1afa97a40023bd48ea41bef0a9c7435b97b608551dcbf15388b584d2047e4326`  
		Last Modified: Tue, 09 Dec 2025 02:08:22 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:0e98bbc3daae66df44ae11a5588f2309b4d0b0a3d5759a236557a26319c2c5b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:e6772d070a574f00e1ad07efb0f799b7e9d9020fccf9887c7f6378c50bdbe816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d6aeb77e4a5a773edcad5fc10b5e08d8f387161a9b7b5d93e1cb1aac4e3735`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3881e591a9050bd6250b7975f2a62d69ce9d4bc181a569e43d583973bfffafd6`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 3.6 MB (3625726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7763c1732252c316b49e1a5ebe3d01e0ad636198993b3e20e7267f9fe62d4283`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59987cb0b364dad0627b12e7ef72104aea08b23fff39930f94dac5b79cf2585`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91714d8e9de2a6eab65bf534a21daeac5f710d6f823714736754481479f25eb`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 111.3 KB (111253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74faf561f221e4ff0722a9a6a5469d286311b0d29d710a50c1c2f2d408089335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5093bdb0233d5e701687d2c9157af64b57724e81b512be660289bb7a4c8f7216`

```dockerfile
```

-	Layers:
	-	`sha256:288a50939bde1611937533ae039c8544b98d95d75331e8bde2456927a7ddea17`  
		Last Modified: Fri, 14 Nov 2025 02:07:40 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941444796f9904d69ff28378466addce903b01de5df5c0c291ea8d117c6aff74`  
		Last Modified: Fri, 14 Nov 2025 02:07:41 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:09ed49f28825e5330d749e8aa583e2f0c2c88ace7f935f79fd1b4ee7cfd6502a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31094789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170be1c0c9e62fba389535f45096cb097ffcd73e82e10f8e5f2bbeb7101e7716`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:30:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:30:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:30:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:30:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4fc061e7db4abc03b992399d4d51a6e96a401904e29c8c7cfff6c2b0ef4cbc`  
		Last Modified: Thu, 13 Nov 2025 23:31:03 GMT  
		Size: 3.6 MB (3598146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e356cef2bd87e42a124fc4d5e82057772ca5cf202c6c194f6884f04283430a`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7f921b9372d265e8d3805815b0e98436f5f4b92fc0dae86070b7f4f269f992`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562a8628e6dc417f84896302f26a4b6c43f921ca7ce9b73b785936f7e5d51be2`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 110.6 KB (110588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4d3a9691d374823b1b504cf09f6f82049355ef10aa41d07d3be46ed00124eda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb368a6d54f82c2cad7c303b49a01491c62b68e3a47065952793b1df828ae`

```dockerfile
```

-	Layers:
	-	`sha256:c8a0004225abd4f8c618461be1e72c1192172f7ccfd4fa7f0839dbdc35d24f43`  
		Last Modified: Fri, 14 Nov 2025 02:07:45 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200a3136b60277a7c0dac564342f17944ff690ca89305553d8bd0bcd74108f3a`  
		Last Modified: Fri, 14 Nov 2025 02:07:46 GMT  
		Size: 14.1 KB (14056 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:120b8715dd3a26a2af4049512591dcbb112d36e4accff9d7fded93e27ce47062
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ef9dcfb5426525d36ca828760110823e06e065cca0c4ac0682d0a506e9cf12e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33276245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abbe750921d6da2c2bf91fa655875aa86d26da7d2c93cd08dc4d8b4f91445af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3881e591a9050bd6250b7975f2a62d69ce9d4bc181a569e43d583973bfffafd6`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 3.6 MB (3625726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7763c1732252c316b49e1a5ebe3d01e0ad636198993b3e20e7267f9fe62d4283`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59987cb0b364dad0627b12e7ef72104aea08b23fff39930f94dac5b79cf2585`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91714d8e9de2a6eab65bf534a21daeac5f710d6f823714736754481479f25eb`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 111.3 KB (111253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87663c843a43743cb4efbfd154e030c6591b4085d0c1d047a156158b9c47142a`  
		Last Modified: Thu, 13 Nov 2025 23:31:58 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8b9b5e291adc948bf145496030828a9a408c3399355380347b0ff72c16e2a880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970a1d784b637f4a06999658bbd7cfd5f71517ef14610d1888be4fc2d5614399`

```dockerfile
```

-	Layers:
	-	`sha256:19ad39194fba9b75b47c96c260e5431b390f0c1f40747e8857c995d53dd228f0`  
		Last Modified: Fri, 14 Nov 2025 02:07:48 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd46be2a48617b0b0891f5fe27958f8e2350a649da215ce9a4995e5a9a62d43d`  
		Last Modified: Fri, 14 Nov 2025 02:07:48 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8c05f54ab64c544f5b1833f0d31ef94804c914c6debd693acfce0dc0320660cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31095110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2b987bf931381f750375f7be732736b38d67dd928c373fb3ac7f7703364fd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608dccde847e272476e52044e62fdf40902fdf981eba3f9e853d9bb36c3ebdf5`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 3.6 MB (3598157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff367c25857e7c190e4c69803b560c6e428a2f6fdcdef7291ed9c54595fd3a7`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d785e7ece3388bd939c0607e15ed02803f8e48b590bbf43d7b628f2275ed86`  
		Last Modified: Thu, 13 Nov 2025 23:31:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411f09f71214f6303934a66000e111fee3918961b6f6726ed9b784feeceb7fcf`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 110.6 KB (110611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa2aa73e9807dfaff0d65e73fea59b7275dac6754311bac380e78c75cf4c922`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f02cab47a327aef8e9eea19cc7a8da708ad76b7fd1cee2ccdc47f302f2cade08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5d2870c8ff27e82579456117c17077c9ecc56cf9812adeb91b20dcd8fdb489`

```dockerfile
```

-	Layers:
	-	`sha256:196e2a812f54eccdc16bfcfe68a337ef2397641ccf3672d5f6846a2c19b4a34d`  
		Last Modified: Fri, 14 Nov 2025 02:07:52 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be4dac85cb072f2caede51d4767494f8e063e10991e49a2febf5e030defd53e2`  
		Last Modified: Fri, 14 Nov 2025 02:07:53 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:e0b772fb6c8cbf95b4bbc89d59fce54bd4612bea788c25876003179d85a81dc2
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
$ docker pull neurodebian@sha256:11704eb3e9e87e0bfc0474ec7993332f1a5446fd8fcfb93d5bfa76ddf865487a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59672470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfbefed7e757187bdc0ba33ca6e231ba0ab03e1d8c01c26ec51bffb858b7f8b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:01:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:01:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:01:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170e174478fb49afad823cff539b37cc66f46900a7285d0980c69545228ad17`  
		Last Modified: Tue, 30 Dec 2025 00:01:57 GMT  
		Size: 10.3 MB (10289740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98cfd6b6685e00247a8830717622cc76428a34a65ea509838b1ef1cf5f05c74`  
		Last Modified: Tue, 30 Dec 2025 00:01:56 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c93be1b43a47437859927119984568576e4e7035c09a3328ef782132ad5794`  
		Last Modified: Tue, 30 Dec 2025 00:01:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3130c56d9674187b01ccfa85c055fa9f25023403e80cc08d3bd3fedb46556a5e`  
		Last Modified: Tue, 30 Dec 2025 00:01:56 GMT  
		Size: 90.2 KB (90240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1fb327732ae3459a5ace9ae68da17e6b718a91b6edec2e4ba30e8a6c1ce4cc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dafd6febb344bc094cee781197ce68c717521a93152c82a6b3faef2618045e4`

```dockerfile
```

-	Layers:
	-	`sha256:a4c38d6616572e011521486de1ca5c77b753c05e8ac2873b363b81ebd8663c8b`  
		Last Modified: Tue, 30 Dec 2025 02:08:59 GMT  
		Size: 3.6 MB (3613029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e815c9c1e880979ed5797e8604eda18f89cdbc2a0f33a15aa08c9c99c1babfe2`  
		Last Modified: Tue, 30 Dec 2025 02:08:59 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f08af078412593f5e90c7ccc438b36a60853c367d5b1c02977191e59b42e2140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc02347a607123200510623e11328eccf357ded43e2b4c688cf6f3cbd87d6cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:02:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:02:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809d9a2a116ddb1b5044a05d97a74f3b666af6ebf3396b8bd1959b09b2c1dd97`  
		Last Modified: Tue, 30 Dec 2025 00:02:25 GMT  
		Size: 10.1 MB (10073354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43bf434a486a4ffeb412351889920cd853dafb22023f8b56041c1f5d9551def`  
		Last Modified: Tue, 30 Dec 2025 00:02:23 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fc09b5259d60baa90e66794a8eee4353a12a09741ddf610bc593a7d1a33885`  
		Last Modified: Tue, 30 Dec 2025 00:02:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d0d5e7c0fe7290044e8a33d358ea3fb2637f4a077ae7d449ac0eda02e54e27`  
		Last Modified: Tue, 30 Dec 2025 00:02:23 GMT  
		Size: 90.9 KB (90861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f741d89d851cb0175bc345ebf91d0267a3fd846824aff01df647a8423163d3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa99d1b3e6f5e16c3a14b8a2671503fc5c6d885230e3d8d99a1e1783b14e6c5a`

```dockerfile
```

-	Layers:
	-	`sha256:3e2489caeeb90f29d36cf18405d9c354b196ce6768875a219a8c2483595e7b82`  
		Last Modified: Tue, 30 Dec 2025 02:09:03 GMT  
		Size: 3.6 MB (3614556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6028461904b5f9e69fd501748e03c048131c821c768f588bfb954e678cb0680`  
		Last Modified: Tue, 30 Dec 2025 02:09:04 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:c8dc1f5965291d82532beb930b4b8dd9d2857dcffb348f41946ce7525f9d1868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4224f54fb533cad2f8b9b30d2e785eb1fd843e4fd63e905343da0c070c075d03`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:15:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e964d190139b1aba3de28d11b605a95f92489da3beb9d80e9099db336eb72530`  
		Last Modified: Mon, 08 Dec 2025 23:15:43 GMT  
		Size: 10.5 MB (10463020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ec584c96f35b189d796255e99284eb2b5a60beac79d3aa5e9e38511057c721`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9b780ecf3cdbfe9614a0f6fb11f3ac440968fc9859f8381cdd325606eb10d5`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e72d44ba44c44786256e5c59963306628e9bc4225d957dc3c3f88b69404871`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 90.6 KB (90608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8feb71ee0324566413295afd412d3e8536f97cd4923d4b4e3a66a630eb6b5e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f48fe17c7803c7f0a740da48d64460f0e14b205e6ef00e468dd25f6d417492`

```dockerfile
```

-	Layers:
	-	`sha256:6565d47d0408e99891700b9f73772b468617ffa2decbf66dd47aa2f3825e0c46`  
		Last Modified: Tue, 09 Dec 2025 02:08:59 GMT  
		Size: 3.6 MB (3610978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928694ae3cbda82a9b5864d3bb2e6e8cc4bfd721706dd53996bd42268ab412db`  
		Last Modified: Tue, 09 Dec 2025 02:09:00 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:e21fa53efda88c069dd1c2878a1b2f28855ae3ee762fde42098e7d168170874e
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
$ docker pull neurodebian@sha256:035b7f627535f4f213b8df77e7501d898cb8535b31d3b0ea9ec6190b526c72e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60527446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0620c75bef2ca94f3e2085bef9f7b070219d80eea5f03cb046e443a39f5142`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:04:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36a4985327850927961426bc6fcb1fb8dc1f9b5e7f69f8061c7daf2f4aee58a7`  
		Last Modified: Mon, 29 Dec 2025 22:29:41 GMT  
		Size: 48.8 MB (48821118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2afb24b11b414a91690e2de9e1bbf94e8ef9c750303e10a1f474612a1608bc`  
		Last Modified: Tue, 30 Dec 2025 00:04:23 GMT  
		Size: 11.6 MB (11613260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f117d692e9d33c678c15a431856f5a53a13f3a6dad3cfb64ccb90d53565b68`  
		Last Modified: Tue, 30 Dec 2025 00:04:22 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fe440ad283dfa1ff5bc20d76a5aa1943e3a0725babf9323e9f7a8952a30b8`  
		Last Modified: Tue, 30 Dec 2025 00:04:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778a5fe0dc6f45c67af4e740f0b16570ab7430e78dec361704c0dba2c7ea76b0`  
		Last Modified: Tue, 30 Dec 2025 00:04:22 GMT  
		Size: 90.2 KB (90165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f63b8514f32c1fa215e0e8aba690d5e7f4a1973d624c81ae66df879b1946506c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8190f725cf92a2460e1c1a62399edd64257b02d78eb697d0b072a2334c250c5a`

```dockerfile
```

-	Layers:
	-	`sha256:d736499878e3cfd7bfcde74cbf7a0c4d6ab9912f74fe399ac8ede60eacd6a960`  
		Last Modified: Tue, 30 Dec 2025 02:09:06 GMT  
		Size: 3.6 MB (3589915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb93f903cb7d91c8b2fa32e73adc52adb5dc551b0c5b78c36b7ac7d1501e204`  
		Last Modified: Tue, 30 Dec 2025 02:09:07 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b0cbcd07d5581034cf518ae998bf872b0fa8fc1dddbc5199ead7b0b2e16ce097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60160061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1a53b3bdb4de5c84e64777050843a0aa26b83af4ef0f1bf919ba80c7fd612e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:04:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e81a19d37d9900498b0ca8a841e2e3fe3dfde06146f7d10d1e71e1df7a8ae8ab`  
		Last Modified: Mon, 29 Dec 2025 22:29:24 GMT  
		Size: 48.8 MB (48801029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f99e5f3335c2ff6d9abb774351bfb55d384d817ade2187270b9fe3558779b90`  
		Last Modified: Tue, 30 Dec 2025 00:04:53 GMT  
		Size: 11.3 MB (11265267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347a2a6ce4512291bdc3028015b54c7df8357a7fdb3630aecd4a3a33d44e4fd`  
		Last Modified: Tue, 30 Dec 2025 00:04:52 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb44e37c3ff6fd90ab92d83969c35acdcfe3f7adaf5820e89aa01d683814c5ba`  
		Last Modified: Tue, 30 Dec 2025 00:04:52 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15704ec8aa9e145af8c6e5e21f510adeeed85f82e7d9a5f45154a9b0bf54f18`  
		Last Modified: Tue, 30 Dec 2025 00:04:52 GMT  
		Size: 90.9 KB (90864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:06ec310696b16f7e4166904a3ae30305fd9b5fd8d88454fcca2fd4971032862f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3604820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8beb211810ee03db5a4aa15f811c77314d39d61a9836ec43ddda805e26c7fed`

```dockerfile
```

-	Layers:
	-	`sha256:c6d26cb601684ef686b4ef4357a1051102513ec62e85fa194fca69df15f5438f`  
		Last Modified: Tue, 30 Dec 2025 02:09:11 GMT  
		Size: 3.6 MB (3590791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4295813137038125b1d76dbc6634cf4378020e2cdb7ad404da9ecb210548650`  
		Last Modified: Tue, 30 Dec 2025 02:09:12 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:8f5cfc00500cc0d446db7aa634f75cf84b12afe95e95ebdb31af23e36dd652c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61813318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574cb528275d8e08c0c2aba8f98ebea411e3d9e83b8666ec032897e9890a4e3b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:15:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:16:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:67f7fae0ea3bb931c627a66604e60b0a242047b0c8f9186d188cf96e0133593f`  
		Last Modified: Mon, 08 Dec 2025 22:16:33 GMT  
		Size: 49.9 MB (49947966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0266c0513022413f6a42ac8de173ef0db6a7fd70a6d1859fdaee0ff7c1f1a52`  
		Last Modified: Mon, 08 Dec 2025 23:16:17 GMT  
		Size: 11.8 MB (11771438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54d5b89513ee9aefb4cbaeb149aac108b65168fa8016ced6820617134e33cc7`  
		Last Modified: Mon, 08 Dec 2025 23:16:16 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44066a3eb12e5a62aeb429ee8e2fa4e039a016510b0053f5b6d5a21937982b57`  
		Last Modified: Mon, 08 Dec 2025 23:16:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469a39499ff4a4700821efc8a4595a0a54ee4dd2c440d4d7d1bd6a635aeb8f41`  
		Last Modified: Mon, 08 Dec 2025 23:16:16 GMT  
		Size: 91.0 KB (91009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:683dbe22bfe3d344489dcd587c30032ec24bcc1eec3ddd9dc64298a5a3b44fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d30d3a82ccd78c8e1f82eefd7dd5e1a1c671e68a0c3acffd7baa9d15c330adc`

```dockerfile
```

-	Layers:
	-	`sha256:61532c3563e04ec54407712519658270da6406a9e32a333a448571a3a74f36e1`  
		Last Modified: Tue, 09 Dec 2025 02:08:41 GMT  
		Size: 3.6 MB (3589161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce849a1ac7c09b2ee06fbd7089981ce600c9dc4944c42e11cbeaf60a93c90dbb`  
		Last Modified: Tue, 09 Dec 2025 02:08:41 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:4c47943431a034a06d6528a4199cece13a394a2b96aeb031b6674e306a5e8e8d
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
$ docker pull neurodebian@sha256:8e836983d8ef8af9b77b72e439f8c371405a985ae951915e508cacdf4a304887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60527842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8bd8e109166c8ab6131500dc2a65312eb0f2e7a0531b090d7e5c49e83624e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:04:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:36a4985327850927961426bc6fcb1fb8dc1f9b5e7f69f8061c7daf2f4aee58a7`  
		Last Modified: Mon, 29 Dec 2025 22:29:41 GMT  
		Size: 48.8 MB (48821118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a76feb401b8397b66d8f4ee4936caf4ce66640e5ad62ce2473a4370b983974e`  
		Last Modified: Tue, 30 Dec 2025 00:04:46 GMT  
		Size: 11.6 MB (11613267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4349a5f502c1a41bee3f9bf35364bcf75672e22eea699cf80c9742688a9bdd9`  
		Last Modified: Tue, 30 Dec 2025 00:04:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1275f6a063430aa6e6996dcdd80dc6350cd45a3c55323e8c72a3d7f93c7ab857`  
		Last Modified: Tue, 30 Dec 2025 00:04:44 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecf663483821f0c91f02e7906d1438595ba40438f653018436cb2c42eead2c0`  
		Last Modified: Tue, 30 Dec 2025 00:04:44 GMT  
		Size: 90.1 KB (90133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01e8ccfe03ffa296f783478d077dbf0dc04351cd9d661d0d11173bdf4d7bbb5`  
		Last Modified: Tue, 30 Dec 2025 00:04:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e2dde03b8446743a564589f52ad69e2183a9252feb374a8e65c51d5759d9b6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9f3512fc510055e8351d926027811d826fe487e04bcbe47540f3aa04f22947`

```dockerfile
```

-	Layers:
	-	`sha256:3bf02161c82deaa0c916d8c52dc679930df16850c8f23833ee058f9e94dd5bba`  
		Last Modified: Tue, 30 Dec 2025 02:09:14 GMT  
		Size: 3.6 MB (3589951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4666962ca4a0e7945f18ef88ea3a1626cacb025b5f89518de52002eede6468f7`  
		Last Modified: Tue, 30 Dec 2025 02:09:17 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a517ce131a941205f708b3d0db016d341984a51a9da4b10a3a4f792a41b64302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60160491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59cd14e3fa38d095e6db623d1c695f978b5d759f00906273db739db2e07ccc0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:04:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:55 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:59 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e81a19d37d9900498b0ca8a841e2e3fe3dfde06146f7d10d1e71e1df7a8ae8ab`  
		Last Modified: Mon, 29 Dec 2025 22:29:24 GMT  
		Size: 48.8 MB (48801029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834c8f50bd273c3b0a7e017c0b2cad1be20ff06b111037ed997e1b7e6c74d504`  
		Last Modified: Tue, 30 Dec 2025 00:05:15 GMT  
		Size: 11.3 MB (11265282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3d5914282d0f6ff41770baa19a5d797df7b98ceee7055fe0306a26b4b0cc90`  
		Last Modified: Tue, 30 Dec 2025 00:05:14 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7c39fcf0f25e352a9f478db51398f77c3977758ef5e7f4651da4740f38b6e5`  
		Last Modified: Tue, 30 Dec 2025 00:05:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac86f94f45a5f89d87e751860014d3c51dafdc0cceb4980f31e30c5154808f95`  
		Last Modified: Tue, 30 Dec 2025 00:05:14 GMT  
		Size: 90.9 KB (90856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4149473e2827caf5858b119dccfd23f16d508c25dadd652c6dc5402c067a013c`  
		Last Modified: Tue, 30 Dec 2025 00:05:20 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1fb1bd97e59cf21d0763d7ec666274764119ad57b35bfa3ae21a888a6b6ab2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b617c4be66c925f9ed0de633f487fd9131079ab60e35c2b1f0e31bc1b0dca1`

```dockerfile
```

-	Layers:
	-	`sha256:f48cef6f3cfd0ca31efc667f4faed7db31163b52a638ba7e96feae0b216d00fe`  
		Last Modified: Tue, 30 Dec 2025 02:09:20 GMT  
		Size: 3.6 MB (3590827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89bee813be1895a2e6cbc85ebbcc9b2756e96af992934777f53b651b4667b93b`  
		Last Modified: Tue, 30 Dec 2025 02:09:21 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:49afcad16d105fd19bae60cd14158c11b083cd49993f77a1b4f650c6ab293be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61813645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23040b5c36dbefc61179d2d7deeda5abfc71fea09f198c632c1abe65282f03b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:16:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:16:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:16:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:16:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:16:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:67f7fae0ea3bb931c627a66604e60b0a242047b0c8f9186d188cf96e0133593f`  
		Last Modified: Mon, 08 Dec 2025 22:16:33 GMT  
		Size: 49.9 MB (49947966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec12c3df770257e87a24e89f178be2debdfa70110f149c64f33fafe3e06b0bb2`  
		Last Modified: Mon, 08 Dec 2025 23:16:29 GMT  
		Size: 11.8 MB (11771378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d9aa372e7ef553d58fcd21aed06e967b22c56495ff93ff4db7ba9cb7dded3a`  
		Last Modified: Mon, 08 Dec 2025 23:16:28 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a6aa5a510c3bbd9a734f2af4a0f01c08b189f9964f11c3f81c91174367bb1`  
		Last Modified: Mon, 08 Dec 2025 23:16:28 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca5f7bb75d5cb357f3cf6974aea0182f5878e2b95b614c8d4f0d1ccd309cd70`  
		Last Modified: Mon, 08 Dec 2025 23:16:28 GMT  
		Size: 91.0 KB (90977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137b22bdee3d72723ee405aadd32bb53c6338c92f8ef80e18f5a70cd443b75dc`  
		Last Modified: Mon, 08 Dec 2025 23:16:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3da97abc8582eb66115af61c24725caeb2eb08ae525671a2c9180458e24c5623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f369991e4501a6c1095ea76a75182086694a3acce7d86fbe1e9e5cf75cf0e27`

```dockerfile
```

-	Layers:
	-	`sha256:807a054d1fbda6da8789823823c4862f08b246f336bc67bc357a9a4fcc45dfdd`  
		Last Modified: Tue, 09 Dec 2025 02:08:48 GMT  
		Size: 3.6 MB (3589197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e54569f675797e675d8e53c2f3cbb7f2e4ed87ed2af17c0cc005af7d6f08535`  
		Last Modified: Tue, 09 Dec 2025 02:08:49 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:95ecbfbba64f882290ff4041ece04640458dc215ea8ff57d98776a94fd938281
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
$ docker pull neurodebian@sha256:afc13bda090ecaf3ac1b2accfc3afec40dcd0f9ad3fe289f5460eae326c5aa48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73432b2122fde979a52ac102b60e572c641f4abd553df8e3d3130625749eb7c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:59:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:59:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:59:27 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 29 Dec 2025 23:59:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6feac15215b04fe6ff00ecee76eec1a10d916db11898f37c6ac0f23b40bf85be`  
		Last Modified: Mon, 29 Dec 2025 23:59:47 GMT  
		Size: 11.1 MB (11105092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe720542ed12f17dabcec33ece34d4425ef6060a620d8f6076cd5360bad8491`  
		Last Modified: Mon, 29 Dec 2025 23:59:45 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dce16499536d9b4a500d06ddeacce19bfff247e2d69c5e1aac845a43cf0462`  
		Last Modified: Mon, 29 Dec 2025 23:59:45 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e6fcbf8e20ee654c131fc8c2c917a84faca170627a725144121717c2e29e43`  
		Last Modified: Mon, 29 Dec 2025 23:59:45 GMT  
		Size: 101.4 KB (101395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cdc2f9b9381ab35b4af1725acc1b2ab5e85c6a8b51c0743c28e8ebfb35d14ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac52ebb6f9269638c430bb740475207451ef51c58e47db307c2df6b26cf5119`

```dockerfile
```

-	Layers:
	-	`sha256:ee7697754ee9aa54b472c49c0551b5f949e4095b5060d42305ec024331b4db7a`  
		Last Modified: Tue, 30 Dec 2025 02:08:22 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44bd6525a484172404af1b711d90625f9803ed33211001ea7c4c432aff8c1271`  
		Last Modified: Tue, 30 Dec 2025 02:08:22 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a4b2366a3c691cb717ef4ff43ae49d946de113f2d8007f327ac12bb51dbccc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0e3fc101445c459501393620d0073207fa2601be082724778db9d4e557aba0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:16:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:16:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:16:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:16:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3200e0d5217bd158af22bf7ef8ed42551b408a2592587e3f13308a82d31e96bb`  
		Last Modified: Mon, 08 Dec 2025 23:16:26 GMT  
		Size: 11.1 MB (11106123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c04fc2ea5f436bb3af900d47add9f023d50b01ab6d46415ee6905fdf161698d`  
		Last Modified: Mon, 08 Dec 2025 23:16:25 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50327f1c81ee220fcd0a86f8a92dba7686da3b498d6854d43c0adee0f4e7829b`  
		Last Modified: Mon, 08 Dec 2025 23:16:25 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15161a0070f04ad6a72ee2dbb340ca37f9ee72a97f08db1080e7f4a2d90e620d`  
		Last Modified: Mon, 08 Dec 2025 23:16:25 GMT  
		Size: 101.1 KB (101140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e13c5a1ea24826dd934a8b3455f5111d94040c18e27fbb1c75b053be81694290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04453afce7d3d3215429a6ca2c9c0926d2a85e1b4042694534a4e731b76bb16`

```dockerfile
```

-	Layers:
	-	`sha256:d0879d24ea82e9a10230652eb00867d502c71d0c868c6df7864e3b0e7a1a3eb8`  
		Last Modified: Tue, 09 Dec 2025 05:07:46 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9524159d356d35efeb1eecd138dbffde6b122798fabcc42a773925344e9a3f8`  
		Last Modified: Tue, 09 Dec 2025 05:07:47 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:741d48dae2883591009a5600aea62044c2b47fafc5a28f8df720255339da78bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b054b6156dcfd6ad85f044d2a3d936e2cbeb800ff1f62b1e0c51ee9f56d58a70`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:14:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:14:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:14:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:14:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20381eeb836e270b6cf9dd675babbdf823eb79206c868ce7f8ae8aa6250aa68b`  
		Last Modified: Mon, 08 Dec 2025 22:16:45 GMT  
		Size: 54.7 MB (54699532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8fae04539f9499024dbfb30db944df534e7fc1d3089e4943a312e38b4a69fd`  
		Last Modified: Mon, 08 Dec 2025 23:15:12 GMT  
		Size: 11.5 MB (11500429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bde3f6ae3038114a37d889b3c291f70c9e4c6d29295cd9bb68bfb568819f3a`  
		Last Modified: Mon, 08 Dec 2025 23:15:11 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c97b5d3dc87e66b87ca24b0f615f0c6ac445df09a319a951094c0c2ea7221b`  
		Last Modified: Mon, 08 Dec 2025 23:15:11 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b8827f711faca9a8f1e805dab780dc41cff831485a86f3394c60a2c253ea30`  
		Last Modified: Mon, 08 Dec 2025 23:15:11 GMT  
		Size: 101.2 KB (101246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9fbf1005be46d348fd4575f1b72606610689969d6dba2495e7b642ea7ebffe47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b4bb56f70f428aed7e4e5c892de59dc3151f40220d177495002677e361c169`

```dockerfile
```

-	Layers:
	-	`sha256:ce48fb6b0ec255fb67170a8f79e4a5e0e7621d0b672e562ab0f6c0591a2f47d6`  
		Last Modified: Tue, 09 Dec 2025 02:08:02 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe103c3872070089f9b9327238a702c20145a8365c9719ec3027749e37d1b6a`  
		Last Modified: Tue, 09 Dec 2025 02:08:03 GMT  
		Size: 13.9 KB (13936 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:e3d76255c0105123c24c4f1777801836a8f765b8f223611b4671a46af438b488
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
$ docker pull neurodebian@sha256:6499766008cc053ec0b912ab66f23ce159e90bc18dabcb983bea84e09bfb4d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2604b1395cdb6aeee4e5890085b8fb3d04329bba19f625732b834e8729482f69`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:00:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:00:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:00:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da2c912bbc072214889aeea785d93b1fd8aa6ac61f78f85b74b1a2c7bfcc997`  
		Last Modified: Tue, 30 Dec 2025 00:00:33 GMT  
		Size: 11.1 MB (11105115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ff0255c58351a2bdba00dd012ac2e5cade79fbaf9d1df40944d6c30c6a501e`  
		Last Modified: Tue, 30 Dec 2025 00:00:31 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435192cbd31c304b5fbac1df842572bae61d4fd458e10413c8141aa34964cb6d`  
		Last Modified: Tue, 30 Dec 2025 00:00:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29481e40463e9c197f580cd03ddc64c30c46fa1ba531cf4869bebd8d7d0200b6`  
		Last Modified: Tue, 30 Dec 2025 00:00:31 GMT  
		Size: 101.4 KB (101396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0121127037c15088a06f5d4cc6665309b3f83687431cc5142ec69c3c16e9318a`  
		Last Modified: Tue, 30 Dec 2025 00:00:31 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f83b90058f681f5053a1593fc0a12f4856716795661306bfbc724002d56aa874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46354a8d2d79693e43d1445e84737548a1c54070368dac19159b6f8a606c3a57`

```dockerfile
```

-	Layers:
	-	`sha256:d6ca80cab20a5068344a3e2cc4f3a9d28ce32bb29b29ae87e3fa44e15d05fa59`  
		Last Modified: Tue, 30 Dec 2025 02:08:32 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e34a7b7174f53501b30b764d19c594a3452293501cb17a2c945c2de3051d4852`  
		Last Modified: Tue, 30 Dec 2025 02:08:33 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:539dd8660e2085bb168825edb74d4ed15382a70e2c498682da2b9efc8749db51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282bd03ed2f4cb666de301ace1692498c449a676a3e2c09c050d43280b7a47d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:00:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:00:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:00:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4150bee3f59a90f4911382dc6222dd13cc4f90ea24737fa822fd838c5c900b89`  
		Last Modified: Tue, 30 Dec 2025 00:00:52 GMT  
		Size: 11.1 MB (11106058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328a05363145dda7feeed31d22415cd120633e3b81ff7951c64a84ae766a7911`  
		Last Modified: Tue, 30 Dec 2025 00:00:51 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1befde1ef3c3cb2133d055bf2666550d14799515f1d229a8dd35bb2678a0198`  
		Last Modified: Tue, 30 Dec 2025 00:00:51 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8894397cad319a6153574c231eca833c7decca9aad1ff7f76c04e4aa734ce365`  
		Last Modified: Tue, 30 Dec 2025 00:00:51 GMT  
		Size: 101.1 KB (101115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f061a44f9b67b704e57c1c4022f0f59aa038e70373c788ac3694c4b6a50689`  
		Last Modified: Tue, 30 Dec 2025 00:00:51 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9689afe7068ec77cd86564703ac070ca70b7920e316aadcbfed21cf14199e90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc0372e30b2dc423cbce0c822c721a46631073ab465a819eaad98fcc76bb19a`

```dockerfile
```

-	Layers:
	-	`sha256:48e4ce2a888502ee2eb216d44b41e5d56c20fc09581f399712611354271eb53d`  
		Last Modified: Tue, 30 Dec 2025 02:08:37 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e192cf3fb3f567c3f4bffa267e219ff497105ed5a570a9011162858883b82d5`  
		Last Modified: Tue, 30 Dec 2025 02:08:38 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b412ef6ea141b35d048e28eeff4fe19392ec52c81625d8a03f10763bc8381a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998a4ceda4a3ee98bc31128d7e959463d63b1bab6339855f76e607d7b810ac60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:15:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:20381eeb836e270b6cf9dd675babbdf823eb79206c868ce7f8ae8aa6250aa68b`  
		Last Modified: Mon, 08 Dec 2025 22:16:45 GMT  
		Size: 54.7 MB (54699532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c030937cbbfb99adaf86783a860ed5d3cebcd1379d49c4e97853f3c1275263`  
		Last Modified: Mon, 08 Dec 2025 23:15:28 GMT  
		Size: 11.5 MB (11500413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805690f6ca6c5f3b783b7101716247b76abb6269b102b76142bbdd7f30da9a05`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46f35f9e3e3ad94601a7da1c16987fdc97b474cc01eeff25d712e4981dcbadb`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6664cf221203a95a3f5caa3fcee991c45d0adbfec5746b52600794de16127980`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 101.3 KB (101264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc295741e813d317bb24d92ab162ac433d018b9c312da7351fd0fe4910911596`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73f0a417e354d3934993bd9981e3ff5ab5cdab551b690bd1a8b8cc43a5d7eecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c9c13fb82aa274bc9b1f02e17f76cbefb5e69a02c99312ab68bbc3d1962f1e`

```dockerfile
```

-	Layers:
	-	`sha256:d8676d57bfa7ce1d1ca06c7ce2221855bc19fc07d1a4c49ce60f6d934b9e718c`  
		Last Modified: Tue, 09 Dec 2025 02:08:06 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:481798e95db057aa84ef00b287c2a69c2566950f493f9240abfff8a2e6a73c5d`  
		Last Modified: Tue, 09 Dec 2025 02:08:07 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:82f76b53bbe4befe34c1cd8c837004b33cc081f9258b3376a8ee0f3463b3ac7f
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
$ docker pull neurodebian@sha256:9df40b0ea9c95868d65e0d4230bc6cf3af140542662751ad4858fc2818faad93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a2827ed3ae4e6c34042eead78d08bf2cbd5ca365feda35134f83f64d5a78fa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:00:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:00:33 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:00:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360a3db99ecdb732a16f1f126976d4207aa9d983372d036f2b27c3fe152fcb7d`  
		Last Modified: Tue, 30 Dec 2025 00:00:54 GMT  
		Size: 11.3 MB (11269725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d2f319fdaefa9ea946357280ed31787a8424d1c2fb90c5c04233a3421762b2`  
		Last Modified: Tue, 30 Dec 2025 00:00:53 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b35ba6c19f111c946178b9e375dadc3d8f1ae76f9a5eae2ff0ae89ae98090a6`  
		Last Modified: Tue, 30 Dec 2025 00:00:53 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a28bdb6feee559d1cd4dfcb333fa279e90a66e33e29f8ded0cc4d368faad44`  
		Last Modified: Tue, 30 Dec 2025 00:00:53 GMT  
		Size: 93.4 KB (93362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:32a86f15faa5dcc16bf6c784d55a31b761c66ab7c8529554d1657d0458cef74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5312d8239141252c42ebf8df81bc38e3b7cffbc8a79c6beb0c2a61fb1aca054f`

```dockerfile
```

-	Layers:
	-	`sha256:47bf88e7f96240e091e5766b95388b68ff7beed8b87d60f0b4fc52a3a2dd6b44`  
		Last Modified: Tue, 30 Dec 2025 02:08:04 GMT  
		Size: 4.1 MB (4075236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0bed509e4049d93b04efaaf9a8cea41fe2da5b01edcea80dc537c82f331659f`  
		Last Modified: Tue, 30 Dec 2025 02:08:05 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6833c0bd4b9f3b8516fff1dabd1be547a6755435608d0c7d5bfb73bbe5896b70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac88fb8f2f18c14f33633d001057ccd8332f2b7e183bcfb88b19303409bd080`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:00:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:01:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:01:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76de6c96e27597369b524e7338a949708ab094acfce0ab9acf41063372d76b11`  
		Last Modified: Tue, 30 Dec 2025 00:01:21 GMT  
		Size: 11.3 MB (11253479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cb27afeb28fbf93480fe947d17b3bbc43b3b8413a6e64f2718c9eb6798bbbd`  
		Last Modified: Tue, 30 Dec 2025 00:01:20 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01298f07bbc2cddc4313c6e7a20c79eb3b315e8de19434e19c11f9b8060cf534`  
		Last Modified: Tue, 30 Dec 2025 00:01:20 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5267428ab28b53f5994fcac1d5a6d79dd9b2e94492fee8c05b7d29f5c115377e`  
		Last Modified: Tue, 30 Dec 2025 00:01:20 GMT  
		Size: 93.5 KB (93507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6f2599c0efdadf08ab22a3d433cf5372b7aa1621c29b1a9da6a236725c60046a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7e3b4ad787579bf2b2289c8d421f4fa997cdef176d24b19bd2425ac6d8feeb`

```dockerfile
```

-	Layers:
	-	`sha256:34f8520afdf262ef9c568b886a0ed65c06d34bf6c59174fd757244317d01bc25`  
		Last Modified: Tue, 30 Dec 2025 02:08:09 GMT  
		Size: 4.1 MB (4075478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d952abe5c366f262ecf4300fd673502af65a4e9c98038025db08ffad9834a4`  
		Last Modified: Tue, 30 Dec 2025 02:08:10 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:e541bd3d6e8c2e350585ff969178f5b1eb50d8c9ba616b7bdbf2f8399c5f14aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7d620a96142dcd3f186a6fe338504785161072efe1e215f5852fcfc5f84864`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:15:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f52798efde006ed1cd5f8b1568731b4e192bb8d42469448e91e101a0db4474`  
		Last Modified: Mon, 08 Dec 2025 23:15:29 GMT  
		Size: 11.7 MB (11690144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ab9b17f9e8302b4007852306001a4fec79b4040b0206f90e41917f36c14aaf`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80fb5d370b48a0007fee996c5762d278fe813640bb9c94a63fb41e8d8b2e096`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b644a9afbba75e07f7cce8cdc7ddff087b8ce4f882d4922da7656fe6eae3e1cf`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 93.4 KB (93393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:682023088122f95448d674072ec064ed9c5f200510c386b7da9b9572a60dcf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb59ba0285827e553a3b085b7aa8dcc0cb47e214ae0b993a08817c9ad3cfb10`

```dockerfile
```

-	Layers:
	-	`sha256:ee7b2db1f021c38b521cae01de099d8549088a69985b97fdf1eae25474abc095`  
		Last Modified: Tue, 09 Dec 2025 02:07:38 GMT  
		Size: 4.1 MB (4073204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a489f0243008eccca8a2550085e9994ad5c7db757f3065e9cbac12ae22242e1d`  
		Last Modified: Tue, 09 Dec 2025 02:07:39 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:1df3d441b412b21428738a991ef82ec761861eece4e78a72435307753613749e
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
$ docker pull neurodebian@sha256:abd11df33ce94245c5b308a02ac07a8a0db9d3ba22e30bf2ba86b8e53105a48d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd504540067624ec06b2c5272b16151d76e122ffa720c3875f296e98a8ba9713`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:01:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:01:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:01:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9219b618e4e6182d17706ece800345bbb50e09f73c77956af27105335ff597f5`  
		Last Modified: Tue, 30 Dec 2025 00:01:25 GMT  
		Size: 11.3 MB (11269781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13e191d6357ce5e635c96f1043c54d607e416a6266aa6d684bed72db3a5f010`  
		Last Modified: Tue, 30 Dec 2025 00:01:24 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6854b4553261e47e94358955f111b2475846ef1c8a4dab48857bb9f1a27e410`  
		Last Modified: Tue, 30 Dec 2025 00:01:24 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da4d2477a14e4cb069f0a2140cc894b75cd66ad7b520df1deed197c3530388a`  
		Last Modified: Tue, 30 Dec 2025 00:01:24 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ff8688eea57caa57840fef43d615760ba7ce668911891c755024d88ed3e7d8`  
		Last Modified: Tue, 30 Dec 2025 00:01:24 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2cddb674f7050215234bc8be391bca98e2b8d08870fa1d3f4d46b017e1cb39c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caec4de3b585e2c59818c179bff8a44609e5c58a301c70740835e9fc19e0714b`

```dockerfile
```

-	Layers:
	-	`sha256:7e55eee76bcffd1b4113daa63da2b2545d8f22a76ff8fabf8dfe0fcfbcf62e79`  
		Last Modified: Tue, 30 Dec 2025 02:08:14 GMT  
		Size: 4.1 MB (4075272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6521059055acdbe9eb6d741b62ff7e9c9d935dd808f3f6a5f29606ff245f7f43`  
		Last Modified: Tue, 30 Dec 2025 02:08:15 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:16b167b5084868ee4438b040d0e853f0983d1dbe370ecd6afc27b0cab1dd553e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544fa085ce3c72e8d91d7823155b0f299415f72adca3cf4159d4e6c780d05d8d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:01:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:01:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:01:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:24 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9572c2275cab572abb5887a4d4189ac1d16a900d802307d56f56d04e6ffc7dec`  
		Last Modified: Tue, 30 Dec 2025 00:01:39 GMT  
		Size: 11.3 MB (11253500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344bd7ca3dca19b442c7c96748dd10cee6b42422065e4b78e1c1e0d0c3eb1fc9`  
		Last Modified: Tue, 30 Dec 2025 00:01:38 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70da94820edfa3b121d63698dbf16aa22dd1b90df6bf21411a9dee8ad9e8c199`  
		Last Modified: Tue, 30 Dec 2025 00:01:38 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4555cee033ceaef40afc778e219498e0cbeaf00aa94df88e40ddf1ebc1ce47`  
		Last Modified: Tue, 30 Dec 2025 00:01:38 GMT  
		Size: 93.5 KB (93530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62a2808c0e83420cf223b94befb2e48d1db29559e1a334c89e015733151897e`  
		Last Modified: Tue, 30 Dec 2025 00:01:38 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8ca76a295a3584e1bba1a47d6224e58411fa0045cddfc42c11a2ed387162ff3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401e8b75ebeac47608271b90d088a56c0313183c4d4f84a5ca3293b0c2e19e49`

```dockerfile
```

-	Layers:
	-	`sha256:2aa7cfce6cff107c6e71a07fa4f85fc560fdfc5532c1e67d4016539deacdd99a`  
		Last Modified: Tue, 30 Dec 2025 02:08:20 GMT  
		Size: 4.1 MB (4075514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20b0b3436e8d94f4f58c2bc0b789bbb969fae42b5437cbd6c8860d487d798f33`  
		Last Modified: Tue, 30 Dec 2025 02:08:21 GMT  
		Size: 16.1 KB (16131 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:9a32e796340a46ccaa79995c6356a8ee8907a0384617d3ca1d62bc7abbc519dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a7cf4fb69ad656303e0cbb42407cb0e78b11763a461bc4b707dc5d83aa0cf8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:15:14 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:15 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:15 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfea0d8e4e48d2ed88857fa647a44ad0812430118aaf423ca71393709f1e738`  
		Last Modified: Mon, 08 Dec 2025 23:15:33 GMT  
		Size: 11.7 MB (11690094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9eb22c650699e169eb028f46c41221994a2556ec3bd4be0d2559aeb1d5fe1b`  
		Last Modified: Mon, 08 Dec 2025 23:15:32 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b82668d4fe89353db6e2d50cb43e936051f8ebc7377922145ef6e183043053d`  
		Last Modified: Mon, 08 Dec 2025 23:15:32 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c5501984a937c9a1905dfe66b2ebd4e0cbd9fe1232880dc1e283b1a8d0a14b`  
		Last Modified: Mon, 08 Dec 2025 23:15:32 GMT  
		Size: 93.4 KB (93374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61f029ba16f9cf3b81359ae9885b6449a1378e50b4f21041be43a2208e75f04`  
		Last Modified: Mon, 08 Dec 2025 23:15:32 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8d24dd4a17c911e8f6b1d6df7fdd2a5884a56ddacd395ba9fe61b20d9b737d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914ea91f455df92d0644bf85fad635d2b920cfbc7b9cbd368e7c5abbbd7539f9`

```dockerfile
```

-	Layers:
	-	`sha256:ea5f6d542df3b6cf1041a0765816de213980e146ac726111d73f5413e827ca07`  
		Last Modified: Tue, 09 Dec 2025 02:07:46 GMT  
		Size: 4.1 MB (4073240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83b94969bb82f97c4f66bf4ec317e7ef048252032a76a327ede5483777308620`  
		Last Modified: Tue, 09 Dec 2025 02:07:47 GMT  
		Size: 16.0 KB (15961 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:e0b772fb6c8cbf95b4bbc89d59fce54bd4612bea788c25876003179d85a81dc2
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
$ docker pull neurodebian@sha256:11704eb3e9e87e0bfc0474ec7993332f1a5446fd8fcfb93d5bfa76ddf865487a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59672470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfbefed7e757187bdc0ba33ca6e231ba0ab03e1d8c01c26ec51bffb858b7f8b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:01:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:01:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:01:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170e174478fb49afad823cff539b37cc66f46900a7285d0980c69545228ad17`  
		Last Modified: Tue, 30 Dec 2025 00:01:57 GMT  
		Size: 10.3 MB (10289740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98cfd6b6685e00247a8830717622cc76428a34a65ea509838b1ef1cf5f05c74`  
		Last Modified: Tue, 30 Dec 2025 00:01:56 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c93be1b43a47437859927119984568576e4e7035c09a3328ef782132ad5794`  
		Last Modified: Tue, 30 Dec 2025 00:01:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3130c56d9674187b01ccfa85c055fa9f25023403e80cc08d3bd3fedb46556a5e`  
		Last Modified: Tue, 30 Dec 2025 00:01:56 GMT  
		Size: 90.2 KB (90240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1fb327732ae3459a5ace9ae68da17e6b718a91b6edec2e4ba30e8a6c1ce4cc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dafd6febb344bc094cee781197ce68c717521a93152c82a6b3faef2618045e4`

```dockerfile
```

-	Layers:
	-	`sha256:a4c38d6616572e011521486de1ca5c77b753c05e8ac2873b363b81ebd8663c8b`  
		Last Modified: Tue, 30 Dec 2025 02:08:59 GMT  
		Size: 3.6 MB (3613029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e815c9c1e880979ed5797e8604eda18f89cdbc2a0f33a15aa08c9c99c1babfe2`  
		Last Modified: Tue, 30 Dec 2025 02:08:59 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f08af078412593f5e90c7ccc438b36a60853c367d5b1c02977191e59b42e2140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc02347a607123200510623e11328eccf357ded43e2b4c688cf6f3cbd87d6cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:02:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:02:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809d9a2a116ddb1b5044a05d97a74f3b666af6ebf3396b8bd1959b09b2c1dd97`  
		Last Modified: Tue, 30 Dec 2025 00:02:25 GMT  
		Size: 10.1 MB (10073354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43bf434a486a4ffeb412351889920cd853dafb22023f8b56041c1f5d9551def`  
		Last Modified: Tue, 30 Dec 2025 00:02:23 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fc09b5259d60baa90e66794a8eee4353a12a09741ddf610bc593a7d1a33885`  
		Last Modified: Tue, 30 Dec 2025 00:02:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d0d5e7c0fe7290044e8a33d358ea3fb2637f4a077ae7d449ac0eda02e54e27`  
		Last Modified: Tue, 30 Dec 2025 00:02:23 GMT  
		Size: 90.9 KB (90861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f741d89d851cb0175bc345ebf91d0267a3fd846824aff01df647a8423163d3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa99d1b3e6f5e16c3a14b8a2671503fc5c6d885230e3d8d99a1e1783b14e6c5a`

```dockerfile
```

-	Layers:
	-	`sha256:3e2489caeeb90f29d36cf18405d9c354b196ce6768875a219a8c2483595e7b82`  
		Last Modified: Tue, 30 Dec 2025 02:09:03 GMT  
		Size: 3.6 MB (3614556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6028461904b5f9e69fd501748e03c048131c821c768f588bfb954e678cb0680`  
		Last Modified: Tue, 30 Dec 2025 02:09:04 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:c8dc1f5965291d82532beb930b4b8dd9d2857dcffb348f41946ce7525f9d1868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4224f54fb533cad2f8b9b30d2e785eb1fd843e4fd63e905343da0c070c075d03`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:15:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e964d190139b1aba3de28d11b605a95f92489da3beb9d80e9099db336eb72530`  
		Last Modified: Mon, 08 Dec 2025 23:15:43 GMT  
		Size: 10.5 MB (10463020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ec584c96f35b189d796255e99284eb2b5a60beac79d3aa5e9e38511057c721`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9b780ecf3cdbfe9614a0f6fb11f3ac440968fc9859f8381cdd325606eb10d5`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e72d44ba44c44786256e5c59963306628e9bc4225d957dc3c3f88b69404871`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 90.6 KB (90608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8feb71ee0324566413295afd412d3e8536f97cd4923d4b4e3a66a630eb6b5e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f48fe17c7803c7f0a740da48d64460f0e14b205e6ef00e468dd25f6d417492`

```dockerfile
```

-	Layers:
	-	`sha256:6565d47d0408e99891700b9f73772b468617ffa2decbf66dd47aa2f3825e0c46`  
		Last Modified: Tue, 09 Dec 2025 02:08:59 GMT  
		Size: 3.6 MB (3610978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928694ae3cbda82a9b5864d3bb2e6e8cc4bfd721706dd53996bd42268ab412db`  
		Last Modified: Tue, 09 Dec 2025 02:09:00 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:7dfc8a363c3b6e2cb32e9e2807a2a143dfae159e132d3b06b8fecac0382c67da
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
$ docker pull neurodebian@sha256:f9de03dc15e6ea47894139ca860bbb7df3077eab69fee2b7f574967ad636e9a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59673092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36ae580edbfff25806f71d9e496b6985ec835b7fd8a4331978b9aafd98429cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:02:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:02:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:02:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4a3e55a52a3bf7a028c11cdd04765722bc5909c81b4d67215b6fa19d3e51a7`  
		Last Modified: Tue, 30 Dec 2025 00:02:19 GMT  
		Size: 10.3 MB (10289887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b144061b331bab67819cd04897b89738b7005071a8f0875b77226d420effb7`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49967f5f696ae80e5840802cbcb2bd1f5e73b290f75172b8fcc962647c0538b7`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ba8cfd8ea320a2d392ad2e66f06a7a61cdee8570bad69c5e59e12d224a8bb4`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 90.3 KB (90266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55878b042946a13598f4bc44dab8bd8b5c6cf92a29a5f88dd01768154044ca34`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:542fe53f92c587702cec1372b3bafb21975558dfbeb872f904af747a99edc817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad7da224205c770167075916abace896d69b70e42afeb45c22180a13d042950`

```dockerfile
```

-	Layers:
	-	`sha256:c281aa682144cfe81a19cf027fcc803adcd513786f32a54c63545a32824764bc`  
		Last Modified: Tue, 30 Dec 2025 02:09:34 GMT  
		Size: 3.6 MB (3613069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa707ba4df079680f05d88b1e02fb0f6aa7c05fc1835434c541f175e0a0ad6c9`  
		Last Modified: Tue, 30 Dec 2025 02:09:34 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:52252804a1c2803a046b7458af3a67b1982db6f527659eaa683317a8d0704c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d283cdfd359f8c32663dc926ca67419f8a476ffbc12a174e8172b39e9d52f28d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:03:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56e05de75caf223c899f57bdb45b54d71c3938e099e2fff63698d83c6515769`  
		Last Modified: Tue, 30 Dec 2025 00:03:20 GMT  
		Size: 10.1 MB (10073442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a034755a9ced70509ae5e0173325f4fb3174e73369ad3dc2a0bc0ede6eada`  
		Last Modified: Tue, 30 Dec 2025 00:03:19 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370de170d9d2bd026322648863277da5d88439f4c023954ff3d26321f8995899`  
		Last Modified: Tue, 30 Dec 2025 00:03:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5caeb08aa3984f98b10526c397fc882cf49ca878092e1ed0a2694b29f74951`  
		Last Modified: Tue, 30 Dec 2025 00:03:25 GMT  
		Size: 90.9 KB (90916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6250ad169fb763f2e49938340ca45af94a4284570dfb659a3dd2df016500f84`  
		Last Modified: Tue, 30 Dec 2025 00:03:19 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:deaa6d6c962198eee187acdc117bcaf95cf20c5fa346b8bd13094f3981e74053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068f0dea854818442fbd9729cba1275127ce475030eba6ea6efd526437a4fb78`

```dockerfile
```

-	Layers:
	-	`sha256:892de4cfc5deb2e9340d4e17d825664258f8fa9bed32590cf1722dd856a82e8e`  
		Last Modified: Tue, 30 Dec 2025 02:09:39 GMT  
		Size: 3.6 MB (3614596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e515d0a2d41c8e48b890fe2c645ee20c1d65a39b3c49ac8c1a7315fa7e210b1`  
		Last Modified: Tue, 30 Dec 2025 02:09:39 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b187bea3f10f39ea07ee4101dc0a3f18abbe7be34d2cff2bd6f7b49e13f3155b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafef6df1ba7f540161567b41abc65dc5bdb8501cc5fbcddaf3cacc06c4bdaf2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:15:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4b33922c04dbc376b8a5e1f0f1e92e63bb89043733e9f1faa4310e1504bd7f`  
		Last Modified: Mon, 08 Dec 2025 23:15:56 GMT  
		Size: 10.5 MB (10462938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288115e75d815edb522e43eef503792b7e9e6c88509ee7e9ba4a8f7072e4f953`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641aa24ee325190ed8096c6c9438150c637d751260dc4f24335265186be298f3`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30ad08df9b38bd944f88c550208c2de69c4c644bcc8a39159b8149bbcab36a`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 90.6 KB (90624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48e15f7f8648267c2768f3207e320a23c1769e635224feb1f62bd2181b3e786`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7406b4bee75ddf498b716c53bb3d974de73215e6a867b443f199125346ea588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84d6396779efcbbaa4d5ca3717a85cea53fa601f8499d1d5e4932ecd0830673`

```dockerfile
```

-	Layers:
	-	`sha256:9689b9651a4bdf918275574dedc207d7f9b6a4d8deb9f363c0f94ac3816b45e0`  
		Last Modified: Tue, 09 Dec 2025 02:09:11 GMT  
		Size: 3.6 MB (3611018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134c12f5888db88b0afd397425b7c86d8d384dd6dcfee36c93eb7abe2abb0f15`  
		Last Modified: Tue, 09 Dec 2025 02:09:12 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:150bf0efbc0cf3e71c4e917e1365f4ce12f068b52f78b4b3ad7edf35b51bac84
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
$ docker pull neurodebian@sha256:2302018712146863aeb4690550a5b76df8b7df13e0d802be71a0c3c38149a135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60548458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec708323e8e211beffa0a80ae7bba5f384b434ce88123b60733a0d195d8aa7b6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:03:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e1869079ab5cc3b00301445717c112f3ddb9424b5d7b2a41713bc70d9482ee85`  
		Last Modified: Mon, 29 Dec 2025 22:28:05 GMT  
		Size: 48.8 MB (48830058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4e5a600b42af7e7249a38577cc844cd06b82d1f22fca446507bc4d97304e37`  
		Last Modified: Tue, 30 Dec 2025 00:03:22 GMT  
		Size: 11.6 MB (11625089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24bf27c0bb0ed449a81b5fa6ada1e384d2e5ab45f9922c801299bb91e5dab52`  
		Last Modified: Tue, 30 Dec 2025 00:03:21 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e586810401da99692985a5491071e4faf2cbeba2c773b81a6c74603b1ef3e30d`  
		Last Modified: Tue, 30 Dec 2025 00:03:21 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fe4dcbbac465ccc98a30e7771909d8458a9f36baedec710f84603defa1dcba`  
		Last Modified: Tue, 30 Dec 2025 00:03:21 GMT  
		Size: 90.4 KB (90408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f519e2e0c5660ae6c3b23a247879ae3da45a30261b90d6a9e855c44ab69afa65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf20aec7ddfa5fede50a25e0ed3e08a788b1e122a1f045868785e829dd18b35`

```dockerfile
```

-	Layers:
	-	`sha256:5a0737d7a8f7467ed51fc907ab110086336b2a8248f44a46f1cf3e860d5b3651`  
		Last Modified: Tue, 30 Dec 2025 02:08:39 GMT  
		Size: 3.6 MB (3592069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba3fc4fd325b4e974cb70b4248875c0c5cd5f6d01a0aa49b27aeda7b7ea9fa01`  
		Last Modified: Tue, 30 Dec 2025 02:08:40 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7cb33f542c2b2416b8360d80bf270f017394a8248f5547bd25b910d362907e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60209869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52d523ae26b69c0e69f59c722a906ef5e749bc1b0072a349d4b47e66752980ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:03:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:24 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:24 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6ed83950a3f675536ad8634cde3cf4c241d5faea11ae3192ff5909f826256f2`  
		Last Modified: Mon, 29 Dec 2025 22:27:42 GMT  
		Size: 48.8 MB (48831993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2c77bf93408787969c8c3f6ff7213d99a7e697e69620cca332ac58446528bf`  
		Last Modified: Tue, 30 Dec 2025 00:03:43 GMT  
		Size: 11.3 MB (11283854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffa76c7561f8431bcf2d9458d0b5122c83188cb1a0af66ba63739670f119ad8`  
		Last Modified: Tue, 30 Dec 2025 00:03:42 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f90c9596551e2e36dca68165bdffea5d2e3885d8c814d8ec39b6430e18051a`  
		Last Modified: Tue, 30 Dec 2025 00:03:42 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8891a2507db7acd33db08d268da2d5cfe43517b88b3c5e4d64e7746d884a2120`  
		Last Modified: Tue, 30 Dec 2025 00:03:42 GMT  
		Size: 91.1 KB (91115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:677e960c2528d3f9423b79824ad6bd592c57b82a587b2e13c10fe717f1ced255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec4e91d533b3762f44007169dfd298ae15029e6c51d8049c5674a2410e24c89`

```dockerfile
```

-	Layers:
	-	`sha256:bbd84bbc74533abe8bf8740104e0d06c186ae3cff091c08be59b46b536a3e3ec`  
		Last Modified: Tue, 30 Dec 2025 02:08:44 GMT  
		Size: 3.6 MB (3592945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c39f6fcbfd1dc80794642dc576dfd48079c6de50372df3ff1ac44eef02c17cc3`  
		Last Modified: Tue, 30 Dec 2025 02:08:45 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; 386

```console
$ docker pull neurodebian@sha256:ed17bf7744b05e17a7f5a07512b499f7853d80ca2634d1b3091f724ec12704c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61720534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4a7e442293c27bab1441b206d263cbbfda95db72021a246e34633483d87277`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:15:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a5d3e60f8c1eac1ccb5aac1ab5735dd586fe448287d7c7d1d7f59a687bd9b9b1`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 49.9 MB (49874580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339cee8645950fcb2cac8e786ded94810e24e89ade2e4f5cc4099b37f01809d5`  
		Last Modified: Mon, 08 Dec 2025 23:16:12 GMT  
		Size: 11.8 MB (11752135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b16c5bf742f0f200c67b5041f2cf3e97f655ef571b984e5b607960988763c66`  
		Last Modified: Mon, 08 Dec 2025 23:16:07 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec3e51522085c44202103858e4b4bc149caf3ac8be3196028e5327cc90b577e`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a58fde9f6b48ef00bb0ab006f68aaa17d9c356d37254ac44110fe0f3dadc452`  
		Last Modified: Mon, 08 Dec 2025 23:16:07 GMT  
		Size: 90.9 KB (90913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ade3efb3c881d0f2aebde1a8dfd977b7cec6e59eadd851d32e96d5442cdd4c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3597435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac31d7558920461a59e82693d3c70a6a3ec175dbf6017f477e182186218a2197`

```dockerfile
```

-	Layers:
	-	`sha256:16859a3d98038419a32fbc0eb7b4a65dfc2adab665a924d9bb3ff4e6dfb608c8`  
		Last Modified: Tue, 09 Dec 2025 02:08:11 GMT  
		Size: 3.6 MB (3583531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104b1ce751d490df8412608415756e6158e3a99cfc6d9d66a088c869af428201`  
		Last Modified: Tue, 09 Dec 2025 02:08:12 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:d635200f4e3f15d9c13d3bc4c8a68ef05d2a992afddd547ca59eb2450c05994d
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
$ docker pull neurodebian@sha256:56ea8c0eba2929e786fc26a4b61337bbcd45c6602c0e633949dd1a233d86d173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60548879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa82304520ea72936c1f1be9740090de2d22dd3eeb4175e3f9f0d6287e2765c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:03:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:23 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e1869079ab5cc3b00301445717c112f3ddb9424b5d7b2a41713bc70d9482ee85`  
		Last Modified: Mon, 29 Dec 2025 22:28:05 GMT  
		Size: 48.8 MB (48830058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebaf0ac99f659bb6461220191a78a66c276d9816bf54d5b7182576ada79daa7`  
		Last Modified: Tue, 30 Dec 2025 00:03:39 GMT  
		Size: 11.6 MB (11625073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f62653a9582b12b399b318130654cb00f1e7633a7dee96cbd1cbdb492a173b`  
		Last Modified: Tue, 30 Dec 2025 00:03:38 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fbae46621e155e25e4836a84dd7ca71e6e4f31f86ddb9924239ceefb1fcc0c`  
		Last Modified: Tue, 30 Dec 2025 00:05:14 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5677abe2abd0ea16c83243a95dfa4d82828123fe243948ebecaf73a1a2137`  
		Last Modified: Tue, 30 Dec 2025 00:03:38 GMT  
		Size: 90.4 KB (90394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6c1cf3b8f91aa7794755a003db44fc5c2f67b48acf65c7a0b9c8a7e7b4fa93`  
		Last Modified: Tue, 30 Dec 2025 00:03:38 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0d38eca5c86573632d19313a058b0ecbc0e568e302f0426ebe28033b93e719d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e043b1451aeae3d0b9327ad512efe6438e8f08fadd4e6cc75b4d8880a188dca`

```dockerfile
```

-	Layers:
	-	`sha256:b9e68dda9c60e65ccae7d20c80d1f74a3829b61170430a31144926ffacba2427`  
		Last Modified: Tue, 30 Dec 2025 02:08:48 GMT  
		Size: 3.6 MB (3592105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd14da38b318103abc72d4da22409c4d400f464e564ab525e1d80436718605ba`  
		Last Modified: Tue, 30 Dec 2025 02:08:49 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e3f88edb3744a1481d41725b392334f62ffe29db0291e3c93b61dd2df66c9a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60210263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ec30ac7f439988b4368dfd9dfa11d36be4411c8128c0f32ec915cb65d02c20`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:04:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:11 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d6ed83950a3f675536ad8634cde3cf4c241d5faea11ae3192ff5909f826256f2`  
		Last Modified: Mon, 29 Dec 2025 22:27:42 GMT  
		Size: 48.8 MB (48831993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278e9ed2ac59aa8e052b8c075a014ec12973527aa13dcfc47386b5fc849d09dc`  
		Last Modified: Tue, 30 Dec 2025 00:04:30 GMT  
		Size: 11.3 MB (11283833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e5e80e4b2f6c88528a91fe91f2b355ed86bbfb9e96088827682cf0dd2fe3f0`  
		Last Modified: Tue, 30 Dec 2025 00:04:29 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28c95221e4cea56d32ff27ac8a53bb48fe70456cc900191a16be091be283769`  
		Last Modified: Tue, 30 Dec 2025 00:04:29 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f473be47c5749d5d961e89ec52f21d33af161fbde6fa39bf270b3682b3906d`  
		Last Modified: Tue, 30 Dec 2025 00:04:29 GMT  
		Size: 91.1 KB (91085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ec3638ca167076fc05df171bfda204d00eb1f3ea1d007ef3b85db710e0582d`  
		Last Modified: Tue, 30 Dec 2025 00:04:29 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef6bb4894931f521530b7db4fd13f66c4226fe5bf1425c4d024c2f567edd946f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3609079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0b389ba0fe727bd64ef60b5007f1271d09508c42e0364b7dc035f445ca4e7b`

```dockerfile
```

-	Layers:
	-	`sha256:5f14d023f73b435b23489a0d89f2a5bad5a57d6efc8da662e4abbb50418a0fa2`  
		Last Modified: Tue, 30 Dec 2025 02:08:54 GMT  
		Size: 3.6 MB (3592981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad81100e36b669c78cf4ab2bf837b7bcafd554fe4f55a126cc3bf816defae711`  
		Last Modified: Tue, 30 Dec 2025 02:08:54 GMT  
		Size: 16.1 KB (16098 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:310986ea6782ef724d41e8f67240e005c3c0fbfe36d6e9779c703452978b2061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61721053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75690de1cdcfaaa39c9be4ef65273d76e990e6fab068d68efa4f94bb0ba85995`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:15:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a5d3e60f8c1eac1ccb5aac1ab5735dd586fe448287d7c7d1d7f59a687bd9b9b1`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 49.9 MB (49874580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae4cf933beea0d74190c5108f5592160b361455d8d0aca4852d56b28f1816ec`  
		Last Modified: Mon, 08 Dec 2025 23:16:08 GMT  
		Size: 11.8 MB (11752199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69195fca673288bc2be238012fb534a989339e533d6a8f67d5d4ee43d28117d5`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3571e3ea3babea5298321571e0ecff849e4104964f3e97b88921df3717d1aa`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d10761b27d78d3cab80c345eade32d07c1317137a5ae92a9998e523977655ab`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 90.9 KB (90921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6e1907cacf4ae722d1b080f12e49ca31d368e482e1835e219185719e6c1090`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3638e2924b6b21634a03c10613ef941641ea6b6d835763bb584846dbb4776e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9d1adf120a2f484750d4044e9113b7a12ad4287c721ee006427934f80f2ef3`

```dockerfile
```

-	Layers:
	-	`sha256:536b0ea1c809e7d334f738198e24640d9fdcc2284f7ea5394d9ac75a89aa1e12`  
		Last Modified: Tue, 09 Dec 2025 02:08:21 GMT  
		Size: 3.6 MB (3583567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1afa97a40023bd48ea41bef0a9c7435b97b608551dcbf15388b584d2047e4326`  
		Last Modified: Tue, 09 Dec 2025 02:08:22 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:0e98bbc3daae66df44ae11a5588f2309b4d0b0a3d5759a236557a26319c2c5b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:e6772d070a574f00e1ad07efb0f799b7e9d9020fccf9887c7f6378c50bdbe816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33275957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d6aeb77e4a5a773edcad5fc10b5e08d8f387161a9b7b5d93e1cb1aac4e3735`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3881e591a9050bd6250b7975f2a62d69ce9d4bc181a569e43d583973bfffafd6`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 3.6 MB (3625726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7763c1732252c316b49e1a5ebe3d01e0ad636198993b3e20e7267f9fe62d4283`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59987cb0b364dad0627b12e7ef72104aea08b23fff39930f94dac5b79cf2585`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91714d8e9de2a6eab65bf534a21daeac5f710d6f823714736754481479f25eb`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 111.3 KB (111253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:74faf561f221e4ff0722a9a6a5469d286311b0d29d710a50c1c2f2d408089335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5093bdb0233d5e701687d2c9157af64b57724e81b512be660289bb7a4c8f7216`

```dockerfile
```

-	Layers:
	-	`sha256:288a50939bde1611937533ae039c8544b98d95d75331e8bde2456927a7ddea17`  
		Last Modified: Fri, 14 Nov 2025 02:07:40 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941444796f9904d69ff28378466addce903b01de5df5c0c291ea8d117c6aff74`  
		Last Modified: Fri, 14 Nov 2025 02:07:41 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:09ed49f28825e5330d749e8aa583e2f0c2c88ace7f935f79fd1b4ee7cfd6502a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31094789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170be1c0c9e62fba389535f45096cb097ffcd73e82e10f8e5f2bbeb7101e7716`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:30:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:30:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:30:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:30:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4fc061e7db4abc03b992399d4d51a6e96a401904e29c8c7cfff6c2b0ef4cbc`  
		Last Modified: Thu, 13 Nov 2025 23:31:03 GMT  
		Size: 3.6 MB (3598146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e356cef2bd87e42a124fc4d5e82057772ca5cf202c6c194f6884f04283430a`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7f921b9372d265e8d3805815b0e98436f5f4b92fc0dae86070b7f4f269f992`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562a8628e6dc417f84896302f26a4b6c43f921ca7ce9b73b785936f7e5d51be2`  
		Last Modified: Thu, 13 Nov 2025 23:31:02 GMT  
		Size: 110.6 KB (110588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4d3a9691d374823b1b504cf09f6f82049355ef10aa41d07d3be46ed00124eda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98eb368a6d54f82c2cad7c303b49a01491c62b68e3a47065952793b1df828ae`

```dockerfile
```

-	Layers:
	-	`sha256:c8a0004225abd4f8c618461be1e72c1192172f7ccfd4fa7f0839dbdc35d24f43`  
		Last Modified: Fri, 14 Nov 2025 02:07:45 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200a3136b60277a7c0dac564342f17944ff690ca89305553d8bd0bcd74108f3a`  
		Last Modified: Fri, 14 Nov 2025 02:07:46 GMT  
		Size: 14.1 KB (14056 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:120b8715dd3a26a2af4049512591dcbb112d36e4accff9d7fded93e27ce47062
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:ef9dcfb5426525d36ca828760110823e06e065cca0c4ac0682d0a506e9cf12e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33276245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abbe750921d6da2c2bf91fa655875aa86d26da7d2c93cd08dc4d8b4f91445af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:16 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3881e591a9050bd6250b7975f2a62d69ce9d4bc181a569e43d583973bfffafd6`  
		Last Modified: Thu, 13 Nov 2025 23:31:35 GMT  
		Size: 3.6 MB (3625726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7763c1732252c316b49e1a5ebe3d01e0ad636198993b3e20e7267f9fe62d4283`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59987cb0b364dad0627b12e7ef72104aea08b23fff39930f94dac5b79cf2585`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91714d8e9de2a6eab65bf534a21daeac5f710d6f823714736754481479f25eb`  
		Last Modified: Thu, 13 Nov 2025 23:31:34 GMT  
		Size: 111.3 KB (111253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87663c843a43743cb4efbfd154e030c6591b4085d0c1d047a156158b9c47142a`  
		Last Modified: Thu, 13 Nov 2025 23:31:58 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8b9b5e291adc948bf145496030828a9a408c3399355380347b0ff72c16e2a880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970a1d784b637f4a06999658bbd7cfd5f71517ef14610d1888be4fc2d5614399`

```dockerfile
```

-	Layers:
	-	`sha256:19ad39194fba9b75b47c96c260e5431b390f0c1f40747e8857c995d53dd228f0`  
		Last Modified: Fri, 14 Nov 2025 02:07:48 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd46be2a48617b0b0891f5fe27958f8e2350a649da215ce9a4995e5a9a62d43d`  
		Last Modified: Fri, 14 Nov 2025 02:07:48 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8c05f54ab64c544f5b1833f0d31ef94804c914c6debd693acfce0dc0320660cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31095110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2b987bf931381f750375f7be732736b38d67dd928c373fb3ac7f7703364fd3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608dccde847e272476e52044e62fdf40902fdf981eba3f9e853d9bb36c3ebdf5`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 3.6 MB (3598157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff367c25857e7c190e4c69803b560c6e428a2f6fdcdef7291ed9c54595fd3a7`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d785e7ece3388bd939c0607e15ed02803f8e48b590bbf43d7b628f2275ed86`  
		Last Modified: Thu, 13 Nov 2025 23:31:37 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411f09f71214f6303934a66000e111fee3918961b6f6726ed9b784feeceb7fcf`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 110.6 KB (110611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa2aa73e9807dfaff0d65e73fea59b7275dac6754311bac380e78c75cf4c922`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f02cab47a327aef8e9eea19cc7a8da708ad76b7fd1cee2ccdc47f302f2cade08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5d2870c8ff27e82579456117c17077c9ecc56cf9812adeb91b20dcd8fdb489`

```dockerfile
```

-	Layers:
	-	`sha256:196e2a812f54eccdc16bfcfe68a337ef2397641ccf3672d5f6846a2c19b4a34d`  
		Last Modified: Fri, 14 Nov 2025 02:07:52 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be4dac85cb072f2caede51d4767494f8e063e10991e49a2febf5e030defd53e2`  
		Last Modified: Fri, 14 Nov 2025 02:07:53 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:86ac08e0cbf2640750a131de8ddf9bb285ed3c0359b84a4489b870b5bd4b9d73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:2f888be4d7159ed9a03884f72b0a18d428983c3c093c51acf701c4f3a8f58db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33394268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e41a68f6806fe09a43691a06544a172872ab66d56d34fd116ac854f53aa973a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:32:05 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a0ad9b4aaae6e7e946573addf6867a419111a60fc9323198684be47d29ab8e`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 3.6 MB (3562811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2192c9cd8ae78f10eb620c49dd6c3f1c97dbc3a99b8e0e54442bf4c4085d50be`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3fd385eef297b7ab043fbd27de442eb44e742de653f6f0beec541e5624920c`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9ba4094a4680b7c79b70bf18ec8e50552bb4bcde925a278b84fdf831ae1ce`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 103.9 KB (103855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:30e09776cbad0fdeb6250eeb59b6c85db722439c89e9ea463b8846b520362ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fcd14e1e482b89c9f2956dd0d711c27c1041d1eecbc57b8cee5f200fb7e014`

```dockerfile
```

-	Layers:
	-	`sha256:7cb594c99ab7f7379858b0869eccc55ee5d16dd0c7a117ec2ea6286621e09d2e`  
		Last Modified: Fri, 14 Nov 2025 02:08:05 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874d5cd16621b1ee0eb69f6c404dabe165681b10474bdb7a0c987170e3243da9`  
		Last Modified: Fri, 14 Nov 2025 02:08:06 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:96b42b877a4656e7863be6795ffe062410d426123d20fcbe050944554329e1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79a782002d75afde88daf47c99b398edb58da7b5d5cca3827577832434b8abc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a253dba035401f762d0613aa4d977ce12d945bc1918bfb08a17ba7331fe815`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 3.6 MB (3561049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bd3e1c5570e7cd4878353726e4bd0fe6a358ae3cd2dad02e393d59d98803f9`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 2.6 KB (2640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b495cbf000ce9a258736ce76444ca683648a9ba468ca5d3d6cfde0d8bc89402`  
		Last Modified: Thu, 13 Nov 2025 23:31:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a7199ab9252b8ed239c8c34dd3a013dd0b7c2c06d87c00c361824931df4c86`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 104.6 KB (104607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5f3d14db57b4fa3eeb6cbb447024bf03395dfe359f372b7f4917ee462f439907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe6e66c6e7d0f92c843a2215edea604807c6be3f7f5ff9f9929c74d8d3d52f9`

```dockerfile
```

-	Layers:
	-	`sha256:ad647f1003e7e0dec3bdc34b289daefb923cc8e0c1305ba7b14f3a2108d14a3a`  
		Last Modified: Fri, 14 Nov 2025 02:08:10 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c6007dbe7aee0b4fb818dc38799ebc8efd1b7438bf95762182955214aecc0d`  
		Last Modified: Fri, 14 Nov 2025 02:08:11 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:184659c45ef82521389ee748e1ee4bbe1449f0946581307e3e93d86e0e058f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c299aad60e1e7f11d4286835ce579930df7f598ed9b1015fcaa7c79713c42957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33394810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ed87def879102b787b9246c739018511b4b589c34932b0ef713c6c61de668d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:32:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c0e1d7b3f111e4566e1d12f6c0632e153c201260a9826542321f8ea23bcafa`  
		Last Modified: Thu, 13 Nov 2025 23:32:28 GMT  
		Size: 3.6 MB (3562936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b40e8d70ead7cc4f0cd07dae1ee6920efb006cb20528bcc7de39094ddf9874`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5ee6c709ae7dad0afff7391eaaa68296673cf0205a608f9bce6d4f7500e650`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd86eb2b24e5478ee0f7d4c55df8e6c357a999c4083997d6162434e36abba3f`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 103.8 KB (103841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b41bb95e32d18baa23088cddd23dfe1c3c097445ffe768613d34800b4c0c5`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93bbbca7ef64d9156a3013b0c4e3fa3312e91da86a098db01ea9d83029661afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2465328c5c5e8df05ad265eb773fbf3e584134d29936e5a21430c0d9164a3e3`

```dockerfile
```

-	Layers:
	-	`sha256:aabcb977352301fab1d6dabefc144dcce2ebf0a3030cecf40cf83bc2aa92770b`  
		Last Modified: Fri, 14 Nov 2025 02:08:20 GMT  
		Size: 2.1 MB (2120901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82c114f49a06e6a45987c7131d46b1fe1220101c4997f7726a576f2a5543d25b`  
		Last Modified: Fri, 14 Nov 2025 02:08:21 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c6af2ae93699e738b6c0895055144b4bb347920aca7f91e4451aa75dde146236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32531089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989acad9c141ce3dcea15e9a18df4c3ea56ceedb189ef7a6b8b8dfac6823e87c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876648f4bcbbd9a79fe03bc85730393c6e24075dde48714e37bee27c5e932691`  
		Last Modified: Thu, 13 Nov 2025 23:32:17 GMT  
		Size: 3.6 MB (3561120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c874b0b5bacc6d952a7735777f05b95f3c5bcbe6b7f7d50b6dabee2398abad59`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660eaa03fbbddfa884bad13382570eba092d15224cbac502584ceb4f39f1bc8c`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05849e9ea827053df3f7378003dad6aefab958b313dcfc532a8b8cd4826355d`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 104.7 KB (104669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa5566c0de4309a0ef6703f3bee20e95197bb23f5d2a711b7cd280db22508a1`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:da8153a7c5dabd74fc895825a81e69cddc07810acc5675ecc956059d31108d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71031b6901d4ed1fbb3d94ff534deb64c3c8c0902724a95d29584e35420ca5f2`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ac3e4bbdc32139f4d1a5d2b49adbffdd230b9c2f1f6cbc7952707749b342d`  
		Last Modified: Fri, 14 Nov 2025 02:08:25 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:024cf6e9493f7a6f8cac5b000f292b1bc84bfbbc6fb5d69d25b04d6d3c090a55`  
		Last Modified: Fri, 14 Nov 2025 02:08:26 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd25.04`

```console
$ docker pull neurodebian@sha256:ab139e2ef8b811558941eff017d1f467deaa77fcebcdf3189633727ef717dc92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd25.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdc67ac4dd0d651097ba75d3f513b34e66af0bdfa85db80045d15880faf9ef04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36682742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc9a62b14ecbd0c50b253059091a66a5c95e0809527bce9cdece2619b81e21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Tue, 02 Dec 2025 13:58:07 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807958f6dce95c2cf132ab919d751d642e0834efea8afabde5dd80a06382164`  
		Last Modified: Tue, 23 Dec 2025 18:33:36 GMT  
		Size: 6.9 MB (6862222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d85781ba57065c27119c5b829ede85b21f4be4c79ed21b52b5dd18e69324e`  
		Last Modified: Fri, 12 Dec 2025 18:34:28 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6000f4f29de58b9c57f46bf4c2915a41aecfde0ffe93b519dc150c2e05839`  
		Last Modified: Fri, 12 Dec 2025 18:34:28 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b298e1353c735a6385e6a62cecbfe1d1b59a32feea6c006fe2970e9a377fb0`  
		Last Modified: Thu, 25 Dec 2025 08:42:10 GMT  
		Size: 103.6 KB (103644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:87fb8fcdc3533806d68ebce00bcfcf60c95a4fd2ca27173aa2131f4e12b9a92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7aa5c68eb77711d7c5504ea0dd43319dc6ba5a495e2a39b29e42dd4613450`

```dockerfile
```

-	Layers:
	-	`sha256:34e86114d346aa4146ae590dee647494234ddff44dc9bf93ed557394aed25887`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 2.1 MB (2129387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb29516268d88fbe0487f9e71585d01a2863eda154c3b84c932731ccf47ffd8`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 14.0 KB (13987 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd25.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d0215dbda4b85ac69b750d98f8f3eb9aba18829cafe490ef6c04e7f1b5d3575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34803835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6196b8372a58dd339a5cd7b297736021c12b067eaa196975ee6481a581ec22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Tue, 02 Dec 2025 14:40:05 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b8d7c0516946e6186f0c1918a80da44ccc80465d586f0db577e9c5e3fa309`  
		Last Modified: Thu, 25 Dec 2025 08:42:33 GMT  
		Size: 6.4 MB (6392372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccd7c148caa4ff621b2e8f1407d0680d8b216fd3b91aade2da4e3bcf67242ab`  
		Last Modified: Thu, 25 Dec 2025 08:42:33 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63a7c688f7b81b2251c0096fc2033ac1c2243330fd41da718cf8002ec93dae1`  
		Last Modified: Thu, 25 Dec 2025 08:42:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a8bb23e4d96a15bc63dda952317ea8ba3a8efd39c025f4e5d59b26d5afc57c`  
		Last Modified: Thu, 25 Dec 2025 08:42:33 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b6e0e2468e055fd3994fdd22716a6516ca822a0b893af378cfe9b7c8c92ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b634830ed4e5ae3eba300cf243790465b87b6d976898e0bdc93781f17d3473b`

```dockerfile
```

-	Layers:
	-	`sha256:73f73f1097d47935c4c36115e56c20ae5811fee70906bb8d0100cacf857414df`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 2.1 MB (2129631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3369301dca599eb9decd9b13cef9db3cbe5da13f1a35be39a2983729b9cd67db`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd25.04-non-free`

```console
$ docker pull neurodebian@sha256:843d307ce6bc09a7cd1b57e44466adef4c4764ea1c793ae5816c4c23f5fd2e42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd25.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7e3b0aa3a1e9664cb5a8951141d1855604212beb174f638ffd32f46742ed4bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36683143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b635066dc43129e20e37c95f2235d3e316b7d3b9c2aba40f0ffde2b54e2e6e2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Tue, 02 Dec 2025 13:58:07 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e95813fe4718cf415f65b5a2a6aff41cf1ca472b75f81f0e71c88a2c1e75e9`  
		Last Modified: Fri, 12 Dec 2025 18:36:41 GMT  
		Size: 6.9 MB (6862197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c069ba67e04af50034555225735086ac2d283d240d8ce7e46a9d3308c6398c25`  
		Last Modified: Thu, 25 Dec 2025 08:41:48 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7163aa66b2f0788a2fd8bfb24efa8a573ed390b32865ae0266981836fb3f2a`  
		Last Modified: Fri, 19 Dec 2025 18:37:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744d7aa582d29cc5ee3a878017b70e760a48aaf077eeaf1aa5c0b98f225a81b`  
		Last Modified: Tue, 09 Dec 2025 18:36:08 GMT  
		Size: 103.6 KB (103637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709942cf2f7b8bc52d31c967ec725251f89630a82eb3debdaafff34b2502aec6`  
		Last Modified: Thu, 25 Dec 2025 08:41:48 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b03d30cc46e85e007f546cd2c4a415622d8016571f0fcd74004ece8a9d69a9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b1b3d34374f9d8719267a2de2de8be8524966deb0e192f3a0d0b9e95bbf7e6`

```dockerfile
```

-	Layers:
	-	`sha256:75abe1e107a33427871261a37ffd5362e38bd76021a38d45be8b8ecfd67cf1a7`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 2.1 MB (2129423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f0d6a23d261b81b7b10446e66dbf147c195e56727be3c4c4095beb8744927b`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd25.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8bb52949ffdc66d1b1c45b166770d0321d7082209a408f0dde0ce50355c437d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34804334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6029e77c7f8a48311858bca5d16c501aebcd7dbababb443b3c892392f8506a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Tue, 02 Dec 2025 14:40:05 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d08ff3fe3897ede8ef5bf7e75a8c754e9da90066ad638138411914e6569fcb`  
		Last Modified: Thu, 25 Dec 2025 08:42:23 GMT  
		Size: 6.4 MB (6392412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87458cf3c50f45fec6029a8e2d31f7dc2c30d63c5e92c7e4f4d7ddbf1fd1fb4`  
		Last Modified: Thu, 25 Dec 2025 08:42:22 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fabfa39ef821d160c97bf91453f07634d072ad956ea83de4da94873f2b71a97`  
		Last Modified: Thu, 25 Dec 2025 08:42:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d80fbf3cdda43cd93b73ef0b7215c959689c5073a718bc28b1a88b435aeda`  
		Last Modified: Thu, 25 Dec 2025 08:42:23 GMT  
		Size: 104.2 KB (104235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3181f804aca7e1622946b1391b32ee30ccebfbdb03426caab02bcd300d54cd8b`  
		Last Modified: Thu, 25 Dec 2025 08:42:23 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd25.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:29ea36baad60d33ffbfb5fd8152d415e121532b4008b174a68251c71851548a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5656dffee277d964d7af531bee03d767b53dc21bddc33bbedf5b7d1e0c3a1668`

```dockerfile
```

-	Layers:
	-	`sha256:a897c9f03a98ed8cc43baa74786f9234dccd6f6c51fe452db7dab397fb9c66a0`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 2.1 MB (2129667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0912356738dd5be0731ed4354e13efdb3bb03dfc003407132e1ed93bde4ad42a`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:86ac08e0cbf2640750a131de8ddf9bb285ed3c0359b84a4489b870b5bd4b9d73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:2f888be4d7159ed9a03884f72b0a18d428983c3c093c51acf701c4f3a8f58db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33394268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e41a68f6806fe09a43691a06544a172872ab66d56d34fd116ac854f53aa973a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:32:05 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a0ad9b4aaae6e7e946573addf6867a419111a60fc9323198684be47d29ab8e`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 3.6 MB (3562811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2192c9cd8ae78f10eb620c49dd6c3f1c97dbc3a99b8e0e54442bf4c4085d50be`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3fd385eef297b7ab043fbd27de442eb44e742de653f6f0beec541e5624920c`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9ba4094a4680b7c79b70bf18ec8e50552bb4bcde925a278b84fdf831ae1ce`  
		Last Modified: Thu, 13 Nov 2025 23:32:22 GMT  
		Size: 103.9 KB (103855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:30e09776cbad0fdeb6250eeb59b6c85db722439c89e9ea463b8846b520362ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fcd14e1e482b89c9f2956dd0d711c27c1041d1eecbc57b8cee5f200fb7e014`

```dockerfile
```

-	Layers:
	-	`sha256:7cb594c99ab7f7379858b0869eccc55ee5d16dd0c7a117ec2ea6286621e09d2e`  
		Last Modified: Fri, 14 Nov 2025 02:08:05 GMT  
		Size: 2.1 MB (2120865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:874d5cd16621b1ee0eb69f6c404dabe165681b10474bdb7a0c987170e3243da9`  
		Last Modified: Fri, 14 Nov 2025 02:08:06 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:96b42b877a4656e7863be6795ffe062410d426123d20fcbe050944554329e1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32530527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79a782002d75afde88daf47c99b398edb58da7b5d5cca3827577832434b8abc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:20 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:31:26 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a253dba035401f762d0613aa4d977ce12d945bc1918bfb08a17ba7331fe815`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 3.6 MB (3561049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bd3e1c5570e7cd4878353726e4bd0fe6a358ae3cd2dad02e393d59d98803f9`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 2.6 KB (2640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b495cbf000ce9a258736ce76444ca683648a9ba468ca5d3d6cfde0d8bc89402`  
		Last Modified: Thu, 13 Nov 2025 23:31:39 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a7199ab9252b8ed239c8c34dd3a013dd0b7c2c06d87c00c361824931df4c86`  
		Last Modified: Thu, 13 Nov 2025 23:31:38 GMT  
		Size: 104.6 KB (104607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5f3d14db57b4fa3eeb6cbb447024bf03395dfe359f372b7f4917ee462f439907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe6e66c6e7d0f92c843a2215edea604807c6be3f7f5ff9f9929c74d8d3d52f9`

```dockerfile
```

-	Layers:
	-	`sha256:ad647f1003e7e0dec3bdc34b289daefb923cc8e0c1305ba7b14f3a2108d14a3a`  
		Last Modified: Fri, 14 Nov 2025 02:08:10 GMT  
		Size: 2.1 MB (2121910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c6007dbe7aee0b4fb818dc38799ebc8efd1b7438bf95762182955214aecc0d`  
		Last Modified: Fri, 14 Nov 2025 02:08:11 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:184659c45ef82521389ee748e1ee4bbe1449f0946581307e3e93d86e0e058f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c299aad60e1e7f11d4286835ce579930df7f598ed9b1015fcaa7c79713c42957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33394810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ed87def879102b787b9246c739018511b4b589c34932b0ef713c6c61de668d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:32:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:15 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:16 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c0e1d7b3f111e4566e1d12f6c0632e153c201260a9826542321f8ea23bcafa`  
		Last Modified: Thu, 13 Nov 2025 23:32:28 GMT  
		Size: 3.6 MB (3562936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b40e8d70ead7cc4f0cd07dae1ee6920efb006cb20528bcc7de39094ddf9874`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5ee6c709ae7dad0afff7391eaaa68296673cf0205a608f9bce6d4f7500e650`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd86eb2b24e5478ee0f7d4c55df8e6c357a999c4083997d6162434e36abba3f`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 103.8 KB (103841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b41bb95e32d18baa23088cddd23dfe1c3c097445ffe768613d34800b4c0c5`  
		Last Modified: Thu, 13 Nov 2025 23:32:27 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:93bbbca7ef64d9156a3013b0c4e3fa3312e91da86a098db01ea9d83029661afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2465328c5c5e8df05ad265eb773fbf3e584134d29936e5a21430c0d9164a3e3`

```dockerfile
```

-	Layers:
	-	`sha256:aabcb977352301fab1d6dabefc144dcce2ebf0a3030cecf40cf83bc2aa92770b`  
		Last Modified: Fri, 14 Nov 2025 02:08:20 GMT  
		Size: 2.1 MB (2120901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82c114f49a06e6a45987c7131d46b1fe1220101c4997f7726a576f2a5543d25b`  
		Last Modified: Fri, 14 Nov 2025 02:08:21 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c6af2ae93699e738b6c0895055144b4bb347920aca7f91e4451aa75dde146236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32531089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989acad9c141ce3dcea15e9a18df4c3ea56ceedb189ef7a6b8b8dfac6823e87c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:31:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:31:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 13 Nov 2025 23:31:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 13 Nov 2025 23:32:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:32:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876648f4bcbbd9a79fe03bc85730393c6e24075dde48714e37bee27c5e932691`  
		Last Modified: Thu, 13 Nov 2025 23:32:17 GMT  
		Size: 3.6 MB (3561120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c874b0b5bacc6d952a7735777f05b95f3c5bcbe6b7f7d50b6dabee2398abad59`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660eaa03fbbddfa884bad13382570eba092d15224cbac502584ceb4f39f1bc8c`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05849e9ea827053df3f7378003dad6aefab958b313dcfc532a8b8cd4826355d`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 104.7 KB (104669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa5566c0de4309a0ef6703f3bee20e95197bb23f5d2a711b7cd280db22508a1`  
		Last Modified: Thu, 13 Nov 2025 23:32:15 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:da8153a7c5dabd74fc895825a81e69cddc07810acc5675ecc956059d31108d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71031b6901d4ed1fbb3d94ff534deb64c3c8c0902724a95d29584e35420ca5f2`

```dockerfile
```

-	Layers:
	-	`sha256:6e2ac3e4bbdc32139f4d1a5d2b49adbffdd230b9c2f1f6cbc7952707749b342d`  
		Last Modified: Fri, 14 Nov 2025 02:08:25 GMT  
		Size: 2.1 MB (2121946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:024cf6e9493f7a6f8cac5b000f292b1bc84bfbbc6fb5d69d25b04d6d3c090a55`  
		Last Modified: Fri, 14 Nov 2025 02:08:26 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:7dfc8a363c3b6e2cb32e9e2807a2a143dfae159e132d3b06b8fecac0382c67da
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
$ docker pull neurodebian@sha256:f9de03dc15e6ea47894139ca860bbb7df3077eab69fee2b7f574967ad636e9a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59673092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36ae580edbfff25806f71d9e496b6985ec835b7fd8a4331978b9aafd98429cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:02:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:02:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:02:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4a3e55a52a3bf7a028c11cdd04765722bc5909c81b4d67215b6fa19d3e51a7`  
		Last Modified: Tue, 30 Dec 2025 00:02:19 GMT  
		Size: 10.3 MB (10289887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b144061b331bab67819cd04897b89738b7005071a8f0875b77226d420effb7`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49967f5f696ae80e5840802cbcb2bd1f5e73b290f75172b8fcc962647c0538b7`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ba8cfd8ea320a2d392ad2e66f06a7a61cdee8570bad69c5e59e12d224a8bb4`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 90.3 KB (90266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55878b042946a13598f4bc44dab8bd8b5c6cf92a29a5f88dd01768154044ca34`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:542fe53f92c587702cec1372b3bafb21975558dfbeb872f904af747a99edc817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad7da224205c770167075916abace896d69b70e42afeb45c22180a13d042950`

```dockerfile
```

-	Layers:
	-	`sha256:c281aa682144cfe81a19cf027fcc803adcd513786f32a54c63545a32824764bc`  
		Last Modified: Tue, 30 Dec 2025 02:09:34 GMT  
		Size: 3.6 MB (3613069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa707ba4df079680f05d88b1e02fb0f6aa7c05fc1835434c541f175e0a0ad6c9`  
		Last Modified: Tue, 30 Dec 2025 02:09:34 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:52252804a1c2803a046b7458af3a67b1982db6f527659eaa683317a8d0704c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d283cdfd359f8c32663dc926ca67419f8a476ffbc12a174e8172b39e9d52f28d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:03:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56e05de75caf223c899f57bdb45b54d71c3938e099e2fff63698d83c6515769`  
		Last Modified: Tue, 30 Dec 2025 00:03:20 GMT  
		Size: 10.1 MB (10073442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a034755a9ced70509ae5e0173325f4fb3174e73369ad3dc2a0bc0ede6eada`  
		Last Modified: Tue, 30 Dec 2025 00:03:19 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370de170d9d2bd026322648863277da5d88439f4c023954ff3d26321f8995899`  
		Last Modified: Tue, 30 Dec 2025 00:03:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5caeb08aa3984f98b10526c397fc882cf49ca878092e1ed0a2694b29f74951`  
		Last Modified: Tue, 30 Dec 2025 00:03:25 GMT  
		Size: 90.9 KB (90916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6250ad169fb763f2e49938340ca45af94a4284570dfb659a3dd2df016500f84`  
		Last Modified: Tue, 30 Dec 2025 00:03:19 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:deaa6d6c962198eee187acdc117bcaf95cf20c5fa346b8bd13094f3981e74053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068f0dea854818442fbd9729cba1275127ce475030eba6ea6efd526437a4fb78`

```dockerfile
```

-	Layers:
	-	`sha256:892de4cfc5deb2e9340d4e17d825664258f8fa9bed32590cf1722dd856a82e8e`  
		Last Modified: Tue, 30 Dec 2025 02:09:39 GMT  
		Size: 3.6 MB (3614596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e515d0a2d41c8e48b890fe2c645ee20c1d65a39b3c49ac8c1a7315fa7e210b1`  
		Last Modified: Tue, 30 Dec 2025 02:09:39 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b187bea3f10f39ea07ee4101dc0a3f18abbe7be34d2cff2bd6f7b49e13f3155b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafef6df1ba7f540161567b41abc65dc5bdb8501cc5fbcddaf3cacc06c4bdaf2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:15:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4b33922c04dbc376b8a5e1f0f1e92e63bb89043733e9f1faa4310e1504bd7f`  
		Last Modified: Mon, 08 Dec 2025 23:15:56 GMT  
		Size: 10.5 MB (10462938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288115e75d815edb522e43eef503792b7e9e6c88509ee7e9ba4a8f7072e4f953`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641aa24ee325190ed8096c6c9438150c637d751260dc4f24335265186be298f3`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30ad08df9b38bd944f88c550208c2de69c4c644bcc8a39159b8149bbcab36a`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 90.6 KB (90624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48e15f7f8648267c2768f3207e320a23c1769e635224feb1f62bd2181b3e786`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7406b4bee75ddf498b716c53bb3d974de73215e6a867b443f199125346ea588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84d6396779efcbbaa4d5ca3717a85cea53fa601f8499d1d5e4932ecd0830673`

```dockerfile
```

-	Layers:
	-	`sha256:9689b9651a4bdf918275574dedc207d7f9b6a4d8deb9f363c0f94ac3816b45e0`  
		Last Modified: Tue, 09 Dec 2025 02:09:11 GMT  
		Size: 3.6 MB (3611018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134c12f5888db88b0afd397425b7c86d8d384dd6dcfee36c93eb7abe2abb0f15`  
		Last Modified: Tue, 09 Dec 2025 02:09:12 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:plucky`

```console
$ docker pull neurodebian@sha256:ab139e2ef8b811558941eff017d1f467deaa77fcebcdf3189633727ef717dc92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky` - linux; amd64

```console
$ docker pull neurodebian@sha256:fdc67ac4dd0d651097ba75d3f513b34e66af0bdfa85db80045d15880faf9ef04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36682742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fc9a62b14ecbd0c50b253059091a66a5c95e0809527bce9cdece2619b81e21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Tue, 02 Dec 2025 13:58:07 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d807958f6dce95c2cf132ab919d751d642e0834efea8afabde5dd80a06382164`  
		Last Modified: Tue, 23 Dec 2025 18:33:36 GMT  
		Size: 6.9 MB (6862222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d85781ba57065c27119c5b829ede85b21f4be4c79ed21b52b5dd18e69324e`  
		Last Modified: Fri, 12 Dec 2025 18:34:28 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6000f4f29de58b9c57f46bf4c2915a41aecfde0ffe93b519dc150c2e05839`  
		Last Modified: Fri, 12 Dec 2025 18:34:28 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b298e1353c735a6385e6a62cecbfe1d1b59a32feea6c006fe2970e9a377fb0`  
		Last Modified: Thu, 25 Dec 2025 08:42:10 GMT  
		Size: 103.6 KB (103644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:87fb8fcdc3533806d68ebce00bcfcf60c95a4fd2ca27173aa2131f4e12b9a92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f7aa5c68eb77711d7c5504ea0dd43319dc6ba5a495e2a39b29e42dd4613450`

```dockerfile
```

-	Layers:
	-	`sha256:34e86114d346aa4146ae590dee647494234ddff44dc9bf93ed557394aed25887`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 2.1 MB (2129387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb29516268d88fbe0487f9e71585d01a2863eda154c3b84c932731ccf47ffd8`  
		Last Modified: Thu, 09 Oct 2025 21:20:57 GMT  
		Size: 14.0 KB (13987 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:plucky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d0215dbda4b85ac69b750d98f8f3eb9aba18829cafe490ef6c04e7f1b5d3575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34803835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6196b8372a58dd339a5cd7b297736021c12b067eaa196975ee6481a581ec22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Tue, 02 Dec 2025 14:40:05 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40b8d7c0516946e6186f0c1918a80da44ccc80465d586f0db577e9c5e3fa309`  
		Last Modified: Thu, 25 Dec 2025 08:42:33 GMT  
		Size: 6.4 MB (6392372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccd7c148caa4ff621b2e8f1407d0680d8b216fd3b91aade2da4e3bcf67242ab`  
		Last Modified: Thu, 25 Dec 2025 08:42:33 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b63a7c688f7b81b2251c0096fc2033ac1c2243330fd41da718cf8002ec93dae1`  
		Last Modified: Thu, 25 Dec 2025 08:42:33 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a8bb23e4d96a15bc63dda952317ea8ba3a8efd39c025f4e5d59b26d5afc57c`  
		Last Modified: Thu, 25 Dec 2025 08:42:33 GMT  
		Size: 104.2 KB (104205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6b6e0e2468e055fd3994fdd22716a6516ca822a0b893af378cfe9b7c8c92ee14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b634830ed4e5ae3eba300cf243790465b87b6d976898e0bdc93781f17d3473b`

```dockerfile
```

-	Layers:
	-	`sha256:73f73f1097d47935c4c36115e56c20ae5811fee70906bb8d0100cacf857414df`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 2.1 MB (2129631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3369301dca599eb9decd9b13cef9db3cbe5da13f1a35be39a2983729b9cd67db`  
		Last Modified: Thu, 09 Oct 2025 21:21:52 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:plucky-non-free`

```console
$ docker pull neurodebian@sha256:843d307ce6bc09a7cd1b57e44466adef4c4764ea1c793ae5816c4c23f5fd2e42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:plucky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7e3b0aa3a1e9664cb5a8951141d1855604212beb174f638ffd32f46742ed4bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36683143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b635066dc43129e20e37c95f2235d3e316b7d3b9c2aba40f0ffde2b54e2e6e2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:5c208fb70b021afc05727d8dc78f4c389e873e38646fc0f247ced1cb261ea370 in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:c62190a9ab61c5fadad5c83c08965df006562241538b21f41b5efd457dc50ccf`  
		Last Modified: Tue, 02 Dec 2025 13:58:07 GMT  
		Size: 29.7 MB (29713967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e95813fe4718cf415f65b5a2a6aff41cf1ca472b75f81f0e71c88a2c1e75e9`  
		Last Modified: Fri, 12 Dec 2025 18:36:41 GMT  
		Size: 6.9 MB (6862197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c069ba67e04af50034555225735086ac2d283d240d8ce7e46a9d3308c6398c25`  
		Last Modified: Thu, 25 Dec 2025 08:41:48 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7163aa66b2f0788a2fd8bfb24efa8a573ed390b32865ae0266981836fb3f2a`  
		Last Modified: Fri, 19 Dec 2025 18:37:32 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4744d7aa582d29cc5ee3a878017b70e760a48aaf077eeaf1aa5c0b98f225a81b`  
		Last Modified: Tue, 09 Dec 2025 18:36:08 GMT  
		Size: 103.6 KB (103637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709942cf2f7b8bc52d31c967ec725251f89630a82eb3debdaafff34b2502aec6`  
		Last Modified: Thu, 25 Dec 2025 08:41:48 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b03d30cc46e85e007f546cd2c4a415622d8016571f0fcd74004ece8a9d69a9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b1b3d34374f9d8719267a2de2de8be8524966deb0e192f3a0d0b9e95bbf7e6`

```dockerfile
```

-	Layers:
	-	`sha256:75abe1e107a33427871261a37ffd5362e38bd76021a38d45be8b8ecfd67cf1a7`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 2.1 MB (2129423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f0d6a23d261b81b7b10446e66dbf147c195e56727be3c4c4095beb8744927b`  
		Last Modified: Thu, 09 Oct 2025 21:20:56 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:plucky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8bb52949ffdc66d1b1c45b166770d0321d7082209a408f0dde0ce50355c437d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34804334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6029e77c7f8a48311858bca5d16c501aebcd7dbababb443b3c892392f8506a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
ARG RELEASE
# Tue, 23 Sep 2025 14:32:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Sep 2025 14:32:09 GMT
LABEL org.opencontainers.image.version=25.04
# Tue, 23 Sep 2025 14:32:09 GMT
ADD file:2e32d5ba6a5a96833b0deaf9c5a7ed2559bab3a9addcff92dfe49254b9cc654e in / 
# Tue, 23 Sep 2025 14:32:09 GMT
CMD ["/bin/bash"]
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian plucky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel plucky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:49236737bff0862bb8b036b6c3ef5438b02eff6a137b08f62499d2764ac53431`  
		Last Modified: Tue, 02 Dec 2025 14:40:05 GMT  
		Size: 28.3 MB (28304343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d08ff3fe3897ede8ef5bf7e75a8c754e9da90066ad638138411914e6569fcb`  
		Last Modified: Thu, 25 Dec 2025 08:42:23 GMT  
		Size: 6.4 MB (6392412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87458cf3c50f45fec6029a8e2d31f7dc2c30d63c5e92c7e4f4d7ddbf1fd1fb4`  
		Last Modified: Thu, 25 Dec 2025 08:42:22 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fabfa39ef821d160c97bf91453f07634d072ad956ea83de4da94873f2b71a97`  
		Last Modified: Thu, 25 Dec 2025 08:42:23 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9d80fbf3cdda43cd93b73ef0b7215c959689c5073a718bc28b1a88b435aeda`  
		Last Modified: Thu, 25 Dec 2025 08:42:23 GMT  
		Size: 104.2 KB (104235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3181f804aca7e1622946b1391b32ee30ccebfbdb03426caab02bcd300d54cd8b`  
		Last Modified: Thu, 25 Dec 2025 08:42:23 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:plucky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:29ea36baad60d33ffbfb5fd8152d415e121532b4008b174a68251c71851548a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5656dffee277d964d7af531bee03d767b53dc21bddc33bbedf5b7d1e0c3a1668`

```dockerfile
```

-	Layers:
	-	`sha256:a897c9f03a98ed8cc43baa74786f9234dccd6f6c51fe452db7dab397fb9c66a0`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 2.1 MB (2129667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0912356738dd5be0731ed4354e13efdb3bb03dfc003407132e1ed93bde4ad42a`  
		Last Modified: Thu, 09 Oct 2025 21:22:06 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:e21fa53efda88c069dd1c2878a1b2f28855ae3ee762fde42098e7d168170874e
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
$ docker pull neurodebian@sha256:035b7f627535f4f213b8df77e7501d898cb8535b31d3b0ea9ec6190b526c72e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60527446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0620c75bef2ca94f3e2085bef9f7b070219d80eea5f03cb046e443a39f5142`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:04:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36a4985327850927961426bc6fcb1fb8dc1f9b5e7f69f8061c7daf2f4aee58a7`  
		Last Modified: Mon, 29 Dec 2025 22:29:41 GMT  
		Size: 48.8 MB (48821118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2afb24b11b414a91690e2de9e1bbf94e8ef9c750303e10a1f474612a1608bc`  
		Last Modified: Tue, 30 Dec 2025 00:04:23 GMT  
		Size: 11.6 MB (11613260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f117d692e9d33c678c15a431856f5a53a13f3a6dad3cfb64ccb90d53565b68`  
		Last Modified: Tue, 30 Dec 2025 00:04:22 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fe440ad283dfa1ff5bc20d76a5aa1943e3a0725babf9323e9f7a8952a30b8`  
		Last Modified: Tue, 30 Dec 2025 00:04:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778a5fe0dc6f45c67af4e740f0b16570ab7430e78dec361704c0dba2c7ea76b0`  
		Last Modified: Tue, 30 Dec 2025 00:04:22 GMT  
		Size: 90.2 KB (90165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f63b8514f32c1fa215e0e8aba690d5e7f4a1973d624c81ae66df879b1946506c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8190f725cf92a2460e1c1a62399edd64257b02d78eb697d0b072a2334c250c5a`

```dockerfile
```

-	Layers:
	-	`sha256:d736499878e3cfd7bfcde74cbf7a0c4d6ab9912f74fe399ac8ede60eacd6a960`  
		Last Modified: Tue, 30 Dec 2025 02:09:06 GMT  
		Size: 3.6 MB (3589915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb93f903cb7d91c8b2fa32e73adc52adb5dc551b0c5b78c36b7ac7d1501e204`  
		Last Modified: Tue, 30 Dec 2025 02:09:07 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b0cbcd07d5581034cf518ae998bf872b0fa8fc1dddbc5199ead7b0b2e16ce097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60160061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1a53b3bdb4de5c84e64777050843a0aa26b83af4ef0f1bf919ba80c7fd612e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:04:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e81a19d37d9900498b0ca8a841e2e3fe3dfde06146f7d10d1e71e1df7a8ae8ab`  
		Last Modified: Mon, 29 Dec 2025 22:29:24 GMT  
		Size: 48.8 MB (48801029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f99e5f3335c2ff6d9abb774351bfb55d384d817ade2187270b9fe3558779b90`  
		Last Modified: Tue, 30 Dec 2025 00:04:53 GMT  
		Size: 11.3 MB (11265267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347a2a6ce4512291bdc3028015b54c7df8357a7fdb3630aecd4a3a33d44e4fd`  
		Last Modified: Tue, 30 Dec 2025 00:04:52 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb44e37c3ff6fd90ab92d83969c35acdcfe3f7adaf5820e89aa01d683814c5ba`  
		Last Modified: Tue, 30 Dec 2025 00:04:52 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15704ec8aa9e145af8c6e5e21f510adeeed85f82e7d9a5f45154a9b0bf54f18`  
		Last Modified: Tue, 30 Dec 2025 00:04:52 GMT  
		Size: 90.9 KB (90864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:06ec310696b16f7e4166904a3ae30305fd9b5fd8d88454fcca2fd4971032862f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3604820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8beb211810ee03db5a4aa15f811c77314d39d61a9836ec43ddda805e26c7fed`

```dockerfile
```

-	Layers:
	-	`sha256:c6d26cb601684ef686b4ef4357a1051102513ec62e85fa194fca69df15f5438f`  
		Last Modified: Tue, 30 Dec 2025 02:09:11 GMT  
		Size: 3.6 MB (3590791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4295813137038125b1d76dbc6634cf4378020e2cdb7ad404da9ecb210548650`  
		Last Modified: Tue, 30 Dec 2025 02:09:12 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:8f5cfc00500cc0d446db7aa634f75cf84b12afe95e95ebdb31af23e36dd652c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61813318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574cb528275d8e08c0c2aba8f98ebea411e3d9e83b8666ec032897e9890a4e3b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:15:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:16:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:67f7fae0ea3bb931c627a66604e60b0a242047b0c8f9186d188cf96e0133593f`  
		Last Modified: Mon, 08 Dec 2025 22:16:33 GMT  
		Size: 49.9 MB (49947966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0266c0513022413f6a42ac8de173ef0db6a7fd70a6d1859fdaee0ff7c1f1a52`  
		Last Modified: Mon, 08 Dec 2025 23:16:17 GMT  
		Size: 11.8 MB (11771438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54d5b89513ee9aefb4cbaeb149aac108b65168fa8016ced6820617134e33cc7`  
		Last Modified: Mon, 08 Dec 2025 23:16:16 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44066a3eb12e5a62aeb429ee8e2fa4e039a016510b0053f5b6d5a21937982b57`  
		Last Modified: Mon, 08 Dec 2025 23:16:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469a39499ff4a4700821efc8a4595a0a54ee4dd2c440d4d7d1bd6a635aeb8f41`  
		Last Modified: Mon, 08 Dec 2025 23:16:16 GMT  
		Size: 91.0 KB (91009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:683dbe22bfe3d344489dcd587c30032ec24bcc1eec3ddd9dc64298a5a3b44fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d30d3a82ccd78c8e1f82eefd7dd5e1a1c671e68a0c3acffd7baa9d15c330adc`

```dockerfile
```

-	Layers:
	-	`sha256:61532c3563e04ec54407712519658270da6406a9e32a333a448571a3a74f36e1`  
		Last Modified: Tue, 09 Dec 2025 02:08:41 GMT  
		Size: 3.6 MB (3589161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce849a1ac7c09b2ee06fbd7089981ce600c9dc4944c42e11cbeaf60a93c90dbb`  
		Last Modified: Tue, 09 Dec 2025 02:08:41 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:4c47943431a034a06d6528a4199cece13a394a2b96aeb031b6674e306a5e8e8d
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
$ docker pull neurodebian@sha256:8e836983d8ef8af9b77b72e439f8c371405a985ae951915e508cacdf4a304887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60527842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8bd8e109166c8ab6131500dc2a65312eb0f2e7a0531b090d7e5c49e83624e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:04:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:36a4985327850927961426bc6fcb1fb8dc1f9b5e7f69f8061c7daf2f4aee58a7`  
		Last Modified: Mon, 29 Dec 2025 22:29:41 GMT  
		Size: 48.8 MB (48821118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a76feb401b8397b66d8f4ee4936caf4ce66640e5ad62ce2473a4370b983974e`  
		Last Modified: Tue, 30 Dec 2025 00:04:46 GMT  
		Size: 11.6 MB (11613267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4349a5f502c1a41bee3f9bf35364bcf75672e22eea699cf80c9742688a9bdd9`  
		Last Modified: Tue, 30 Dec 2025 00:04:44 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1275f6a063430aa6e6996dcdd80dc6350cd45a3c55323e8c72a3d7f93c7ab857`  
		Last Modified: Tue, 30 Dec 2025 00:04:44 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecf663483821f0c91f02e7906d1438595ba40438f653018436cb2c42eead2c0`  
		Last Modified: Tue, 30 Dec 2025 00:04:44 GMT  
		Size: 90.1 KB (90133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01e8ccfe03ffa296f783478d077dbf0dc04351cd9d661d0d11173bdf4d7bbb5`  
		Last Modified: Tue, 30 Dec 2025 00:04:44 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e2dde03b8446743a564589f52ad69e2183a9252feb374a8e65c51d5759d9b6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9f3512fc510055e8351d926027811d826fe487e04bcbe47540f3aa04f22947`

```dockerfile
```

-	Layers:
	-	`sha256:3bf02161c82deaa0c916d8c52dc679930df16850c8f23833ee058f9e94dd5bba`  
		Last Modified: Tue, 30 Dec 2025 02:09:14 GMT  
		Size: 3.6 MB (3589951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4666962ca4a0e7945f18ef88ea3a1626cacb025b5f89518de52002eede6468f7`  
		Last Modified: Tue, 30 Dec 2025 02:09:17 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a517ce131a941205f708b3d0db016d341984a51a9da4b10a3a4f792a41b64302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60160491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59cd14e3fa38d095e6db623d1c695f978b5d759f00906273db739db2e07ccc0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:04:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:55 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:59 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e81a19d37d9900498b0ca8a841e2e3fe3dfde06146f7d10d1e71e1df7a8ae8ab`  
		Last Modified: Mon, 29 Dec 2025 22:29:24 GMT  
		Size: 48.8 MB (48801029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834c8f50bd273c3b0a7e017c0b2cad1be20ff06b111037ed997e1b7e6c74d504`  
		Last Modified: Tue, 30 Dec 2025 00:05:15 GMT  
		Size: 11.3 MB (11265282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3d5914282d0f6ff41770baa19a5d797df7b98ceee7055fe0306a26b4b0cc90`  
		Last Modified: Tue, 30 Dec 2025 00:05:14 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7c39fcf0f25e352a9f478db51398f77c3977758ef5e7f4651da4740f38b6e5`  
		Last Modified: Tue, 30 Dec 2025 00:05:14 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac86f94f45a5f89d87e751860014d3c51dafdc0cceb4980f31e30c5154808f95`  
		Last Modified: Tue, 30 Dec 2025 00:05:14 GMT  
		Size: 90.9 KB (90856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4149473e2827caf5858b119dccfd23f16d508c25dadd652c6dc5402c067a013c`  
		Last Modified: Tue, 30 Dec 2025 00:05:20 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1fb1bd97e59cf21d0763d7ec666274764119ad57b35bfa3ae21a888a6b6ab2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b617c4be66c925f9ed0de633f487fd9131079ab60e35c2b1f0e31bc1b0dca1`

```dockerfile
```

-	Layers:
	-	`sha256:f48cef6f3cfd0ca31efc667f4faed7db31163b52a638ba7e96feae0b216d00fe`  
		Last Modified: Tue, 30 Dec 2025 02:09:20 GMT  
		Size: 3.6 MB (3590827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89bee813be1895a2e6cbc85ebbcc9b2756e96af992934777f53b651b4667b93b`  
		Last Modified: Tue, 30 Dec 2025 02:09:21 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:49afcad16d105fd19bae60cd14158c11b083cd49993f77a1b4f650c6ab293be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61813645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23040b5c36dbefc61179d2d7deeda5abfc71fea09f198c632c1abe65282f03b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:16:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:16:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:16:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:16:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:16:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:67f7fae0ea3bb931c627a66604e60b0a242047b0c8f9186d188cf96e0133593f`  
		Last Modified: Mon, 08 Dec 2025 22:16:33 GMT  
		Size: 49.9 MB (49947966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec12c3df770257e87a24e89f178be2debdfa70110f149c64f33fafe3e06b0bb2`  
		Last Modified: Mon, 08 Dec 2025 23:16:29 GMT  
		Size: 11.8 MB (11771378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d9aa372e7ef553d58fcd21aed06e967b22c56495ff93ff4db7ba9cb7dded3a`  
		Last Modified: Mon, 08 Dec 2025 23:16:28 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a6aa5a510c3bbd9a734f2af4a0f01c08b189f9964f11c3f81c91174367bb1`  
		Last Modified: Mon, 08 Dec 2025 23:16:28 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca5f7bb75d5cb357f3cf6974aea0182f5878e2b95b614c8d4f0d1ccd309cd70`  
		Last Modified: Mon, 08 Dec 2025 23:16:28 GMT  
		Size: 91.0 KB (90977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137b22bdee3d72723ee405aadd32bb53c6338c92f8ef80e18f5a70cd443b75dc`  
		Last Modified: Mon, 08 Dec 2025 23:16:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3da97abc8582eb66115af61c24725caeb2eb08ae525671a2c9180458e24c5623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f369991e4501a6c1095ea76a75182086694a3acce7d86fbe1e9e5cf75cf0e27`

```dockerfile
```

-	Layers:
	-	`sha256:807a054d1fbda6da8789823823c4862f08b246f336bc67bc357a9a4fcc45dfdd`  
		Last Modified: Tue, 09 Dec 2025 02:08:48 GMT  
		Size: 3.6 MB (3589197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e54569f675797e675d8e53c2f3cbb7f2e4ed87ed2af17c0cc005af7d6f08535`  
		Last Modified: Tue, 09 Dec 2025 02:08:49 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:e0b772fb6c8cbf95b4bbc89d59fce54bd4612bea788c25876003179d85a81dc2
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
$ docker pull neurodebian@sha256:11704eb3e9e87e0bfc0474ec7993332f1a5446fd8fcfb93d5bfa76ddf865487a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59672470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfbefed7e757187bdc0ba33ca6e231ba0ab03e1d8c01c26ec51bffb858b7f8b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:01:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:01:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:01:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:01:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9170e174478fb49afad823cff539b37cc66f46900a7285d0980c69545228ad17`  
		Last Modified: Tue, 30 Dec 2025 00:01:57 GMT  
		Size: 10.3 MB (10289740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98cfd6b6685e00247a8830717622cc76428a34a65ea509838b1ef1cf5f05c74`  
		Last Modified: Tue, 30 Dec 2025 00:01:56 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c93be1b43a47437859927119984568576e4e7035c09a3328ef782132ad5794`  
		Last Modified: Tue, 30 Dec 2025 00:01:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3130c56d9674187b01ccfa85c055fa9f25023403e80cc08d3bd3fedb46556a5e`  
		Last Modified: Tue, 30 Dec 2025 00:01:56 GMT  
		Size: 90.2 KB (90240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1fb327732ae3459a5ace9ae68da17e6b718a91b6edec2e4ba30e8a6c1ce4cc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dafd6febb344bc094cee781197ce68c717521a93152c82a6b3faef2618045e4`

```dockerfile
```

-	Layers:
	-	`sha256:a4c38d6616572e011521486de1ca5c77b753c05e8ac2873b363b81ebd8663c8b`  
		Last Modified: Tue, 30 Dec 2025 02:08:59 GMT  
		Size: 3.6 MB (3613029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e815c9c1e880979ed5797e8604eda18f89cdbc2a0f33a15aa08c9c99c1babfe2`  
		Last Modified: Tue, 30 Dec 2025 02:08:59 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f08af078412593f5e90c7ccc438b36a60853c367d5b1c02977191e59b42e2140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc02347a607123200510623e11328eccf357ded43e2b4c688cf6f3cbd87d6cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:02:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:02:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809d9a2a116ddb1b5044a05d97a74f3b666af6ebf3396b8bd1959b09b2c1dd97`  
		Last Modified: Tue, 30 Dec 2025 00:02:25 GMT  
		Size: 10.1 MB (10073354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43bf434a486a4ffeb412351889920cd853dafb22023f8b56041c1f5d9551def`  
		Last Modified: Tue, 30 Dec 2025 00:02:23 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fc09b5259d60baa90e66794a8eee4353a12a09741ddf610bc593a7d1a33885`  
		Last Modified: Tue, 30 Dec 2025 00:02:23 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d0d5e7c0fe7290044e8a33d358ea3fb2637f4a077ae7d449ac0eda02e54e27`  
		Last Modified: Tue, 30 Dec 2025 00:02:23 GMT  
		Size: 90.9 KB (90861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f741d89d851cb0175bc345ebf91d0267a3fd846824aff01df647a8423163d3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa99d1b3e6f5e16c3a14b8a2671503fc5c6d885230e3d8d99a1e1783b14e6c5a`

```dockerfile
```

-	Layers:
	-	`sha256:3e2489caeeb90f29d36cf18405d9c354b196ce6768875a219a8c2483595e7b82`  
		Last Modified: Tue, 30 Dec 2025 02:09:03 GMT  
		Size: 3.6 MB (3614556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6028461904b5f9e69fd501748e03c048131c821c768f588bfb954e678cb0680`  
		Last Modified: Tue, 30 Dec 2025 02:09:04 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:c8dc1f5965291d82532beb930b4b8dd9d2857dcffb348f41946ce7525f9d1868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4224f54fb533cad2f8b9b30d2e785eb1fd843e4fd63e905343da0c070c075d03`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:15:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e964d190139b1aba3de28d11b605a95f92489da3beb9d80e9099db336eb72530`  
		Last Modified: Mon, 08 Dec 2025 23:15:43 GMT  
		Size: 10.5 MB (10463020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ec584c96f35b189d796255e99284eb2b5a60beac79d3aa5e9e38511057c721`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9b780ecf3cdbfe9614a0f6fb11f3ac440968fc9859f8381cdd325606eb10d5`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e72d44ba44c44786256e5c59963306628e9bc4225d957dc3c3f88b69404871`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 90.6 KB (90608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8feb71ee0324566413295afd412d3e8536f97cd4923d4b4e3a66a630eb6b5e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f48fe17c7803c7f0a740da48d64460f0e14b205e6ef00e468dd25f6d417492`

```dockerfile
```

-	Layers:
	-	`sha256:6565d47d0408e99891700b9f73772b468617ffa2decbf66dd47aa2f3825e0c46`  
		Last Modified: Tue, 09 Dec 2025 02:08:59 GMT  
		Size: 3.6 MB (3610978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928694ae3cbda82a9b5864d3bb2e6e8cc4bfd721706dd53996bd42268ab412db`  
		Last Modified: Tue, 09 Dec 2025 02:09:00 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:7dfc8a363c3b6e2cb32e9e2807a2a143dfae159e132d3b06b8fecac0382c67da
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
$ docker pull neurodebian@sha256:f9de03dc15e6ea47894139ca860bbb7df3077eab69fee2b7f574967ad636e9a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59673092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f36ae580edbfff25806f71d9e496b6985ec835b7fd8a4331978b9aafd98429cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:02:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:02:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:02:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:02:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4a3e55a52a3bf7a028c11cdd04765722bc5909c81b4d67215b6fa19d3e51a7`  
		Last Modified: Tue, 30 Dec 2025 00:02:19 GMT  
		Size: 10.3 MB (10289887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b144061b331bab67819cd04897b89738b7005071a8f0875b77226d420effb7`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49967f5f696ae80e5840802cbcb2bd1f5e73b290f75172b8fcc962647c0538b7`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ba8cfd8ea320a2d392ad2e66f06a7a61cdee8570bad69c5e59e12d224a8bb4`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 90.3 KB (90266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55878b042946a13598f4bc44dab8bd8b5c6cf92a29a5f88dd01768154044ca34`  
		Last Modified: Tue, 30 Dec 2025 00:02:17 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:542fe53f92c587702cec1372b3bafb21975558dfbeb872f904af747a99edc817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad7da224205c770167075916abace896d69b70e42afeb45c22180a13d042950`

```dockerfile
```

-	Layers:
	-	`sha256:c281aa682144cfe81a19cf027fcc803adcd513786f32a54c63545a32824764bc`  
		Last Modified: Tue, 30 Dec 2025 02:09:34 GMT  
		Size: 3.6 MB (3613069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa707ba4df079680f05d88b1e02fb0f6aa7c05fc1835434c541f175e0a0ad6c9`  
		Last Modified: Tue, 30 Dec 2025 02:09:34 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:52252804a1c2803a046b7458af3a67b1982db6f527659eaa683317a8d0704c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d283cdfd359f8c32663dc926ca67419f8a476ffbc12a174e8172b39e9d52f28d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:03:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:03:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:03:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:03:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56e05de75caf223c899f57bdb45b54d71c3938e099e2fff63698d83c6515769`  
		Last Modified: Tue, 30 Dec 2025 00:03:20 GMT  
		Size: 10.1 MB (10073442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627a034755a9ced70509ae5e0173325f4fb3174e73369ad3dc2a0bc0ede6eada`  
		Last Modified: Tue, 30 Dec 2025 00:03:19 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:370de170d9d2bd026322648863277da5d88439f4c023954ff3d26321f8995899`  
		Last Modified: Tue, 30 Dec 2025 00:03:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5caeb08aa3984f98b10526c397fc882cf49ca878092e1ed0a2694b29f74951`  
		Last Modified: Tue, 30 Dec 2025 00:03:25 GMT  
		Size: 90.9 KB (90916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6250ad169fb763f2e49938340ca45af94a4284570dfb659a3dd2df016500f84`  
		Last Modified: Tue, 30 Dec 2025 00:03:19 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:deaa6d6c962198eee187acdc117bcaf95cf20c5fa346b8bd13094f3981e74053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068f0dea854818442fbd9729cba1275127ce475030eba6ea6efd526437a4fb78`

```dockerfile
```

-	Layers:
	-	`sha256:892de4cfc5deb2e9340d4e17d825664258f8fa9bed32590cf1722dd856a82e8e`  
		Last Modified: Tue, 30 Dec 2025 02:09:39 GMT  
		Size: 3.6 MB (3614596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e515d0a2d41c8e48b890fe2c645ee20c1d65a39b3c49ac8c1a7315fa7e210b1`  
		Last Modified: Tue, 30 Dec 2025 02:09:39 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b187bea3f10f39ea07ee4101dc0a3f18abbe7be34d2cff2bd6f7b49e13f3155b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafef6df1ba7f540161567b41abc65dc5bdb8501cc5fbcddaf3cacc06c4bdaf2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:15:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4b33922c04dbc376b8a5e1f0f1e92e63bb89043733e9f1faa4310e1504bd7f`  
		Last Modified: Mon, 08 Dec 2025 23:15:56 GMT  
		Size: 10.5 MB (10462938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288115e75d815edb522e43eef503792b7e9e6c88509ee7e9ba4a8f7072e4f953`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641aa24ee325190ed8096c6c9438150c637d751260dc4f24335265186be298f3`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30ad08df9b38bd944f88c550208c2de69c4c644bcc8a39159b8149bbcab36a`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 90.6 KB (90624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48e15f7f8648267c2768f3207e320a23c1769e635224feb1f62bd2181b3e786`  
		Last Modified: Mon, 08 Dec 2025 23:15:54 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7406b4bee75ddf498b716c53bb3d974de73215e6a867b443f199125346ea588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84d6396779efcbbaa4d5ca3717a85cea53fa601f8499d1d5e4932ecd0830673`

```dockerfile
```

-	Layers:
	-	`sha256:9689b9651a4bdf918275574dedc207d7f9b6a4d8deb9f363c0f94ac3816b45e0`  
		Last Modified: Tue, 09 Dec 2025 02:09:11 GMT  
		Size: 3.6 MB (3611018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134c12f5888db88b0afd397425b7c86d8d384dd6dcfee36c93eb7abe2abb0f15`  
		Last Modified: Tue, 09 Dec 2025 02:09:12 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
