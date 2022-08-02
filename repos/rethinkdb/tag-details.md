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
$ docker pull rethinkdb@sha256:349d90d37424c299d23196e2ef3d8821fbc409731963ba0cb9456b3942b86ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:8d3a6848c23c5eb7c5936de3fc75d84dc904154f6c6532a0804c7dea97009841
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47933695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b535431c6e2086300d242bc661bae4597bbdd9f5075d47caa85529137c057bad`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:46:46 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:48 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 12:46:48 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 12:46:53 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:53 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 12:46:53 GMT
WORKDIR /data
# Tue, 02 Aug 2022 12:46:53 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 12:46:53 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9658d3e40358a32fad96ece20eee7ef0d804284e37a80faa8d8be5d49689ad7f`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 6.3 MB (6328381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048aa934dab21974b3e48fa7de51c9b3a78444726d74c879be2119c97990ebd6`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3716e23539870975f4f809e8e7030d9f53a77986645d2748c4223d6b0c0b9002`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 10.2 MB (10235741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f612adae7822d56cff91ff5ea875f1d7a4e635ab592ef16fed6208691f8dd5fb`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:17d7c9cde5375503e4d61ff9019b33e6521fe0e59ce921ba96f4c68bf707ba7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45736592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a85a60426b38b58b0447a563ace957c33cd16e38ec2f010be09a69c03be2a1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 12:58:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 12 Jul 2022 12:58:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 12 Jul 2022 12:58:58 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:58 GMT
VOLUME [/data]
# Tue, 12 Jul 2022 12:58:59 GMT
WORKDIR /data
# Tue, 12 Jul 2022 12:59:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 12 Jul 2022 12:59:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd64d21079be01bfbfc2e3c03b980dae2555e3cde8f67989d6548e0a0c4b9e1`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 6.3 MB (6307438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4867547263d5c578be8d148bf9a3b99b196f59f9627d30c077b367aceb822369`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6caa23d65e5714906e1c7785d47a85e8dbff934bdcce0d4c02133f88182274`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 9.4 MB (9372166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f74bd782c64b26192fdef2ea0fce33f70798cf991501e67b01d016173cf896`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:40e237281ee93fee08a956576e0bc0a0119bfe0057ed79726b58804229d0c213
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45419310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcbbb88a70cac8bc2a678c7c328755208c1f97dd27c326db1694d388764f0f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:55:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:04 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 10:55:04 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 10:55:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:10 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 10:55:10 GMT
WORKDIR /data
# Tue, 02 Aug 2022 10:55:10 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 10:55:10 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fe87117e4568bfb6add8dd26572b21afd5c396e49590d988b6eeaee85209e7`  
		Last Modified: Tue, 02 Aug 2022 10:55:39 GMT  
		Size: 6.2 MB (6203854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dcc841a94ada0274732111adc797208e2b26799304e564e96cfe9d93a22165`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71783e804788ed52350649312270c194bc364ca483f0e786efd704615e184a68`  
		Last Modified: Tue, 02 Aug 2022 10:55:40 GMT  
		Size: 9.6 MB (9572383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d483a35165a8fe3b67822a81ac6ebc1c4f71229c351a1f26d309b4c3014b08`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:349d90d37424c299d23196e2ef3d8821fbc409731963ba0cb9456b3942b86ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:8d3a6848c23c5eb7c5936de3fc75d84dc904154f6c6532a0804c7dea97009841
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47933695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b535431c6e2086300d242bc661bae4597bbdd9f5075d47caa85529137c057bad`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:46:46 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:48 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 12:46:48 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 12:46:53 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:53 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 12:46:53 GMT
WORKDIR /data
# Tue, 02 Aug 2022 12:46:53 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 12:46:53 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9658d3e40358a32fad96ece20eee7ef0d804284e37a80faa8d8be5d49689ad7f`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 6.3 MB (6328381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048aa934dab21974b3e48fa7de51c9b3a78444726d74c879be2119c97990ebd6`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3716e23539870975f4f809e8e7030d9f53a77986645d2748c4223d6b0c0b9002`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 10.2 MB (10235741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f612adae7822d56cff91ff5ea875f1d7a4e635ab592ef16fed6208691f8dd5fb`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:17d7c9cde5375503e4d61ff9019b33e6521fe0e59ce921ba96f4c68bf707ba7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45736592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a85a60426b38b58b0447a563ace957c33cd16e38ec2f010be09a69c03be2a1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 12:58:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 12 Jul 2022 12:58:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 12 Jul 2022 12:58:58 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:58 GMT
VOLUME [/data]
# Tue, 12 Jul 2022 12:58:59 GMT
WORKDIR /data
# Tue, 12 Jul 2022 12:59:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 12 Jul 2022 12:59:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd64d21079be01bfbfc2e3c03b980dae2555e3cde8f67989d6548e0a0c4b9e1`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 6.3 MB (6307438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4867547263d5c578be8d148bf9a3b99b196f59f9627d30c077b367aceb822369`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6caa23d65e5714906e1c7785d47a85e8dbff934bdcce0d4c02133f88182274`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 9.4 MB (9372166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f74bd782c64b26192fdef2ea0fce33f70798cf991501e67b01d016173cf896`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:40e237281ee93fee08a956576e0bc0a0119bfe0057ed79726b58804229d0c213
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45419310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcbbb88a70cac8bc2a678c7c328755208c1f97dd27c326db1694d388764f0f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:55:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:04 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 10:55:04 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 10:55:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:10 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 10:55:10 GMT
WORKDIR /data
# Tue, 02 Aug 2022 10:55:10 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 10:55:10 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fe87117e4568bfb6add8dd26572b21afd5c396e49590d988b6eeaee85209e7`  
		Last Modified: Tue, 02 Aug 2022 10:55:39 GMT  
		Size: 6.2 MB (6203854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dcc841a94ada0274732111adc797208e2b26799304e564e96cfe9d93a22165`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71783e804788ed52350649312270c194bc364ca483f0e786efd704615e184a68`  
		Last Modified: Tue, 02 Aug 2022 10:55:40 GMT  
		Size: 9.6 MB (9572383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d483a35165a8fe3b67822a81ac6ebc1c4f71229c351a1f26d309b4c3014b08`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4`

```console
$ docker pull rethinkdb@sha256:349d90d37424c299d23196e2ef3d8821fbc409731963ba0cb9456b3942b86ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4` - linux; amd64

```console
$ docker pull rethinkdb@sha256:8d3a6848c23c5eb7c5936de3fc75d84dc904154f6c6532a0804c7dea97009841
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47933695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b535431c6e2086300d242bc661bae4597bbdd9f5075d47caa85529137c057bad`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:46:46 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:48 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 12:46:48 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 12:46:53 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:53 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 12:46:53 GMT
WORKDIR /data
# Tue, 02 Aug 2022 12:46:53 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 12:46:53 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9658d3e40358a32fad96ece20eee7ef0d804284e37a80faa8d8be5d49689ad7f`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 6.3 MB (6328381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048aa934dab21974b3e48fa7de51c9b3a78444726d74c879be2119c97990ebd6`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3716e23539870975f4f809e8e7030d9f53a77986645d2748c4223d6b0c0b9002`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 10.2 MB (10235741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f612adae7822d56cff91ff5ea875f1d7a4e635ab592ef16fed6208691f8dd5fb`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:17d7c9cde5375503e4d61ff9019b33e6521fe0e59ce921ba96f4c68bf707ba7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45736592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a85a60426b38b58b0447a563ace957c33cd16e38ec2f010be09a69c03be2a1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 12:58:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 12 Jul 2022 12:58:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 12 Jul 2022 12:58:58 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:58 GMT
VOLUME [/data]
# Tue, 12 Jul 2022 12:58:59 GMT
WORKDIR /data
# Tue, 12 Jul 2022 12:59:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 12 Jul 2022 12:59:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd64d21079be01bfbfc2e3c03b980dae2555e3cde8f67989d6548e0a0c4b9e1`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 6.3 MB (6307438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4867547263d5c578be8d148bf9a3b99b196f59f9627d30c077b367aceb822369`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6caa23d65e5714906e1c7785d47a85e8dbff934bdcce0d4c02133f88182274`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 9.4 MB (9372166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f74bd782c64b26192fdef2ea0fce33f70798cf991501e67b01d016173cf896`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4` - linux; s390x

```console
$ docker pull rethinkdb@sha256:40e237281ee93fee08a956576e0bc0a0119bfe0057ed79726b58804229d0c213
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45419310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcbbb88a70cac8bc2a678c7c328755208c1f97dd27c326db1694d388764f0f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:55:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:04 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 10:55:04 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 10:55:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:10 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 10:55:10 GMT
WORKDIR /data
# Tue, 02 Aug 2022 10:55:10 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 10:55:10 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fe87117e4568bfb6add8dd26572b21afd5c396e49590d988b6eeaee85209e7`  
		Last Modified: Tue, 02 Aug 2022 10:55:39 GMT  
		Size: 6.2 MB (6203854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dcc841a94ada0274732111adc797208e2b26799304e564e96cfe9d93a22165`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71783e804788ed52350649312270c194bc364ca483f0e786efd704615e184a68`  
		Last Modified: Tue, 02 Aug 2022 10:55:40 GMT  
		Size: 9.6 MB (9572383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d483a35165a8fe3b67822a81ac6ebc1c4f71229c351a1f26d309b4c3014b08`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:349d90d37424c299d23196e2ef3d8821fbc409731963ba0cb9456b3942b86ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:8d3a6848c23c5eb7c5936de3fc75d84dc904154f6c6532a0804c7dea97009841
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47933695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b535431c6e2086300d242bc661bae4597bbdd9f5075d47caa85529137c057bad`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:46:46 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:48 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 12:46:48 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 12:46:53 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:53 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 12:46:53 GMT
WORKDIR /data
# Tue, 02 Aug 2022 12:46:53 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 12:46:53 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9658d3e40358a32fad96ece20eee7ef0d804284e37a80faa8d8be5d49689ad7f`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 6.3 MB (6328381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048aa934dab21974b3e48fa7de51c9b3a78444726d74c879be2119c97990ebd6`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3716e23539870975f4f809e8e7030d9f53a77986645d2748c4223d6b0c0b9002`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 10.2 MB (10235741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f612adae7822d56cff91ff5ea875f1d7a4e635ab592ef16fed6208691f8dd5fb`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:17d7c9cde5375503e4d61ff9019b33e6521fe0e59ce921ba96f4c68bf707ba7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45736592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a85a60426b38b58b0447a563ace957c33cd16e38ec2f010be09a69c03be2a1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 12:58:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 12 Jul 2022 12:58:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 12 Jul 2022 12:58:58 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:58 GMT
VOLUME [/data]
# Tue, 12 Jul 2022 12:58:59 GMT
WORKDIR /data
# Tue, 12 Jul 2022 12:59:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 12 Jul 2022 12:59:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd64d21079be01bfbfc2e3c03b980dae2555e3cde8f67989d6548e0a0c4b9e1`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 6.3 MB (6307438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4867547263d5c578be8d148bf9a3b99b196f59f9627d30c077b367aceb822369`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6caa23d65e5714906e1c7785d47a85e8dbff934bdcce0d4c02133f88182274`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 9.4 MB (9372166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f74bd782c64b26192fdef2ea0fce33f70798cf991501e67b01d016173cf896`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:40e237281ee93fee08a956576e0bc0a0119bfe0057ed79726b58804229d0c213
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45419310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcbbb88a70cac8bc2a678c7c328755208c1f97dd27c326db1694d388764f0f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:55:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:04 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 10:55:04 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 10:55:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:10 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 10:55:10 GMT
WORKDIR /data
# Tue, 02 Aug 2022 10:55:10 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 10:55:10 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fe87117e4568bfb6add8dd26572b21afd5c396e49590d988b6eeaee85209e7`  
		Last Modified: Tue, 02 Aug 2022 10:55:39 GMT  
		Size: 6.2 MB (6203854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dcc841a94ada0274732111adc797208e2b26799304e564e96cfe9d93a22165`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71783e804788ed52350649312270c194bc364ca483f0e786efd704615e184a68`  
		Last Modified: Tue, 02 Aug 2022 10:55:40 GMT  
		Size: 9.6 MB (9572383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d483a35165a8fe3b67822a81ac6ebc1c4f71229c351a1f26d309b4c3014b08`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.2`

```console
$ docker pull rethinkdb@sha256:349d90d37424c299d23196e2ef3d8821fbc409731963ba0cb9456b3942b86ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4.2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:8d3a6848c23c5eb7c5936de3fc75d84dc904154f6c6532a0804c7dea97009841
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47933695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b535431c6e2086300d242bc661bae4597bbdd9f5075d47caa85529137c057bad`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:46:46 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:48 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 12:46:48 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 12:46:53 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:53 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 12:46:53 GMT
WORKDIR /data
# Tue, 02 Aug 2022 12:46:53 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 12:46:53 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9658d3e40358a32fad96ece20eee7ef0d804284e37a80faa8d8be5d49689ad7f`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 6.3 MB (6328381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048aa934dab21974b3e48fa7de51c9b3a78444726d74c879be2119c97990ebd6`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3716e23539870975f4f809e8e7030d9f53a77986645d2748c4223d6b0c0b9002`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 10.2 MB (10235741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f612adae7822d56cff91ff5ea875f1d7a4e635ab592ef16fed6208691f8dd5fb`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:17d7c9cde5375503e4d61ff9019b33e6521fe0e59ce921ba96f4c68bf707ba7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45736592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a85a60426b38b58b0447a563ace957c33cd16e38ec2f010be09a69c03be2a1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 12:58:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 12 Jul 2022 12:58:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 12 Jul 2022 12:58:58 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:58 GMT
VOLUME [/data]
# Tue, 12 Jul 2022 12:58:59 GMT
WORKDIR /data
# Tue, 12 Jul 2022 12:59:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 12 Jul 2022 12:59:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd64d21079be01bfbfc2e3c03b980dae2555e3cde8f67989d6548e0a0c4b9e1`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 6.3 MB (6307438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4867547263d5c578be8d148bf9a3b99b196f59f9627d30c077b367aceb822369`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6caa23d65e5714906e1c7785d47a85e8dbff934bdcce0d4c02133f88182274`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 9.4 MB (9372166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f74bd782c64b26192fdef2ea0fce33f70798cf991501e67b01d016173cf896`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2` - linux; s390x

```console
$ docker pull rethinkdb@sha256:40e237281ee93fee08a956576e0bc0a0119bfe0057ed79726b58804229d0c213
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45419310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcbbb88a70cac8bc2a678c7c328755208c1f97dd27c326db1694d388764f0f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:55:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:04 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 10:55:04 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 10:55:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:10 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 10:55:10 GMT
WORKDIR /data
# Tue, 02 Aug 2022 10:55:10 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 10:55:10 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fe87117e4568bfb6add8dd26572b21afd5c396e49590d988b6eeaee85209e7`  
		Last Modified: Tue, 02 Aug 2022 10:55:39 GMT  
		Size: 6.2 MB (6203854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dcc841a94ada0274732111adc797208e2b26799304e564e96cfe9d93a22165`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71783e804788ed52350649312270c194bc364ca483f0e786efd704615e184a68`  
		Last Modified: Tue, 02 Aug 2022 10:55:40 GMT  
		Size: 9.6 MB (9572383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d483a35165a8fe3b67822a81ac6ebc1c4f71229c351a1f26d309b4c3014b08`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.4.2-bullseye-slim`

```console
$ docker pull rethinkdb@sha256:349d90d37424c299d23196e2ef3d8821fbc409731963ba0cb9456b3942b86ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:2.4.2-bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:8d3a6848c23c5eb7c5936de3fc75d84dc904154f6c6532a0804c7dea97009841
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47933695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b535431c6e2086300d242bc661bae4597bbdd9f5075d47caa85529137c057bad`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:46:46 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:48 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 12:46:48 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 12:46:53 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:53 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 12:46:53 GMT
WORKDIR /data
# Tue, 02 Aug 2022 12:46:53 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 12:46:53 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9658d3e40358a32fad96ece20eee7ef0d804284e37a80faa8d8be5d49689ad7f`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 6.3 MB (6328381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048aa934dab21974b3e48fa7de51c9b3a78444726d74c879be2119c97990ebd6`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3716e23539870975f4f809e8e7030d9f53a77986645d2748c4223d6b0c0b9002`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 10.2 MB (10235741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f612adae7822d56cff91ff5ea875f1d7a4e635ab592ef16fed6208691f8dd5fb`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:17d7c9cde5375503e4d61ff9019b33e6521fe0e59ce921ba96f4c68bf707ba7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45736592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a85a60426b38b58b0447a563ace957c33cd16e38ec2f010be09a69c03be2a1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 12:58:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 12 Jul 2022 12:58:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 12 Jul 2022 12:58:58 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:58 GMT
VOLUME [/data]
# Tue, 12 Jul 2022 12:58:59 GMT
WORKDIR /data
# Tue, 12 Jul 2022 12:59:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 12 Jul 2022 12:59:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd64d21079be01bfbfc2e3c03b980dae2555e3cde8f67989d6548e0a0c4b9e1`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 6.3 MB (6307438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4867547263d5c578be8d148bf9a3b99b196f59f9627d30c077b367aceb822369`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6caa23d65e5714906e1c7785d47a85e8dbff934bdcce0d4c02133f88182274`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 9.4 MB (9372166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f74bd782c64b26192fdef2ea0fce33f70798cf991501e67b01d016173cf896`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:2.4.2-bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:40e237281ee93fee08a956576e0bc0a0119bfe0057ed79726b58804229d0c213
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45419310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcbbb88a70cac8bc2a678c7c328755208c1f97dd27c326db1694d388764f0f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:55:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:04 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 10:55:04 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 10:55:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:10 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 10:55:10 GMT
WORKDIR /data
# Tue, 02 Aug 2022 10:55:10 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 10:55:10 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fe87117e4568bfb6add8dd26572b21afd5c396e49590d988b6eeaee85209e7`  
		Last Modified: Tue, 02 Aug 2022 10:55:39 GMT  
		Size: 6.2 MB (6203854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dcc841a94ada0274732111adc797208e2b26799304e564e96cfe9d93a22165`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71783e804788ed52350649312270c194bc364ca483f0e786efd704615e184a68`  
		Last Modified: Tue, 02 Aug 2022 10:55:40 GMT  
		Size: 9.6 MB (9572383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d483a35165a8fe3b67822a81ac6ebc1c4f71229c351a1f26d309b4c3014b08`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:bullseye-slim`

```console
$ docker pull rethinkdb@sha256:349d90d37424c299d23196e2ef3d8821fbc409731963ba0cb9456b3942b86ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:8d3a6848c23c5eb7c5936de3fc75d84dc904154f6c6532a0804c7dea97009841
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47933695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b535431c6e2086300d242bc661bae4597bbdd9f5075d47caa85529137c057bad`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:46:46 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:48 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 12:46:48 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 12:46:53 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:53 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 12:46:53 GMT
WORKDIR /data
# Tue, 02 Aug 2022 12:46:53 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 12:46:53 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9658d3e40358a32fad96ece20eee7ef0d804284e37a80faa8d8be5d49689ad7f`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 6.3 MB (6328381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048aa934dab21974b3e48fa7de51c9b3a78444726d74c879be2119c97990ebd6`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3716e23539870975f4f809e8e7030d9f53a77986645d2748c4223d6b0c0b9002`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 10.2 MB (10235741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f612adae7822d56cff91ff5ea875f1d7a4e635ab592ef16fed6208691f8dd5fb`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:17d7c9cde5375503e4d61ff9019b33e6521fe0e59ce921ba96f4c68bf707ba7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45736592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a85a60426b38b58b0447a563ace957c33cd16e38ec2f010be09a69c03be2a1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 12:58:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 12 Jul 2022 12:58:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 12 Jul 2022 12:58:58 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:58 GMT
VOLUME [/data]
# Tue, 12 Jul 2022 12:58:59 GMT
WORKDIR /data
# Tue, 12 Jul 2022 12:59:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 12 Jul 2022 12:59:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd64d21079be01bfbfc2e3c03b980dae2555e3cde8f67989d6548e0a0c4b9e1`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 6.3 MB (6307438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4867547263d5c578be8d148bf9a3b99b196f59f9627d30c077b367aceb822369`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6caa23d65e5714906e1c7785d47a85e8dbff934bdcce0d4c02133f88182274`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 9.4 MB (9372166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f74bd782c64b26192fdef2ea0fce33f70798cf991501e67b01d016173cf896`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:40e237281ee93fee08a956576e0bc0a0119bfe0057ed79726b58804229d0c213
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45419310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcbbb88a70cac8bc2a678c7c328755208c1f97dd27c326db1694d388764f0f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:55:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:04 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 10:55:04 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 10:55:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:10 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 10:55:10 GMT
WORKDIR /data
# Tue, 02 Aug 2022 10:55:10 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 10:55:10 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fe87117e4568bfb6add8dd26572b21afd5c396e49590d988b6eeaee85209e7`  
		Last Modified: Tue, 02 Aug 2022 10:55:39 GMT  
		Size: 6.2 MB (6203854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dcc841a94ada0274732111adc797208e2b26799304e564e96cfe9d93a22165`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71783e804788ed52350649312270c194bc364ca483f0e786efd704615e184a68`  
		Last Modified: Tue, 02 Aug 2022 10:55:40 GMT  
		Size: 9.6 MB (9572383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d483a35165a8fe3b67822a81ac6ebc1c4f71229c351a1f26d309b4c3014b08`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:349d90d37424c299d23196e2ef3d8821fbc409731963ba0cb9456b3942b86ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:8d3a6848c23c5eb7c5936de3fc75d84dc904154f6c6532a0804c7dea97009841
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47933695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b535431c6e2086300d242bc661bae4597bbdd9f5075d47caa85529137c057bad`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:46:46 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:48 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 12:46:48 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 12:46:53 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:46:53 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 12:46:53 GMT
WORKDIR /data
# Tue, 02 Aug 2022 12:46:53 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 12:46:53 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9658d3e40358a32fad96ece20eee7ef0d804284e37a80faa8d8be5d49689ad7f`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 6.3 MB (6328381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048aa934dab21974b3e48fa7de51c9b3a78444726d74c879be2119c97990ebd6`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 2.7 KB (2689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3716e23539870975f4f809e8e7030d9f53a77986645d2748c4223d6b0c0b9002`  
		Last Modified: Tue, 02 Aug 2022 12:47:12 GMT  
		Size: 10.2 MB (10235741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f612adae7822d56cff91ff5ea875f1d7a4e635ab592ef16fed6208691f8dd5fb`  
		Last Modified: Tue, 02 Aug 2022 12:47:11 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:17d7c9cde5375503e4d61ff9019b33e6521fe0e59ce921ba96f4c68bf707ba7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45736592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a85a60426b38b58b0447a563ace957c33cd16e38ec2f010be09a69c03be2a1`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 12 Jul 2022 00:40:34 GMT
ADD file:f3a33075f4c3324c6a634ef37a1965ddd5606b4449c0f5909ce18eeb8268b612 in / 
# Tue, 12 Jul 2022 00:40:35 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 12:58:49 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:52 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 12 Jul 2022 12:58:53 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 12 Jul 2022 12:58:58 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 12:58:58 GMT
VOLUME [/data]
# Tue, 12 Jul 2022 12:58:59 GMT
WORKDIR /data
# Tue, 12 Jul 2022 12:59:00 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 12 Jul 2022 12:59:01 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:60197a4c18d4b386d371cf39d01c48e98c357bba06da0b070a3c1f75006fd838`  
		Last Modified: Tue, 12 Jul 2022 00:46:13 GMT  
		Size: 30.1 MB (30054226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd64d21079be01bfbfc2e3c03b980dae2555e3cde8f67989d6548e0a0c4b9e1`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 6.3 MB (6307438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4867547263d5c578be8d148bf9a3b99b196f59f9627d30c077b367aceb822369`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 2.7 KB (2669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6caa23d65e5714906e1c7785d47a85e8dbff934bdcce0d4c02133f88182274`  
		Last Modified: Tue, 12 Jul 2022 12:59:28 GMT  
		Size: 9.4 MB (9372166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f74bd782c64b26192fdef2ea0fce33f70798cf991501e67b01d016173cf896`  
		Last Modified: Tue, 12 Jul 2022 12:59:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:latest` - linux; s390x

```console
$ docker pull rethinkdb@sha256:40e237281ee93fee08a956576e0bc0a0119bfe0057ed79726b58804229d0c213
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45419310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcbbb88a70cac8bc2a678c7c328755208c1f97dd27c326db1694d388764f0f7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:27 GMT
ADD file:c2afc8990930846fbe7c99bfdfe9ea562c75feb6e3c9122431f7c9f8b5e51a7f in / 
# Tue, 02 Aug 2022 00:42:29 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 10:55:02 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:04 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 02 Aug 2022 10:55:04 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 02 Aug 2022 10:55:09 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 10:55:10 GMT
VOLUME [/data]
# Tue, 02 Aug 2022 10:55:10 GMT
WORKDIR /data
# Tue, 02 Aug 2022 10:55:10 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 02 Aug 2022 10:55:10 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:026d311d0716db60eba0572ea784c21031f420960510cebcc383dc53949b4db8`  
		Last Modified: Tue, 02 Aug 2022 00:48:01 GMT  
		Size: 29.6 MB (29640259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fe87117e4568bfb6add8dd26572b21afd5c396e49590d988b6eeaee85209e7`  
		Last Modified: Tue, 02 Aug 2022 10:55:39 GMT  
		Size: 6.2 MB (6203854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48dcc841a94ada0274732111adc797208e2b26799304e564e96cfe9d93a22165`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71783e804788ed52350649312270c194bc364ca483f0e786efd704615e184a68`  
		Last Modified: Tue, 02 Aug 2022 10:55:40 GMT  
		Size: 9.6 MB (9572383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d483a35165a8fe3b67822a81ac6ebc1c4f71229c351a1f26d309b4c3014b08`  
		Last Modified: Tue, 02 Aug 2022 10:55:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
