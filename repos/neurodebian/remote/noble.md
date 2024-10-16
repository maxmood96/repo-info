## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:4867617d7c4a621227aa6915cf5703a0d75df7b888f203f50dfdd9d8822e162c
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
$ docker pull neurodebian@sha256:1a935b6c4bc11684f09930d0b9391f0db414645a05ca2795760d5194620e291e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32547139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee26915a3722f1f7401b6f1ce035233a1a654c8bb05c81b62417d418099d3b5`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
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
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea789099bd6ebe3942b142207baca153ba915bdc75730edccd488aed6d041b`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 3.6 MB (3557475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4a09b01ed47f9b471c2c8ae48b7053ab1d51c00307579e122f2e75623a215e`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942a820a9345a6a033d2fd85db18607d4fd8370d06efc055972c5e44aecac5d9`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eeed11615938af4f334098e62ba967cd10313041ccf1762ab55e8c506f8a93f`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 101.8 KB (101826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:01a91a3b061811a551707c6df5c26cae458b00315f8ca31651bc11a321d48fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1987684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73776da87cd8801b4dc0c2ccf5dd9f2ad91d46bf0bd60c1a5a15e27e86a265fa`

```dockerfile
```

-	Layers:
	-	`sha256:49317efb7958f179c63ef030afe475a8d88eb05a4f179d243b89a30a0ceeb447`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 2.0 MB (1974121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7871391a76e34455997ee18c3efa74d7a4da063e5b0f6d1be022c8ba189c6f4`  
		Last Modified: Wed, 16 Oct 2024 03:53:43 GMT  
		Size: 13.6 KB (13563 bytes)  
		MIME: application/vnd.in-toto+json
