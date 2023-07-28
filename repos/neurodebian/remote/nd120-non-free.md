## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:b30bda47e6eb1ff8c88035abfd72918561ea3376e301b0f83f956fa4a92b48d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:858cd4251e5ccd3fbb654f024e79fe6d3786b31324d61bb2832d6eb00071df8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61302839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797808e1fb4f66aa79fb78e8df33ba10bd6cf5312edeefb5670e3937854d6ecf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:19:44 GMT
ADD file:5d17ca085473e890bd6eca4abf6d324c3181f80692523b83ef25d1c42576b99f in / 
# Tue, 04 Jul 2023 01:19:44 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 13:12:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 13:12:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 13:12:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 13:12:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:d52e4f012db158bb7c0fe215b98af1facaddcbaee530efd69b1bae07d597b711`  
		Last Modified: Tue, 04 Jul 2023 01:24:39 GMT  
		Size: 49.6 MB (49551432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0363adf9305a6b41761d438d2a99d852e8ff75744469ba09ffb36630191c6a2`  
		Last Modified: Tue, 04 Jul 2023 13:14:54 GMT  
		Size: 11.5 MB (11462689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9217394c3a8c00efd3ed3df63117ff1d5235d1493d0d9927ece4457ad9643c1`  
		Last Modified: Tue, 04 Jul 2023 13:14:54 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697199bf9c91bfcc1d3bc1cfcd2bcd5a643b7976d86981f5a8e6c72a1cb97dd0`  
		Last Modified: Tue, 04 Jul 2023 13:14:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f82f7b82921a5b3474b30a4c42596d5eb0025120b94f4c4c9f9019497651ac7`  
		Last Modified: Tue, 04 Jul 2023 13:14:53 GMT  
		Size: 286.3 KB (286275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a06c5cf996db9fe8ee9a4f77e2915465281718a38555d47d2a777d5c47be3c`  
		Last Modified: Tue, 04 Jul 2023 13:15:02 GMT  
		Size: 428.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4d5edae74ae1b942b9502023f23837e250589e2d6207ea008ffcccacd2a3bddb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61288346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a893555b6a968518c5160f8448e510094af5263207b10262bad8add5ec68801`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:26 GMT
ADD file:ab1761d899751c4d24e15179fc9e7e7ac3fb83798ee37ca13d6a6ac44fbeded3 in / 
# Tue, 04 Jul 2023 01:57:27 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 04 Jul 2023 04:04:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 04 Jul 2023 04:04:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 04:04:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:42cbebf8bc116ba1aed7897e2d0566bf49da9d5c70be71b6a7cb07805d2f5b7a`  
		Last Modified: Tue, 04 Jul 2023 02:00:57 GMT  
		Size: 49.6 MB (49572781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:861df767d9558c0b849a1f9d8e7152ef4412cc9cd8d7779f02887e1482df404d`  
		Last Modified: Tue, 04 Jul 2023 04:06:36 GMT  
		Size: 11.4 MB (11426584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cf1db022c44ac364b74d3dc15420bbfd4234ce595f93aa6e88357d7764831c`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fb2908699cc879f5983cad2800da4109b3863df1907fbcc836091a72b1c54b`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb64c88df5b726c53838a6567c16434972a07a424384ad17628e12ae7e3966db`  
		Last Modified: Tue, 04 Jul 2023 04:06:35 GMT  
		Size: 286.5 KB (286542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4daedea9b78dacce29febd8344cde1d29ea62c63bcf4282f8ca56f870c9892af`  
		Last Modified: Tue, 04 Jul 2023 04:06:44 GMT  
		Size: 427.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e93626359a36a48bcc52dafc8f06c0314f34e2363d5222491aca6992aec03a08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62740074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfc1e630f7cf429a188bd3ae4877ca5fe4084dec8cbdfb63969279c8e6a03e5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 27 Jul 2023 23:38:44 GMT
ADD file:bfd1a38bf0df9f79f82223093a7cc153dd7b622ab08d82845c29e6c6a2b63344 in / 
# Thu, 27 Jul 2023 23:38:46 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 00:26:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 28 Jul 2023 00:26:48 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 28 Jul 2023 00:26:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 28 Jul 2023 00:26:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:7edd5f0eb761ecec3cc6497cb7ea8914684087583488efe885ab62bb56ddb33b`  
		Last Modified: Thu, 27 Jul 2023 23:42:57 GMT  
		Size: 50.6 MB (50567875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d955a37bc16f78384964e9fe3eaea19c7ce73126226143d91ad06904f88f6c`  
		Last Modified: Fri, 28 Jul 2023 00:28:21 GMT  
		Size: 11.9 MB (11883326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bffc2e83e61fafba4c775d5e49f245f6c41fec6fb974344eba3e8413a9efe79`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28982312586fa3fb6b226464fdb7d7012bd3b791fd5861afdf90710edd6eadce`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77d2ebb426ec21ab46e2606841ee798e7cb0ac271b2c9496e806d0796628983`  
		Last Modified: Fri, 28 Jul 2023 00:28:19 GMT  
		Size: 286.4 KB (286430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7712c30fa50f50f5023f34c834fc38657c999b4b7016a15b5456d677e8b50d3d`  
		Last Modified: Fri, 28 Jul 2023 00:28:29 GMT  
		Size: 431.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
