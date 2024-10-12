## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:f0d2c548585c0ade0fbc7d35e2fbc09381d72009a332dd8e49999de54b092492
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:4147b590f0c98c72ae50c752bf3382e387cae05b642f93ffb6b644046e3e0fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33412067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b22f2d7809c8879aecc8484a3540c85852ef0023b0d038e86254a5db530057b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a526c1c4c467bfa8fd4dbac14089df74cffeb60f091268f46e8d6e56c3975a6b`  
		Last Modified: Sat, 12 Oct 2024 00:00:31 GMT  
		Size: 3.6 MB (3558356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93739b962388adcbd0dd68b1879e82c02ca36ac4d3c1e05330e62b5d9639f5da`  
		Last Modified: Sat, 12 Oct 2024 00:00:31 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f8bcf22fb48c57ec3cc91300e107c6fce790c42da57f4a2af2905d3b292af0`  
		Last Modified: Sat, 12 Oct 2024 00:00:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2d58d9afb2818a7011ddc547e13767c1b9183ff77b815cb476a6b543797ece`  
		Last Modified: Sat, 12 Oct 2024 00:00:31 GMT  
		Size: 101.3 KB (101261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e56f4043f26ae3475c25818bbaf4043b956464244dcde7545794d07e3210f037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1986519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b730ac11fa743e0f6bb19b4db64dbfca9bb9c293fc0316976e6ad2d307aed39`

```dockerfile
```

-	Layers:
	-	`sha256:5ea1495eb32c9b038ddbd301a3fa1ab443bffc2dbf4b1cec7942d79a03f6da58`  
		Last Modified: Sat, 12 Oct 2024 00:00:31 GMT  
		Size: 2.0 MB (1973076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:783a012f6a6ad08b185879c1eefc5c402f6b1fbccb9849e941997bae473b76ed`  
		Last Modified: Sat, 12 Oct 2024 00:00:31 GMT  
		Size: 13.4 KB (13443 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:185df34b5235dc2751059673c3fa19070ad8b7f71bd74a618ddedcfb84da878a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32546939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f03cf35dc1db17cdd50657f1129a2bd1244eb94bd79c2a9f9df984ff7e64b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b618f3f3cddb65c88794a06b33f6df2350e72e9bc020bcaf987a41fcbeea7557 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian noble main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0741829382faee1dada646b49acf3f4349f0c757e16139b7bb1874c6339d996e`  
		Last Modified: Thu, 10 Oct 2024 08:59:51 GMT  
		Size: 28.9 MB (28885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694da64a024fe13f3d4d9143af767afb8bbe3957540ecd5c81ea6cdf80db8517`  
		Last Modified: Sat, 12 Oct 2024 01:59:38 GMT  
		Size: 3.6 MB (3557461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356d53001c95e5fcaa45a20a18402fd7a18e55a15b6387e83ce6a03bdff6abfb`  
		Last Modified: Sat, 12 Oct 2024 01:59:37 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8092c91500d2264f319ce4fc971712a08fa877cecac92797486bc318142917`  
		Last Modified: Sat, 12 Oct 2024 01:59:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f356fa4bc5c3cda1cbc524270b0663c14081385bb464ebedc301bf8fd213a89`  
		Last Modified: Sat, 12 Oct 2024 01:59:37 GMT  
		Size: 101.9 KB (101869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5f5e03cc7106d893d3cc62a577c54f3d3b745c9a1fc5df2f27017191d5885a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f75db2607171a3324ee066bf234d187891efa090b760bd59c120203ed9aca6c`

```dockerfile
```

-	Layers:
	-	`sha256:c4041a33f81ac63aeadb9f290b82aa7a29c01070b27f7323a5e3cd6201b16b4a`  
		Last Modified: Sat, 12 Oct 2024 01:59:38 GMT  
		Size: 2.0 MB (1974121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9379d7a5dcdb3b766b045a3f3fa02b63b9a6a5a1dee30402bb70569089e0a3a8`  
		Last Modified: Sat, 12 Oct 2024 01:59:37 GMT  
		Size: 13.6 KB (13563 bytes)  
		MIME: application/vnd.in-toto+json
