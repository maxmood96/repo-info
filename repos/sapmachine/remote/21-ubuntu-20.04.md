## `sapmachine:21-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:e0108437daa9f6d6224ef3eaf049bb5bf628238b10aed729422b1dc14f4138ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ca4c119e480f311719f763284a5d28fa4a7d810909ee7229419a7546b29dac6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242272057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db7b0008a3237ffb644e54edf31e7542dbe2c938861ad4e3b9490812456d6de`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71471dc2de9f4d33e8a4b92b2fe209972d7f44f5776879c3f3cddb751b90c63a`  
		Last Modified: Fri, 19 Jul 2024 18:00:38 GMT  
		Size: 214.8 MB (214760288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1ec4325d840376a705111a1b6ff020f791b99894a7cc69a3fab46935254179ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0df16f25bc86a7a9c053817464a2d1550e3d3ae5258f8ef2f11d1eefa85280`

```dockerfile
```

-	Layers:
	-	`sha256:081c8a7e05a1f6429d86e48f2408e057fbdf783c17f66d02b3cde347bc706a77`  
		Last Modified: Fri, 19 Jul 2024 18:00:35 GMT  
		Size: 2.4 MB (2367821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47fdc51f0ca908d1a0b77a77069751f9d60f8ad3ce2041367343561912d41ee5`  
		Last Modified: Fri, 19 Jul 2024 18:00:35 GMT  
		Size: 11.2 KB (11191 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:82d964857b984878e7b8b9ac27a9fe9a3db8768deacd0b410aa3460bf64e6d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.8 MB (238812620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720cdb5a6b4e1123664a3aeaef364a5266a934f1ebe1e4f1ddf757c319f241cb`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db9da0a7fccc4bd91d4252ed84565bfaa1cd2c6ee438515f097c2f4b6faa85b`  
		Last Modified: Sat, 20 Jul 2024 00:17:25 GMT  
		Size: 212.8 MB (212838403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3e6abac0564d63fb08f4dc01043b1072b29356a31f86999d85c48206b9d5291b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98a7d8909ea6f438253d96e01ceeb59d48a7636b2235ec06e32d962a2d4f3de`

```dockerfile
```

-	Layers:
	-	`sha256:5ede74942b7254746f43a0886eb9535468e1e74f3b19d911f582eab7fc176679`  
		Last Modified: Sat, 20 Jul 2024 00:17:20 GMT  
		Size: 2.4 MB (2367553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbfa9c4f1bc6fe15224b894e1640b7ec1ee1ac84fb8e26f6100775e185ecd4ff`  
		Last Modified: Sat, 20 Jul 2024 00:17:20 GMT  
		Size: 11.6 KB (11588 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fe6bbada68da6c8161f90fa24601bd922814f45ce3d6716ad719ef95ba94c017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247780190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8095eea874a866c625cc7449c958aae6db29a6c886ca5354f7ed3aecd8239820`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74050146167b59c56dd5024b1b37926f7efe1360b7df682425deb67fc518facc`  
		Last Modified: Fri, 19 Jul 2024 23:24:48 GMT  
		Size: 215.7 MB (215703050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d6b3da19baa54ff66a971847cea9ee6846dfd674230f4e7bee71b9c009b3079e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9b95a60b1cf340d285adb35b8b1ca32285bbf4d8b5ec040eac6237cba940dc`

```dockerfile
```

-	Layers:
	-	`sha256:09761c8d952b8fcd890c3ef46a6ce5733333ac87b1a761c3c0393886da60716a`  
		Last Modified: Fri, 19 Jul 2024 23:24:43 GMT  
		Size: 2.4 MB (2369685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:849e1543d8e9da8435bd08896886a4d1bccfba4a8dea26909fa437c648fb6c83`  
		Last Modified: Fri, 19 Jul 2024 23:24:42 GMT  
		Size: 11.3 KB (11277 bytes)  
		MIME: application/vnd.in-toto+json
