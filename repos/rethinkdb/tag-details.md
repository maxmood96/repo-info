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
$ docker pull rethinkdb@sha256:970849ef4bc32c7f8527505eae4f226642206fa735a6bc5df90dcb256039c6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:b6be0f84acf4874044054c34f303028d34c08b6e3fe60716cef323cc33dd2367
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49117652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500977bd1ddcf525547277af1ffe2e88d71f945bfb479a3356b9d84e05754c0c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 13:16:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 10 Apr 2024 13:16:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 10 Apr 2024 13:16:57 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:57 GMT
VOLUME [/data]
# Wed, 10 Apr 2024 13:16:58 GMT
WORKDIR /data
# Wed, 10 Apr 2024 13:16:58 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 10 Apr 2024 13:16:58 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28cb05aed215bfea37c062c57c6af6e0db55081dd901784537ec43ec3f930ee`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 9.8 MB (9786082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6725a6b062d7d686cf47cb52f45dfe25c1ec196c0dd2542cf9995c4fc6a4c26`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89350d47a12bfac59162ea0f7ebd2922862f37cbda97c932776d3f62e0a8ebca`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 10.2 MB (10197394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbee74a2d07cc27382e81e18cc744b8a340991d54a485db2eea8c6e92b24cc6`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:161e52d1adaddd71bf4a0acfe5189d1848364a6cb00a41484d3b39839440a1e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48337826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f264f6824063afe6f31545dd8351a851a4ea550aeb4f9aa23b1c54db5257b48b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:49:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 04:49:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 04:49:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:59 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 04:49:59 GMT
WORKDIR /data
# Wed, 24 Apr 2024 04:49:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 04:49:59 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc0de14d782bc0e476cc0196ae3518fa98f27d11bd27575470ec1038a9d27db`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9586328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab8b57f6e349893d2559c48c31675572b8330a600fa83e437461b3abd4d2ea`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d35ca603a2301536d6e94d426d002c1338d15aec4f67f0e2019983b832842`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9568748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbf530bbb9d4a0f020ddaf2c5b2390cd2e2d733a5890a22a534b2f741111fdb`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:6b6a8a2c9d1589951ca814ea9729cffea3f1ddfdc0ee04687cabde6af63532d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46310148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45092f5be6e118397a74195faa22b8c3b8c7f12240a47a25c5e5489114821749`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:25:01 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:02 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 07:25:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 07:25:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:08 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 07:25:08 GMT
WORKDIR /data
# Wed, 24 Apr 2024 07:25:08 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 07:25:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c146ae76c40a636b316d03e67c65662f5de7c831d30baf4731978d98b3deaab8`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.3 MB (9285344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cbc6100cd15ca3bc75038e0e6518dcad6857b2c70d23e1d188306deac9474f`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25a13af602417073a7a057d59e94fd81f6185c6a78c138e6f7cbb51635420c9`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.5 MB (9509633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68df4505a02404af93c8f916cf5b5786cd1d9fdb6679edf5243af6898f8f3cc`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:970849ef4bc32c7f8527505eae4f226642206fa735a6bc5df90dcb256039c6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:b6be0f84acf4874044054c34f303028d34c08b6e3fe60716cef323cc33dd2367
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49117652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500977bd1ddcf525547277af1ffe2e88d71f945bfb479a3356b9d84e05754c0c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 13:16:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 10 Apr 2024 13:16:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 10 Apr 2024 13:16:57 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:57 GMT
VOLUME [/data]
# Wed, 10 Apr 2024 13:16:58 GMT
WORKDIR /data
# Wed, 10 Apr 2024 13:16:58 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 10 Apr 2024 13:16:58 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28cb05aed215bfea37c062c57c6af6e0db55081dd901784537ec43ec3f930ee`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 9.8 MB (9786082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6725a6b062d7d686cf47cb52f45dfe25c1ec196c0dd2542cf9995c4fc6a4c26`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89350d47a12bfac59162ea0f7ebd2922862f37cbda97c932776d3f62e0a8ebca`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 10.2 MB (10197394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbee74a2d07cc27382e81e18cc744b8a340991d54a485db2eea8c6e92b24cc6`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:161e52d1adaddd71bf4a0acfe5189d1848364a6cb00a41484d3b39839440a1e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48337826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f264f6824063afe6f31545dd8351a851a4ea550aeb4f9aa23b1c54db5257b48b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:49:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 04:49:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 04:49:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:59 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 04:49:59 GMT
WORKDIR /data
# Wed, 24 Apr 2024 04:49:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 04:49:59 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc0de14d782bc0e476cc0196ae3518fa98f27d11bd27575470ec1038a9d27db`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9586328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab8b57f6e349893d2559c48c31675572b8330a600fa83e437461b3abd4d2ea`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d35ca603a2301536d6e94d426d002c1338d15aec4f67f0e2019983b832842`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9568748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbf530bbb9d4a0f020ddaf2c5b2390cd2e2d733a5890a22a534b2f741111fdb`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:6b6a8a2c9d1589951ca814ea9729cffea3f1ddfdc0ee04687cabde6af63532d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46310148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45092f5be6e118397a74195faa22b8c3b8c7f12240a47a25c5e5489114821749`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:25:01 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:02 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 07:25:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 07:25:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:08 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 07:25:08 GMT
WORKDIR /data
# Wed, 24 Apr 2024 07:25:08 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 07:25:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c146ae76c40a636b316d03e67c65662f5de7c831d30baf4731978d98b3deaab8`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.3 MB (9285344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cbc6100cd15ca3bc75038e0e6518dcad6857b2c70d23e1d188306deac9474f`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25a13af602417073a7a057d59e94fd81f6185c6a78c138e6f7cbb51635420c9`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.5 MB (9509633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68df4505a02404af93c8f916cf5b5786cd1d9fdb6679edf5243af6898f8f3cc`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:970849ef4bc32c7f8527505eae4f226642206fa735a6bc5df90dcb256039c6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:b6be0f84acf4874044054c34f303028d34c08b6e3fe60716cef323cc33dd2367
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49117652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500977bd1ddcf525547277af1ffe2e88d71f945bfb479a3356b9d84e05754c0c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 13:16:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 10 Apr 2024 13:16:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 10 Apr 2024 13:16:57 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:57 GMT
VOLUME [/data]
# Wed, 10 Apr 2024 13:16:58 GMT
WORKDIR /data
# Wed, 10 Apr 2024 13:16:58 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 10 Apr 2024 13:16:58 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28cb05aed215bfea37c062c57c6af6e0db55081dd901784537ec43ec3f930ee`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 9.8 MB (9786082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6725a6b062d7d686cf47cb52f45dfe25c1ec196c0dd2542cf9995c4fc6a4c26`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89350d47a12bfac59162ea0f7ebd2922862f37cbda97c932776d3f62e0a8ebca`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 10.2 MB (10197394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbee74a2d07cc27382e81e18cc744b8a340991d54a485db2eea8c6e92b24cc6`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:161e52d1adaddd71bf4a0acfe5189d1848364a6cb00a41484d3b39839440a1e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48337826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f264f6824063afe6f31545dd8351a851a4ea550aeb4f9aa23b1c54db5257b48b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:49:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 04:49:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 04:49:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:59 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 04:49:59 GMT
WORKDIR /data
# Wed, 24 Apr 2024 04:49:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 04:49:59 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc0de14d782bc0e476cc0196ae3518fa98f27d11bd27575470ec1038a9d27db`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9586328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab8b57f6e349893d2559c48c31675572b8330a600fa83e437461b3abd4d2ea`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d35ca603a2301536d6e94d426d002c1338d15aec4f67f0e2019983b832842`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9568748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbf530bbb9d4a0f020ddaf2c5b2390cd2e2d733a5890a22a534b2f741111fdb`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4` - linux; s390x

```console
$ docker pull rethinkdb@sha256:6b6a8a2c9d1589951ca814ea9729cffea3f1ddfdc0ee04687cabde6af63532d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46310148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45092f5be6e118397a74195faa22b8c3b8c7f12240a47a25c5e5489114821749`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:25:01 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:02 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 07:25:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 07:25:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:08 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 07:25:08 GMT
WORKDIR /data
# Wed, 24 Apr 2024 07:25:08 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 07:25:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c146ae76c40a636b316d03e67c65662f5de7c831d30baf4731978d98b3deaab8`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.3 MB (9285344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cbc6100cd15ca3bc75038e0e6518dcad6857b2c70d23e1d188306deac9474f`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25a13af602417073a7a057d59e94fd81f6185c6a78c138e6f7cbb51635420c9`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.5 MB (9509633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68df4505a02404af93c8f916cf5b5786cd1d9fdb6679edf5243af6898f8f3cc`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:970849ef4bc32c7f8527505eae4f226642206fa735a6bc5df90dcb256039c6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:b6be0f84acf4874044054c34f303028d34c08b6e3fe60716cef323cc33dd2367
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49117652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500977bd1ddcf525547277af1ffe2e88d71f945bfb479a3356b9d84e05754c0c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 13:16:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 10 Apr 2024 13:16:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 10 Apr 2024 13:16:57 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:57 GMT
VOLUME [/data]
# Wed, 10 Apr 2024 13:16:58 GMT
WORKDIR /data
# Wed, 10 Apr 2024 13:16:58 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 10 Apr 2024 13:16:58 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28cb05aed215bfea37c062c57c6af6e0db55081dd901784537ec43ec3f930ee`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 9.8 MB (9786082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6725a6b062d7d686cf47cb52f45dfe25c1ec196c0dd2542cf9995c4fc6a4c26`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89350d47a12bfac59162ea0f7ebd2922862f37cbda97c932776d3f62e0a8ebca`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 10.2 MB (10197394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbee74a2d07cc27382e81e18cc744b8a340991d54a485db2eea8c6e92b24cc6`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:161e52d1adaddd71bf4a0acfe5189d1848364a6cb00a41484d3b39839440a1e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48337826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f264f6824063afe6f31545dd8351a851a4ea550aeb4f9aa23b1c54db5257b48b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:49:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 04:49:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 04:49:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:59 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 04:49:59 GMT
WORKDIR /data
# Wed, 24 Apr 2024 04:49:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 04:49:59 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc0de14d782bc0e476cc0196ae3518fa98f27d11bd27575470ec1038a9d27db`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9586328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab8b57f6e349893d2559c48c31675572b8330a600fa83e437461b3abd4d2ea`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d35ca603a2301536d6e94d426d002c1338d15aec4f67f0e2019983b832842`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9568748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbf530bbb9d4a0f020ddaf2c5b2390cd2e2d733a5890a22a534b2f741111fdb`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:6b6a8a2c9d1589951ca814ea9729cffea3f1ddfdc0ee04687cabde6af63532d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46310148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45092f5be6e118397a74195faa22b8c3b8c7f12240a47a25c5e5489114821749`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:25:01 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:02 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 07:25:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 07:25:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:08 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 07:25:08 GMT
WORKDIR /data
# Wed, 24 Apr 2024 07:25:08 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 07:25:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c146ae76c40a636b316d03e67c65662f5de7c831d30baf4731978d98b3deaab8`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.3 MB (9285344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cbc6100cd15ca3bc75038e0e6518dcad6857b2c70d23e1d188306deac9474f`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25a13af602417073a7a057d59e94fd81f6185c6a78c138e6f7cbb51635420c9`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.5 MB (9509633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68df4505a02404af93c8f916cf5b5786cd1d9fdb6679edf5243af6898f8f3cc`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.3`

```console
$ docker pull rethinkdb@sha256:970849ef4bc32c7f8527505eae4f226642206fa735a6bc5df90dcb256039c6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4.3` - linux; amd64

```console
$ docker pull rethinkdb@sha256:b6be0f84acf4874044054c34f303028d34c08b6e3fe60716cef323cc33dd2367
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49117652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500977bd1ddcf525547277af1ffe2e88d71f945bfb479a3356b9d84e05754c0c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 13:16:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 10 Apr 2024 13:16:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 10 Apr 2024 13:16:57 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:57 GMT
VOLUME [/data]
# Wed, 10 Apr 2024 13:16:58 GMT
WORKDIR /data
# Wed, 10 Apr 2024 13:16:58 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 10 Apr 2024 13:16:58 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28cb05aed215bfea37c062c57c6af6e0db55081dd901784537ec43ec3f930ee`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 9.8 MB (9786082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6725a6b062d7d686cf47cb52f45dfe25c1ec196c0dd2542cf9995c4fc6a4c26`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89350d47a12bfac59162ea0f7ebd2922862f37cbda97c932776d3f62e0a8ebca`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 10.2 MB (10197394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbee74a2d07cc27382e81e18cc744b8a340991d54a485db2eea8c6e92b24cc6`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.3` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:161e52d1adaddd71bf4a0acfe5189d1848364a6cb00a41484d3b39839440a1e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48337826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f264f6824063afe6f31545dd8351a851a4ea550aeb4f9aa23b1c54db5257b48b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:49:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 04:49:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 04:49:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:59 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 04:49:59 GMT
WORKDIR /data
# Wed, 24 Apr 2024 04:49:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 04:49:59 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc0de14d782bc0e476cc0196ae3518fa98f27d11bd27575470ec1038a9d27db`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9586328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab8b57f6e349893d2559c48c31675572b8330a600fa83e437461b3abd4d2ea`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d35ca603a2301536d6e94d426d002c1338d15aec4f67f0e2019983b832842`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9568748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbf530bbb9d4a0f020ddaf2c5b2390cd2e2d733a5890a22a534b2f741111fdb`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.3` - linux; s390x

```console
$ docker pull rethinkdb@sha256:6b6a8a2c9d1589951ca814ea9729cffea3f1ddfdc0ee04687cabde6af63532d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46310148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45092f5be6e118397a74195faa22b8c3b8c7f12240a47a25c5e5489114821749`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:25:01 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:02 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 07:25:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 07:25:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:08 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 07:25:08 GMT
WORKDIR /data
# Wed, 24 Apr 2024 07:25:08 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 07:25:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c146ae76c40a636b316d03e67c65662f5de7c831d30baf4731978d98b3deaab8`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.3 MB (9285344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cbc6100cd15ca3bc75038e0e6518dcad6857b2c70d23e1d188306deac9474f`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25a13af602417073a7a057d59e94fd81f6185c6a78c138e6f7cbb51635420c9`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.5 MB (9509633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68df4505a02404af93c8f916cf5b5786cd1d9fdb6679edf5243af6898f8f3cc`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.4-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:970849ef4bc32c7f8527505eae4f226642206fa735a6bc5df90dcb256039c6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4.4-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:b6be0f84acf4874044054c34f303028d34c08b6e3fe60716cef323cc33dd2367
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49117652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500977bd1ddcf525547277af1ffe2e88d71f945bfb479a3356b9d84e05754c0c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 13:16:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 10 Apr 2024 13:16:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 10 Apr 2024 13:16:57 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:57 GMT
VOLUME [/data]
# Wed, 10 Apr 2024 13:16:58 GMT
WORKDIR /data
# Wed, 10 Apr 2024 13:16:58 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 10 Apr 2024 13:16:58 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28cb05aed215bfea37c062c57c6af6e0db55081dd901784537ec43ec3f930ee`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 9.8 MB (9786082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6725a6b062d7d686cf47cb52f45dfe25c1ec196c0dd2542cf9995c4fc6a4c26`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89350d47a12bfac59162ea0f7ebd2922862f37cbda97c932776d3f62e0a8ebca`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 10.2 MB (10197394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbee74a2d07cc27382e81e18cc744b8a340991d54a485db2eea8c6e92b24cc6`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.4-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:161e52d1adaddd71bf4a0acfe5189d1848364a6cb00a41484d3b39839440a1e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48337826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f264f6824063afe6f31545dd8351a851a4ea550aeb4f9aa23b1c54db5257b48b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:49:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 04:49:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 04:49:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:59 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 04:49:59 GMT
WORKDIR /data
# Wed, 24 Apr 2024 04:49:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 04:49:59 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc0de14d782bc0e476cc0196ae3518fa98f27d11bd27575470ec1038a9d27db`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9586328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab8b57f6e349893d2559c48c31675572b8330a600fa83e437461b3abd4d2ea`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d35ca603a2301536d6e94d426d002c1338d15aec4f67f0e2019983b832842`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9568748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbf530bbb9d4a0f020ddaf2c5b2390cd2e2d733a5890a22a534b2f741111fdb`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.4-bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:6b6a8a2c9d1589951ca814ea9729cffea3f1ddfdc0ee04687cabde6af63532d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46310148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45092f5be6e118397a74195faa22b8c3b8c7f12240a47a25c5e5489114821749`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:25:01 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:02 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 07:25:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 07:25:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:08 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 07:25:08 GMT
WORKDIR /data
# Wed, 24 Apr 2024 07:25:08 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 07:25:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c146ae76c40a636b316d03e67c65662f5de7c831d30baf4731978d98b3deaab8`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.3 MB (9285344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cbc6100cd15ca3bc75038e0e6518dcad6857b2c70d23e1d188306deac9474f`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25a13af602417073a7a057d59e94fd81f6185c6a78c138e6f7cbb51635420c9`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.5 MB (9509633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68df4505a02404af93c8f916cf5b5786cd1d9fdb6679edf5243af6898f8f3cc`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:970849ef4bc32c7f8527505eae4f226642206fa735a6bc5df90dcb256039c6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:b6be0f84acf4874044054c34f303028d34c08b6e3fe60716cef323cc33dd2367
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49117652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500977bd1ddcf525547277af1ffe2e88d71f945bfb479a3356b9d84e05754c0c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 13:16:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 10 Apr 2024 13:16:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 10 Apr 2024 13:16:57 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:57 GMT
VOLUME [/data]
# Wed, 10 Apr 2024 13:16:58 GMT
WORKDIR /data
# Wed, 10 Apr 2024 13:16:58 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 10 Apr 2024 13:16:58 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28cb05aed215bfea37c062c57c6af6e0db55081dd901784537ec43ec3f930ee`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 9.8 MB (9786082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6725a6b062d7d686cf47cb52f45dfe25c1ec196c0dd2542cf9995c4fc6a4c26`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89350d47a12bfac59162ea0f7ebd2922862f37cbda97c932776d3f62e0a8ebca`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 10.2 MB (10197394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbee74a2d07cc27382e81e18cc744b8a340991d54a485db2eea8c6e92b24cc6`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:161e52d1adaddd71bf4a0acfe5189d1848364a6cb00a41484d3b39839440a1e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48337826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f264f6824063afe6f31545dd8351a851a4ea550aeb4f9aa23b1c54db5257b48b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:49:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 04:49:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 04:49:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:59 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 04:49:59 GMT
WORKDIR /data
# Wed, 24 Apr 2024 04:49:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 04:49:59 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc0de14d782bc0e476cc0196ae3518fa98f27d11bd27575470ec1038a9d27db`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9586328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab8b57f6e349893d2559c48c31675572b8330a600fa83e437461b3abd4d2ea`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d35ca603a2301536d6e94d426d002c1338d15aec4f67f0e2019983b832842`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9568748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbf530bbb9d4a0f020ddaf2c5b2390cd2e2d733a5890a22a534b2f741111fdb`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:6b6a8a2c9d1589951ca814ea9729cffea3f1ddfdc0ee04687cabde6af63532d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46310148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45092f5be6e118397a74195faa22b8c3b8c7f12240a47a25c5e5489114821749`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:25:01 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:02 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 07:25:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 07:25:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:08 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 07:25:08 GMT
WORKDIR /data
# Wed, 24 Apr 2024 07:25:08 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 07:25:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c146ae76c40a636b316d03e67c65662f5de7c831d30baf4731978d98b3deaab8`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.3 MB (9285344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cbc6100cd15ca3bc75038e0e6518dcad6857b2c70d23e1d188306deac9474f`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25a13af602417073a7a057d59e94fd81f6185c6a78c138e6f7cbb51635420c9`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.5 MB (9509633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68df4505a02404af93c8f916cf5b5786cd1d9fdb6679edf5243af6898f8f3cc`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:970849ef4bc32c7f8527505eae4f226642206fa735a6bc5df90dcb256039c6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:b6be0f84acf4874044054c34f303028d34c08b6e3fe60716cef323cc33dd2367
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49117652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500977bd1ddcf525547277af1ffe2e88d71f945bfb479a3356b9d84e05754c0c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 13:16:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 10 Apr 2024 13:16:52 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 10 Apr 2024 13:16:57 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:16:57 GMT
VOLUME [/data]
# Wed, 10 Apr 2024 13:16:58 GMT
WORKDIR /data
# Wed, 10 Apr 2024 13:16:58 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 10 Apr 2024 13:16:58 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28cb05aed215bfea37c062c57c6af6e0db55081dd901784537ec43ec3f930ee`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 9.8 MB (9786082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6725a6b062d7d686cf47cb52f45dfe25c1ec196c0dd2542cf9995c4fc6a4c26`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89350d47a12bfac59162ea0f7ebd2922862f37cbda97c932776d3f62e0a8ebca`  
		Last Modified: Wed, 10 Apr 2024 13:17:10 GMT  
		Size: 10.2 MB (10197394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbee74a2d07cc27382e81e18cc744b8a340991d54a485db2eea8c6e92b24cc6`  
		Last Modified: Wed, 10 Apr 2024 13:17:09 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:161e52d1adaddd71bf4a0acfe5189d1848364a6cb00a41484d3b39839440a1e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48337826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f264f6824063afe6f31545dd8351a851a4ea550aeb4f9aa23b1c54db5257b48b`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:49:53 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:55 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 04:49:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 04:49:59 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:49:59 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 04:49:59 GMT
WORKDIR /data
# Wed, 24 Apr 2024 04:49:59 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 04:49:59 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc0de14d782bc0e476cc0196ae3518fa98f27d11bd27575470ec1038a9d27db`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9586328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ab8b57f6e349893d2559c48c31675572b8330a600fa83e437461b3abd4d2ea`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d35ca603a2301536d6e94d426d002c1338d15aec4f67f0e2019983b832842`  
		Last Modified: Wed, 24 Apr 2024 04:50:11 GMT  
		Size: 9.6 MB (9568748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbf530bbb9d4a0f020ddaf2c5b2390cd2e2d733a5890a22a534b2f741111fdb`  
		Last Modified: Wed, 24 Apr 2024 04:50:10 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:6b6a8a2c9d1589951ca814ea9729cffea3f1ddfdc0ee04687cabde6af63532d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46310148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45092f5be6e118397a74195faa22b8c3b8c7f12240a47a25c5e5489114821749`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:25:01 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:02 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 07:25:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 07:25:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:25:08 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 07:25:08 GMT
WORKDIR /data
# Wed, 24 Apr 2024 07:25:08 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 07:25:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c146ae76c40a636b316d03e67c65662f5de7c831d30baf4731978d98b3deaab8`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.3 MB (9285344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cbc6100cd15ca3bc75038e0e6518dcad6857b2c70d23e1d188306deac9474f`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25a13af602417073a7a057d59e94fd81f6185c6a78c138e6f7cbb51635420c9`  
		Last Modified: Wed, 24 Apr 2024 07:25:26 GMT  
		Size: 9.5 MB (9509633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68df4505a02404af93c8f916cf5b5786cd1d9fdb6679edf5243af6898f8f3cc`  
		Last Modified: Wed, 24 Apr 2024 07:25:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
