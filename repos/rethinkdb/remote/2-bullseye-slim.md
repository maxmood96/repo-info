## `rethinkdb:2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:fd62e55e35cb96bc451fb8afde797024c598ee63dc548bcc10f6ba1c79778266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:47ce162da5b38ab925199f3fdd1afc3cf0f7d6b12d7afcac8d7192cdb9b7a056
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47982287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d316adf0b5e1da7359901f9a7130e119bc49803bdf917b5512065eac8aca1ee`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 14:07:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:07:51 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 15 Nov 2022 14:07:51 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 15 Nov 2022 14:07:56 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 14:07:56 GMT
VOLUME [/data]
# Tue, 15 Nov 2022 14:07:56 GMT
WORKDIR /data
# Tue, 15 Nov 2022 14:07:57 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 15 Nov 2022 14:07:57 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c3d907c81a02cec1310ced02ff0e21788dabfc822819b65c93801244172016`  
		Last Modified: Tue, 15 Nov 2022 14:08:13 GMT  
		Size: 6.3 MB (6330161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179f9af0a3d48bd5e3954f27a80863110e0492444666a0af357fba32b0d17c89`  
		Last Modified: Tue, 15 Nov 2022 14:08:12 GMT  
		Size: 2.7 KB (2685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c6640bd3d29e08a2fe912e138f71b54f6b9c8a21d1695240c784a9b2315ad2`  
		Last Modified: Tue, 15 Nov 2022 14:08:13 GMT  
		Size: 10.2 MB (10236684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85868eee933d701f1ebaa6f0ef0fe495a52191e06f12caf07a864ca2cd8cdf8`  
		Last Modified: Tue, 15 Nov 2022 14:08:12 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:b7a9d55b65e588c8cea5d1299d6c8288aea69ec12e98c346bc78beec13078430
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45962666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593cb8c6863721682f6b1403d9b508371c3c73baa3863a385cc5f5e90936f97a`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:26:18 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:26:19 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 15 Nov 2022 13:26:19 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 15 Nov 2022 13:26:23 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:26:23 GMT
VOLUME [/data]
# Tue, 15 Nov 2022 13:26:24 GMT
WORKDIR /data
# Tue, 15 Nov 2022 13:26:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 15 Nov 2022 13:26:24 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f080479308b0a99b5914a6598c168078a62ee662c43546d7e626551ca592d0`  
		Last Modified: Tue, 15 Nov 2022 13:26:41 GMT  
		Size: 6.3 MB (6310717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de88b0dd01aac73857e8b271674784b6fda7a2f7f75acbb8a0f6d6f11771c1da`  
		Last Modified: Tue, 15 Nov 2022 13:26:39 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eeb7bd2ff7043cc43bf127e0c0c1c39b53b6e177f9751550b7c51c383ba6dc`  
		Last Modified: Tue, 15 Nov 2022 13:26:41 GMT  
		Size: 9.6 MB (9588532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6837886e49ed64583269d28e6d086a3fd1fcc90052754d650e442e96edfc40b5`  
		Last Modified: Tue, 15 Nov 2022 13:26:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:e70e937a0a4e7a5cdd5537fe80d31bdc8a2078886ff945bf42a2aa23bf2d86e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45427041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77615cd9ba533045006e5c3bd66f14b6a4aaa027060f271f05ca39636f9e9fff`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 06 Dec 2022 01:43:03 GMT
ADD file:f9243ad65309c3c458bf646b21aced55c055f7601340b3bda80ec30ff2f62159 in / 
# Tue, 06 Dec 2022 01:43:06 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 06:03:17 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 06:03:21 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 06 Dec 2022 06:03:21 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 06 Dec 2022 06:03:27 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 06:03:28 GMT
VOLUME [/data]
# Tue, 06 Dec 2022 06:03:28 GMT
WORKDIR /data
# Tue, 06 Dec 2022 06:03:28 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 06 Dec 2022 06:03:28 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:66bc250ceea32b3e395aec7bb63aad4ac079791df67a2732692841e8dfacac94`  
		Last Modified: Tue, 06 Dec 2022 01:48:46 GMT  
		Size: 29.6 MB (29643886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f371bc64ab72156751e46470bbf8a4912d5cb73322a840fe2ac16d78c8b986e`  
		Last Modified: Tue, 06 Dec 2022 06:03:58 GMT  
		Size: 6.2 MB (6207184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3e0705316e1acdc4317c6bc49bb6fad18b6e45e59ec4473f02a696c96b6c82`  
		Last Modified: Tue, 06 Dec 2022 06:03:57 GMT  
		Size: 2.7 KB (2685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab23f086b853f2aaa9fe161f2c02b549cd954b32fc67757f5610559c6e0c4b29`  
		Last Modified: Tue, 06 Dec 2022 06:03:58 GMT  
		Size: 9.6 MB (9573159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b048751048c2987c37a12cd0b680a33715d2429ce5d5cc4f82934642d1b2612`  
		Last Modified: Tue, 06 Dec 2022 06:03:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
