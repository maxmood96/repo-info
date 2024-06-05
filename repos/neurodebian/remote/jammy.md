## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:d145f6e010ec66e7c8d6acb944dabb11fd2972aa1ae20b527fdbebc61d90558c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:62b21ea23ab0099bb7bb3c5dff41f062348f26f984ce63d7adbdce9523debbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33268509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d480dfd32cd52adab70bf29d18e316284e516732cd7b64ca8fa74057e78b2bf9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13680b52a20c7f7235a12148a3b749ac0b8059a27ccf65a67280b22ab004496`  
		Last Modified: Wed, 05 Jun 2024 02:20:23 GMT  
		Size: 3.6 MB (3622659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc9c4675fb06f3f04ba34fc069e9b8352212d06376d2db5919df67d4861e337`  
		Last Modified: Wed, 05 Jun 2024 02:20:22 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15fe517f5124a0cd3234b7e232a0eb9bf389b9b8927d1108f376ba18f4a602f3`  
		Last Modified: Wed, 05 Jun 2024 02:20:22 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5c2f84665972fd9fb9573b2bc00b57c4d6633e031d81eca30d1f1a26e9c4a2`  
		Last Modified: Wed, 05 Jun 2024 02:20:23 GMT  
		Size: 110.1 KB (110101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b4eed60b439ab7b3dd6a8b8b389e08f83980039978671105075d770d2e36f4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94a87947aadbdb67abbf4192622756c526f7bcd4b104de43c0ae0302f13f532`

```dockerfile
```

-	Layers:
	-	`sha256:47a512237c86f29a05d8cd78319ca62f3d23f9959e965f73984dc89c544cfc9c`  
		Last Modified: Wed, 05 Jun 2024 02:20:23 GMT  
		Size: 2.0 MB (2015658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40b7dcb1333f9cb8c4f4713875a80365a39445f7452398c4a29dcfca3d6e82bd`  
		Last Modified: Wed, 05 Jun 2024 02:20:22 GMT  
		Size: 13.4 KB (13357 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5f543b59036464a59946ab9f73c998f71ecc609ab2c5ca2dc834af647bf8638a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31067211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f362e6117a66f67a5b0cde15ce0b8b078691e3ec78709d4ce540e2b08457060`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba218d1d7b661878c14487bced886a52a613db7b35be93fd5606033d2ee7cdb`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 3.6 MB (3594346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cbb193b892b230325e0954e37f9cc5888e4f5be69eac2c00586f369fa71eed`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b9f9da838e49a37d396367d4f8b41a6efa775664ae714448be35174fb50dc1`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f64b85fb3b544ce5bca4e7f032da3c58413de4c1e771a6265988ed8513dac92`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 110.3 KB (110337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9131086119189da2119fc9d99e995c97fdf410d3ca601e23e491fe8e5d6c0737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c9ec91fe7e2d937b57cbf4d8b162a8c1a426b035b5c35b1fb4e27b983f9f278`

```dockerfile
```

-	Layers:
	-	`sha256:b09c69bb51cc9910fe5d3c1336f479b01906e19f21020f8966c5895bcf361bab`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 2.0 MB (2015917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc63a7363629720e2d76cee0af880ee53688d49b19199609270d58688489f6b9`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 13.6 KB (13634 bytes)  
		MIME: application/vnd.in-toto+json
