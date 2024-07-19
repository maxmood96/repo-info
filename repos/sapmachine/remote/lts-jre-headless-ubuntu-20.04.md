## `sapmachine:lts-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:e221b7cef9bf0d83c3b211c4e079a9aeab06d264039a1472b0bb1a67550b5004
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:bab4e454b9482cbcffca9ac0caeb90d2b1524c98a38de010a629e08598d390de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85798175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfd453222a7b17e82c613a6f287f4de1c38596a403a6e91156baf0911f838a4`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:01982e13f8151edcd691c0146b3429792f57bab64b871e2bf790f656bcdcb547`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 58.3 MB (58286406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e12818e0bdaed520806adbb5d1ff905d56c4695bdb2543e2b067b3147d87c864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcfc1dd10d8206c5677b49a1e2426b70b5dd7d31249002f148ae2979e2bc863`

```dockerfile
```

-	Layers:
	-	`sha256:27bac716555b372bd4a20acf36ee6d8109b536191b77b673b3b98447bd7c9e10`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 2.0 MB (2044953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08150a2c58ca722bbad3fb5dbbe478e9f24472b706c5cedbce37b1c881c56372`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:38201a7d57235d3797d0609a5c402ee8b418c0027030f0cc7a8b02abcfd7c386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83286842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84fffd83ad01d5430d5ba03cf7599df9a95655534ae96cdfaaeb62ff00ed078`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f52226b5ce1b5b42da52669d71fe1e92445f217076563bc31e42e36a809194`  
		Last Modified: Wed, 26 Jun 2024 00:13:52 GMT  
		Size: 57.3 MB (57312625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:71a2596d9d6eb0cf76da7f5b2bf1a9d35797ec7e3a4fbf3ebdc36cfe95a8c9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f827c0342548a4e3ca50e3653e436f641ee9fb8aa69df1ad2ea4e52dbd8797c`

```dockerfile
```

-	Layers:
	-	`sha256:7b981505530d5657f251610b42cfce9b2f969a55e194176a8fece0769a32828e`  
		Last Modified: Wed, 26 Jun 2024 00:13:50 GMT  
		Size: 2.0 MB (2021019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd511515b679d61b158dd784278ce939e8dd436f44e5946dcc43a4e64b04ed85`  
		Last Modified: Wed, 26 Jun 2024 00:13:50 GMT  
		Size: 9.7 KB (9716 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:db1478f177580b1ccdde9fee938d2b592ca271cc92614bfdb041a1a598ab26a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91316548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218080600033b254d799f4440d8614127a5aed90f62fecae2b61ae75173fde0f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc60add6ce4237c41e57e3846008bcebb9fb10ad600449fc499e526e112f1be`  
		Last Modified: Wed, 26 Jun 2024 00:45:39 GMT  
		Size: 59.2 MB (59239408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b23ddca9a8a4cb7407b74286a3b6e52690ba33e97f8fde5797637d7a81e95bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2034523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84edeeecf20a930f7957533bc5ac9e234e4cd2412f9c3ee8337a3b3dd841969`

```dockerfile
```

-	Layers:
	-	`sha256:be7e5e39703d40ee4dbc860d14ea072fa5f82c34e674be0be2239bcab6b88226`  
		Last Modified: Wed, 26 Jun 2024 00:45:37 GMT  
		Size: 2.0 MB (2025082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a511755b8af28c66c25d7984d5b1c5baf789940b12849f70c074844e12b16d`  
		Last Modified: Wed, 26 Jun 2024 00:45:37 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json
