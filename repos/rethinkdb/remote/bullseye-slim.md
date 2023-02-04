## `rethinkdb:bullseye-slim`

```console
$ docker pull rethinkdb@sha256:7cc70b26fce4023a3daeca56872125216092fbdf17b431335cad784fa42fadd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `rethinkdb:bullseye-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:e139ebd9e9fdbdb86f71c332b44f7dedc4b0c4820591f6fd56d5c73c63a82796
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (47964214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e717e8739141ed1e8b51f7fc9ac3eb4185c922a828d31e9bcaa10fe5e082ac7`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 09:19:30 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 09:19:32 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 11 Jan 2023 09:19:32 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 11 Jan 2023 09:19:38 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 09:19:38 GMT
VOLUME [/data]
# Wed, 11 Jan 2023 09:19:38 GMT
WORKDIR /data
# Wed, 11 Jan 2023 09:19:38 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 11 Jan 2023 09:19:38 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2998c7e739db6bcaea9a7b3cabf4f25b597db88ef9f7d65ceb33939c8bec2749`  
		Last Modified: Wed, 11 Jan 2023 09:19:52 GMT  
		Size: 6.3 MB (6328626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f361d5a132ddacfec2789fd00ec40bf38d752166cbcead43fa1fe10c55a55f0`  
		Last Modified: Wed, 11 Jan 2023 09:19:51 GMT  
		Size: 2.7 KB (2690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3470b3635b2e9a1fec37cbf7b34bcc4865ddbee9e3caec9baa15b78c266e10a9`  
		Last Modified: Wed, 11 Jan 2023 09:19:53 GMT  
		Size: 10.2 MB (10235799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b2558bd19c4122ebfd94cf162670cfde08ded89beff593f70e2d043c5e618c`  
		Last Modified: Wed, 11 Jan 2023 09:19:51 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull rethinkdb@sha256:1ced779c11a27d90afd1e1726e7f2047c5280526fd601c7a0ed73e6fb50d0a89
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45945064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ea22f06b9a74f45d7e87d6d71cb5e50d009092d3d7ebcddd3dfe2139b2aab3`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 11 Jan 2023 02:57:34 GMT
ADD file:92cf2c9ffaaea1a6bc1baa7b681303b1029dfd6ddbfef1792be8b21aaf09235c in / 
# Wed, 11 Jan 2023 02:57:35 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 15:08:13 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 15:08:15 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 11 Jan 2023 15:08:15 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Wed, 11 Jan 2023 15:08:19 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 15:08:19 GMT
VOLUME [/data]
# Wed, 11 Jan 2023 15:08:19 GMT
WORKDIR /data
# Wed, 11 Jan 2023 15:08:19 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 11 Jan 2023 15:08:19 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:934ce60d1040c5d4922bae5879321a398777457b7514de02ef69ece49e6aa907`  
		Last Modified: Wed, 11 Jan 2023 03:01:19 GMT  
		Size: 30.0 MB (30044814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337e7241eafef12e53defd2307dc110facd44b6a59a466d17b00405e846c2dcd`  
		Last Modified: Wed, 11 Jan 2023 15:08:35 GMT  
		Size: 6.3 MB (6309612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bac949029660534ebba3318694b679fb69eb42439fa4b6a5c139ea459666fb6`  
		Last Modified: Wed, 11 Jan 2023 15:08:34 GMT  
		Size: 2.7 KB (2688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9ce14fe62cca8962c9faaeddb626bb3b97175d49acd06453c65227ea33ee43`  
		Last Modified: Wed, 11 Jan 2023 15:08:36 GMT  
		Size: 9.6 MB (9587823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356174cc74f6526ea66148e326454b6568edebbac471a475ba9592fad4a9bf78`  
		Last Modified: Wed, 11 Jan 2023 15:08:34 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `rethinkdb:bullseye-slim` - linux; s390x

```console
$ docker pull rethinkdb@sha256:1567a44f73035de2de947502fc8224261a375ab8c79a63c0fc85a4211e345de6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45410584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12267b01c5b6c39e19ffcdd7e5d76921f2cb0a0fe4e80c777398e700861fa286`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Sat, 04 Feb 2023 04:06:15 GMT
ADD file:29a3ecb38611dbbb6f45b2d10ad3cee60c0198429376f999e9a397f9c405820e in / 
# Sat, 04 Feb 2023 04:06:17 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 10:47:13 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2 curl     && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:47:15 GMT
RUN GNUPGHOME="$(mktemp -d)" && export GNUPGHOME     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F     && gpg --batch --export 539A3A8C6692E6E3F69B3FE81D85E93F801BB43F > /usr/share/keyrings/rethinkdb.gpg     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb [signed-by=/usr/share/keyrings/rethinkdb.gpg] https://download.rethinkdb.com/repository/debian-bullseye bullseye main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 04 Feb 2023 10:47:16 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.2~0bullseye
# Sat, 04 Feb 2023 10:47:40 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 10:47:41 GMT
VOLUME [/data]
# Sat, 04 Feb 2023 10:47:42 GMT
WORKDIR /data
# Sat, 04 Feb 2023 10:47:43 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 04 Feb 2023 10:47:43 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:7c6fe4d1ef15da79055e0a71952e1a38f799d4f36e9acebdb1ec1512651b39f1`  
		Last Modified: Sat, 04 Feb 2023 04:10:27 GMT  
		Size: 29.6 MB (29629678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e5e72ee4c59c1fc0c1d59c59af193c4439d9df9996ede4495bc6394f0f6af4`  
		Last Modified: Sat, 04 Feb 2023 10:48:09 GMT  
		Size: 6.2 MB (6205602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d836436dbcf9d9f4399b2af6e84652810d276716d7d98eb0845e4fb20f5bca`  
		Last Modified: Sat, 04 Feb 2023 10:48:08 GMT  
		Size: 2.7 KB (2686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1764374150ce8e8f40aa48ec1fafe22c89a1a8e9cc3227dada8f6cc58edbb193`  
		Last Modified: Sat, 04 Feb 2023 10:48:10 GMT  
		Size: 9.6 MB (9572491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8911a3baa2d75738a19fde86281776ceed51fbaee06e87ec0fda3f76928390`  
		Last Modified: Sat, 04 Feb 2023 10:48:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
