## `rethinkdb:bullseye-slim`

```console
$ docker pull rethinkdb@sha256:98e963c20370dac70997fa01896650335ac157cd6f3ad4101b3b07637abb914f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7185bc3208cb67880882c1e394dafe109882c6cbcfe2dfe4d1505427498d6563
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47985235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da27470ebb24720a148a1f702aee0e4d04ea93e879869e18ebafa98bd36f0c9`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 06:43:21 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:43:23 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 28 Jul 2023 06:43:23 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Fri, 28 Jul 2023 06:43:27 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 06:43:27 GMT
VOLUME [/data]
# Fri, 28 Jul 2023 06:43:27 GMT
WORKDIR /data
# Fri, 28 Jul 2023 06:43:28 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 28 Jul 2023 06:43:28 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b172eab5a6f3a78512b1c90ea230d0fcb54a116e99d1d1bd85031b1e1ecff1`  
		Last Modified: Fri, 28 Jul 2023 06:43:39 GMT  
		Size: 6.3 MB (6328864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b106b21df117121bd8043857ae54b073664e97ef4a3ffed6c5adcb0bd1b16a`  
		Last Modified: Fri, 28 Jul 2023 06:43:38 GMT  
		Size: 2.7 KB (2692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487521c812227025b75716700a8ae506b29d0073c6eaa6ad4e1fd8cdb9b5a709`  
		Last Modified: Fri, 28 Jul 2023 06:43:39 GMT  
		Size: 10.2 MB (10235950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ed3d2a8bf00db84c38872c44f8037e37baab508e247fba50c92bd4c8923b4`  
		Last Modified: Fri, 28 Jul 2023 06:43:38 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:dec90b0b0ab1413a310c6787a1c54f817baab5cb4a40d4a6775513ac38f9313d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45963278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1731b638c50360d564002e3531cc6fdc7934f962ffd2e129620a8abf7045c742`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 10:39:25 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 10:39:28 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 28 Jul 2023 10:39:28 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Fri, 28 Jul 2023 10:39:32 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 10:39:32 GMT
VOLUME [/data]
# Fri, 28 Jul 2023 10:39:32 GMT
WORKDIR /data
# Fri, 28 Jul 2023 10:39:32 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 28 Jul 2023 10:39:32 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b857cece3e37f933269712362543ae25628e1fea03f26d0d5cd312d7c263f185`  
		Last Modified: Fri, 28 Jul 2023 10:39:43 GMT  
		Size: 6.3 MB (6309714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f863076a0dbdd1d65678c91494ccfbcf4d7a45536be9880125b9ba6b6131c84`  
		Last Modified: Fri, 28 Jul 2023 10:39:42 GMT  
		Size: 2.7 KB (2691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082f2d233d029d6f33fbe44852ee6f8615925ab0246da18fb37f318b06eece43`  
		Last Modified: Fri, 28 Jul 2023 10:39:43 GMT  
		Size: 9.6 MB (9587915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d42bd4c243c15f149e36a11511f5dba22554618f8bbc5d509f2a5f2055e57f`  
		Last Modified: Fri, 28 Jul 2023 10:39:42 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:c3dc2d7121f6835e0c4b4c123e5c2591a263d3fab36effd40b9a8261496791c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45433643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7144da494e14b2b3a3fec43369c6f4184c112282024ef6cefcb06e62014caf2`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Jul 2023 01:32:44 GMT
ADD file:799c0afa70fa3bf4bb7804964481cba79e80aa3fad5c7a25beadde206ed6a8ff in / 
# Tue, 04 Jul 2023 01:32:46 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 15:29:15 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:29:18 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Tue, 04 Jul 2023 15:29:18 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Tue, 04 Jul 2023 15:29:23 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 15:29:24 GMT
VOLUME [/data]
# Tue, 04 Jul 2023 15:29:24 GMT
WORKDIR /data
# Tue, 04 Jul 2023 15:29:24 GMT
CMD ["rethinkdb" "--bind" "all"]
# Tue, 04 Jul 2023 15:29:24 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bbee891481f2623da9c7d37a49947926519c858c2b06773370a6189440d4b4de`  
		Last Modified: Tue, 04 Jul 2023 01:37:37 GMT  
		Size: 29.7 MB (29652540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d68900db98922447645c2cc554583c01a3e2a694c509242a91825dbc3829b23`  
		Last Modified: Tue, 04 Jul 2023 15:29:41 GMT  
		Size: 6.2 MB (6205715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b32ce839ea647eb94c2de63c246ff170767a6a3b46faf90655e9acb2c343326`  
		Last Modified: Tue, 04 Jul 2023 15:29:40 GMT  
		Size: 2.7 KB (2687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c496f2632917e986f8daebbab33d2d6d13bf16457c1cecb6aa3a5493afa07332`  
		Last Modified: Tue, 04 Jul 2023 15:29:42 GMT  
		Size: 9.6 MB (9572574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e4129f50d6675ba63ab59750d612ba83b0a0d8277002e2cffcf3910ea9b142`  
		Last Modified: Tue, 04 Jul 2023 15:29:41 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
