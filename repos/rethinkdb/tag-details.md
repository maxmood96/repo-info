<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2-bullseye-slim`](#rethinkdb2-bullseye-slim)
-	[`rethinkdb:2.4`](#rethinkdb24)
-	[`rethinkdb:2.4-bullseye-slim`](#rethinkdb24-bullseye-slim)
-	[`rethinkdb:2.4.2`](#rethinkdb242)
-	[`rethinkdb:2.4.2-bullseye-slim`](#rethinkdb242-bullseye-slim)
-	[`rethinkdb:bullseye-slim`](#rethinkdbbullseye-slim)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:8ef4d8f0081704c7215c433177e17473137877e926f58af45559d3715b6820a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:70f6faa59f8b4967db6d28bbe84444c7fe627b03fe1a489b82e58f13b0a8b666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47964340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acffac2bf53c51984a36f3906662056528df679e3ea208beacf5c287187212a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:01:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:01:56 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 13:01:56 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 13:02:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:02:02 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 13:02:02 GMT
WORKDIR /data
# Sat, 04 Feb 2023 13:02:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 13:02:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53fa130c1287ce339095f98c31e66efa9fd01726eb298f6645bff2667c9f7f0`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 6.3 MB (6328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75ff9d0caee22fca325efbb885a0a0a25fbf216384fb1b1fe1bc75e09319d6b`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38873e24b4376c03c1a284f0ba0bc52dced59107fc146c04e44504b678e77d40`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 10.2 MB (10235828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48054ab7bc7eb6d00ba095d1bda52291ae36fef7dfa8da5a0b8a88a6ea7cd932`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:a03b9bb9465a2ebe19f2322431bf274c1c26e330a328a7dfa2e17dffc2385cf3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45944921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168a189f7011ca6f003ea49717e21ae698d3950dee0281e8a0729222100b875d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:21:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:51 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 17:21:51 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 17:21:56 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:56 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 17:21:56 GMT
WORKDIR /data
# Sat, 04 Feb 2023 17:21:56 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 17:21:56 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38dd4390268ea82788f4098c01533d8c4288e51254613dc8a7c269092d6be5`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 6.3 MB (6309522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f40f152e66346a5e4c31f57e37f58cdb7eadbd06d3a5689406ed0671da805c`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b7c10637f23d56c21cc1ab7e09007f63ff491a20e0b96e1595abbaf278b5c`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 9.6 MB (9587793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858cd5a01bebdd3edc1105d92f7126fdf29a90b40efac1f106027b5e919a7e7f`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:49235255a6b6d0955e3e1e1548759aef3429084a817c358ac42534bd358422d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45428666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f841ffa700f7229003abc4dadd1553762da95dbfcb8f0f1c2d70fefaab4d7159`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 02:41:45 GMT
ADD file:dc3c16b50baeac5b9644e607c8df9606e9583f8598e3ba34bcdd69c669a5904c in / 
# Thu, 09 Feb 2023 02:41:46 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:22:07 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:16 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 10:22:17 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 10:22:30 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:33 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 10:22:34 GMT
WORKDIR /data
# Thu, 09 Feb 2023 10:22:34 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 10:22:35 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:c2f78940fdfbfc5ce5d1d3cff3c27a319451aeb3ec12ff2473073516907fbce9`  
		Last Modified: Thu, 09 Feb 2023 02:46:06 GMT  
		Size: 29.6 MB (29647513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4138c859a689329935867764f236c9c95ffeab4e0c2684b2bdb0fd543661df26`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 6.2 MB (6205774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a0a817fa4f6c77dcdc8990a2ad21a0bd5233343fac9d0513022e5a7c31a2c7`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b5453cd4e003356c6f3f72a4bed2fcd1a70a6ee556ccaa3d3796f31ba7f7ba`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 9.6 MB (9572564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2f805b6a7ac07b467cfb6d16ce3a1a5c56ecd65f188481c6b6e65eb009c93e`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:8ef4d8f0081704c7215c433177e17473137877e926f58af45559d3715b6820a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:70f6faa59f8b4967db6d28bbe84444c7fe627b03fe1a489b82e58f13b0a8b666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47964340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acffac2bf53c51984a36f3906662056528df679e3ea208beacf5c287187212a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:01:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:01:56 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 13:01:56 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 13:02:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:02:02 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 13:02:02 GMT
WORKDIR /data
# Sat, 04 Feb 2023 13:02:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 13:02:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53fa130c1287ce339095f98c31e66efa9fd01726eb298f6645bff2667c9f7f0`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 6.3 MB (6328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75ff9d0caee22fca325efbb885a0a0a25fbf216384fb1b1fe1bc75e09319d6b`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38873e24b4376c03c1a284f0ba0bc52dced59107fc146c04e44504b678e77d40`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 10.2 MB (10235828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48054ab7bc7eb6d00ba095d1bda52291ae36fef7dfa8da5a0b8a88a6ea7cd932`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:a03b9bb9465a2ebe19f2322431bf274c1c26e330a328a7dfa2e17dffc2385cf3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45944921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168a189f7011ca6f003ea49717e21ae698d3950dee0281e8a0729222100b875d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:21:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:51 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 17:21:51 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 17:21:56 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:56 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 17:21:56 GMT
WORKDIR /data
# Sat, 04 Feb 2023 17:21:56 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 17:21:56 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38dd4390268ea82788f4098c01533d8c4288e51254613dc8a7c269092d6be5`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 6.3 MB (6309522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f40f152e66346a5e4c31f57e37f58cdb7eadbd06d3a5689406ed0671da805c`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b7c10637f23d56c21cc1ab7e09007f63ff491a20e0b96e1595abbaf278b5c`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 9.6 MB (9587793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858cd5a01bebdd3edc1105d92f7126fdf29a90b40efac1f106027b5e919a7e7f`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:49235255a6b6d0955e3e1e1548759aef3429084a817c358ac42534bd358422d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45428666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f841ffa700f7229003abc4dadd1553762da95dbfcb8f0f1c2d70fefaab4d7159`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 02:41:45 GMT
ADD file:dc3c16b50baeac5b9644e607c8df9606e9583f8598e3ba34bcdd69c669a5904c in / 
# Thu, 09 Feb 2023 02:41:46 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:22:07 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:16 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 10:22:17 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 10:22:30 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:33 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 10:22:34 GMT
WORKDIR /data
# Thu, 09 Feb 2023 10:22:34 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 10:22:35 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:c2f78940fdfbfc5ce5d1d3cff3c27a319451aeb3ec12ff2473073516907fbce9`  
		Last Modified: Thu, 09 Feb 2023 02:46:06 GMT  
		Size: 29.6 MB (29647513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4138c859a689329935867764f236c9c95ffeab4e0c2684b2bdb0fd543661df26`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 6.2 MB (6205774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a0a817fa4f6c77dcdc8990a2ad21a0bd5233343fac9d0513022e5a7c31a2c7`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b5453cd4e003356c6f3f72a4bed2fcd1a70a6ee556ccaa3d3796f31ba7f7ba`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 9.6 MB (9572564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2f805b6a7ac07b467cfb6d16ce3a1a5c56ecd65f188481c6b6e65eb009c93e`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:8ef4d8f0081704c7215c433177e17473137877e926f58af45559d3715b6820a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:70f6faa59f8b4967db6d28bbe84444c7fe627b03fe1a489b82e58f13b0a8b666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47964340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acffac2bf53c51984a36f3906662056528df679e3ea208beacf5c287187212a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:01:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:01:56 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 13:01:56 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 13:02:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:02:02 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 13:02:02 GMT
WORKDIR /data
# Sat, 04 Feb 2023 13:02:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 13:02:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53fa130c1287ce339095f98c31e66efa9fd01726eb298f6645bff2667c9f7f0`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 6.3 MB (6328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75ff9d0caee22fca325efbb885a0a0a25fbf216384fb1b1fe1bc75e09319d6b`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38873e24b4376c03c1a284f0ba0bc52dced59107fc146c04e44504b678e77d40`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 10.2 MB (10235828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48054ab7bc7eb6d00ba095d1bda52291ae36fef7dfa8da5a0b8a88a6ea7cd932`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:a03b9bb9465a2ebe19f2322431bf274c1c26e330a328a7dfa2e17dffc2385cf3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45944921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168a189f7011ca6f003ea49717e21ae698d3950dee0281e8a0729222100b875d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:21:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:51 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 17:21:51 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 17:21:56 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:56 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 17:21:56 GMT
WORKDIR /data
# Sat, 04 Feb 2023 17:21:56 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 17:21:56 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38dd4390268ea82788f4098c01533d8c4288e51254613dc8a7c269092d6be5`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 6.3 MB (6309522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f40f152e66346a5e4c31f57e37f58cdb7eadbd06d3a5689406ed0671da805c`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b7c10637f23d56c21cc1ab7e09007f63ff491a20e0b96e1595abbaf278b5c`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 9.6 MB (9587793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858cd5a01bebdd3edc1105d92f7126fdf29a90b40efac1f106027b5e919a7e7f`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4` - linux; s390x

```console
$ docker pull rethinkdb@sha256:49235255a6b6d0955e3e1e1548759aef3429084a817c358ac42534bd358422d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45428666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f841ffa700f7229003abc4dadd1553762da95dbfcb8f0f1c2d70fefaab4d7159`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 02:41:45 GMT
ADD file:dc3c16b50baeac5b9644e607c8df9606e9583f8598e3ba34bcdd69c669a5904c in / 
# Thu, 09 Feb 2023 02:41:46 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:22:07 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:16 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 10:22:17 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 10:22:30 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:33 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 10:22:34 GMT
WORKDIR /data
# Thu, 09 Feb 2023 10:22:34 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 10:22:35 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:c2f78940fdfbfc5ce5d1d3cff3c27a319451aeb3ec12ff2473073516907fbce9`  
		Last Modified: Thu, 09 Feb 2023 02:46:06 GMT  
		Size: 29.6 MB (29647513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4138c859a689329935867764f236c9c95ffeab4e0c2684b2bdb0fd543661df26`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 6.2 MB (6205774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a0a817fa4f6c77dcdc8990a2ad21a0bd5233343fac9d0513022e5a7c31a2c7`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b5453cd4e003356c6f3f72a4bed2fcd1a70a6ee556ccaa3d3796f31ba7f7ba`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 9.6 MB (9572564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2f805b6a7ac07b467cfb6d16ce3a1a5c56ecd65f188481c6b6e65eb009c93e`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:8ef4d8f0081704c7215c433177e17473137877e926f58af45559d3715b6820a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:70f6faa59f8b4967db6d28bbe84444c7fe627b03fe1a489b82e58f13b0a8b666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47964340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acffac2bf53c51984a36f3906662056528df679e3ea208beacf5c287187212a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:01:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:01:56 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 13:01:56 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 13:02:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:02:02 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 13:02:02 GMT
WORKDIR /data
# Sat, 04 Feb 2023 13:02:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 13:02:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53fa130c1287ce339095f98c31e66efa9fd01726eb298f6645bff2667c9f7f0`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 6.3 MB (6328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75ff9d0caee22fca325efbb885a0a0a25fbf216384fb1b1fe1bc75e09319d6b`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38873e24b4376c03c1a284f0ba0bc52dced59107fc146c04e44504b678e77d40`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 10.2 MB (10235828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48054ab7bc7eb6d00ba095d1bda52291ae36fef7dfa8da5a0b8a88a6ea7cd932`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:a03b9bb9465a2ebe19f2322431bf274c1c26e330a328a7dfa2e17dffc2385cf3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45944921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168a189f7011ca6f003ea49717e21ae698d3950dee0281e8a0729222100b875d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:21:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:51 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 17:21:51 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 17:21:56 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:56 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 17:21:56 GMT
WORKDIR /data
# Sat, 04 Feb 2023 17:21:56 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 17:21:56 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38dd4390268ea82788f4098c01533d8c4288e51254613dc8a7c269092d6be5`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 6.3 MB (6309522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f40f152e66346a5e4c31f57e37f58cdb7eadbd06d3a5689406ed0671da805c`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b7c10637f23d56c21cc1ab7e09007f63ff491a20e0b96e1595abbaf278b5c`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 9.6 MB (9587793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858cd5a01bebdd3edc1105d92f7126fdf29a90b40efac1f106027b5e919a7e7f`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:49235255a6b6d0955e3e1e1548759aef3429084a817c358ac42534bd358422d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45428666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f841ffa700f7229003abc4dadd1553762da95dbfcb8f0f1c2d70fefaab4d7159`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 02:41:45 GMT
ADD file:dc3c16b50baeac5b9644e607c8df9606e9583f8598e3ba34bcdd69c669a5904c in / 
# Thu, 09 Feb 2023 02:41:46 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:22:07 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:16 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 10:22:17 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 10:22:30 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:33 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 10:22:34 GMT
WORKDIR /data
# Thu, 09 Feb 2023 10:22:34 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 10:22:35 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:c2f78940fdfbfc5ce5d1d3cff3c27a319451aeb3ec12ff2473073516907fbce9`  
		Last Modified: Thu, 09 Feb 2023 02:46:06 GMT  
		Size: 29.6 MB (29647513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4138c859a689329935867764f236c9c95ffeab4e0c2684b2bdb0fd543661df26`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 6.2 MB (6205774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a0a817fa4f6c77dcdc8990a2ad21a0bd5233343fac9d0513022e5a7c31a2c7`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b5453cd4e003356c6f3f72a4bed2fcd1a70a6ee556ccaa3d3796f31ba7f7ba`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 9.6 MB (9572564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2f805b6a7ac07b467cfb6d16ce3a1a5c56ecd65f188481c6b6e65eb009c93e`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.2`

```console
$ docker pull rethinkdb@sha256:8ef4d8f0081704c7215c433177e17473137877e926f58af45559d3715b6820a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4.2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:70f6faa59f8b4967db6d28bbe84444c7fe627b03fe1a489b82e58f13b0a8b666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47964340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acffac2bf53c51984a36f3906662056528df679e3ea208beacf5c287187212a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:01:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:01:56 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 13:01:56 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 13:02:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:02:02 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 13:02:02 GMT
WORKDIR /data
# Sat, 04 Feb 2023 13:02:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 13:02:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53fa130c1287ce339095f98c31e66efa9fd01726eb298f6645bff2667c9f7f0`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 6.3 MB (6328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75ff9d0caee22fca325efbb885a0a0a25fbf216384fb1b1fe1bc75e09319d6b`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38873e24b4376c03c1a284f0ba0bc52dced59107fc146c04e44504b678e77d40`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 10.2 MB (10235828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48054ab7bc7eb6d00ba095d1bda52291ae36fef7dfa8da5a0b8a88a6ea7cd932`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:a03b9bb9465a2ebe19f2322431bf274c1c26e330a328a7dfa2e17dffc2385cf3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45944921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168a189f7011ca6f003ea49717e21ae698d3950dee0281e8a0729222100b875d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:21:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:51 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 17:21:51 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 17:21:56 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:56 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 17:21:56 GMT
WORKDIR /data
# Sat, 04 Feb 2023 17:21:56 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 17:21:56 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38dd4390268ea82788f4098c01533d8c4288e51254613dc8a7c269092d6be5`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 6.3 MB (6309522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f40f152e66346a5e4c31f57e37f58cdb7eadbd06d3a5689406ed0671da805c`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b7c10637f23d56c21cc1ab7e09007f63ff491a20e0b96e1595abbaf278b5c`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 9.6 MB (9587793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858cd5a01bebdd3edc1105d92f7126fdf29a90b40efac1f106027b5e919a7e7f`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:49235255a6b6d0955e3e1e1548759aef3429084a817c358ac42534bd358422d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45428666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f841ffa700f7229003abc4dadd1553762da95dbfcb8f0f1c2d70fefaab4d7159`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 02:41:45 GMT
ADD file:dc3c16b50baeac5b9644e607c8df9606e9583f8598e3ba34bcdd69c669a5904c in / 
# Thu, 09 Feb 2023 02:41:46 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:22:07 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:16 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 10:22:17 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 10:22:30 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:33 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 10:22:34 GMT
WORKDIR /data
# Thu, 09 Feb 2023 10:22:34 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 10:22:35 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:c2f78940fdfbfc5ce5d1d3cff3c27a319451aeb3ec12ff2473073516907fbce9`  
		Last Modified: Thu, 09 Feb 2023 02:46:06 GMT  
		Size: 29.6 MB (29647513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4138c859a689329935867764f236c9c95ffeab4e0c2684b2bdb0fd543661df26`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 6.2 MB (6205774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a0a817fa4f6c77dcdc8990a2ad21a0bd5233343fac9d0513022e5a7c31a2c7`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b5453cd4e003356c6f3f72a4bed2fcd1a70a6ee556ccaa3d3796f31ba7f7ba`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 9.6 MB (9572564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2f805b6a7ac07b467cfb6d16ce3a1a5c56ecd65f188481c6b6e65eb009c93e`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:8ef4d8f0081704c7215c433177e17473137877e926f58af45559d3715b6820a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4.2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:70f6faa59f8b4967db6d28bbe84444c7fe627b03fe1a489b82e58f13b0a8b666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47964340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acffac2bf53c51984a36f3906662056528df679e3ea208beacf5c287187212a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:01:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:01:56 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 13:01:56 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 13:02:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:02:02 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 13:02:02 GMT
WORKDIR /data
# Sat, 04 Feb 2023 13:02:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 13:02:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53fa130c1287ce339095f98c31e66efa9fd01726eb298f6645bff2667c9f7f0`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 6.3 MB (6328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75ff9d0caee22fca325efbb885a0a0a25fbf216384fb1b1fe1bc75e09319d6b`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38873e24b4376c03c1a284f0ba0bc52dced59107fc146c04e44504b678e77d40`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 10.2 MB (10235828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48054ab7bc7eb6d00ba095d1bda52291ae36fef7dfa8da5a0b8a88a6ea7cd932`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:a03b9bb9465a2ebe19f2322431bf274c1c26e330a328a7dfa2e17dffc2385cf3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45944921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168a189f7011ca6f003ea49717e21ae698d3950dee0281e8a0729222100b875d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:21:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:51 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 17:21:51 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 17:21:56 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:56 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 17:21:56 GMT
WORKDIR /data
# Sat, 04 Feb 2023 17:21:56 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 17:21:56 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38dd4390268ea82788f4098c01533d8c4288e51254613dc8a7c269092d6be5`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 6.3 MB (6309522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f40f152e66346a5e4c31f57e37f58cdb7eadbd06d3a5689406ed0671da805c`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b7c10637f23d56c21cc1ab7e09007f63ff491a20e0b96e1595abbaf278b5c`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 9.6 MB (9587793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858cd5a01bebdd3edc1105d92f7126fdf29a90b40efac1f106027b5e919a7e7f`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:49235255a6b6d0955e3e1e1548759aef3429084a817c358ac42534bd358422d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45428666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f841ffa700f7229003abc4dadd1553762da95dbfcb8f0f1c2d70fefaab4d7159`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 02:41:45 GMT
ADD file:dc3c16b50baeac5b9644e607c8df9606e9583f8598e3ba34bcdd69c669a5904c in / 
# Thu, 09 Feb 2023 02:41:46 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:22:07 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:16 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 10:22:17 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 10:22:30 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:33 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 10:22:34 GMT
WORKDIR /data
# Thu, 09 Feb 2023 10:22:34 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 10:22:35 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:c2f78940fdfbfc5ce5d1d3cff3c27a319451aeb3ec12ff2473073516907fbce9`  
		Last Modified: Thu, 09 Feb 2023 02:46:06 GMT  
		Size: 29.6 MB (29647513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4138c859a689329935867764f236c9c95ffeab4e0c2684b2bdb0fd543661df26`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 6.2 MB (6205774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a0a817fa4f6c77dcdc8990a2ad21a0bd5233343fac9d0513022e5a7c31a2c7`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b5453cd4e003356c6f3f72a4bed2fcd1a70a6ee556ccaa3d3796f31ba7f7ba`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 9.6 MB (9572564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2f805b6a7ac07b467cfb6d16ce3a1a5c56ecd65f188481c6b6e65eb009c93e`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:bullseye-slim`

```console
$ docker pull rethinkdb@sha256:8ef4d8f0081704c7215c433177e17473137877e926f58af45559d3715b6820a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:70f6faa59f8b4967db6d28bbe84444c7fe627b03fe1a489b82e58f13b0a8b666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47964340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acffac2bf53c51984a36f3906662056528df679e3ea208beacf5c287187212a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:01:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:01:56 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 13:01:56 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 13:02:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:02:02 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 13:02:02 GMT
WORKDIR /data
# Sat, 04 Feb 2023 13:02:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 13:02:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53fa130c1287ce339095f98c31e66efa9fd01726eb298f6645bff2667c9f7f0`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 6.3 MB (6328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75ff9d0caee22fca325efbb885a0a0a25fbf216384fb1b1fe1bc75e09319d6b`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38873e24b4376c03c1a284f0ba0bc52dced59107fc146c04e44504b678e77d40`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 10.2 MB (10235828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48054ab7bc7eb6d00ba095d1bda52291ae36fef7dfa8da5a0b8a88a6ea7cd932`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:a03b9bb9465a2ebe19f2322431bf274c1c26e330a328a7dfa2e17dffc2385cf3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45944921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168a189f7011ca6f003ea49717e21ae698d3950dee0281e8a0729222100b875d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:21:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:51 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 17:21:51 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 17:21:56 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:56 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 17:21:56 GMT
WORKDIR /data
# Sat, 04 Feb 2023 17:21:56 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 17:21:56 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38dd4390268ea82788f4098c01533d8c4288e51254613dc8a7c269092d6be5`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 6.3 MB (6309522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f40f152e66346a5e4c31f57e37f58cdb7eadbd06d3a5689406ed0671da805c`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b7c10637f23d56c21cc1ab7e09007f63ff491a20e0b96e1595abbaf278b5c`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 9.6 MB (9587793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858cd5a01bebdd3edc1105d92f7126fdf29a90b40efac1f106027b5e919a7e7f`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:49235255a6b6d0955e3e1e1548759aef3429084a817c358ac42534bd358422d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45428666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f841ffa700f7229003abc4dadd1553762da95dbfcb8f0f1c2d70fefaab4d7159`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 02:41:45 GMT
ADD file:dc3c16b50baeac5b9644e607c8df9606e9583f8598e3ba34bcdd69c669a5904c in / 
# Thu, 09 Feb 2023 02:41:46 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:22:07 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:16 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 10:22:17 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 10:22:30 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:33 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 10:22:34 GMT
WORKDIR /data
# Thu, 09 Feb 2023 10:22:34 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 10:22:35 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:c2f78940fdfbfc5ce5d1d3cff3c27a319451aeb3ec12ff2473073516907fbce9`  
		Last Modified: Thu, 09 Feb 2023 02:46:06 GMT  
		Size: 29.6 MB (29647513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4138c859a689329935867764f236c9c95ffeab4e0c2684b2bdb0fd543661df26`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 6.2 MB (6205774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a0a817fa4f6c77dcdc8990a2ad21a0bd5233343fac9d0513022e5a7c31a2c7`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b5453cd4e003356c6f3f72a4bed2fcd1a70a6ee556ccaa3d3796f31ba7f7ba`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 9.6 MB (9572564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2f805b6a7ac07b467cfb6d16ce3a1a5c56ecd65f188481c6b6e65eb009c93e`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:8ef4d8f0081704c7215c433177e17473137877e926f58af45559d3715b6820a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:70f6faa59f8b4967db6d28bbe84444c7fe627b03fe1a489b82e58f13b0a8b666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47964340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6acffac2bf53c51984a36f3906662056528df679e3ea208beacf5c287187212a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 13:01:54 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:01:56 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 13:01:56 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 13:02:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 13:02:02 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 13:02:02 GMT
WORKDIR /data
# Sat, 04 Feb 2023 13:02:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 13:02:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53fa130c1287ce339095f98c31e66efa9fd01726eb298f6645bff2667c9f7f0`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 6.3 MB (6328775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75ff9d0caee22fca325efbb885a0a0a25fbf216384fb1b1fe1bc75e09319d6b`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38873e24b4376c03c1a284f0ba0bc52dced59107fc146c04e44504b678e77d40`  
		Last Modified: Sat, 04 Feb 2023 13:02:17 GMT  
		Size: 10.2 MB (10235828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48054ab7bc7eb6d00ba095d1bda52291ae36fef7dfa8da5a0b8a88a6ea7cd932`  
		Last Modified: Sat, 04 Feb 2023 13:02:15 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:a03b9bb9465a2ebe19f2322431bf274c1c26e330a328a7dfa2e17dffc2385cf3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45944921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168a189f7011ca6f003ea49717e21ae698d3950dee0281e8a0729222100b875d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:37 GMT
ADD file:f613775c59ebd3ca219dc6bbad83115eb74bbbc1980ca4b63e7cb8ab3fa364e4 in / 
# Sat, 04 Feb 2023 06:17:37 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:21:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:51 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 17:21:51 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 17:21:56 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 17:21:56 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 17:21:56 GMT
WORKDIR /data
# Sat, 04 Feb 2023 17:21:56 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 17:21:56 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f79f8cc5c20d534298dd6317333f38b7691da6d66e063ff10699727982c852be`  
		Last Modified: Sat, 04 Feb 2023 06:21:25 GMT  
		Size: 30.0 MB (30044792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d38dd4390268ea82788f4098c01533d8c4288e51254613dc8a7c269092d6be5`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 6.3 MB (6309522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f40f152e66346a5e4c31f57e37f58cdb7eadbd06d3a5689406ed0671da805c`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073b7c10637f23d56c21cc1ab7e09007f63ff491a20e0b96e1595abbaf278b5c`  
		Last Modified: Sat, 04 Feb 2023 17:22:12 GMT  
		Size: 9.6 MB (9587793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858cd5a01bebdd3edc1105d92f7126fdf29a90b40efac1f106027b5e919a7e7f`  
		Last Modified: Sat, 04 Feb 2023 17:22:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:49235255a6b6d0955e3e1e1548759aef3429084a817c358ac42534bd358422d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45428666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f841ffa700f7229003abc4dadd1553762da95dbfcb8f0f1c2d70fefaab4d7159`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 09 Feb 2023 02:41:45 GMT
ADD file:dc3c16b50baeac5b9644e607c8df9606e9583f8598e3ba34bcdd69c669a5904c in / 
# Thu, 09 Feb 2023 02:41:46 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:22:07 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:16 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 09 Feb 2023 10:22:17 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 09 Feb 2023 10:22:30 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:22:33 GMT
VOLUME [/data]
# Thu, 09 Feb 2023 10:22:34 GMT
WORKDIR /data
# Thu, 09 Feb 2023 10:22:34 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 09 Feb 2023 10:22:35 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:c2f78940fdfbfc5ce5d1d3cff3c27a319451aeb3ec12ff2473073516907fbce9`  
		Last Modified: Thu, 09 Feb 2023 02:46:06 GMT  
		Size: 29.6 MB (29647513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4138c859a689329935867764f236c9c95ffeab4e0c2684b2bdb0fd543661df26`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 6.2 MB (6205774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a0a817fa4f6c77dcdc8990a2ad21a0bd5233343fac9d0513022e5a7c31a2c7`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b5453cd4e003356c6f3f72a4bed2fcd1a70a6ee556ccaa3d3796f31ba7f7ba`  
		Last Modified: Thu, 09 Feb 2023 10:23:07 GMT  
		Size: 9.6 MB (9572564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2f805b6a7ac07b467cfb6d16ce3a1a5c56ecd65f188481c6b6e65eb009c93e`  
		Last Modified: Thu, 09 Feb 2023 10:23:06 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
