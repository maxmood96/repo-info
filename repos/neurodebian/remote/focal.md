## `neurodebian:focal`

```console
$ docker pull neurodebian@sha256:8bcdb02c955c552289fb14468e3d0eccac712d0a170f1fff5601f3f3af9d8a49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:focal` - linux; amd64

```console
$ docker pull neurodebian@sha256:a0c6cb45ac1cfbe06c47f14d684929ff5f5907ef7f083c360195214c3ac6aca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.0 MB (32978658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1335fc867ea7b822d1b6882dc96ad365e5cc4643152d61c5fc8a7bc5f85a988`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49fa7316f784f5cf307546c8c97bd1b9f3a1fd2943c27fceb71ec2dd6409f48`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 5.4 MB (5360278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb7c65bbf482527df64ccec5d79c08cb11cf2d1f4054f4977e47dad48ff8435`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e678bedd7e50e1ba3e947302d4a3badb36d988b369aab4b47c1fa78259c23552`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9792897da4dcee6732822377f46272804fb1e9b7f31dd60d17894a127edb839`  
		Last Modified: Wed, 16 Oct 2024 16:13:43 GMT  
		Size: 105.3 KB (105327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:848d25161f517586e1457fc807e778d3305bad2daae744ec21fc37849f68173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820220dbbd11c6d8f3103b1a3ed83da871c77d7b02f18798badcf3237303dcae`

```dockerfile
```

-	Layers:
	-	`sha256:27970857ec501c025d084e20e5352a5d5ddc17824cc89a85f49e7025cdcb4a02`  
		Last Modified: Wed, 16 Oct 2024 16:13:42 GMT  
		Size: 2.0 MB (2002651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:849d52e89f42eba3812416ede3dd4d1badb9a69a5a982f874e39c325041eb9a2`  
		Size: 13.4 KB (13444 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:focal` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1a3f2e41cb72abdd7dcab281d6513ce2dc547865fa3b4ba0776bd58ea8a5de97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.4 MB (31421807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2c98411bfbdccf11946d245a8061c56c6ce058ada6075d911256dd80fadff8`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6101036d9458690903008f9743d7d9982835f206b38bec0aee1147faccc7c0`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 5.3 MB (5340575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159a29390bcc04ab62cd8664a0c5eb9c2c8529bc1cf5a8fc1e442f9740f53d73`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a06a5898141ddee96056f1057c0595e290735b4831567d9e98c36af5687cba6`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ead23b60010d07ced4212e4cf8a6c4f69eae17b7d32e4a35b7bf00c6df7eacd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 105.4 KB (105412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:focal` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1f3f34f75e1a4bc32b849a9ffc880a30708443a7fdc0da8a50c2e90180094f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2016442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5772b0ce1260ce48effc24ad2f6bdefdb4674ee0d585774b4464dfdaa8df07f`

```dockerfile
```

-	Layers:
	-	`sha256:71ee94546588c20b92a492d129395aac336c0ae8677f9f8048b6890a1e640901`  
		Size: 2.0 MB (2002879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa10decb4cbaa5f56d95540086539ce9a7bfee79f97ecf26a18eb6160c482bbd`  
		Last Modified: Wed, 16 Oct 2024 03:52:53 GMT  
		Size: 13.6 KB (13563 bytes)  
		MIME: application/vnd.in-toto+json
