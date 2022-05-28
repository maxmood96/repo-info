## `rethinkdb:2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:889f762306b99f7f10e0b63c541c993d54b9f041c4a5c0016bd1fb4cc2d9b132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:9569972071c8147960897d43d09bf948cb2100cca9770f06832040190a28f389
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47944607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a469b93d52632feb345acf0c9944b92f8428de0371c5f44399b0b77ac6881582`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 May 2022 01:20:16 GMT
ADD file:4a0bb88956083aa56032fdd9601d9b66c39b18c896ba35ea33594cd75621640a in / 
# Wed, 11 May 2022 01:20:16 GMT
CMD ["bash"]
# Thu, 12 May 2022 17:21:27 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Thu, 12 May 2022 17:21:29 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Thu, 12 May 2022 17:21:29 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Thu, 12 May 2022 17:21:35 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 May 2022 17:21:35 GMT
VOLUME [/data]
# Thu, 12 May 2022 17:21:35 GMT
WORKDIR /data
# Thu, 12 May 2022 17:21:35 GMT
CMD ["rethinkdb" "--bind" "all"]
# Thu, 12 May 2022 17:21:35 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:214ca5fb90323fe769c63a12af092f2572bf1c6b300263e09883909fc865d260`  
		Last Modified: Wed, 11 May 2022 01:25:13 GMT  
		Size: 31.4 MB (31379476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ee87d47f552e4c6bb9037c8da8d655f54ac1d431fbf376a58a0a013d811e1a`  
		Last Modified: Thu, 12 May 2022 17:21:53 GMT  
		Size: 6.3 MB (6326489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1867077eb8d5784aea01b10464c16b4510db67f755692a6f5bb275922fe764bb`  
		Last Modified: Thu, 12 May 2022 17:21:51 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328d9c58ff6f73a2293105d6c8c13c552cafa81f6edd5417b11b7d8526543c83`  
		Last Modified: Thu, 12 May 2022 17:21:53 GMT  
		Size: 10.2 MB (10235826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2956a81ee9c4df9210fdcb626f3b162426c1ac73114b52ac5de50037381c69a5`  
		Last Modified: Thu, 12 May 2022 17:21:52 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:a954878f552e5f047b9f1a49857ebef0795435297735e46c665e5caab4318c53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45543960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86ae2a0a34801ba4ea44048a01025fd5437d38951c4cc82b2135db10d52c069`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 28 May 2022 00:40:39 GMT
ADD file:55b4fe3115c684f545e4e4148c93745f12192976a08c37d090fcac708fb709a7 in / 
# Sat, 28 May 2022 00:40:39 GMT
CMD ["bash"]
# Sat, 28 May 2022 09:29:43 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:29:46 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 28 May 2022 09:29:46 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 28 May 2022 09:29:52 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 09:29:52 GMT
VOLUME [/data]
# Sat, 28 May 2022 09:29:53 GMT
WORKDIR /data
# Sat, 28 May 2022 09:29:54 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 28 May 2022 09:29:55 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:dc1f00a5d701e86e2cd2568b860c61b393d66be1341e7267d07e6e57448ceeba`  
		Last Modified: Sat, 28 May 2022 00:47:35 GMT  
		Size: 30.1 MB (30065728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b59bde64cef75e6f3b25cad2b815ecef10e7cbfaff8ffca2c0a4bbb56c3c9f`  
		Last Modified: Sat, 28 May 2022 09:30:22 GMT  
		Size: 6.1 MB (6103294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6f5f167561e97fd27e8a4f20f857e6cb9a4ada30937ff941aec443f9204c0a`  
		Last Modified: Sat, 28 May 2022 09:30:21 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4391f153d9e2a3fe5f0d92b26db5043423b897aec22ce1c2214c3acca77fa0ca`  
		Last Modified: Sat, 28 May 2022 09:30:23 GMT  
		Size: 9.4 MB (9372180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca29a2e42d8068c963f682a33a6bcf06d98d5369e0d2db696ff05e0889d23005`  
		Last Modified: Sat, 28 May 2022 09:30:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:d634be356e773eb1233155d046cd21a1b3de8c235ff2a228ca1b7ced8cffd6be
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45434371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdabbcd7dcac34349c6c15032f701918d4feb332d634127ff11661e2504be1a6`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 May 2022 00:44:17 GMT
ADD file:d93a1cf64a813d01774cd628dfd683c006e20159e2ab3464c2159c8d9897c725 in / 
# Wed, 11 May 2022 00:44:19 GMT
CMD ["bash"]
# Mon, 23 May 2022 18:53:16 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2022 18:53:22 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Mon, 23 May 2022 18:53:22 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Mon, 23 May 2022 18:53:35 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Mon, 23 May 2022 18:53:37 GMT
VOLUME [/data]
# Mon, 23 May 2022 18:53:38 GMT
WORKDIR /data
# Mon, 23 May 2022 18:53:39 GMT
CMD ["rethinkdb" "--bind" "all"]
# Mon, 23 May 2022 18:53:39 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:9f3750f6094217808e26d471752341db88153c8d5b5f9bb11577b74671303bbc`  
		Last Modified: Wed, 11 May 2022 00:50:03 GMT  
		Size: 29.7 MB (29654739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1705f08fe78d49bdf63dcfaccef415e86bedec5214d1699fc99993982eea4641`  
		Last Modified: Mon, 23 May 2022 18:54:20 GMT  
		Size: 6.2 MB (6204236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd938faa9a3598a5d8f3347c1c6358ef751d9e01733467a8c56734ef710d1ff`  
		Last Modified: Mon, 23 May 2022 18:54:19 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42f99f7b0e8e9738dacac91e1d4c2bfbd36113e455fab0f144d5dd3ecf4716d`  
		Last Modified: Mon, 23 May 2022 18:54:21 GMT  
		Size: 9.6 MB (9572578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b1b429a92c0cdd5d2a457acba4c6c24354bd30aee995af8d67b58803b12f52`  
		Last Modified: Mon, 23 May 2022 18:54:19 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
