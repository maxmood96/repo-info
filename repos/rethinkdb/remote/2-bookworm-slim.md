## `rethinkdb:2-bookworm-slim`

```console
$ docker pull rethinkdb@sha256:ded66e2aa8611199483778ee38746c3d8f796e8509a3f4ba62d1def5b528a25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2-bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:ea9b7b0dc7ae26cd29714e7df8a5a537fae0d4537b2611a1357c5ee291bb5e80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49141590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830099f65c358d289727dccc97cda8a8a8cb5e75f98d2e476b8812e60ad760f5`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:38:35 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:38:37 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 24 Apr 2024 08:38:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Wed, 24 Apr 2024 08:38:42 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:38:42 GMT
VOLUME [/data]
# Wed, 24 Apr 2024 08:38:42 GMT
WORKDIR /data
# Wed, 24 Apr 2024 08:38:42 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 24 Apr 2024 08:38:42 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811f1f5f65861187edb2cdfbd26f8bacf9c8751b4c32285cf7832585830884c5`  
		Last Modified: Wed, 24 Apr 2024 08:38:56 GMT  
		Size: 9.8 MB (9789565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23acfb916b8573536a7540b21cb499edfd3e653c2125da515b73ba1edc07a0d9`  
		Last Modified: Wed, 24 Apr 2024 08:38:54 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21ee001743eaeaceb402752098c4889d0efe7d04309c123c6ffa0be493e53cb`  
		Last Modified: Wed, 24 Apr 2024 08:38:56 GMT  
		Size: 10.2 MB (10198729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fee7b493de5b6a2ab7fa8c6c4519776f92948bf3c287a358c7b1c102ed7423`  
		Last Modified: Wed, 24 Apr 2024 08:38:54 GMT  
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
