## `sapmachine:jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:ccb729dd6bfd9d123f4b46184800a97918c650e7217218ae60c98b25aa8312fd
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
$ docker pull sapmachine@sha256:a8234ee576e18172236a8f0d334ae39e2c0781b38f13cfc70e2785a0f77ffd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85228669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd092f68e9ec561b2a6e8a0039e2cb05783d9f255159de055cec58fd431a601`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf0ce764e3a1cc5fd3f7167b32bb9ed6e8bfa21f617661e6881851dc8fce072`  
		Last Modified: Fri, 20 Sep 2024 16:57:46 GMT  
		Size: 57.7 MB (57716900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:585d5e5961d7d3ce3e4848364fbce85eb965fe85833e9633b3c8dfe4ead39285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 KB (11064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8198ae5fe99d4705ea3d1fd14c0d69a1de6e753d8e1a343696a6ae652be94205`

```dockerfile
```

-	Layers:
	-	`sha256:8c27f5c57cb9f7ac356b56ba89021e373c2fcb4ae131056731ceafa47077c36b`  
		Last Modified: Fri, 20 Sep 2024 16:57:46 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37418435a97a3bfc705a8dd971cb7641b143d0c5ef45c515affa56943d03fe5`  
		Last Modified: Fri, 20 Sep 2024 16:57:46 GMT  
		Size: 8.6 KB (8633 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f3ee5bff7367f78421513d6fc0a9b272a2dfa9b65b1d1e47ee4738318dfabe17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82730973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074a01e2c49b5f94e925016e9fc3a16ce94d6de468f98964156374d9ce82a756`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843bcb43a86484857a00a31ffad5218ec2888d2b6bb87f4fa2ebd09208f30a27`  
		Last Modified: Fri, 20 Sep 2024 17:14:40 GMT  
		Size: 56.8 MB (56756756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:23b21568ffb9231aac5adf3501eb9bd21170334112adddb7fd615b37612c415c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2053414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e101a370685baa49ef74ff8f9be607167ddf396d4a1eadc3a4b0965f913e8f8d`

```dockerfile
```

-	Layers:
	-	`sha256:da86d2fe5d8b6d5d551a781b744bd48543fcfd819e380fbfd4eaf8b090c59cda`  
		Last Modified: Fri, 20 Sep 2024 17:14:39 GMT  
		Size: 2.0 MB (2044481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a0f8e941137caa374b4c0c72baca097588028d62c38dd394f463addd7d18650`  
		Last Modified: Fri, 20 Sep 2024 17:14:38 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d1ee7464d55af470b82ce286e2f3d54eb094221aeb13680354a66b2ca6554242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90636589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72aa80bb58f1d9a335db9e64f83914957bf84b6540b4d3ac34252124227ff581`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dc326ec944b7858d5d87a7b0cb86c8d0aacc5f789574834b5e1a503f685abba1`  
		Last Modified: Tue, 13 Aug 2024 10:24:07 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ea8994a5113c77a48df6d818d1b7f0ad13b681ffec48e6a51f8addd9c885b2`  
		Last Modified: Fri, 20 Sep 2024 17:20:44 GMT  
		Size: 58.6 MB (58559449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3f83af805d2e3db69d2aa194709a010a17f7047aa7777e1f2f199139702be7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088e335e2f0d0a93f395b4a9ab0399b386125c2f5893b07d018e81041abe0099`

```dockerfile
```

-	Layers:
	-	`sha256:660e4ad9fa378c9f647fabded7595f3352fd49b934428653176a4707915b4a1b`  
		Last Modified: Fri, 20 Sep 2024 17:20:43 GMT  
		Size: 2.0 MB (2048556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa2b6d47c46e121524d6a7e6b94f1bf042dd58a765447b4f2d92f28ba628faa`  
		Last Modified: Fri, 20 Sep 2024 17:20:42 GMT  
		Size: 8.7 KB (8671 bytes)  
		MIME: application/vnd.in-toto+json
