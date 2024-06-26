## `sapmachine:jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:773c7147322fe0aed487aa0fb664ad6029457965b1f1d8bb1d41af2faf7189ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:0d124bec003235e774143d761b6a9170ecbc9717f41d077d7ad7c38b38293998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85181253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f565544c6196293cfc6821f68a99e21c7948b6dbfd2697cecbd0dac1c1c30a4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e8953c312ca4f568f8a24d0c1a258cde168978a216332f9aeaf1077af1293b`  
		Last Modified: Tue, 25 Jun 2024 22:58:40 GMT  
		Size: 57.7 MB (57669484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:30b7e3ad31ed80deb33d3c0eaaa5040fe04771b564d82c4dadabe9f28f9da8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60310d0f453d167167b0e066a6c8b6c01296d1c9c2c712d0ef9e3d4d396361e`

```dockerfile
```

-	Layers:
	-	`sha256:317965c1571f013ce3a53668586251173b23eb50db5c4e3f8d12ab44fd39126c`  
		Last Modified: Tue, 25 Jun 2024 22:58:39 GMT  
		Size: 2.0 MB (2021983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbce22ab94e3d4f2843fc9af4e5e8aabf51f474d343daabbbdd20025a5c4ceac`  
		Last Modified: Tue, 25 Jun 2024 22:58:39 GMT  
		Size: 9.4 KB (9375 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c4da7e7360c7a9338ff1bce0d8f345f933b3318c5a7149e00e91258bb717ccd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82684565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7934aa5921c7546cace8c1d766bdcfa75ac83c695f2bfa0b420232b751428c8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2dd5a1ac6bc87d6a3eca3aabe50adc55ee41d8a430ff0b12a1edd13f4fa870f`  
		Last Modified: Wed, 26 Jun 2024 00:01:52 GMT  
		Size: 56.7 MB (56710348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:752081042b85e65ccd48787c4472a3f152c9612d9699a119b4bcb31bfd429532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f053e72d583d084f755994eb1475af6aa541326d70b870ae20a13f25fcf0f889`

```dockerfile
```

-	Layers:
	-	`sha256:b0c38fae80d1e9370fe62c734177cc145b49cc7cdb47d88d70828321d85664f2`  
		Last Modified: Wed, 26 Jun 2024 00:01:50 GMT  
		Size: 2.0 MB (2021003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c918531539f07fb9871f6575af7b875bf5b39feb3eaa988e059eced1736a31b1`  
		Last Modified: Wed, 26 Jun 2024 00:01:50 GMT  
		Size: 9.7 KB (9700 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b0e4635a6e7e0828730c7af9bedf833920b2380318d908ced5d324a7af91b9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90641904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb392f580363c5ffb022f3c3dd85f5f01fb625e6b49cb07f11fe7824fe6c140`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3567dd8c0eb2baa518cd94d136d3c44a3a72e7334e17d6a19bb04cf06056fb`  
		Last Modified: Wed, 26 Jun 2024 00:25:09 GMT  
		Size: 58.6 MB (58564764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:75d3ed6caa8bf867e16e5ec210a3741c7f93eb796135bf5f8c092123a1fcd929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a548682c5e7f332662605a0cb4b58774f7ff9650eb784c5990c53f68318460`

```dockerfile
```

-	Layers:
	-	`sha256:4f38f3fc69ceb54e9e32b981518d793dbf7af141c5da52d86f45a0a7cd9a3338`  
		Last Modified: Wed, 26 Jun 2024 00:25:08 GMT  
		Size: 2.0 MB (2025066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0467c360195406a20d35cfc47086359a8fb8da379af504efa272885d475cecbc`  
		Last Modified: Wed, 26 Jun 2024 00:25:07 GMT  
		Size: 9.4 KB (9425 bytes)  
		MIME: application/vnd.in-toto+json
