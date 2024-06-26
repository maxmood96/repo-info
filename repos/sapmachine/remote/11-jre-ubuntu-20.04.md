## `sapmachine:11-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:3792ffd95f93d237d90c131f5dd5e0714c27c8425b8c0e3c89cea4ff19818340
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:b93bcf9e80383beccf585ed8e9dc5aff16ef3a017063078740692e9d488eebae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (76997855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765310c806b5dacfdf7c11f51c9ba81cea66b69bd34983e9a1b238a3509ae89b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a4cdb0c3088ef4d381030e56d36209b3544d1e297d5ef771b057118272239e`  
		Last Modified: Tue, 25 Jun 2024 22:59:01 GMT  
		Size: 49.5 MB (49486086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c7441c8ae5209be66311af7ffc7ac2abb519ccbc55ed4c3008925ab2c3e09a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2274972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9093813562536b7d528358d64a2cdcbaff48342a2fe45ab5fcabc32e3c1bb629`

```dockerfile
```

-	Layers:
	-	`sha256:e64d122c4e1fc04fad5dc4876e869e3725dbf36621fd528ac4d89a085101502e`  
		Last Modified: Tue, 25 Jun 2024 22:59:01 GMT  
		Size: 2.3 MB (2266387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf0802a471c3b75abf2eac6e9be300e60eca4f6ae854e23108ee22e705c37e92`  
		Last Modified: Tue, 25 Jun 2024 22:59:00 GMT  
		Size: 8.6 KB (8585 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:dcdf6dc9552cf6f19555824bedae46f388159ed257a2aa47f6b75453adcd5544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74770064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5128e067ae3d3c903e9e79678182aae62f8ab0aaebfcabdbe8aae36932b1a117`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ceefc2e6682a61b34f6dc26d558d6f57906cda33e825f08e0decfc5e182b0d`  
		Last Modified: Wed, 26 Jun 2024 00:37:51 GMT  
		Size: 48.8 MB (48795847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:734c1ed679b8f892debbd35df24da0fe10e83c96ba6579ed987885e6e98034ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2275537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb9ece6ebbfd7e9e01b2ebe176ed68c9c4546e9f44cd5e1e4ad3bb8ab8e6d44`

```dockerfile
```

-	Layers:
	-	`sha256:7ef7e5f31bb4abf859307113a33713432fce30346e7d53ca99bfbad7a9bac7ab`  
		Last Modified: Wed, 26 Jun 2024 00:37:49 GMT  
		Size: 2.3 MB (2266651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b649da0b3dbd44c91e1e4497a5ecebe0ebc85cc252bc3c0dbaf44a8556461d01`  
		Last Modified: Wed, 26 Jun 2024 00:37:49 GMT  
		Size: 8.9 KB (8886 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b578129784751d71692da996034eaf8160906a21dd7d22e820d79592a66b2918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79803136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d43dfa40abe116f739cdef64e02b256a80149d377fdc6a91a31c973b1366cf`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ce05921cc8ae97ec38d1365e4bd429ec77db438ca00a8ff7a08d2a08a5504f`  
		Last Modified: Wed, 26 Jun 2024 01:24:13 GMT  
		Size: 47.7 MB (47725996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fa7a88c90e6f602ac47d817bf5227e348fee9174012de1359ffc8b354dc3e1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2278781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbce8e8eea035a6c90ec9d00fd981a1ee70afc8ac7fc4960db1ebe08c3fbc018`

```dockerfile
```

-	Layers:
	-	`sha256:ff7900ae58fe8106000b3783233284c05633af097aadf1f35dd804123613d183`  
		Last Modified: Wed, 26 Jun 2024 01:24:12 GMT  
		Size: 2.3 MB (2270158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5236c221dadbf7c9fcc8919c95d411f77ab12dd64e808c3ec0a4f51ebe21460d`  
		Last Modified: Wed, 26 Jun 2024 01:24:11 GMT  
		Size: 8.6 KB (8623 bytes)  
		MIME: application/vnd.in-toto+json
