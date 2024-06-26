## `sapmachine:lts-jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:8bae5d42aa6262307319f3959f2bfcdb2d7a57617ace546f659a7e2072b46fcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:2d64f83ee01b2068f232cbdb779e7f1fe141eb0262729f373ddbbbdcdf13794e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85738669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb83641241d53c10e252b795bad2530d8fdc87fc9f3d39ba0371d4e5c2f342b0`
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
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
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
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513ebd2edfca466c6ecc754f6410a1da1c9bb4dc461b40430e48b68a4339107`  
		Last Modified: Tue, 25 Jun 2024 22:58:43 GMT  
		Size: 58.2 MB (58226900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c292ceb0a966f5bb221e02ae0aefd8bc45f4b6eea35851aed09c96eb742d5be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2030759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1353d0883680705de8552fa7b36eaa5cde5f45cecfbaf546224561ea88613f07`

```dockerfile
```

-	Layers:
	-	`sha256:ece26eaa6443b0e5764b5cad7200a934466f6e8084d16755fa35fd55e61c6f10`  
		Last Modified: Tue, 25 Jun 2024 22:58:42 GMT  
		Size: 2.0 MB (2021368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fb82457f5c04ea9274a790f1e797aed0c9d883aef91d57b6747ea45197c5866`  
		Last Modified: Tue, 25 Jun 2024 22:58:42 GMT  
		Size: 9.4 KB (9391 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-focal` - linux; arm64 variant v8

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

### `sapmachine:lts-jre-headless-ubuntu-focal` - unknown; unknown

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

### `sapmachine:lts-jre-headless-ubuntu-focal` - linux; ppc64le

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

### `sapmachine:lts-jre-headless-ubuntu-focal` - unknown; unknown

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
