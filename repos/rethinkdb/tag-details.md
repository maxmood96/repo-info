<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2-bookworm-slim`](#rethinkdb2-bookworm-slim)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4-bookworm-slim`](#rethinkdb24-bookworm-slim)
-	[`rethinkdb:2.4.3`](#rethinkdb243)
-	[`rethinkdb:2.4.4-bookworm-slim`](#rethinkdb244-bookworm-slim)
-	[`rethinkdb:bookworm-slim`](#rethinkdbbookworm-slim)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:0c87ac98f37f5ade72c5c4218189b2c7b7093817f37ce8954331214374a8db8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7a460ebfaf3049f5f52c46c822d8b21138c794f3871051b27c9afc1365bb47ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8287eec78c315282f752db1658b3156424a228cc01ce9b7026619e6dcce73fd7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:41:11 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:41:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:41:18 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:41:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:41:18 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4832f674ae7f81aefe4e388501bb4d922ad428ada50502a664e559b7e27b26bc`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 9.8 MB (9797406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977c35c08a5797b9e4a33bf3fb238215a8db6e39e14eafeb32b215c662ab87e`  
		Last Modified: Mon, 29 Dec 2025 23:41:31 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215d0d78f358a516da03ebf61b4e4bc3fbe9ccd8ba23a6bc0c1cbb579bf03e9`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 10.0 MB (9993054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af971e9a86801f69b70f2ac8e0ee675a82f433d06705075b6463be351c61354e`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:5cd590de0ac457b6bc7965d1327964460074a67fa93a9a7657048f221736f739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c42bfe7553bc21a8144114b0378a9e9bd73798ed69edbb8e1de4f165b1860c9`

```dockerfile
```

-	Layers:
	-	`sha256:ca20cd0f2cd2cb7542ea12bb9fbe12e7ca047fac8bbd51ad1c06c00155542fed`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64df6df3a8534aaf2ca9b3f6d5432244dd0004bc0f4601af0947de13efe6bfb`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:1b8639b5e386183659fba21589e268b76fcf47cf507612ddf695fae3a3a88bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5a1416112ef012e36e5f8d3be9aa54d57077596c95cf7bf4d6e7f5fdaa7a40`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:43:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:03 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:43:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:43:09 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:43:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:43:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81811df2764e9bacc9abe1ef6a9f8d86b5433fa241ab42a66388de265138b850`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.6 MB (9627867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351eec8c6b5887c984f0da09b28cfdac4ab3c4eb114213b5b9675d4f46414781`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 2.7 KB (2664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa70e611204c36424b485de7ab3a856d78907c4e9e804fb7a426400049568419`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.4 MB (9362967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d589ac0e447a384a106f6f0b7b47bb058cffa595668cbfe28bc799af0be`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:d317ca27aab510e0ca4f821993d7f9f5dbb597094a30bcb84653fd5961725ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4c162bebf2e83a25b00b8983b9e6100799313ce45d9ad550f8301276054529`

```dockerfile
```

-	Layers:
	-	`sha256:eb8290e8b26202420a09b1c8af34b7223a1242257df405f90c40ee9c5e5c5dfa`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124851da9d31c929d0034f3ee849d14104dbef464d87d6814b0cd933306fd98c`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 13.6 KB (13584 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:390a58811e17be80cb4ca3b97bb38b1e417402304726b9b76f01192e942590bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c930322a04e93088e71a73aabb6c42c24879feba61a402a3aff7a0641fb6ac6d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:37:03 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:05 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 30 Dec 2025 00:37:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
VOLUME [/data]
# Tue, 30 Dec 2025 00:37:09 GMT
WORKDIR /data
# Tue, 30 Dec 2025 00:37:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 30 Dec 2025 00:37:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5562933824310e1cbf2b5b7d292290f835858aaf213b7d7f805eca83d623e67`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04cced1892bd5ff40dc3e30507764248d87a97486c0a331d0119b8d58016b09`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b65f6c4c6c502de05c984709ecd87bba0f4f447fd76edc815a89379ea463ba5`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9303717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f5f646224922110dc1afca90434df6ceb9968ed3cfe48fd68ff10b6c19d215`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:eb945fe1eed56013ebe8c3a1aaf4d08a2f8a2ca9fd09ac0a49639f5de9706153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b6180b1bd7b5d7142deb96ac83c8ef19ebe01e27e7a2eabe2b5e7f5c668e8b`

```dockerfile
```

-	Layers:
	-	`sha256:b86ad88ea813140162109c96c8bb58e0dbb2ccd4d1c252557252056438a91918`  
		Last Modified: Tue, 30 Dec 2025 02:04:11 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7a5481318b7863846d52233fea67774bc918ab95503b85ffdfa42ffdb5a2b2`  
		Last Modified: Tue, 30 Dec 2025 02:04:12 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:0c87ac98f37f5ade72c5c4218189b2c7b7093817f37ce8954331214374a8db8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7a460ebfaf3049f5f52c46c822d8b21138c794f3871051b27c9afc1365bb47ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8287eec78c315282f752db1658b3156424a228cc01ce9b7026619e6dcce73fd7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:41:11 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:41:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:41:18 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:41:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:41:18 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4832f674ae7f81aefe4e388501bb4d922ad428ada50502a664e559b7e27b26bc`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 9.8 MB (9797406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977c35c08a5797b9e4a33bf3fb238215a8db6e39e14eafeb32b215c662ab87e`  
		Last Modified: Mon, 29 Dec 2025 23:41:31 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215d0d78f358a516da03ebf61b4e4bc3fbe9ccd8ba23a6bc0c1cbb579bf03e9`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 10.0 MB (9993054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af971e9a86801f69b70f2ac8e0ee675a82f433d06705075b6463be351c61354e`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:5cd590de0ac457b6bc7965d1327964460074a67fa93a9a7657048f221736f739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c42bfe7553bc21a8144114b0378a9e9bd73798ed69edbb8e1de4f165b1860c9`

```dockerfile
```

-	Layers:
	-	`sha256:ca20cd0f2cd2cb7542ea12bb9fbe12e7ca047fac8bbd51ad1c06c00155542fed`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64df6df3a8534aaf2ca9b3f6d5432244dd0004bc0f4601af0947de13efe6bfb`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:1b8639b5e386183659fba21589e268b76fcf47cf507612ddf695fae3a3a88bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5a1416112ef012e36e5f8d3be9aa54d57077596c95cf7bf4d6e7f5fdaa7a40`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:43:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:03 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:43:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:43:09 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:43:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:43:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81811df2764e9bacc9abe1ef6a9f8d86b5433fa241ab42a66388de265138b850`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.6 MB (9627867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351eec8c6b5887c984f0da09b28cfdac4ab3c4eb114213b5b9675d4f46414781`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 2.7 KB (2664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa70e611204c36424b485de7ab3a856d78907c4e9e804fb7a426400049568419`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.4 MB (9362967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d589ac0e447a384a106f6f0b7b47bb058cffa595668cbfe28bc799af0be`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:d317ca27aab510e0ca4f821993d7f9f5dbb597094a30bcb84653fd5961725ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4c162bebf2e83a25b00b8983b9e6100799313ce45d9ad550f8301276054529`

```dockerfile
```

-	Layers:
	-	`sha256:eb8290e8b26202420a09b1c8af34b7223a1242257df405f90c40ee9c5e5c5dfa`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124851da9d31c929d0034f3ee849d14104dbef464d87d6814b0cd933306fd98c`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 13.6 KB (13584 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:390a58811e17be80cb4ca3b97bb38b1e417402304726b9b76f01192e942590bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c930322a04e93088e71a73aabb6c42c24879feba61a402a3aff7a0641fb6ac6d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:37:03 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:05 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 30 Dec 2025 00:37:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
VOLUME [/data]
# Tue, 30 Dec 2025 00:37:09 GMT
WORKDIR /data
# Tue, 30 Dec 2025 00:37:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 30 Dec 2025 00:37:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5562933824310e1cbf2b5b7d292290f835858aaf213b7d7f805eca83d623e67`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04cced1892bd5ff40dc3e30507764248d87a97486c0a331d0119b8d58016b09`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b65f6c4c6c502de05c984709ecd87bba0f4f447fd76edc815a89379ea463ba5`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9303717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f5f646224922110dc1afca90434df6ceb9968ed3cfe48fd68ff10b6c19d215`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:eb945fe1eed56013ebe8c3a1aaf4d08a2f8a2ca9fd09ac0a49639f5de9706153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b6180b1bd7b5d7142deb96ac83c8ef19ebe01e27e7a2eabe2b5e7f5c668e8b`

```dockerfile
```

-	Layers:
	-	`sha256:b86ad88ea813140162109c96c8bb58e0dbb2ccd4d1c252557252056438a91918`  
		Last Modified: Tue, 30 Dec 2025 02:04:11 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7a5481318b7863846d52233fea67774bc918ab95503b85ffdfa42ffdb5a2b2`  
		Last Modified: Tue, 30 Dec 2025 02:04:12 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:0c87ac98f37f5ade72c5c4218189b2c7b7093817f37ce8954331214374a8db8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7a460ebfaf3049f5f52c46c822d8b21138c794f3871051b27c9afc1365bb47ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8287eec78c315282f752db1658b3156424a228cc01ce9b7026619e6dcce73fd7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:41:11 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:41:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:41:18 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:41:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:41:18 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4832f674ae7f81aefe4e388501bb4d922ad428ada50502a664e559b7e27b26bc`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 9.8 MB (9797406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977c35c08a5797b9e4a33bf3fb238215a8db6e39e14eafeb32b215c662ab87e`  
		Last Modified: Mon, 29 Dec 2025 23:41:31 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215d0d78f358a516da03ebf61b4e4bc3fbe9ccd8ba23a6bc0c1cbb579bf03e9`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 10.0 MB (9993054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af971e9a86801f69b70f2ac8e0ee675a82f433d06705075b6463be351c61354e`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:5cd590de0ac457b6bc7965d1327964460074a67fa93a9a7657048f221736f739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c42bfe7553bc21a8144114b0378a9e9bd73798ed69edbb8e1de4f165b1860c9`

```dockerfile
```

-	Layers:
	-	`sha256:ca20cd0f2cd2cb7542ea12bb9fbe12e7ca047fac8bbd51ad1c06c00155542fed`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64df6df3a8534aaf2ca9b3f6d5432244dd0004bc0f4601af0947de13efe6bfb`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:1b8639b5e386183659fba21589e268b76fcf47cf507612ddf695fae3a3a88bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5a1416112ef012e36e5f8d3be9aa54d57077596c95cf7bf4d6e7f5fdaa7a40`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:43:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:03 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:43:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:43:09 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:43:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:43:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81811df2764e9bacc9abe1ef6a9f8d86b5433fa241ab42a66388de265138b850`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.6 MB (9627867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351eec8c6b5887c984f0da09b28cfdac4ab3c4eb114213b5b9675d4f46414781`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 2.7 KB (2664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa70e611204c36424b485de7ab3a856d78907c4e9e804fb7a426400049568419`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.4 MB (9362967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d589ac0e447a384a106f6f0b7b47bb058cffa595668cbfe28bc799af0be`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:d317ca27aab510e0ca4f821993d7f9f5dbb597094a30bcb84653fd5961725ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4c162bebf2e83a25b00b8983b9e6100799313ce45d9ad550f8301276054529`

```dockerfile
```

-	Layers:
	-	`sha256:eb8290e8b26202420a09b1c8af34b7223a1242257df405f90c40ee9c5e5c5dfa`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124851da9d31c929d0034f3ee849d14104dbef464d87d6814b0cd933306fd98c`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 13.6 KB (13584 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; s390x

```console
$ docker pull rethinkdb@sha256:390a58811e17be80cb4ca3b97bb38b1e417402304726b9b76f01192e942590bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c930322a04e93088e71a73aabb6c42c24879feba61a402a3aff7a0641fb6ac6d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:37:03 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:05 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 30 Dec 2025 00:37:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
VOLUME [/data]
# Tue, 30 Dec 2025 00:37:09 GMT
WORKDIR /data
# Tue, 30 Dec 2025 00:37:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 30 Dec 2025 00:37:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5562933824310e1cbf2b5b7d292290f835858aaf213b7d7f805eca83d623e67`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04cced1892bd5ff40dc3e30507764248d87a97486c0a331d0119b8d58016b09`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b65f6c4c6c502de05c984709ecd87bba0f4f447fd76edc815a89379ea463ba5`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9303717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f5f646224922110dc1afca90434df6ceb9968ed3cfe48fd68ff10b6c19d215`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:eb945fe1eed56013ebe8c3a1aaf4d08a2f8a2ca9fd09ac0a49639f5de9706153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b6180b1bd7b5d7142deb96ac83c8ef19ebe01e27e7a2eabe2b5e7f5c668e8b`

```dockerfile
```

-	Layers:
	-	`sha256:b86ad88ea813140162109c96c8bb58e0dbb2ccd4d1c252557252056438a91918`  
		Last Modified: Tue, 30 Dec 2025 02:04:11 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7a5481318b7863846d52233fea67774bc918ab95503b85ffdfa42ffdb5a2b2`  
		Last Modified: Tue, 30 Dec 2025 02:04:12 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:0c87ac98f37f5ade72c5c4218189b2c7b7093817f37ce8954331214374a8db8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7a460ebfaf3049f5f52c46c822d8b21138c794f3871051b27c9afc1365bb47ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8287eec78c315282f752db1658b3156424a228cc01ce9b7026619e6dcce73fd7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:41:11 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:41:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:41:18 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:41:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:41:18 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4832f674ae7f81aefe4e388501bb4d922ad428ada50502a664e559b7e27b26bc`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 9.8 MB (9797406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977c35c08a5797b9e4a33bf3fb238215a8db6e39e14eafeb32b215c662ab87e`  
		Last Modified: Mon, 29 Dec 2025 23:41:31 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215d0d78f358a516da03ebf61b4e4bc3fbe9ccd8ba23a6bc0c1cbb579bf03e9`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 10.0 MB (9993054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af971e9a86801f69b70f2ac8e0ee675a82f433d06705075b6463be351c61354e`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:5cd590de0ac457b6bc7965d1327964460074a67fa93a9a7657048f221736f739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c42bfe7553bc21a8144114b0378a9e9bd73798ed69edbb8e1de4f165b1860c9`

```dockerfile
```

-	Layers:
	-	`sha256:ca20cd0f2cd2cb7542ea12bb9fbe12e7ca047fac8bbd51ad1c06c00155542fed`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64df6df3a8534aaf2ca9b3f6d5432244dd0004bc0f4601af0947de13efe6bfb`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:1b8639b5e386183659fba21589e268b76fcf47cf507612ddf695fae3a3a88bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5a1416112ef012e36e5f8d3be9aa54d57077596c95cf7bf4d6e7f5fdaa7a40`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:43:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:03 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:43:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:43:09 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:43:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:43:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81811df2764e9bacc9abe1ef6a9f8d86b5433fa241ab42a66388de265138b850`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.6 MB (9627867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351eec8c6b5887c984f0da09b28cfdac4ab3c4eb114213b5b9675d4f46414781`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 2.7 KB (2664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa70e611204c36424b485de7ab3a856d78907c4e9e804fb7a426400049568419`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.4 MB (9362967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d589ac0e447a384a106f6f0b7b47bb058cffa595668cbfe28bc799af0be`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:d317ca27aab510e0ca4f821993d7f9f5dbb597094a30bcb84653fd5961725ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4c162bebf2e83a25b00b8983b9e6100799313ce45d9ad550f8301276054529`

```dockerfile
```

-	Layers:
	-	`sha256:eb8290e8b26202420a09b1c8af34b7223a1242257df405f90c40ee9c5e5c5dfa`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124851da9d31c929d0034f3ee849d14104dbef464d87d6814b0cd933306fd98c`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 13.6 KB (13584 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:390a58811e17be80cb4ca3b97bb38b1e417402304726b9b76f01192e942590bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c930322a04e93088e71a73aabb6c42c24879feba61a402a3aff7a0641fb6ac6d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:37:03 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:05 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 30 Dec 2025 00:37:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
VOLUME [/data]
# Tue, 30 Dec 2025 00:37:09 GMT
WORKDIR /data
# Tue, 30 Dec 2025 00:37:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 30 Dec 2025 00:37:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5562933824310e1cbf2b5b7d292290f835858aaf213b7d7f805eca83d623e67`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04cced1892bd5ff40dc3e30507764248d87a97486c0a331d0119b8d58016b09`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b65f6c4c6c502de05c984709ecd87bba0f4f447fd76edc815a89379ea463ba5`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9303717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f5f646224922110dc1afca90434df6ceb9968ed3cfe48fd68ff10b6c19d215`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:eb945fe1eed56013ebe8c3a1aaf4d08a2f8a2ca9fd09ac0a49639f5de9706153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b6180b1bd7b5d7142deb96ac83c8ef19ebe01e27e7a2eabe2b5e7f5c668e8b`

```dockerfile
```

-	Layers:
	-	`sha256:b86ad88ea813140162109c96c8bb58e0dbb2ccd4d1c252557252056438a91918`  
		Last Modified: Tue, 30 Dec 2025 02:04:11 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7a5481318b7863846d52233fea67774bc918ab95503b85ffdfa42ffdb5a2b2`  
		Last Modified: Tue, 30 Dec 2025 02:04:12 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.3`

```console
$ docker pull rethinkdb@sha256:0c87ac98f37f5ade72c5c4218189b2c7b7093817f37ce8954331214374a8db8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4.3` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7a460ebfaf3049f5f52c46c822d8b21138c794f3871051b27c9afc1365bb47ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8287eec78c315282f752db1658b3156424a228cc01ce9b7026619e6dcce73fd7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:41:11 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:41:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:41:18 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:41:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:41:18 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4832f674ae7f81aefe4e388501bb4d922ad428ada50502a664e559b7e27b26bc`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 9.8 MB (9797406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977c35c08a5797b9e4a33bf3fb238215a8db6e39e14eafeb32b215c662ab87e`  
		Last Modified: Mon, 29 Dec 2025 23:41:31 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215d0d78f358a516da03ebf61b4e4bc3fbe9ccd8ba23a6bc0c1cbb579bf03e9`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 10.0 MB (9993054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af971e9a86801f69b70f2ac8e0ee675a82f433d06705075b6463be351c61354e`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:5cd590de0ac457b6bc7965d1327964460074a67fa93a9a7657048f221736f739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c42bfe7553bc21a8144114b0378a9e9bd73798ed69edbb8e1de4f165b1860c9`

```dockerfile
```

-	Layers:
	-	`sha256:ca20cd0f2cd2cb7542ea12bb9fbe12e7ca047fac8bbd51ad1c06c00155542fed`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64df6df3a8534aaf2ca9b3f6d5432244dd0004bc0f4601af0947de13efe6bfb`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:1b8639b5e386183659fba21589e268b76fcf47cf507612ddf695fae3a3a88bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5a1416112ef012e36e5f8d3be9aa54d57077596c95cf7bf4d6e7f5fdaa7a40`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:43:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:03 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:43:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:43:09 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:43:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:43:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81811df2764e9bacc9abe1ef6a9f8d86b5433fa241ab42a66388de265138b850`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.6 MB (9627867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351eec8c6b5887c984f0da09b28cfdac4ab3c4eb114213b5b9675d4f46414781`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 2.7 KB (2664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa70e611204c36424b485de7ab3a856d78907c4e9e804fb7a426400049568419`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.4 MB (9362967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d589ac0e447a384a106f6f0b7b47bb058cffa595668cbfe28bc799af0be`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:d317ca27aab510e0ca4f821993d7f9f5dbb597094a30bcb84653fd5961725ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4c162bebf2e83a25b00b8983b9e6100799313ce45d9ad550f8301276054529`

```dockerfile
```

-	Layers:
	-	`sha256:eb8290e8b26202420a09b1c8af34b7223a1242257df405f90c40ee9c5e5c5dfa`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124851da9d31c929d0034f3ee849d14104dbef464d87d6814b0cd933306fd98c`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 13.6 KB (13584 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; s390x

```console
$ docker pull rethinkdb@sha256:390a58811e17be80cb4ca3b97bb38b1e417402304726b9b76f01192e942590bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c930322a04e93088e71a73aabb6c42c24879feba61a402a3aff7a0641fb6ac6d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:37:03 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:05 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 30 Dec 2025 00:37:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
VOLUME [/data]
# Tue, 30 Dec 2025 00:37:09 GMT
WORKDIR /data
# Tue, 30 Dec 2025 00:37:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 30 Dec 2025 00:37:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5562933824310e1cbf2b5b7d292290f835858aaf213b7d7f805eca83d623e67`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04cced1892bd5ff40dc3e30507764248d87a97486c0a331d0119b8d58016b09`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b65f6c4c6c502de05c984709ecd87bba0f4f447fd76edc815a89379ea463ba5`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9303717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f5f646224922110dc1afca90434df6ceb9968ed3cfe48fd68ff10b6c19d215`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:eb945fe1eed56013ebe8c3a1aaf4d08a2f8a2ca9fd09ac0a49639f5de9706153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b6180b1bd7b5d7142deb96ac83c8ef19ebe01e27e7a2eabe2b5e7f5c668e8b`

```dockerfile
```

-	Layers:
	-	`sha256:b86ad88ea813140162109c96c8bb58e0dbb2ccd4d1c252557252056438a91918`  
		Last Modified: Tue, 30 Dec 2025 02:04:11 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7a5481318b7863846d52233fea67774bc918ab95503b85ffdfa42ffdb5a2b2`  
		Last Modified: Tue, 30 Dec 2025 02:04:12 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:0c87ac98f37f5ade72c5c4218189b2c7b7093817f37ce8954331214374a8db8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:2.4.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7a460ebfaf3049f5f52c46c822d8b21138c794f3871051b27c9afc1365bb47ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8287eec78c315282f752db1658b3156424a228cc01ce9b7026619e6dcce73fd7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:41:11 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:41:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:41:18 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:41:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:41:18 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4832f674ae7f81aefe4e388501bb4d922ad428ada50502a664e559b7e27b26bc`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 9.8 MB (9797406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977c35c08a5797b9e4a33bf3fb238215a8db6e39e14eafeb32b215c662ab87e`  
		Last Modified: Mon, 29 Dec 2025 23:41:31 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215d0d78f358a516da03ebf61b4e4bc3fbe9ccd8ba23a6bc0c1cbb579bf03e9`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 10.0 MB (9993054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af971e9a86801f69b70f2ac8e0ee675a82f433d06705075b6463be351c61354e`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:5cd590de0ac457b6bc7965d1327964460074a67fa93a9a7657048f221736f739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c42bfe7553bc21a8144114b0378a9e9bd73798ed69edbb8e1de4f165b1860c9`

```dockerfile
```

-	Layers:
	-	`sha256:ca20cd0f2cd2cb7542ea12bb9fbe12e7ca047fac8bbd51ad1c06c00155542fed`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64df6df3a8534aaf2ca9b3f6d5432244dd0004bc0f4601af0947de13efe6bfb`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:1b8639b5e386183659fba21589e268b76fcf47cf507612ddf695fae3a3a88bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5a1416112ef012e36e5f8d3be9aa54d57077596c95cf7bf4d6e7f5fdaa7a40`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:43:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:03 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:43:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:43:09 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:43:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:43:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81811df2764e9bacc9abe1ef6a9f8d86b5433fa241ab42a66388de265138b850`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.6 MB (9627867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351eec8c6b5887c984f0da09b28cfdac4ab3c4eb114213b5b9675d4f46414781`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 2.7 KB (2664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa70e611204c36424b485de7ab3a856d78907c4e9e804fb7a426400049568419`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.4 MB (9362967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d589ac0e447a384a106f6f0b7b47bb058cffa595668cbfe28bc799af0be`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:d317ca27aab510e0ca4f821993d7f9f5dbb597094a30bcb84653fd5961725ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4c162bebf2e83a25b00b8983b9e6100799313ce45d9ad550f8301276054529`

```dockerfile
```

-	Layers:
	-	`sha256:eb8290e8b26202420a09b1c8af34b7223a1242257df405f90c40ee9c5e5c5dfa`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124851da9d31c929d0034f3ee849d14104dbef464d87d6814b0cd933306fd98c`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 13.6 KB (13584 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:390a58811e17be80cb4ca3b97bb38b1e417402304726b9b76f01192e942590bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c930322a04e93088e71a73aabb6c42c24879feba61a402a3aff7a0641fb6ac6d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:37:03 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:05 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 30 Dec 2025 00:37:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
VOLUME [/data]
# Tue, 30 Dec 2025 00:37:09 GMT
WORKDIR /data
# Tue, 30 Dec 2025 00:37:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 30 Dec 2025 00:37:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5562933824310e1cbf2b5b7d292290f835858aaf213b7d7f805eca83d623e67`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04cced1892bd5ff40dc3e30507764248d87a97486c0a331d0119b8d58016b09`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b65f6c4c6c502de05c984709ecd87bba0f4f447fd76edc815a89379ea463ba5`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9303717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f5f646224922110dc1afca90434df6ceb9968ed3cfe48fd68ff10b6c19d215`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:eb945fe1eed56013ebe8c3a1aaf4d08a2f8a2ca9fd09ac0a49639f5de9706153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b6180b1bd7b5d7142deb96ac83c8ef19ebe01e27e7a2eabe2b5e7f5c668e8b`

```dockerfile
```

-	Layers:
	-	`sha256:b86ad88ea813140162109c96c8bb58e0dbb2ccd4d1c252557252056438a91918`  
		Last Modified: Tue, 30 Dec 2025 02:04:11 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7a5481318b7863846d52233fea67774bc918ab95503b85ffdfa42ffdb5a2b2`  
		Last Modified: Tue, 30 Dec 2025 02:04:12 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:0c87ac98f37f5ade72c5c4218189b2c7b7093817f37ce8954331214374a8db8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7a460ebfaf3049f5f52c46c822d8b21138c794f3871051b27c9afc1365bb47ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8287eec78c315282f752db1658b3156424a228cc01ce9b7026619e6dcce73fd7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:41:11 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:41:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:41:18 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:41:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:41:18 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4832f674ae7f81aefe4e388501bb4d922ad428ada50502a664e559b7e27b26bc`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 9.8 MB (9797406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977c35c08a5797b9e4a33bf3fb238215a8db6e39e14eafeb32b215c662ab87e`  
		Last Modified: Mon, 29 Dec 2025 23:41:31 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215d0d78f358a516da03ebf61b4e4bc3fbe9ccd8ba23a6bc0c1cbb579bf03e9`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 10.0 MB (9993054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af971e9a86801f69b70f2ac8e0ee675a82f433d06705075b6463be351c61354e`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:5cd590de0ac457b6bc7965d1327964460074a67fa93a9a7657048f221736f739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c42bfe7553bc21a8144114b0378a9e9bd73798ed69edbb8e1de4f165b1860c9`

```dockerfile
```

-	Layers:
	-	`sha256:ca20cd0f2cd2cb7542ea12bb9fbe12e7ca047fac8bbd51ad1c06c00155542fed`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64df6df3a8534aaf2ca9b3f6d5432244dd0004bc0f4601af0947de13efe6bfb`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:1b8639b5e386183659fba21589e268b76fcf47cf507612ddf695fae3a3a88bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5a1416112ef012e36e5f8d3be9aa54d57077596c95cf7bf4d6e7f5fdaa7a40`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:43:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:03 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:43:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:43:09 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:43:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:43:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81811df2764e9bacc9abe1ef6a9f8d86b5433fa241ab42a66388de265138b850`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.6 MB (9627867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351eec8c6b5887c984f0da09b28cfdac4ab3c4eb114213b5b9675d4f46414781`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 2.7 KB (2664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa70e611204c36424b485de7ab3a856d78907c4e9e804fb7a426400049568419`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.4 MB (9362967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d589ac0e447a384a106f6f0b7b47bb058cffa595668cbfe28bc799af0be`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:d317ca27aab510e0ca4f821993d7f9f5dbb597094a30bcb84653fd5961725ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4c162bebf2e83a25b00b8983b9e6100799313ce45d9ad550f8301276054529`

```dockerfile
```

-	Layers:
	-	`sha256:eb8290e8b26202420a09b1c8af34b7223a1242257df405f90c40ee9c5e5c5dfa`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124851da9d31c929d0034f3ee849d14104dbef464d87d6814b0cd933306fd98c`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 13.6 KB (13584 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:390a58811e17be80cb4ca3b97bb38b1e417402304726b9b76f01192e942590bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c930322a04e93088e71a73aabb6c42c24879feba61a402a3aff7a0641fb6ac6d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:37:03 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:05 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 30 Dec 2025 00:37:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
VOLUME [/data]
# Tue, 30 Dec 2025 00:37:09 GMT
WORKDIR /data
# Tue, 30 Dec 2025 00:37:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 30 Dec 2025 00:37:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5562933824310e1cbf2b5b7d292290f835858aaf213b7d7f805eca83d623e67`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04cced1892bd5ff40dc3e30507764248d87a97486c0a331d0119b8d58016b09`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b65f6c4c6c502de05c984709ecd87bba0f4f447fd76edc815a89379ea463ba5`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9303717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f5f646224922110dc1afca90434df6ceb9968ed3cfe48fd68ff10b6c19d215`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:eb945fe1eed56013ebe8c3a1aaf4d08a2f8a2ca9fd09ac0a49639f5de9706153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b6180b1bd7b5d7142deb96ac83c8ef19ebe01e27e7a2eabe2b5e7f5c668e8b`

```dockerfile
```

-	Layers:
	-	`sha256:b86ad88ea813140162109c96c8bb58e0dbb2ccd4d1c252557252056438a91918`  
		Last Modified: Tue, 30 Dec 2025 02:04:11 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7a5481318b7863846d52233fea67774bc918ab95503b85ffdfa42ffdb5a2b2`  
		Last Modified: Tue, 30 Dec 2025 02:04:12 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:0c87ac98f37f5ade72c5c4218189b2c7b7093817f37ce8954331214374a8db8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7a460ebfaf3049f5f52c46c822d8b21138c794f3871051b27c9afc1365bb47ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8287eec78c315282f752db1658b3156424a228cc01ce9b7026619e6dcce73fd7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:41:11 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:12 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:41:18 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:41:18 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:41:18 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:41:18 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:41:18 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4832f674ae7f81aefe4e388501bb4d922ad428ada50502a664e559b7e27b26bc`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 9.8 MB (9797406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977c35c08a5797b9e4a33bf3fb238215a8db6e39e14eafeb32b215c662ab87e`  
		Last Modified: Mon, 29 Dec 2025 23:41:31 GMT  
		Size: 2.7 KB (2668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7215d0d78f358a516da03ebf61b4e4bc3fbe9ccd8ba23a6bc0c1cbb579bf03e9`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 10.0 MB (9993054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af971e9a86801f69b70f2ac8e0ee675a82f433d06705075b6463be351c61354e`  
		Last Modified: Mon, 29 Dec 2025 23:41:32 GMT  
		Size: 94.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:5cd590de0ac457b6bc7965d1327964460074a67fa93a9a7657048f221736f739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c42bfe7553bc21a8144114b0378a9e9bd73798ed69edbb8e1de4f165b1860c9`

```dockerfile
```

-	Layers:
	-	`sha256:ca20cd0f2cd2cb7542ea12bb9fbe12e7ca047fac8bbd51ad1c06c00155542fed`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64df6df3a8534aaf2ca9b3f6d5432244dd0004bc0f4601af0947de13efe6bfb`  
		Last Modified: Tue, 30 Dec 2025 02:04:02 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:1b8639b5e386183659fba21589e268b76fcf47cf507612ddf695fae3a3a88bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5a1416112ef012e36e5f8d3be9aa54d57077596c95cf7bf4d6e7f5fdaa7a40`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:43:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:03 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Mon, 29 Dec 2025 23:43:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:43:09 GMT
VOLUME [/data]
# Mon, 29 Dec 2025 23:43:09 GMT
WORKDIR /data
# Mon, 29 Dec 2025 23:43:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 29 Dec 2025 23:43:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81811df2764e9bacc9abe1ef6a9f8d86b5433fa241ab42a66388de265138b850`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.6 MB (9627867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351eec8c6b5887c984f0da09b28cfdac4ab3c4eb114213b5b9675d4f46414781`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 2.7 KB (2664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa70e611204c36424b485de7ab3a856d78907c4e9e804fb7a426400049568419`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 9.4 MB (9362967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e20d589ac0e447a384a106f6f0b7b47bb058cffa595668cbfe28bc799af0be`  
		Last Modified: Mon, 29 Dec 2025 23:43:24 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:d317ca27aab510e0ca4f821993d7f9f5dbb597094a30bcb84653fd5961725ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4c162bebf2e83a25b00b8983b9e6100799313ce45d9ad550f8301276054529`

```dockerfile
```

-	Layers:
	-	`sha256:eb8290e8b26202420a09b1c8af34b7223a1242257df405f90c40ee9c5e5c5dfa`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124851da9d31c929d0034f3ee849d14104dbef464d87d6814b0cd933306fd98c`  
		Last Modified: Tue, 30 Dec 2025 02:04:07 GMT  
		Size: 13.6 KB (13584 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:390a58811e17be80cb4ca3b97bb38b1e417402304726b9b76f01192e942590bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c930322a04e93088e71a73aabb6c42c24879feba61a402a3aff7a0641fb6ac6d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:37:03 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:05 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 30 Dec 2025 00:37:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:37:09 GMT
VOLUME [/data]
# Tue, 30 Dec 2025 00:37:09 GMT
WORKDIR /data
# Tue, 30 Dec 2025 00:37:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 30 Dec 2025 00:37:09 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5562933824310e1cbf2b5b7d292290f835858aaf213b7d7f805eca83d623e67`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04cced1892bd5ff40dc3e30507764248d87a97486c0a331d0119b8d58016b09`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 2.7 KB (2667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b65f6c4c6c502de05c984709ecd87bba0f4f447fd76edc815a89379ea463ba5`  
		Last Modified: Tue, 30 Dec 2025 00:37:27 GMT  
		Size: 9.3 MB (9303717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f5f646224922110dc1afca90434df6ceb9968ed3cfe48fd68ff10b6c19d215`  
		Last Modified: Tue, 30 Dec 2025 00:37:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:eb945fe1eed56013ebe8c3a1aaf4d08a2f8a2ca9fd09ac0a49639f5de9706153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b6180b1bd7b5d7142deb96ac83c8ef19ebe01e27e7a2eabe2b5e7f5c668e8b`

```dockerfile
```

-	Layers:
	-	`sha256:b86ad88ea813140162109c96c8bb58e0dbb2ccd4d1c252557252056438a91918`  
		Last Modified: Tue, 30 Dec 2025 02:04:11 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7a5481318b7863846d52233fea67774bc918ab95503b85ffdfa42ffdb5a2b2`  
		Last Modified: Tue, 30 Dec 2025 02:04:12 GMT  
		Size: 13.4 KB (13404 bytes)  
		MIME: application/vnd.in-toto+json
