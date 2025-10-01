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
$ docker pull rethinkdb@sha256:b418c8d89595a15666738c0d0eb62bdd16042ff2b88510cb992f3efec8d27c8b
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
$ docker pull rethinkdb@sha256:5a18e673ce85f3ef619dae1ff5d007aac763a3be8da9d8268ae553d6a9553792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6c829515e216481c4bf4ff1254c815e142c8c185514b757a8165e583e2993c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21178eaa9ee52ef9aeb518bbe7298d50ea4db803734e34250d6899297757eaf`  
		Last Modified: Tue, 30 Sep 2025 01:05:05 GMT  
		Size: 9.8 MB (9797341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a40a5bc2fe437f2b0280daceb165e2a627bce07891a4f55bcd8241d9971bd6`  
		Last Modified: Tue, 30 Sep 2025 00:25:13 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5490cb8d309240642f1897831c644827ce471aebaa68a8f05df988bf3f78abc`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 10.0 MB (9993135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00085c9c88c2277759525e6fa7dd05c92ff43c5b4e2b7d7018467ecf723f2141`  
		Last Modified: Tue, 30 Sep 2025 00:25:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f4210cbcaf6a033f2a9e5a3d583bbdd8f15fbf41dcd4e9f7a214ed88583baf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011236d719b67dfc54b23510f46199e819c7a772990d1b6e5c69502fda864c0b`

```dockerfile
```

-	Layers:
	-	`sha256:1f509e54e78c57161cdfa3bf94b9776f852b0ae94c050fd2fc0e844f823b41ee`  
		Last Modified: Tue, 30 Sep 2025 01:03:18 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1daa488e0e504cbf08110ce934f59f68cd8b82a637ae63fecab4a4afc874e89`  
		Last Modified: Tue, 30 Sep 2025 01:03:19 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:277c04c62b163225dcbe6048562b38a849e62191569e825b288792c9b1371e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536350e22afda81b9a6b5a61189e0c60af1914b7a61b27cf9b78d74be38d2156`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b95cd747690d3966db74c005b579dc0acc5d3d5dd2dc3953aa1b7fc6b2c3319`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.6 MB (9627792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140f894af5ccfce1600e9ef1aec68862bb572a6c05cdaf4fe21f8d4f59adcd0f`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c50f1aecdff6d3a90c06de0fa3b75ae6a7ef656f55abe521fc8033315d90446`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e887eb8931bbe87cbc8ec34c5adb7da8dad6c5c8ed818299f0dc3aefbf0003ff`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f7ec9f740563e67cbccc3b78c217fc472bbf798c083777a623e2dc6e6a1fdf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052ad9a18c0162e5dbf41510ff9dd35c41d913460032c24a43f64d63732f362a`

```dockerfile
```

-	Layers:
	-	`sha256:d1c79bfa1ad00c0f524d4aaf49281ab7c0fe084f4b6013dffa63826cd5c179a8`  
		Last Modified: Tue, 30 Sep 2025 13:03:23 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fe6b31b7b04136764c6a2d82e2fc70e8ddf4fd6343212e0e0546f41ef822ef`  
		Last Modified: Tue, 30 Sep 2025 13:03:24 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bae7ff2e583a31eb0550035094f8540c7f357df7a16af0665ae1268d249a935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf421ffdcb0df224fbb25f93dd890021bbe75c4e456cdb6eb422d78e42fdcbaf`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a959c1367c08d7204de3bb0109468970980a812b5c4337e798e815c0e9ea2f`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09424b46ccb61f3ef162edf8d13ad2562f1d846ae3746d0293f192af68e91583`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8532449ce1c361e4ee15fbc7c2a432f905bcfb701a1fc40058a423bef0edc1`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9303752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7d27ae9849bf6dcb351d79b0cd44942287d6c575275467ba4e0cfde9b7d39`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a964e7d4b5903b274d925d0bd766f05096ccaad1caf6bc2f3b5e775718e9332e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f901a05f7e319708e98d13963e83b4f2332c84f5a2a11339feb43aceda10f86`

```dockerfile
```

-	Layers:
	-	`sha256:435f5e64358e1da2fff9244350b020e62e6086e9335ed18e7a5208ba301555a2`  
		Last Modified: Wed, 01 Oct 2025 22:03:23 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a381c5d325a55fae7a6dd7a7bc591864f5d68ddbf19eefb960e9ab799658049d`  
		Last Modified: Wed, 01 Oct 2025 22:03:24 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:b418c8d89595a15666738c0d0eb62bdd16042ff2b88510cb992f3efec8d27c8b
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
$ docker pull rethinkdb@sha256:5a18e673ce85f3ef619dae1ff5d007aac763a3be8da9d8268ae553d6a9553792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6c829515e216481c4bf4ff1254c815e142c8c185514b757a8165e583e2993c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21178eaa9ee52ef9aeb518bbe7298d50ea4db803734e34250d6899297757eaf`  
		Last Modified: Tue, 30 Sep 2025 01:05:05 GMT  
		Size: 9.8 MB (9797341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a40a5bc2fe437f2b0280daceb165e2a627bce07891a4f55bcd8241d9971bd6`  
		Last Modified: Tue, 30 Sep 2025 00:25:13 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5490cb8d309240642f1897831c644827ce471aebaa68a8f05df988bf3f78abc`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 10.0 MB (9993135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00085c9c88c2277759525e6fa7dd05c92ff43c5b4e2b7d7018467ecf723f2141`  
		Last Modified: Tue, 30 Sep 2025 00:25:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f4210cbcaf6a033f2a9e5a3d583bbdd8f15fbf41dcd4e9f7a214ed88583baf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011236d719b67dfc54b23510f46199e819c7a772990d1b6e5c69502fda864c0b`

```dockerfile
```

-	Layers:
	-	`sha256:1f509e54e78c57161cdfa3bf94b9776f852b0ae94c050fd2fc0e844f823b41ee`  
		Last Modified: Tue, 30 Sep 2025 01:03:18 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1daa488e0e504cbf08110ce934f59f68cd8b82a637ae63fecab4a4afc874e89`  
		Last Modified: Tue, 30 Sep 2025 01:03:19 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:277c04c62b163225dcbe6048562b38a849e62191569e825b288792c9b1371e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536350e22afda81b9a6b5a61189e0c60af1914b7a61b27cf9b78d74be38d2156`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b95cd747690d3966db74c005b579dc0acc5d3d5dd2dc3953aa1b7fc6b2c3319`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.6 MB (9627792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140f894af5ccfce1600e9ef1aec68862bb572a6c05cdaf4fe21f8d4f59adcd0f`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c50f1aecdff6d3a90c06de0fa3b75ae6a7ef656f55abe521fc8033315d90446`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e887eb8931bbe87cbc8ec34c5adb7da8dad6c5c8ed818299f0dc3aefbf0003ff`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f7ec9f740563e67cbccc3b78c217fc472bbf798c083777a623e2dc6e6a1fdf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052ad9a18c0162e5dbf41510ff9dd35c41d913460032c24a43f64d63732f362a`

```dockerfile
```

-	Layers:
	-	`sha256:d1c79bfa1ad00c0f524d4aaf49281ab7c0fe084f4b6013dffa63826cd5c179a8`  
		Last Modified: Tue, 30 Sep 2025 13:03:23 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fe6b31b7b04136764c6a2d82e2fc70e8ddf4fd6343212e0e0546f41ef822ef`  
		Last Modified: Tue, 30 Sep 2025 13:03:24 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bae7ff2e583a31eb0550035094f8540c7f357df7a16af0665ae1268d249a935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf421ffdcb0df224fbb25f93dd890021bbe75c4e456cdb6eb422d78e42fdcbaf`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a959c1367c08d7204de3bb0109468970980a812b5c4337e798e815c0e9ea2f`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09424b46ccb61f3ef162edf8d13ad2562f1d846ae3746d0293f192af68e91583`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8532449ce1c361e4ee15fbc7c2a432f905bcfb701a1fc40058a423bef0edc1`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9303752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7d27ae9849bf6dcb351d79b0cd44942287d6c575275467ba4e0cfde9b7d39`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a964e7d4b5903b274d925d0bd766f05096ccaad1caf6bc2f3b5e775718e9332e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f901a05f7e319708e98d13963e83b4f2332c84f5a2a11339feb43aceda10f86`

```dockerfile
```

-	Layers:
	-	`sha256:435f5e64358e1da2fff9244350b020e62e6086e9335ed18e7a5208ba301555a2`  
		Last Modified: Wed, 01 Oct 2025 22:03:23 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a381c5d325a55fae7a6dd7a7bc591864f5d68ddbf19eefb960e9ab799658049d`  
		Last Modified: Wed, 01 Oct 2025 22:03:24 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:b418c8d89595a15666738c0d0eb62bdd16042ff2b88510cb992f3efec8d27c8b
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
$ docker pull rethinkdb@sha256:5a18e673ce85f3ef619dae1ff5d007aac763a3be8da9d8268ae553d6a9553792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6c829515e216481c4bf4ff1254c815e142c8c185514b757a8165e583e2993c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21178eaa9ee52ef9aeb518bbe7298d50ea4db803734e34250d6899297757eaf`  
		Last Modified: Tue, 30 Sep 2025 01:05:05 GMT  
		Size: 9.8 MB (9797341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a40a5bc2fe437f2b0280daceb165e2a627bce07891a4f55bcd8241d9971bd6`  
		Last Modified: Tue, 30 Sep 2025 00:25:13 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5490cb8d309240642f1897831c644827ce471aebaa68a8f05df988bf3f78abc`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 10.0 MB (9993135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00085c9c88c2277759525e6fa7dd05c92ff43c5b4e2b7d7018467ecf723f2141`  
		Last Modified: Tue, 30 Sep 2025 00:25:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f4210cbcaf6a033f2a9e5a3d583bbdd8f15fbf41dcd4e9f7a214ed88583baf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011236d719b67dfc54b23510f46199e819c7a772990d1b6e5c69502fda864c0b`

```dockerfile
```

-	Layers:
	-	`sha256:1f509e54e78c57161cdfa3bf94b9776f852b0ae94c050fd2fc0e844f823b41ee`  
		Last Modified: Tue, 30 Sep 2025 01:03:18 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1daa488e0e504cbf08110ce934f59f68cd8b82a637ae63fecab4a4afc874e89`  
		Last Modified: Tue, 30 Sep 2025 01:03:19 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:277c04c62b163225dcbe6048562b38a849e62191569e825b288792c9b1371e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536350e22afda81b9a6b5a61189e0c60af1914b7a61b27cf9b78d74be38d2156`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b95cd747690d3966db74c005b579dc0acc5d3d5dd2dc3953aa1b7fc6b2c3319`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.6 MB (9627792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140f894af5ccfce1600e9ef1aec68862bb572a6c05cdaf4fe21f8d4f59adcd0f`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c50f1aecdff6d3a90c06de0fa3b75ae6a7ef656f55abe521fc8033315d90446`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e887eb8931bbe87cbc8ec34c5adb7da8dad6c5c8ed818299f0dc3aefbf0003ff`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f7ec9f740563e67cbccc3b78c217fc472bbf798c083777a623e2dc6e6a1fdf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052ad9a18c0162e5dbf41510ff9dd35c41d913460032c24a43f64d63732f362a`

```dockerfile
```

-	Layers:
	-	`sha256:d1c79bfa1ad00c0f524d4aaf49281ab7c0fe084f4b6013dffa63826cd5c179a8`  
		Last Modified: Tue, 30 Sep 2025 13:03:23 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fe6b31b7b04136764c6a2d82e2fc70e8ddf4fd6343212e0e0546f41ef822ef`  
		Last Modified: Tue, 30 Sep 2025 13:03:24 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bae7ff2e583a31eb0550035094f8540c7f357df7a16af0665ae1268d249a935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf421ffdcb0df224fbb25f93dd890021bbe75c4e456cdb6eb422d78e42fdcbaf`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a959c1367c08d7204de3bb0109468970980a812b5c4337e798e815c0e9ea2f`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09424b46ccb61f3ef162edf8d13ad2562f1d846ae3746d0293f192af68e91583`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8532449ce1c361e4ee15fbc7c2a432f905bcfb701a1fc40058a423bef0edc1`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9303752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7d27ae9849bf6dcb351d79b0cd44942287d6c575275467ba4e0cfde9b7d39`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a964e7d4b5903b274d925d0bd766f05096ccaad1caf6bc2f3b5e775718e9332e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f901a05f7e319708e98d13963e83b4f2332c84f5a2a11339feb43aceda10f86`

```dockerfile
```

-	Layers:
	-	`sha256:435f5e64358e1da2fff9244350b020e62e6086e9335ed18e7a5208ba301555a2`  
		Last Modified: Wed, 01 Oct 2025 22:03:23 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a381c5d325a55fae7a6dd7a7bc591864f5d68ddbf19eefb960e9ab799658049d`  
		Last Modified: Wed, 01 Oct 2025 22:03:24 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:b418c8d89595a15666738c0d0eb62bdd16042ff2b88510cb992f3efec8d27c8b
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
$ docker pull rethinkdb@sha256:5a18e673ce85f3ef619dae1ff5d007aac763a3be8da9d8268ae553d6a9553792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6c829515e216481c4bf4ff1254c815e142c8c185514b757a8165e583e2993c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21178eaa9ee52ef9aeb518bbe7298d50ea4db803734e34250d6899297757eaf`  
		Last Modified: Tue, 30 Sep 2025 01:05:05 GMT  
		Size: 9.8 MB (9797341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a40a5bc2fe437f2b0280daceb165e2a627bce07891a4f55bcd8241d9971bd6`  
		Last Modified: Tue, 30 Sep 2025 00:25:13 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5490cb8d309240642f1897831c644827ce471aebaa68a8f05df988bf3f78abc`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 10.0 MB (9993135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00085c9c88c2277759525e6fa7dd05c92ff43c5b4e2b7d7018467ecf723f2141`  
		Last Modified: Tue, 30 Sep 2025 00:25:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f4210cbcaf6a033f2a9e5a3d583bbdd8f15fbf41dcd4e9f7a214ed88583baf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011236d719b67dfc54b23510f46199e819c7a772990d1b6e5c69502fda864c0b`

```dockerfile
```

-	Layers:
	-	`sha256:1f509e54e78c57161cdfa3bf94b9776f852b0ae94c050fd2fc0e844f823b41ee`  
		Last Modified: Tue, 30 Sep 2025 01:03:18 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1daa488e0e504cbf08110ce934f59f68cd8b82a637ae63fecab4a4afc874e89`  
		Last Modified: Tue, 30 Sep 2025 01:03:19 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:277c04c62b163225dcbe6048562b38a849e62191569e825b288792c9b1371e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536350e22afda81b9a6b5a61189e0c60af1914b7a61b27cf9b78d74be38d2156`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b95cd747690d3966db74c005b579dc0acc5d3d5dd2dc3953aa1b7fc6b2c3319`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.6 MB (9627792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140f894af5ccfce1600e9ef1aec68862bb572a6c05cdaf4fe21f8d4f59adcd0f`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c50f1aecdff6d3a90c06de0fa3b75ae6a7ef656f55abe521fc8033315d90446`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e887eb8931bbe87cbc8ec34c5adb7da8dad6c5c8ed818299f0dc3aefbf0003ff`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f7ec9f740563e67cbccc3b78c217fc472bbf798c083777a623e2dc6e6a1fdf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052ad9a18c0162e5dbf41510ff9dd35c41d913460032c24a43f64d63732f362a`

```dockerfile
```

-	Layers:
	-	`sha256:d1c79bfa1ad00c0f524d4aaf49281ab7c0fe084f4b6013dffa63826cd5c179a8`  
		Last Modified: Tue, 30 Sep 2025 13:03:23 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fe6b31b7b04136764c6a2d82e2fc70e8ddf4fd6343212e0e0546f41ef822ef`  
		Last Modified: Tue, 30 Sep 2025 13:03:24 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bae7ff2e583a31eb0550035094f8540c7f357df7a16af0665ae1268d249a935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf421ffdcb0df224fbb25f93dd890021bbe75c4e456cdb6eb422d78e42fdcbaf`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a959c1367c08d7204de3bb0109468970980a812b5c4337e798e815c0e9ea2f`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09424b46ccb61f3ef162edf8d13ad2562f1d846ae3746d0293f192af68e91583`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8532449ce1c361e4ee15fbc7c2a432f905bcfb701a1fc40058a423bef0edc1`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9303752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7d27ae9849bf6dcb351d79b0cd44942287d6c575275467ba4e0cfde9b7d39`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a964e7d4b5903b274d925d0bd766f05096ccaad1caf6bc2f3b5e775718e9332e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f901a05f7e319708e98d13963e83b4f2332c84f5a2a11339feb43aceda10f86`

```dockerfile
```

-	Layers:
	-	`sha256:435f5e64358e1da2fff9244350b020e62e6086e9335ed18e7a5208ba301555a2`  
		Last Modified: Wed, 01 Oct 2025 22:03:23 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a381c5d325a55fae7a6dd7a7bc591864f5d68ddbf19eefb960e9ab799658049d`  
		Last Modified: Wed, 01 Oct 2025 22:03:24 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.3`

```console
$ docker pull rethinkdb@sha256:b418c8d89595a15666738c0d0eb62bdd16042ff2b88510cb992f3efec8d27c8b
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
$ docker pull rethinkdb@sha256:5a18e673ce85f3ef619dae1ff5d007aac763a3be8da9d8268ae553d6a9553792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6c829515e216481c4bf4ff1254c815e142c8c185514b757a8165e583e2993c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21178eaa9ee52ef9aeb518bbe7298d50ea4db803734e34250d6899297757eaf`  
		Last Modified: Tue, 30 Sep 2025 01:05:05 GMT  
		Size: 9.8 MB (9797341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a40a5bc2fe437f2b0280daceb165e2a627bce07891a4f55bcd8241d9971bd6`  
		Last Modified: Tue, 30 Sep 2025 00:25:13 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5490cb8d309240642f1897831c644827ce471aebaa68a8f05df988bf3f78abc`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 10.0 MB (9993135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00085c9c88c2277759525e6fa7dd05c92ff43c5b4e2b7d7018467ecf723f2141`  
		Last Modified: Tue, 30 Sep 2025 00:25:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f4210cbcaf6a033f2a9e5a3d583bbdd8f15fbf41dcd4e9f7a214ed88583baf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011236d719b67dfc54b23510f46199e819c7a772990d1b6e5c69502fda864c0b`

```dockerfile
```

-	Layers:
	-	`sha256:1f509e54e78c57161cdfa3bf94b9776f852b0ae94c050fd2fc0e844f823b41ee`  
		Last Modified: Tue, 30 Sep 2025 01:03:18 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1daa488e0e504cbf08110ce934f59f68cd8b82a637ae63fecab4a4afc874e89`  
		Last Modified: Tue, 30 Sep 2025 01:03:19 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:277c04c62b163225dcbe6048562b38a849e62191569e825b288792c9b1371e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536350e22afda81b9a6b5a61189e0c60af1914b7a61b27cf9b78d74be38d2156`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b95cd747690d3966db74c005b579dc0acc5d3d5dd2dc3953aa1b7fc6b2c3319`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.6 MB (9627792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140f894af5ccfce1600e9ef1aec68862bb572a6c05cdaf4fe21f8d4f59adcd0f`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c50f1aecdff6d3a90c06de0fa3b75ae6a7ef656f55abe521fc8033315d90446`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e887eb8931bbe87cbc8ec34c5adb7da8dad6c5c8ed818299f0dc3aefbf0003ff`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f7ec9f740563e67cbccc3b78c217fc472bbf798c083777a623e2dc6e6a1fdf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052ad9a18c0162e5dbf41510ff9dd35c41d913460032c24a43f64d63732f362a`

```dockerfile
```

-	Layers:
	-	`sha256:d1c79bfa1ad00c0f524d4aaf49281ab7c0fe084f4b6013dffa63826cd5c179a8`  
		Last Modified: Tue, 30 Sep 2025 13:03:23 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fe6b31b7b04136764c6a2d82e2fc70e8ddf4fd6343212e0e0546f41ef822ef`  
		Last Modified: Tue, 30 Sep 2025 13:03:24 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.3` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bae7ff2e583a31eb0550035094f8540c7f357df7a16af0665ae1268d249a935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf421ffdcb0df224fbb25f93dd890021bbe75c4e456cdb6eb422d78e42fdcbaf`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a959c1367c08d7204de3bb0109468970980a812b5c4337e798e815c0e9ea2f`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09424b46ccb61f3ef162edf8d13ad2562f1d846ae3746d0293f192af68e91583`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8532449ce1c361e4ee15fbc7c2a432f905bcfb701a1fc40058a423bef0edc1`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9303752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7d27ae9849bf6dcb351d79b0cd44942287d6c575275467ba4e0cfde9b7d39`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.3` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a964e7d4b5903b274d925d0bd766f05096ccaad1caf6bc2f3b5e775718e9332e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f901a05f7e319708e98d13963e83b4f2332c84f5a2a11339feb43aceda10f86`

```dockerfile
```

-	Layers:
	-	`sha256:435f5e64358e1da2fff9244350b020e62e6086e9335ed18e7a5208ba301555a2`  
		Last Modified: Wed, 01 Oct 2025 22:03:23 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a381c5d325a55fae7a6dd7a7bc591864f5d68ddbf19eefb960e9ab799658049d`  
		Last Modified: Wed, 01 Oct 2025 22:03:24 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:2.4.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:b418c8d89595a15666738c0d0eb62bdd16042ff2b88510cb992f3efec8d27c8b
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
$ docker pull rethinkdb@sha256:5a18e673ce85f3ef619dae1ff5d007aac763a3be8da9d8268ae553d6a9553792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6c829515e216481c4bf4ff1254c815e142c8c185514b757a8165e583e2993c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21178eaa9ee52ef9aeb518bbe7298d50ea4db803734e34250d6899297757eaf`  
		Last Modified: Tue, 30 Sep 2025 01:05:05 GMT  
		Size: 9.8 MB (9797341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a40a5bc2fe437f2b0280daceb165e2a627bce07891a4f55bcd8241d9971bd6`  
		Last Modified: Tue, 30 Sep 2025 00:25:13 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5490cb8d309240642f1897831c644827ce471aebaa68a8f05df988bf3f78abc`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 10.0 MB (9993135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00085c9c88c2277759525e6fa7dd05c92ff43c5b4e2b7d7018467ecf723f2141`  
		Last Modified: Tue, 30 Sep 2025 00:25:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f4210cbcaf6a033f2a9e5a3d583bbdd8f15fbf41dcd4e9f7a214ed88583baf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011236d719b67dfc54b23510f46199e819c7a772990d1b6e5c69502fda864c0b`

```dockerfile
```

-	Layers:
	-	`sha256:1f509e54e78c57161cdfa3bf94b9776f852b0ae94c050fd2fc0e844f823b41ee`  
		Last Modified: Tue, 30 Sep 2025 01:03:18 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1daa488e0e504cbf08110ce934f59f68cd8b82a637ae63fecab4a4afc874e89`  
		Last Modified: Tue, 30 Sep 2025 01:03:19 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:277c04c62b163225dcbe6048562b38a849e62191569e825b288792c9b1371e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536350e22afda81b9a6b5a61189e0c60af1914b7a61b27cf9b78d74be38d2156`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b95cd747690d3966db74c005b579dc0acc5d3d5dd2dc3953aa1b7fc6b2c3319`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.6 MB (9627792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140f894af5ccfce1600e9ef1aec68862bb572a6c05cdaf4fe21f8d4f59adcd0f`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c50f1aecdff6d3a90c06de0fa3b75ae6a7ef656f55abe521fc8033315d90446`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e887eb8931bbe87cbc8ec34c5adb7da8dad6c5c8ed818299f0dc3aefbf0003ff`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f7ec9f740563e67cbccc3b78c217fc472bbf798c083777a623e2dc6e6a1fdf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052ad9a18c0162e5dbf41510ff9dd35c41d913460032c24a43f64d63732f362a`

```dockerfile
```

-	Layers:
	-	`sha256:d1c79bfa1ad00c0f524d4aaf49281ab7c0fe084f4b6013dffa63826cd5c179a8`  
		Last Modified: Tue, 30 Sep 2025 13:03:23 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fe6b31b7b04136764c6a2d82e2fc70e8ddf4fd6343212e0e0546f41ef822ef`  
		Last Modified: Tue, 30 Sep 2025 13:03:24 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:2.4.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bae7ff2e583a31eb0550035094f8540c7f357df7a16af0665ae1268d249a935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf421ffdcb0df224fbb25f93dd890021bbe75c4e456cdb6eb422d78e42fdcbaf`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a959c1367c08d7204de3bb0109468970980a812b5c4337e798e815c0e9ea2f`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09424b46ccb61f3ef162edf8d13ad2562f1d846ae3746d0293f192af68e91583`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8532449ce1c361e4ee15fbc7c2a432f905bcfb701a1fc40058a423bef0edc1`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9303752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7d27ae9849bf6dcb351d79b0cd44942287d6c575275467ba4e0cfde9b7d39`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:2.4.4-bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a964e7d4b5903b274d925d0bd766f05096ccaad1caf6bc2f3b5e775718e9332e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f901a05f7e319708e98d13963e83b4f2332c84f5a2a11339feb43aceda10f86`

```dockerfile
```

-	Layers:
	-	`sha256:435f5e64358e1da2fff9244350b020e62e6086e9335ed18e7a5208ba301555a2`  
		Last Modified: Wed, 01 Oct 2025 22:03:23 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a381c5d325a55fae7a6dd7a7bc591864f5d68ddbf19eefb960e9ab799658049d`  
		Last Modified: Wed, 01 Oct 2025 22:03:24 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:b418c8d89595a15666738c0d0eb62bdd16042ff2b88510cb992f3efec8d27c8b
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
$ docker pull rethinkdb@sha256:5a18e673ce85f3ef619dae1ff5d007aac763a3be8da9d8268ae553d6a9553792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6c829515e216481c4bf4ff1254c815e142c8c185514b757a8165e583e2993c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21178eaa9ee52ef9aeb518bbe7298d50ea4db803734e34250d6899297757eaf`  
		Last Modified: Tue, 30 Sep 2025 01:05:05 GMT  
		Size: 9.8 MB (9797341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a40a5bc2fe437f2b0280daceb165e2a627bce07891a4f55bcd8241d9971bd6`  
		Last Modified: Tue, 30 Sep 2025 00:25:13 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5490cb8d309240642f1897831c644827ce471aebaa68a8f05df988bf3f78abc`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 10.0 MB (9993135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00085c9c88c2277759525e6fa7dd05c92ff43c5b4e2b7d7018467ecf723f2141`  
		Last Modified: Tue, 30 Sep 2025 00:25:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f4210cbcaf6a033f2a9e5a3d583bbdd8f15fbf41dcd4e9f7a214ed88583baf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011236d719b67dfc54b23510f46199e819c7a772990d1b6e5c69502fda864c0b`

```dockerfile
```

-	Layers:
	-	`sha256:1f509e54e78c57161cdfa3bf94b9776f852b0ae94c050fd2fc0e844f823b41ee`  
		Last Modified: Tue, 30 Sep 2025 01:03:18 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1daa488e0e504cbf08110ce934f59f68cd8b82a637ae63fecab4a4afc874e89`  
		Last Modified: Tue, 30 Sep 2025 01:03:19 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:277c04c62b163225dcbe6048562b38a849e62191569e825b288792c9b1371e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536350e22afda81b9a6b5a61189e0c60af1914b7a61b27cf9b78d74be38d2156`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b95cd747690d3966db74c005b579dc0acc5d3d5dd2dc3953aa1b7fc6b2c3319`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.6 MB (9627792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140f894af5ccfce1600e9ef1aec68862bb572a6c05cdaf4fe21f8d4f59adcd0f`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c50f1aecdff6d3a90c06de0fa3b75ae6a7ef656f55abe521fc8033315d90446`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e887eb8931bbe87cbc8ec34c5adb7da8dad6c5c8ed818299f0dc3aefbf0003ff`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f7ec9f740563e67cbccc3b78c217fc472bbf798c083777a623e2dc6e6a1fdf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052ad9a18c0162e5dbf41510ff9dd35c41d913460032c24a43f64d63732f362a`

```dockerfile
```

-	Layers:
	-	`sha256:d1c79bfa1ad00c0f524d4aaf49281ab7c0fe084f4b6013dffa63826cd5c179a8`  
		Last Modified: Tue, 30 Sep 2025 13:03:23 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fe6b31b7b04136764c6a2d82e2fc70e8ddf4fd6343212e0e0546f41ef822ef`  
		Last Modified: Tue, 30 Sep 2025 13:03:24 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bae7ff2e583a31eb0550035094f8540c7f357df7a16af0665ae1268d249a935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf421ffdcb0df224fbb25f93dd890021bbe75c4e456cdb6eb422d78e42fdcbaf`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a959c1367c08d7204de3bb0109468970980a812b5c4337e798e815c0e9ea2f`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09424b46ccb61f3ef162edf8d13ad2562f1d846ae3746d0293f192af68e91583`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8532449ce1c361e4ee15fbc7c2a432f905bcfb701a1fc40058a423bef0edc1`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9303752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7d27ae9849bf6dcb351d79b0cd44942287d6c575275467ba4e0cfde9b7d39`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:bookworm-slim` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a964e7d4b5903b274d925d0bd766f05096ccaad1caf6bc2f3b5e775718e9332e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f901a05f7e319708e98d13963e83b4f2332c84f5a2a11339feb43aceda10f86`

```dockerfile
```

-	Layers:
	-	`sha256:435f5e64358e1da2fff9244350b020e62e6086e9335ed18e7a5208ba301555a2`  
		Last Modified: Wed, 01 Oct 2025 22:03:23 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a381c5d325a55fae7a6dd7a7bc591864f5d68ddbf19eefb960e9ab799658049d`  
		Last Modified: Wed, 01 Oct 2025 22:03:24 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:b418c8d89595a15666738c0d0eb62bdd16042ff2b88510cb992f3efec8d27c8b
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
$ docker pull rethinkdb@sha256:5a18e673ce85f3ef619dae1ff5d007aac763a3be8da9d8268ae553d6a9553792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48021573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6c829515e216481c4bf4ff1254c815e142c8c185514b757a8165e583e2993c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21178eaa9ee52ef9aeb518bbe7298d50ea4db803734e34250d6899297757eaf`  
		Last Modified: Tue, 30 Sep 2025 01:05:05 GMT  
		Size: 9.8 MB (9797341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a40a5bc2fe437f2b0280daceb165e2a627bce07891a4f55bcd8241d9971bd6`  
		Last Modified: Tue, 30 Sep 2025 00:25:13 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5490cb8d309240642f1897831c644827ce471aebaa68a8f05df988bf3f78abc`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 10.0 MB (9993135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00085c9c88c2277759525e6fa7dd05c92ff43c5b4e2b7d7018467ecf723f2141`  
		Last Modified: Tue, 30 Sep 2025 00:25:16 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f4210cbcaf6a033f2a9e5a3d583bbdd8f15fbf41dcd4e9f7a214ed88583baf63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2798483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011236d719b67dfc54b23510f46199e819c7a772990d1b6e5c69502fda864c0b`

```dockerfile
```

-	Layers:
	-	`sha256:1f509e54e78c57161cdfa3bf94b9776f852b0ae94c050fd2fc0e844f823b41ee`  
		Last Modified: Tue, 30 Sep 2025 01:03:18 GMT  
		Size: 2.8 MB (2785036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1daa488e0e504cbf08110ce934f59f68cd8b82a637ae63fecab4a4afc874e89`  
		Last Modified: Tue, 30 Sep 2025 01:03:19 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:277c04c62b163225dcbe6048562b38a849e62191569e825b288792c9b1371e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47095658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536350e22afda81b9a6b5a61189e0c60af1914b7a61b27cf9b78d74be38d2156`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b95cd747690d3966db74c005b579dc0acc5d3d5dd2dc3953aa1b7fc6b2c3319`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.6 MB (9627792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140f894af5ccfce1600e9ef1aec68862bb572a6c05cdaf4fe21f8d4f59adcd0f`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 2.7 KB (2666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c50f1aecdff6d3a90c06de0fa3b75ae6a7ef656f55abe521fc8033315d90446`  
		Last Modified: Tue, 30 Sep 2025 00:13:07 GMT  
		Size: 9.4 MB (9362962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e887eb8931bbe87cbc8ec34c5adb7da8dad6c5c8ed818299f0dc3aefbf0003ff`  
		Last Modified: Tue, 30 Sep 2025 00:13:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:f7ec9f740563e67cbccc3b78c217fc472bbf798c083777a623e2dc6e6a1fdf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052ad9a18c0162e5dbf41510ff9dd35c41d913460032c24a43f64d63732f362a`

```dockerfile
```

-	Layers:
	-	`sha256:d1c79bfa1ad00c0f524d4aaf49281ab7c0fe084f4b6013dffa63826cd5c179a8`  
		Last Modified: Tue, 30 Sep 2025 13:03:23 GMT  
		Size: 2.8 MB (2785371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97fe6b31b7b04136764c6a2d82e2fc70e8ddf4fd6343212e0e0546f41ef822ef`  
		Last Modified: Tue, 30 Sep 2025 13:03:24 GMT  
		Size: 13.6 KB (13629 bytes)  
		MIME: application/vnd.in-toto+json

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:5bae7ff2e583a31eb0550035094f8540c7f357df7a16af0665ae1268d249a935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45487702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf421ffdcb0df224fbb25f93dd890021bbe75c4e456cdb6eb422d78e42fdcbaf`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 13 Dec 2023 22:17:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 13 Dec 2023 22:17:20 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 13 Dec 2023 22:17:20 GMT
VOLUME [/data]
# Wed, 13 Dec 2023 22:17:20 GMT
WORKDIR /data
# Wed, 13 Dec 2023 22:17:20 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 13 Dec 2023 22:17:20 GMT
EXPOSE map[28015/tcp:{} 29015/tcp:{} 8080/tcp:{}]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a959c1367c08d7204de3bb0109468970980a812b5c4337e798e815c0e9ea2f`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9296868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09424b46ccb61f3ef162edf8d13ad2562f1d846ae3746d0293f192af68e91583`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8532449ce1c361e4ee15fbc7c2a432f905bcfb701a1fc40058a423bef0edc1`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 9.3 MB (9303752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e7d27ae9849bf6dcb351d79b0cd44942287d6c575275467ba4e0cfde9b7d39`  
		Last Modified: Tue, 30 Sep 2025 03:05:28 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rethinkdb:latest` - unknown; unknown

```console
$ docker pull rethinkdb@sha256:a964e7d4b5903b274d925d0bd766f05096ccaad1caf6bc2f3b5e775718e9332e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2794685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f901a05f7e319708e98d13963e83b4f2332c84f5a2a11339feb43aceda10f86`

```dockerfile
```

-	Layers:
	-	`sha256:435f5e64358e1da2fff9244350b020e62e6086e9335ed18e7a5208ba301555a2`  
		Last Modified: Wed, 01 Oct 2025 22:03:23 GMT  
		Size: 2.8 MB (2781238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a381c5d325a55fae7a6dd7a7bc591864f5d68ddbf19eefb960e9ab799658049d`  
		Last Modified: Wed, 01 Oct 2025 22:03:24 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
