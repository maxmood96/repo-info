## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:0af23b8efe4b5d6a53c257d9f35f692045ed1f7fb51019ff247fac152ae44e8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1a460f508ea63a604eb6e566b9e31bce88b7449210fed79de454bf34c0af6175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33412264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f38e95950ce79563d040ee09442e0ae4c0be4532a0f40042b4037de6d9c6e39`
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
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
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
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bf4fd98272901a80c95a9492d3fa0362b758fd8bfadd9cfeb711c923c0e089`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 3.6 MB (3558315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e523e7036a932e22b290ac9772aafa3b80f0612260428eb5aab15dd9bef114`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4197dd867d3f8b793da103f5dfe1c737c4bfaee73a8672a945090fa574f0acdb`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1628a0bcf70ed588686e77536d73ba54c6d706901aa26543480332b16a3dbc42`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 101.2 KB (101192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5c029479c2a21eed03c7570244830dff6586f5247f7d67b41aaf8362f00b9d`  
		Last Modified: Wed, 16 Oct 2024 16:13:47 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1b1d14591a0c0570c12b6793e6ef272ce176d7687516b271bf7b5320746aba65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1988786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e94dc2dc2a41ca2d0b1476fa8ff9e0587f5d50ea47c45bccdd32b06f4893d56`

```dockerfile
```

-	Layers:
	-	`sha256:4e0276974fe9e75d6545fe8a3fdcd16a04037500b5b70b7b2bad9cdca16598b4`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
		Size: 2.0 MB (1973112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d220a0f4e44151ecbd029dbe933e594a9eaea23bad268002d8014b499549326`  
		Last Modified: Wed, 16 Oct 2024 16:13:46 GMT  
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
