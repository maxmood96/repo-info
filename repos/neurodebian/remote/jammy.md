## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:623b758391fb029c0195fce359139e6ee027655959e76d09fb4ca2e26ffb941f
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
$ docker pull neurodebian@sha256:182965a2a88e752d9531ab95095ea3f137ec86496b97f9e82a9df5c92f2338bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31070904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0020b4b6b75f3fda2b2fd11190ea6b59ae189b71d7fcd254bb3e3df2d195a0`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fee3ef976957c41d04767884cb43799b96170dc7f90b007a26b81ae7b51c1b`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 3.6 MB (3595512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad45b1472436df983642ff6f6d821159f3cd9284d480a5e549b8c52f96c74c6`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154dd0239ee03ec9e4d04dc3e50288d571e148ebe8a49b6b24e5b4dc41e65926`  
		Last Modified: Wed, 05 Jun 2024 16:36:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e65cd6fdcff0083c9d0e5d5a4702ce5a2ae4964d6c7640ff281a2687c2a4f4`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 111.6 KB (111617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3daf4feaf8b1af264759adfc71c17d64177646bcff852e4c561c28ee3ab4296b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2029551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a01233855c07d4d99141d81865bfe4168def1876fa3a1ef37be11dbdf4b2281`

```dockerfile
```

-	Layers:
	-	`sha256:b5128b7a8311295bf17b1da5ff28149668958c562a0f3982ea7b363c9a9ee90e`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 2.0 MB (2015917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09216cc84b65a36876b54e5c68b7ad1aafcc4a002ac17e4e904429aae09512e6`  
		Last Modified: Wed, 05 Jun 2024 16:36:59 GMT  
		Size: 13.6 KB (13634 bytes)  
		MIME: application/vnd.in-toto+json
