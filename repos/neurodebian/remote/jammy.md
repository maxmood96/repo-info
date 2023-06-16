## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:3da659d7cc1c128f239752dbbb86d7a70bb4ad47c48183bcf54217c8637203d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:e9dafc54b81b9daca6a95c2d1c234c87598eaf580216ce38a50ae1850256c16c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34458022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d090035c2ab40d409c8f5db628ce293e1c548e3c827663ddea3b3fd60664c6b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 04:31:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 04:31:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 16 Jun 2023 04:31:04 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 16 Jun 2023 04:31:08 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce54c1f1cbf813d137b4f4335a8b99a07df9e8a7dce08e9dd3d392502f71e035`  
		Last Modified: Fri, 16 Jun 2023 04:32:06 GMT  
		Size: 3.8 MB (3766232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366bbf7f5d2197a3a2550fdfdc62b1d0d794aa5138665e6e54af719f7888091e`  
		Last Modified: Fri, 16 Jun 2023 04:32:05 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091c8554754f3bfb437a9ac3566bbeb3a357fb0ebcae588d17ab356f888b0b31`  
		Last Modified: Fri, 16 Jun 2023 04:32:05 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44fa22ce8b8947493b343aa32084dce28611c1dfbbf34704946be5eeea7f8b76`  
		Last Modified: Fri, 16 Jun 2023 04:32:06 GMT  
		Size: 258.7 KB (258736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:929099403068ad95102f10d1a660f7d1b89cf8f5a156da33e54386a4ce5ecfa9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32389342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae891992461a99a77a00224c50286d9dc6ee0a047f2bb1ca3feca14f6f51b43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 03:17:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 03:17:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 16 Jun 2023 03:17:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 16 Jun 2023 03:17:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9882dda766bbc231b2a2d50c4e9f0f5911920be5bd86587bd5462af9829f2b5`  
		Last Modified: Fri, 16 Jun 2023 03:18:25 GMT  
		Size: 3.7 MB (3738918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e14d679161653dba305ec4af040bd5840d5ca3b504e3900ed5a4a5920c04c4`  
		Last Modified: Fri, 16 Jun 2023 03:18:24 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:482f0cdd7916affa0fd2bd9ba10c480372a63b92f6513c54e94e168653d7de3f`  
		Last Modified: Fri, 16 Jun 2023 03:18:24 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c728e1716d7d6a874fc65e8230d5bfe7849f37d72d6eff88ac6a00f2cfa6558b`  
		Last Modified: Fri, 16 Jun 2023 03:18:24 GMT  
		Size: 259.2 KB (259208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
