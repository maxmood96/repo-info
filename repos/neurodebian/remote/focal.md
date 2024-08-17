## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:8df4e760190f3184795b360080280ad5a9275765869d679e984ad3a1c798e6f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:835645ff640e0142a0d70b8be3ba4638a382ac72c67226aec4e8588ce4ec7c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32979042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390b61ad47378182770a2a820747040d768ff99bf0939b198a7bcbf4f0bf8a7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5889d68f1c611652a413d65837ee20352e00c59841d2e5610ea3b191b17edd7`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 5.4 MB (5360097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25867322675a948e12a50cceab4e3300713f994744099d783b76f2bcdd39e433`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4220848f077408718e98ccc6eb67e4ff521ec7a6b8ac1a5c1a5e7ca67120067`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6c8a677ce3bff8a9a3b154e868b1784552773f214318e5e082d655f2fbd1ac`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 105.2 KB (105183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:09d06e052405a63123040c809e203e9d109b16a84e402292d52bdc7b0a9cdef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d2f3d10af80443a7fa61073ec0bbca0f9204569ca94bf6755608efda7a9a5`

```dockerfile
```

-	Layers:
	-	`sha256:8390bd5dd97a5116688396231b0a1182a18e98fd8ca998f6d264b4887a7fd5a8`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 2.0 MB (2002638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8b174df4e6b1276ca0d9b68a50bf1f8929847cedeece4ea19afc63fcdfe78c`  
		Last Modified: Sat, 17 Aug 2024 02:01:31 GMT  
		Size: 13.4 KB (13406 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c4f9d85053aa89e9a36ce96d6f32bcb36ebf1d565cf38f7e4350dfbc540bfaeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b09eae5c93db890c880b065697968d7411fd7169e3f75e153dcd61251ed72bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian focal main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel focal main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0639d72092b592b944940eaba5264bbabebedc923c867d5cef204e3869370ef7`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 5.3 MB (5340388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140e7d1c2d83050467ab223500a26d141bdd407ae0e6e93886431805ca3d5c22`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f6e4e6a296c9284d095ca5915669b150327bff81a93c81da40429350457fa4`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb6afbc297c547eebfdff6b788637e32acc191d56ab28e1b571477510a8ca5b`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 105.2 KB (105231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f55c5bdee82b1c011271c0c624cd82b39488db7acde45dacbf7146869d0eea3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb2f2b3d0e9dcfe27d3b5ae0242c59d59b5c410d29417b2bf2602ee21d9fa8f`

```dockerfile
```

-	Layers:
	-	`sha256:9c7deba42a44262b8779a5b289447570c109ba28094ec8dd6ee5b71e08203334`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 2.0 MB (2002866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4db5f9492ef8ce64fd0b1771dd024422ff8201a3607ccd5adacb6fc086eac4`  
		Last Modified: Sat, 17 Aug 2024 03:26:33 GMT  
		Size: 13.7 KB (13683 bytes)  
		MIME: application/vnd.in-toto+json
