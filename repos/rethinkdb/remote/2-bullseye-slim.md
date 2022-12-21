## `rethinkdb:2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:3be9d5fbfebcd55f86e8a3e7685d5681b761f7d8f0500136b16824e9f24898da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:5b9705d9965658087fb3f7a81482c40135dd0b1e8539a7dba19646ac7f64eadf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47982557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63457a4c934446fee6991709cfe2333517db4f4a23e3fbaf001bc4988358282`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 16:26:52 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 16:26:54 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 06 Dec 2022 16:26:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 06 Dec 2022 16:27:00 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 16:27:00 GMT
VOLUME [/data]
# Tue, 06 Dec 2022 16:27:00 GMT
WORKDIR /data
# Tue, 06 Dec 2022 16:27:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 06 Dec 2022 16:27:00 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cf29070222d6912138dddfc52eb5459484d37c4bd6bd496c122354fa158076`  
		Last Modified: Tue, 06 Dec 2022 16:27:15 GMT  
		Size: 6.3 MB (6330234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d0bc6eb3b6fcb98938d9922d794ab678f8989a3d2e6c634e8ac68b11f6e1f6`  
		Last Modified: Tue, 06 Dec 2022 16:27:14 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28046af62bf95c53c600611cf5f9304f2dd491f07b024d5398907aac2f6ec6d3`  
		Last Modified: Tue, 06 Dec 2022 16:27:16 GMT  
		Size: 10.2 MB (10236658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728ed4692a28b2910daf2436a9777989bcde293fa0d23ba58f6843b7d94a255e`  
		Last Modified: Tue, 06 Dec 2022 16:27:14 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:e499683edfa945337c278f8e6b94f3a2c94de49c888a8e4e825cc8b12783f4cc
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45962370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841376fe3f83ebf0706d4a9b33b9c6d8d03a2cee29df86df911aaf972d2a31c9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:34:22 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:34:25 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 06 Dec 2022 10:34:25 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 06 Dec 2022 10:34:29 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 10:34:29 GMT
VOLUME [/data]
# Tue, 06 Dec 2022 10:34:29 GMT
WORKDIR /data
# Tue, 06 Dec 2022 10:34:29 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 06 Dec 2022 10:34:29 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516d13f2f2e2a7425b1e4c4977cfbd73588fe367cf8e4545af3fbc1c525dbf54`  
		Last Modified: Tue, 06 Dec 2022 10:34:45 GMT  
		Size: 6.3 MB (6310756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:425e70ea824b24ab8d43ecf4b11c38dca96584d79493bf67ac1af9e72165798e`  
		Last Modified: Tue, 06 Dec 2022 10:34:44 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c156036bb9dd8e483718cdd1bc6ef91e0323701f62b8045f63cbf64f14feefa6`  
		Last Modified: Tue, 06 Dec 2022 10:34:46 GMT  
		Size: 9.6 MB (9588481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd11dea9767c596c2cf6867ef5bdee0533c41f9a810848b8ee73d3262d5bbc03`  
		Last Modified: Tue, 06 Dec 2022 10:34:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:8f5361caba17a5fbc6b90faf1ab1731278c02a54d85d3013b40d1f006a964d58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45410975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f726dfbfd36336bb4f5a0d1c260b8e0492626b1ea2533ee887b4246f906f4a22`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 21 Dec 2022 01:43:11 GMT
ADD file:c1d41928e802c0b63beb07130c33bcc6dbdeb380a7f47510163cb176891e682a in / 
# Wed, 21 Dec 2022 01:43:14 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 08:44:45 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 08:44:48 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 21 Dec 2022 08:44:48 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 21 Dec 2022 08:44:57 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 08:44:59 GMT
VOLUME [/data]
# Wed, 21 Dec 2022 08:44:59 GMT
WORKDIR /data
# Wed, 21 Dec 2022 08:45:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 21 Dec 2022 08:45:00 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:197dcf20f55386b4c3f5fbace4720b64b5b0b606658b4ea9925121b9dbe7d638`  
		Last Modified: Wed, 21 Dec 2022 01:49:12 GMT  
		Size: 29.6 MB (29629760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd980d39d4f64ec0dfe29f7f1d6d422f834c8e9e737714d78839c17bd567e7b`  
		Last Modified: Wed, 21 Dec 2022 08:45:28 GMT  
		Size: 6.2 MB (6205847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d885d31ab20509679eb5d2c798a036502b4117454798cf21ca7d52e23ed2d2`  
		Last Modified: Wed, 21 Dec 2022 08:45:27 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ce13366e4956bf7b9cb9ecc03620f35ddb829ae98e5f774ce7eeb7e519f79e`  
		Last Modified: Wed, 21 Dec 2022 08:45:28 GMT  
		Size: 9.6 MB (9572550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fedf81ad9d84dbcb58f891d9e7b7a2be2a01e977e3cae0b42ba3ca5d8b47b30`  
		Last Modified: Wed, 21 Dec 2022 08:45:27 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
