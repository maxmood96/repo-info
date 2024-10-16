## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:fc1e30bcc7ae287735ede2b07467f68ed7df49b9445f99687fda260140b5fef1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1a9b3ce61717de8bacb0e6a61a6e931a56a8b27f54d1e804ba4703a12f035602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33412517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5dc260fe480ded9861a0b7748f4daffb3ca34afac3d6a63bc11618c31eabff3`
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
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbad116ef7d98ff1bb6e534ed685921f92d98dd482ef4437cad5f993c9668616`  
		Last Modified: Sat, 12 Oct 2024 00:55:07 GMT  
		Size: 3.6 MB (3558388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a63134eaa5ab1fe01757dafe4a01d7e277b1a76ca7d2312217b5905f0c90883`  
		Last Modified: Sat, 12 Oct 2024 00:55:06 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffc7dfceaf20774a734148931b3278f9197ea2511fb9e3fd53572357a21cc09`  
		Last Modified: Sat, 12 Oct 2024 00:55:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d79576fde93702343c2914169e51972d8782ffea423b7321a8f046e4c46f49e`  
		Last Modified: Sat, 12 Oct 2024 00:55:07 GMT  
		Size: 101.3 KB (101276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2f7b5cdf7eb0b8a5b1e03174c3400e9c2089ce1906007e88301b17b1ba9a46`  
		Last Modified: Sat, 12 Oct 2024 00:55:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4b63032cb38eb29e553056377959f1d8218edecaedb16e97f2ca8844a38d0297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc6f52bd27d7f936185a7f78966e6cd3abf8f703d21451858d08cbf7ef16f1e`

```dockerfile
```

-	Layers:
	-	`sha256:d97833cb669a94c41215843faf099f8fc43f857581edef3a18f83e2611e0b524`  
		Last Modified: Sat, 12 Oct 2024 00:55:07 GMT  
		Size: 2.0 MB (1973112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d76f96db1a46659a1946dcc632d3ea7bca51463f22a8e35801a5aec09bbb32eb`  
		Last Modified: Sat, 12 Oct 2024 00:55:06 GMT  
		Size: 15.7 KB (15674 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:22fbd0d6d07a45042210655eb29841152243bf6a9b0647ff180c4e15efa192d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32547544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2846820e80dcd608ecee4f40ddb974b576e02b4e51fcdc26418090c550da1c`
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
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
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
	-	`sha256:7f91b520aaca18d0d1598c30a61a7d75fcaf19f70a644b136a3c8f93d09643a0`  
		Last Modified: Wed, 16 Oct 2024 03:54:09 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:82e80e1c2892a68d88eae2c5913badcac80a27fc4af38a23583c2f4443093b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1989965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1afcb693b18a051ec65e8070c20a38d7d2b3ac864b80d0aacbc8191d4a5ac2`

```dockerfile
```

-	Layers:
	-	`sha256:b07e02d3c73827e6af99190702f368ab085c108d4f2835a8246f8562a803be75`  
		Last Modified: Wed, 16 Oct 2024 03:54:09 GMT  
		Size: 2.0 MB (1974157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c1d36705970b04a363846cc01d3a69ffbedd62aa2338241b5c62df9675fc2b`  
		Last Modified: Wed, 16 Oct 2024 03:54:09 GMT  
		Size: 15.8 KB (15808 bytes)  
		MIME: application/vnd.in-toto+json
