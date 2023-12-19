## `rethinkdb:bookworm-slim`

```console
$ docker pull rethinkdb@sha256:2f8788caa042dd6a3d58fc8d6f85a6a1312f29105e08c0bd9f451cee1f699069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bookworm-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:0ee83237c6a2c9c0f4b38d1ca48652beac9d38846cb9450844ab6ac861c14be8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49111500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30debf8a5123f891a1122ae9865a2aab58a5357838e290553460f748e8bc4405`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:12:36 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:12:38 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 19 Dec 2023 04:12:38 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 19 Dec 2023 04:12:43 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:12:43 GMT
VOLUME [/data]
# Tue, 19 Dec 2023 04:12:43 GMT
WORKDIR /data
# Tue, 19 Dec 2023 04:12:43 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 19 Dec 2023 04:12:43 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eb3a2188b6b353cf28d7fb4e5e43ec807c20b2686a9e78df0836be465514c9`  
		Last Modified: Tue, 19 Dec 2023 04:12:55 GMT  
		Size: 9.8 MB (9785456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52d50deec548879cd07aa62d94afe73286730ded405c969d8240df161f9b9d9`  
		Last Modified: Tue, 19 Dec 2023 04:12:53 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599e71ceec2269c34d9e2a3431e4cada3a2bc7c7dc1564be81e96aa6c180c55b`  
		Last Modified: Tue, 19 Dec 2023 04:12:55 GMT  
		Size: 10.2 MB (10197267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2a0fa25342b49e391e3c87e16665bc1b807dd204aa2963bff4a8ea6c3425ae`  
		Last Modified: Tue, 19 Dec 2023 04:12:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:88aa6e2f49986b89ea18033b102b427b804b2a792785efe66b130dcf92b8741c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48309612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9486f6aa78b926dc5eb8a336c9aacc79d5ab4a1ce381a1ca02fd79f31d5925d`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 09:42:38 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 09:42:40 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 19 Dec 2023 09:42:40 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 19 Dec 2023 09:42:44 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 09:42:44 GMT
VOLUME [/data]
# Tue, 19 Dec 2023 09:42:45 GMT
WORKDIR /data
# Tue, 19 Dec 2023 09:42:45 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 19 Dec 2023 09:42:45 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d9e5d47f92b0d1c3382cd987384a1012cf09ee02b90169ff2fea873491bf2c`  
		Last Modified: Tue, 19 Dec 2023 09:42:56 GMT  
		Size: 9.6 MB (9582560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7a9ba03937dddb0e804b9884f05d43a52f25b23c5a44e05a35e6a2161ed9de`  
		Last Modified: Tue, 19 Dec 2023 09:42:55 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aead305befdd043c9e63052f23660793b434e03d2785fbbb8caf7010463b682`  
		Last Modified: Tue, 19 Dec 2023 09:42:56 GMT  
		Size: 9.6 MB (9566968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d893606a5d64bffd4e58270b3a564988abc4d992912cf189c1f536a132b4c08`  
		Last Modified: Tue, 19 Dec 2023 09:42:55 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bookworm-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:2f8ed6655daba1446f96d4b7ac1022b8151f698ef0029a25ca387b54e53936c9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46283948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4d4fd23774cfc9f0203e53012f2f32b987dbf927ffb649164c63e7723dfa86`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:37 GMT
ADD file:f06f12fa5a93afc3a79ac4371d24b0a471a5a1818cf34c1d90004c8f410914b9 in / 
# Tue, 19 Dec 2023 01:42:39 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 01:51:44 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 01:51:46 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bookworm bookworm main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 19 Dec 2023 01:51:46 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.4~0bookworm
# Tue, 19 Dec 2023 20:27:28 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 20:27:29 GMT
VOLUME [/data]
# Tue, 19 Dec 2023 20:27:29 GMT
WORKDIR /data
# Tue, 19 Dec 2023 20:27:29 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 19 Dec 2023 20:27:29 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bc6b1888979d3ceb063da848b2034e980e2c2613642159c1e856550b79aa620c`  
		Last Modified: Tue, 19 Dec 2023 01:47:38 GMT  
		Size: 27.5 MB (27491874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa67bbbd280a3692dbe0edcb17a1cf58a16b88a21482917eaf4ea604e8ec1b65`  
		Last Modified: Tue, 19 Dec 2023 20:27:46 GMT  
		Size: 9.3 MB (9281499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5698dc0929ce613fea8ece3acafa0cf00afd47a1795223c4705d9ec75beb0b87`  
		Last Modified: Tue, 19 Dec 2023 20:27:44 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfafe628682c000e76bc80b42cf72cfe96a6c3c16dea372a1cea85b05de44ff2`  
		Last Modified: Tue, 19 Dec 2023 20:27:46 GMT  
		Size: 9.5 MB (9507758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b785c8f6e128ef736390e9e68e8611da6fa64bf51cba2d1ace6dc2ac198b5f34`  
		Last Modified: Tue, 19 Dec 2023 20:27:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
