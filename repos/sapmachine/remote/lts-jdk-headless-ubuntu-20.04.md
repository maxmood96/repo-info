## `sapmachine:lts-jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:03a6658e225da51e5056074bc6260545a07bb0f5038f52e9acecda597c4591e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:db160d8707e84c697d2f4474aabd201a79946b948835243fdca83512f1b8bb1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241067979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6b423e455d3fc96855cb4944b1b95052904d3affec92a365b8c170fc527ce4`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1885b5a4ae19c87fc20cec46ed50a06f994749ae89a359fc2b26eee2d804b572`  
		Last Modified: Fri, 19 Jul 2024 18:00:45 GMT  
		Size: 213.6 MB (213556210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:47b8153b0f6da1c03e9979fd0dc680690c684546ebd77144c00c0456f800dac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fcb162e410f2320b59184e366c23713aee3c3911e43bd16d0761add4b70478`

```dockerfile
```

-	Layers:
	-	`sha256:f05610327388ab75a82b120b25adbf4a9fb618f1e89df80967864761909437e6`  
		Last Modified: Fri, 19 Jul 2024 18:00:40 GMT  
		Size: 2.1 MB (2128606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29775c26040a08e36483af60db565d97d10124dc88e94261f074111b1fd01586`  
		Last Modified: Fri, 19 Jul 2024 18:00:40 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2081e2d042133b0d8b1b0871cd18fe0980bbec361eb4a6207af6cebd159b77c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237480198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3afa430be8637bb20a6134bf6aac40a4f00064c38d40c4a0f7549fe0d83d7eb`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:9d02ff887ddc000b6021455fb24bf243ef6b5cd1f91ecb2a726f0359d42ce59d`  
		Last Modified: Wed, 26 Jun 2024 00:12:11 GMT  
		Size: 211.5 MB (211505981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9075ebf4cb501dadba83c9efd14dc8d6e5c30b8b3d79711b836851b19977acd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2113755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e550e8611b0de7ff32cd9e8c26bd0f22da6f9d44c9bf1814e672bb7e5c2b18`

```dockerfile
```

-	Layers:
	-	`sha256:48fae98ff704c0e2909169531911650af31d6b5f09183392910c049642d7c540`  
		Last Modified: Wed, 26 Jun 2024 00:12:05 GMT  
		Size: 2.1 MB (2104038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33815c91dbdcb6a855ceea65d30f1ad2543cc96fb4729396ab00e3cb5627130e`  
		Last Modified: Wed, 26 Jun 2024 00:12:05 GMT  
		Size: 9.7 KB (9717 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:730abde239f9da470a9cb4fcc69280c27b3bb924eb1c54688c6923543fde966a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246277948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1180af7f3b8df2ef2294014d0c204942b5a4a173da0bc24d91a2a6778d420c9d`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:9386ee38920a9f230030f45fa271381749643e72419d03c6cc6d86ef7d4c7a8f`  
		Last Modified: Wed, 26 Jun 2024 00:42:30 GMT  
		Size: 214.2 MB (214200808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c88b47cc1286bd23847cf71f0f9bcfe43f9a474520506e7655dc2a722a4ffa67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2115593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bee03dfa33128ace1e0486a3c1bc693e30ca35eac1a4fcbb9849ec5afa0052`

```dockerfile
```

-	Layers:
	-	`sha256:167e2b8ef64be7717e1d38eabb4ee5a0a5a532bf31f57d1126c7adbad62d5e37`  
		Last Modified: Wed, 26 Jun 2024 00:42:24 GMT  
		Size: 2.1 MB (2106152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b74ccef286528803df39189cfde0f29eb216c322ab9fb24f9839907a73f4a0b2`  
		Last Modified: Wed, 26 Jun 2024 00:42:23 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json
