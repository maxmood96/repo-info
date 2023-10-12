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
$ docker pull rethinkdb@sha256:c249adaf540a6cfbd4d4bff1f67ac1aff28d8cfce3a73db185e7c74af2f73c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5bfce95e5fcd102d3301a0e3b1215ea41b948af8fff10753645cae32280f3044
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47990270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e957f5cf787c84123b2b33884c47a654bcb47e408510261763f43ef660e359fa`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:02:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 00:02:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 00:02:42 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:42 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 00:02:42 GMT
WORKDIR /data
# Thu, 12 Oct 2023 00:02:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 00:02:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3551f800fad0638fc92a6f5ef549613f1af07a0b944701476e29ccca0f6e1b`  
		Last Modified: Thu, 12 Oct 2023 00:02:56 GMT  
		Size: 6.3 MB (6331657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100bd3e3ecc342ed557ccbee8a0e093abacb5c0a17576aae93e2a88e47b68e03`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc67b92892290badfcfb51c38e3d52c817c823303bfa7c7e3dd28b8c457f753`  
		Last Modified: Thu, 12 Oct 2023 00:02:57 GMT  
		Size: 10.2 MB (10237936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99434c85cae415c01529e16d8296717499c8f642666970c860b4b9eb2c1cb9f4`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:6256df94cecb38320f238cfeb03cc984ee1f74ad6222354a46434ebcd11f35bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45968647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b0ee5627ecfe5470485791fb10c6b6d3058d1f0eff96c1fdbbcd29298fa5a9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:40:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 10:40:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 10:40:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:49 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 10:40:49 GMT
WORKDIR /data
# Thu, 12 Oct 2023 10:40:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 10:40:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020c506c04e7041b62569a2e54ed38d94cd845368522d1b890bedc7edc2d37ce`  
		Last Modified: Thu, 12 Oct 2023 10:41:00 GMT  
		Size: 6.3 MB (6312141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960c63a9985e26674ffa5a483fa5650573c5b2dc516f8bc70c4e74c9e65db7f3`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f578868c7863173d2f24adfa9c1eb37d3bb95aedfbeee41eb9cefec0b87e8c`  
		Last Modified: Thu, 12 Oct 2023 10:41:01 GMT  
		Size: 9.6 MB (9589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f590f506eee2c851122506fe95145257e2e5ac0e9a271b7fbfce2082c5fc79`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a9ca443270b2c7832e9e31742ae7a401b2f94fb71a1818be2109eb5838fec3a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45441971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211c44103fb5056300a0b14a73f4a0e5692e815eb28ddcfa9d1182869d14bd27`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:58 GMT
ADD file:0cfc89fea6da8404b2bccfb0c408dde9e7497e8a93304c4ced9e51bd2b3a319a in / 
# Wed, 11 Oct 2023 17:51:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 12:35:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:35:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 12:35:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 12:36:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:36:02 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 12:36:02 GMT
WORKDIR /data
# Thu, 12 Oct 2023 12:36:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 12:36:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a12df18f4c86c0f825c6b30eb023dc9f30ba0de34f6b97dca708a7247f4f6c49`  
		Last Modified: Wed, 11 Oct 2023 17:57:36 GMT  
		Size: 29.7 MB (29656917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915188ba22d04c05f35609c87347568d894094b35dadb4fff0e8c766639e582a`  
		Last Modified: Thu, 12 Oct 2023 12:36:18 GMT  
		Size: 6.2 MB (6207597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810696e6d8c3db01b1ed051c48160ab1507a2b3b6dfc8bbde7dbe53ec6a1cc42`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48be3ea367d1b4978ed31eeaeb52aa58b2e90c3926bd2349be76597dc77a6a1c`  
		Last Modified: Thu, 12 Oct 2023 12:36:19 GMT  
		Size: 9.6 MB (9574640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f46d8cbaeaa36079add81107914b08ea2ca50a5382a498fb01a18685bb6ab`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:c249adaf540a6cfbd4d4bff1f67ac1aff28d8cfce3a73db185e7c74af2f73c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5bfce95e5fcd102d3301a0e3b1215ea41b948af8fff10753645cae32280f3044
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47990270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e957f5cf787c84123b2b33884c47a654bcb47e408510261763f43ef660e359fa`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:02:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 00:02:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 00:02:42 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:42 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 00:02:42 GMT
WORKDIR /data
# Thu, 12 Oct 2023 00:02:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 00:02:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3551f800fad0638fc92a6f5ef549613f1af07a0b944701476e29ccca0f6e1b`  
		Last Modified: Thu, 12 Oct 2023 00:02:56 GMT  
		Size: 6.3 MB (6331657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100bd3e3ecc342ed557ccbee8a0e093abacb5c0a17576aae93e2a88e47b68e03`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc67b92892290badfcfb51c38e3d52c817c823303bfa7c7e3dd28b8c457f753`  
		Last Modified: Thu, 12 Oct 2023 00:02:57 GMT  
		Size: 10.2 MB (10237936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99434c85cae415c01529e16d8296717499c8f642666970c860b4b9eb2c1cb9f4`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:6256df94cecb38320f238cfeb03cc984ee1f74ad6222354a46434ebcd11f35bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45968647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b0ee5627ecfe5470485791fb10c6b6d3058d1f0eff96c1fdbbcd29298fa5a9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:40:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 10:40:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 10:40:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:49 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 10:40:49 GMT
WORKDIR /data
# Thu, 12 Oct 2023 10:40:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 10:40:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020c506c04e7041b62569a2e54ed38d94cd845368522d1b890bedc7edc2d37ce`  
		Last Modified: Thu, 12 Oct 2023 10:41:00 GMT  
		Size: 6.3 MB (6312141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960c63a9985e26674ffa5a483fa5650573c5b2dc516f8bc70c4e74c9e65db7f3`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f578868c7863173d2f24adfa9c1eb37d3bb95aedfbeee41eb9cefec0b87e8c`  
		Last Modified: Thu, 12 Oct 2023 10:41:01 GMT  
		Size: 9.6 MB (9589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f590f506eee2c851122506fe95145257e2e5ac0e9a271b7fbfce2082c5fc79`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a9ca443270b2c7832e9e31742ae7a401b2f94fb71a1818be2109eb5838fec3a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45441971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211c44103fb5056300a0b14a73f4a0e5692e815eb28ddcfa9d1182869d14bd27`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:58 GMT
ADD file:0cfc89fea6da8404b2bccfb0c408dde9e7497e8a93304c4ced9e51bd2b3a319a in / 
# Wed, 11 Oct 2023 17:51:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 12:35:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:35:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 12:35:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 12:36:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:36:02 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 12:36:02 GMT
WORKDIR /data
# Thu, 12 Oct 2023 12:36:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 12:36:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a12df18f4c86c0f825c6b30eb023dc9f30ba0de34f6b97dca708a7247f4f6c49`  
		Last Modified: Wed, 11 Oct 2023 17:57:36 GMT  
		Size: 29.7 MB (29656917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915188ba22d04c05f35609c87347568d894094b35dadb4fff0e8c766639e582a`  
		Last Modified: Thu, 12 Oct 2023 12:36:18 GMT  
		Size: 6.2 MB (6207597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810696e6d8c3db01b1ed051c48160ab1507a2b3b6dfc8bbde7dbe53ec6a1cc42`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48be3ea367d1b4978ed31eeaeb52aa58b2e90c3926bd2349be76597dc77a6a1c`  
		Last Modified: Thu, 12 Oct 2023 12:36:19 GMT  
		Size: 9.6 MB (9574640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f46d8cbaeaa36079add81107914b08ea2ca50a5382a498fb01a18685bb6ab`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:c249adaf540a6cfbd4d4bff1f67ac1aff28d8cfce3a73db185e7c74af2f73c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5bfce95e5fcd102d3301a0e3b1215ea41b948af8fff10753645cae32280f3044
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47990270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e957f5cf787c84123b2b33884c47a654bcb47e408510261763f43ef660e359fa`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:02:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 00:02:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 00:02:42 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:42 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 00:02:42 GMT
WORKDIR /data
# Thu, 12 Oct 2023 00:02:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 00:02:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3551f800fad0638fc92a6f5ef549613f1af07a0b944701476e29ccca0f6e1b`  
		Last Modified: Thu, 12 Oct 2023 00:02:56 GMT  
		Size: 6.3 MB (6331657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100bd3e3ecc342ed557ccbee8a0e093abacb5c0a17576aae93e2a88e47b68e03`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc67b92892290badfcfb51c38e3d52c817c823303bfa7c7e3dd28b8c457f753`  
		Last Modified: Thu, 12 Oct 2023 00:02:57 GMT  
		Size: 10.2 MB (10237936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99434c85cae415c01529e16d8296717499c8f642666970c860b4b9eb2c1cb9f4`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:6256df94cecb38320f238cfeb03cc984ee1f74ad6222354a46434ebcd11f35bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45968647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b0ee5627ecfe5470485791fb10c6b6d3058d1f0eff96c1fdbbcd29298fa5a9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:40:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 10:40:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 10:40:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:49 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 10:40:49 GMT
WORKDIR /data
# Thu, 12 Oct 2023 10:40:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 10:40:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020c506c04e7041b62569a2e54ed38d94cd845368522d1b890bedc7edc2d37ce`  
		Last Modified: Thu, 12 Oct 2023 10:41:00 GMT  
		Size: 6.3 MB (6312141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960c63a9985e26674ffa5a483fa5650573c5b2dc516f8bc70c4e74c9e65db7f3`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f578868c7863173d2f24adfa9c1eb37d3bb95aedfbeee41eb9cefec0b87e8c`  
		Last Modified: Thu, 12 Oct 2023 10:41:01 GMT  
		Size: 9.6 MB (9589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f590f506eee2c851122506fe95145257e2e5ac0e9a271b7fbfce2082c5fc79`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a9ca443270b2c7832e9e31742ae7a401b2f94fb71a1818be2109eb5838fec3a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45441971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211c44103fb5056300a0b14a73f4a0e5692e815eb28ddcfa9d1182869d14bd27`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:58 GMT
ADD file:0cfc89fea6da8404b2bccfb0c408dde9e7497e8a93304c4ced9e51bd2b3a319a in / 
# Wed, 11 Oct 2023 17:51:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 12:35:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:35:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 12:35:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 12:36:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:36:02 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 12:36:02 GMT
WORKDIR /data
# Thu, 12 Oct 2023 12:36:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 12:36:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a12df18f4c86c0f825c6b30eb023dc9f30ba0de34f6b97dca708a7247f4f6c49`  
		Last Modified: Wed, 11 Oct 2023 17:57:36 GMT  
		Size: 29.7 MB (29656917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915188ba22d04c05f35609c87347568d894094b35dadb4fff0e8c766639e582a`  
		Last Modified: Thu, 12 Oct 2023 12:36:18 GMT  
		Size: 6.2 MB (6207597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810696e6d8c3db01b1ed051c48160ab1507a2b3b6dfc8bbde7dbe53ec6a1cc42`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48be3ea367d1b4978ed31eeaeb52aa58b2e90c3926bd2349be76597dc77a6a1c`  
		Last Modified: Thu, 12 Oct 2023 12:36:19 GMT  
		Size: 9.6 MB (9574640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f46d8cbaeaa36079add81107914b08ea2ca50a5382a498fb01a18685bb6ab`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:c249adaf540a6cfbd4d4bff1f67ac1aff28d8cfce3a73db185e7c74af2f73c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5bfce95e5fcd102d3301a0e3b1215ea41b948af8fff10753645cae32280f3044
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47990270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e957f5cf787c84123b2b33884c47a654bcb47e408510261763f43ef660e359fa`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:02:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 00:02:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 00:02:42 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:42 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 00:02:42 GMT
WORKDIR /data
# Thu, 12 Oct 2023 00:02:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 00:02:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3551f800fad0638fc92a6f5ef549613f1af07a0b944701476e29ccca0f6e1b`  
		Last Modified: Thu, 12 Oct 2023 00:02:56 GMT  
		Size: 6.3 MB (6331657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100bd3e3ecc342ed557ccbee8a0e093abacb5c0a17576aae93e2a88e47b68e03`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc67b92892290badfcfb51c38e3d52c817c823303bfa7c7e3dd28b8c457f753`  
		Last Modified: Thu, 12 Oct 2023 00:02:57 GMT  
		Size: 10.2 MB (10237936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99434c85cae415c01529e16d8296717499c8f642666970c860b4b9eb2c1cb9f4`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:6256df94cecb38320f238cfeb03cc984ee1f74ad6222354a46434ebcd11f35bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45968647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b0ee5627ecfe5470485791fb10c6b6d3058d1f0eff96c1fdbbcd29298fa5a9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:40:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 10:40:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 10:40:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:49 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 10:40:49 GMT
WORKDIR /data
# Thu, 12 Oct 2023 10:40:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 10:40:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020c506c04e7041b62569a2e54ed38d94cd845368522d1b890bedc7edc2d37ce`  
		Last Modified: Thu, 12 Oct 2023 10:41:00 GMT  
		Size: 6.3 MB (6312141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960c63a9985e26674ffa5a483fa5650573c5b2dc516f8bc70c4e74c9e65db7f3`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f578868c7863173d2f24adfa9c1eb37d3bb95aedfbeee41eb9cefec0b87e8c`  
		Last Modified: Thu, 12 Oct 2023 10:41:01 GMT  
		Size: 9.6 MB (9589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f590f506eee2c851122506fe95145257e2e5ac0e9a271b7fbfce2082c5fc79`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a9ca443270b2c7832e9e31742ae7a401b2f94fb71a1818be2109eb5838fec3a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45441971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211c44103fb5056300a0b14a73f4a0e5692e815eb28ddcfa9d1182869d14bd27`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:58 GMT
ADD file:0cfc89fea6da8404b2bccfb0c408dde9e7497e8a93304c4ced9e51bd2b3a319a in / 
# Wed, 11 Oct 2023 17:51:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 12:35:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:35:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 12:35:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 12:36:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:36:02 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 12:36:02 GMT
WORKDIR /data
# Thu, 12 Oct 2023 12:36:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 12:36:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a12df18f4c86c0f825c6b30eb023dc9f30ba0de34f6b97dca708a7247f4f6c49`  
		Last Modified: Wed, 11 Oct 2023 17:57:36 GMT  
		Size: 29.7 MB (29656917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915188ba22d04c05f35609c87347568d894094b35dadb4fff0e8c766639e582a`  
		Last Modified: Thu, 12 Oct 2023 12:36:18 GMT  
		Size: 6.2 MB (6207597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810696e6d8c3db01b1ed051c48160ab1507a2b3b6dfc8bbde7dbe53ec6a1cc42`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48be3ea367d1b4978ed31eeaeb52aa58b2e90c3926bd2349be76597dc77a6a1c`  
		Last Modified: Thu, 12 Oct 2023 12:36:19 GMT  
		Size: 9.6 MB (9574640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f46d8cbaeaa36079add81107914b08ea2ca50a5382a498fb01a18685bb6ab`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.2`

```console
$ docker pull rethinkdb@sha256:c249adaf540a6cfbd4d4bff1f67ac1aff28d8cfce3a73db185e7c74af2f73c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4.2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5bfce95e5fcd102d3301a0e3b1215ea41b948af8fff10753645cae32280f3044
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47990270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e957f5cf787c84123b2b33884c47a654bcb47e408510261763f43ef660e359fa`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:02:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 00:02:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 00:02:42 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:42 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 00:02:42 GMT
WORKDIR /data
# Thu, 12 Oct 2023 00:02:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 00:02:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3551f800fad0638fc92a6f5ef549613f1af07a0b944701476e29ccca0f6e1b`  
		Last Modified: Thu, 12 Oct 2023 00:02:56 GMT  
		Size: 6.3 MB (6331657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100bd3e3ecc342ed557ccbee8a0e093abacb5c0a17576aae93e2a88e47b68e03`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc67b92892290badfcfb51c38e3d52c817c823303bfa7c7e3dd28b8c457f753`  
		Last Modified: Thu, 12 Oct 2023 00:02:57 GMT  
		Size: 10.2 MB (10237936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99434c85cae415c01529e16d8296717499c8f642666970c860b4b9eb2c1cb9f4`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:6256df94cecb38320f238cfeb03cc984ee1f74ad6222354a46434ebcd11f35bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45968647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b0ee5627ecfe5470485791fb10c6b6d3058d1f0eff96c1fdbbcd29298fa5a9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:40:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 10:40:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 10:40:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:49 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 10:40:49 GMT
WORKDIR /data
# Thu, 12 Oct 2023 10:40:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 10:40:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020c506c04e7041b62569a2e54ed38d94cd845368522d1b890bedc7edc2d37ce`  
		Last Modified: Thu, 12 Oct 2023 10:41:00 GMT  
		Size: 6.3 MB (6312141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960c63a9985e26674ffa5a483fa5650573c5b2dc516f8bc70c4e74c9e65db7f3`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f578868c7863173d2f24adfa9c1eb37d3bb95aedfbeee41eb9cefec0b87e8c`  
		Last Modified: Thu, 12 Oct 2023 10:41:01 GMT  
		Size: 9.6 MB (9589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f590f506eee2c851122506fe95145257e2e5ac0e9a271b7fbfce2082c5fc79`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a9ca443270b2c7832e9e31742ae7a401b2f94fb71a1818be2109eb5838fec3a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45441971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211c44103fb5056300a0b14a73f4a0e5692e815eb28ddcfa9d1182869d14bd27`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:58 GMT
ADD file:0cfc89fea6da8404b2bccfb0c408dde9e7497e8a93304c4ced9e51bd2b3a319a in / 
# Wed, 11 Oct 2023 17:51:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 12:35:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:35:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 12:35:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 12:36:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:36:02 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 12:36:02 GMT
WORKDIR /data
# Thu, 12 Oct 2023 12:36:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 12:36:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a12df18f4c86c0f825c6b30eb023dc9f30ba0de34f6b97dca708a7247f4f6c49`  
		Last Modified: Wed, 11 Oct 2023 17:57:36 GMT  
		Size: 29.7 MB (29656917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915188ba22d04c05f35609c87347568d894094b35dadb4fff0e8c766639e582a`  
		Last Modified: Thu, 12 Oct 2023 12:36:18 GMT  
		Size: 6.2 MB (6207597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810696e6d8c3db01b1ed051c48160ab1507a2b3b6dfc8bbde7dbe53ec6a1cc42`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48be3ea367d1b4978ed31eeaeb52aa58b2e90c3926bd2349be76597dc77a6a1c`  
		Last Modified: Thu, 12 Oct 2023 12:36:19 GMT  
		Size: 9.6 MB (9574640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f46d8cbaeaa36079add81107914b08ea2ca50a5382a498fb01a18685bb6ab`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:c249adaf540a6cfbd4d4bff1f67ac1aff28d8cfce3a73db185e7c74af2f73c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4.2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5bfce95e5fcd102d3301a0e3b1215ea41b948af8fff10753645cae32280f3044
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47990270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e957f5cf787c84123b2b33884c47a654bcb47e408510261763f43ef660e359fa`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:02:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 00:02:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 00:02:42 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:42 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 00:02:42 GMT
WORKDIR /data
# Thu, 12 Oct 2023 00:02:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 00:02:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3551f800fad0638fc92a6f5ef549613f1af07a0b944701476e29ccca0f6e1b`  
		Last Modified: Thu, 12 Oct 2023 00:02:56 GMT  
		Size: 6.3 MB (6331657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100bd3e3ecc342ed557ccbee8a0e093abacb5c0a17576aae93e2a88e47b68e03`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc67b92892290badfcfb51c38e3d52c817c823303bfa7c7e3dd28b8c457f753`  
		Last Modified: Thu, 12 Oct 2023 00:02:57 GMT  
		Size: 10.2 MB (10237936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99434c85cae415c01529e16d8296717499c8f642666970c860b4b9eb2c1cb9f4`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:6256df94cecb38320f238cfeb03cc984ee1f74ad6222354a46434ebcd11f35bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45968647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b0ee5627ecfe5470485791fb10c6b6d3058d1f0eff96c1fdbbcd29298fa5a9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:40:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 10:40:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 10:40:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:49 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 10:40:49 GMT
WORKDIR /data
# Thu, 12 Oct 2023 10:40:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 10:40:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020c506c04e7041b62569a2e54ed38d94cd845368522d1b890bedc7edc2d37ce`  
		Last Modified: Thu, 12 Oct 2023 10:41:00 GMT  
		Size: 6.3 MB (6312141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960c63a9985e26674ffa5a483fa5650573c5b2dc516f8bc70c4e74c9e65db7f3`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f578868c7863173d2f24adfa9c1eb37d3bb95aedfbeee41eb9cefec0b87e8c`  
		Last Modified: Thu, 12 Oct 2023 10:41:01 GMT  
		Size: 9.6 MB (9589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f590f506eee2c851122506fe95145257e2e5ac0e9a271b7fbfce2082c5fc79`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a9ca443270b2c7832e9e31742ae7a401b2f94fb71a1818be2109eb5838fec3a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45441971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211c44103fb5056300a0b14a73f4a0e5692e815eb28ddcfa9d1182869d14bd27`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:58 GMT
ADD file:0cfc89fea6da8404b2bccfb0c408dde9e7497e8a93304c4ced9e51bd2b3a319a in / 
# Wed, 11 Oct 2023 17:51:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 12:35:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:35:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 12:35:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 12:36:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:36:02 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 12:36:02 GMT
WORKDIR /data
# Thu, 12 Oct 2023 12:36:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 12:36:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a12df18f4c86c0f825c6b30eb023dc9f30ba0de34f6b97dca708a7247f4f6c49`  
		Last Modified: Wed, 11 Oct 2023 17:57:36 GMT  
		Size: 29.7 MB (29656917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915188ba22d04c05f35609c87347568d894094b35dadb4fff0e8c766639e582a`  
		Last Modified: Thu, 12 Oct 2023 12:36:18 GMT  
		Size: 6.2 MB (6207597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810696e6d8c3db01b1ed051c48160ab1507a2b3b6dfc8bbde7dbe53ec6a1cc42`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48be3ea367d1b4978ed31eeaeb52aa58b2e90c3926bd2349be76597dc77a6a1c`  
		Last Modified: Thu, 12 Oct 2023 12:36:19 GMT  
		Size: 9.6 MB (9574640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f46d8cbaeaa36079add81107914b08ea2ca50a5382a498fb01a18685bb6ab`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:bullseye-slim`

```console
$ docker pull rethinkdb@sha256:c249adaf540a6cfbd4d4bff1f67ac1aff28d8cfce3a73db185e7c74af2f73c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5bfce95e5fcd102d3301a0e3b1215ea41b948af8fff10753645cae32280f3044
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47990270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e957f5cf787c84123b2b33884c47a654bcb47e408510261763f43ef660e359fa`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:02:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 00:02:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 00:02:42 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:42 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 00:02:42 GMT
WORKDIR /data
# Thu, 12 Oct 2023 00:02:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 00:02:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3551f800fad0638fc92a6f5ef549613f1af07a0b944701476e29ccca0f6e1b`  
		Last Modified: Thu, 12 Oct 2023 00:02:56 GMT  
		Size: 6.3 MB (6331657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100bd3e3ecc342ed557ccbee8a0e093abacb5c0a17576aae93e2a88e47b68e03`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc67b92892290badfcfb51c38e3d52c817c823303bfa7c7e3dd28b8c457f753`  
		Last Modified: Thu, 12 Oct 2023 00:02:57 GMT  
		Size: 10.2 MB (10237936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99434c85cae415c01529e16d8296717499c8f642666970c860b4b9eb2c1cb9f4`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:6256df94cecb38320f238cfeb03cc984ee1f74ad6222354a46434ebcd11f35bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45968647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b0ee5627ecfe5470485791fb10c6b6d3058d1f0eff96c1fdbbcd29298fa5a9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:40:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 10:40:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 10:40:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:49 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 10:40:49 GMT
WORKDIR /data
# Thu, 12 Oct 2023 10:40:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 10:40:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020c506c04e7041b62569a2e54ed38d94cd845368522d1b890bedc7edc2d37ce`  
		Last Modified: Thu, 12 Oct 2023 10:41:00 GMT  
		Size: 6.3 MB (6312141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960c63a9985e26674ffa5a483fa5650573c5b2dc516f8bc70c4e74c9e65db7f3`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f578868c7863173d2f24adfa9c1eb37d3bb95aedfbeee41eb9cefec0b87e8c`  
		Last Modified: Thu, 12 Oct 2023 10:41:01 GMT  
		Size: 9.6 MB (9589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f590f506eee2c851122506fe95145257e2e5ac0e9a271b7fbfce2082c5fc79`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a9ca443270b2c7832e9e31742ae7a401b2f94fb71a1818be2109eb5838fec3a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45441971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211c44103fb5056300a0b14a73f4a0e5692e815eb28ddcfa9d1182869d14bd27`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:58 GMT
ADD file:0cfc89fea6da8404b2bccfb0c408dde9e7497e8a93304c4ced9e51bd2b3a319a in / 
# Wed, 11 Oct 2023 17:51:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 12:35:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:35:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 12:35:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 12:36:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:36:02 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 12:36:02 GMT
WORKDIR /data
# Thu, 12 Oct 2023 12:36:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 12:36:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a12df18f4c86c0f825c6b30eb023dc9f30ba0de34f6b97dca708a7247f4f6c49`  
		Last Modified: Wed, 11 Oct 2023 17:57:36 GMT  
		Size: 29.7 MB (29656917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915188ba22d04c05f35609c87347568d894094b35dadb4fff0e8c766639e582a`  
		Last Modified: Thu, 12 Oct 2023 12:36:18 GMT  
		Size: 6.2 MB (6207597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810696e6d8c3db01b1ed051c48160ab1507a2b3b6dfc8bbde7dbe53ec6a1cc42`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48be3ea367d1b4978ed31eeaeb52aa58b2e90c3926bd2349be76597dc77a6a1c`  
		Last Modified: Thu, 12 Oct 2023 12:36:19 GMT  
		Size: 9.6 MB (9574640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f46d8cbaeaa36079add81107914b08ea2ca50a5382a498fb01a18685bb6ab`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:c249adaf540a6cfbd4d4bff1f67ac1aff28d8cfce3a73db185e7c74af2f73c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5bfce95e5fcd102d3301a0e3b1215ea41b948af8fff10753645cae32280f3044
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47990270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e957f5cf787c84123b2b33884c47a654bcb47e408510261763f43ef660e359fa`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 00:02:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 00:02:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 00:02:42 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:02:42 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 00:02:42 GMT
WORKDIR /data
# Thu, 12 Oct 2023 00:02:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 00:02:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3551f800fad0638fc92a6f5ef549613f1af07a0b944701476e29ccca0f6e1b`  
		Last Modified: Thu, 12 Oct 2023 00:02:56 GMT  
		Size: 6.3 MB (6331657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100bd3e3ecc342ed557ccbee8a0e093abacb5c0a17576aae93e2a88e47b68e03`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc67b92892290badfcfb51c38e3d52c817c823303bfa7c7e3dd28b8c457f753`  
		Last Modified: Thu, 12 Oct 2023 00:02:57 GMT  
		Size: 10.2 MB (10237936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99434c85cae415c01529e16d8296717499c8f642666970c860b4b9eb2c1cb9f4`  
		Last Modified: Thu, 12 Oct 2023 00:02:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:6256df94cecb38320f238cfeb03cc984ee1f74ad6222354a46434ebcd11f35bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45968647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b0ee5627ecfe5470485791fb10c6b6d3058d1f0eff96c1fdbbcd29298fa5a9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 10:40:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:44 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 10:40:44 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 10:40:49 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 10:40:49 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 10:40:49 GMT
WORKDIR /data
# Thu, 12 Oct 2023 10:40:49 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 10:40:49 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020c506c04e7041b62569a2e54ed38d94cd845368522d1b890bedc7edc2d37ce`  
		Last Modified: Thu, 12 Oct 2023 10:41:00 GMT  
		Size: 6.3 MB (6312141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960c63a9985e26674ffa5a483fa5650573c5b2dc516f8bc70c4e74c9e65db7f3`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f578868c7863173d2f24adfa9c1eb37d3bb95aedfbeee41eb9cefec0b87e8c`  
		Last Modified: Thu, 12 Oct 2023 10:41:01 GMT  
		Size: 9.6 MB (9589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f590f506eee2c851122506fe95145257e2e5ac0e9a271b7fbfce2082c5fc79`  
		Last Modified: Thu, 12 Oct 2023 10:40:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:a9ca443270b2c7832e9e31742ae7a401b2f94fb71a1818be2109eb5838fec3a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45441971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:211c44103fb5056300a0b14a73f4a0e5692e815eb28ddcfa9d1182869d14bd27`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:58 GMT
ADD file:0cfc89fea6da8404b2bccfb0c408dde9e7497e8a93304c4ced9e51bd2b3a319a in / 
# Wed, 11 Oct 2023 17:51:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 12:35:50 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:35:53 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 Oct 2023 12:35:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 Oct 2023 12:36:01 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 12:36:02 GMT
VOLUME [/data]
# Thu, 12 Oct 2023 12:36:02 GMT
WORKDIR /data
# Thu, 12 Oct 2023 12:36:02 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 Oct 2023 12:36:02 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a12df18f4c86c0f825c6b30eb023dc9f30ba0de34f6b97dca708a7247f4f6c49`  
		Last Modified: Wed, 11 Oct 2023 17:57:36 GMT  
		Size: 29.7 MB (29656917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915188ba22d04c05f35609c87347568d894094b35dadb4fff0e8c766639e582a`  
		Last Modified: Thu, 12 Oct 2023 12:36:18 GMT  
		Size: 6.2 MB (6207597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810696e6d8c3db01b1ed051c48160ab1507a2b3b6dfc8bbde7dbe53ec6a1cc42`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48be3ea367d1b4978ed31eeaeb52aa58b2e90c3926bd2349be76597dc77a6a1c`  
		Last Modified: Thu, 12 Oct 2023 12:36:19 GMT  
		Size: 9.6 MB (9574640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f46d8cbaeaa36079add81107914b08ea2ca50a5382a498fb01a18685bb6ab`  
		Last Modified: Thu, 12 Oct 2023 12:36:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
