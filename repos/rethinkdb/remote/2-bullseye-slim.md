## `rethinkdb:2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:84a1029df2456701581cc26407de725b5189db7cab65fabc43fdfa5457467cc8
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
$ docker pull rethinkdb@sha256:98b9d1ff240e7ffabbde6f2d9ead88911fc24932fa1a06a3c204319d25ef013d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45945018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1f67ee184f8eb2a64169c9bf08a35cde45b63cea668571fb5c76de35ef4a9c`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:11:22 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:11:24 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 21 Dec 2022 12:11:24 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 21 Dec 2022 12:11:28 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:11:28 GMT
VOLUME [/data]
# Wed, 21 Dec 2022 12:11:28 GMT
WORKDIR /data
# Wed, 21 Dec 2022 12:11:28 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 21 Dec 2022 12:11:28 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce5e3d19051dfc54d60d52107613ce92403114ab8953db7d5d78ad8e7d517e`  
		Last Modified: Wed, 21 Dec 2022 12:11:45 GMT  
		Size: 6.3 MB (6309647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3eee258e8671b98fc144cb415e949a1fa4b60bce558ed63497947332973fb86`  
		Last Modified: Wed, 21 Dec 2022 12:11:44 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595a83f09cc328bde0b8b8dc1fd1cc19a07bc4d5a210c365649540911b0bc368`  
		Last Modified: Wed, 21 Dec 2022 12:11:47 GMT  
		Size: 9.6 MB (9587782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeedc9f708e9964563f5a897a59807dd585d68b89629a5113dde9e650bbcd7cd`  
		Last Modified: Wed, 21 Dec 2022 12:11:44 GMT  
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
