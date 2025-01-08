## `sapmachine:17-jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:d44841b51b0705d937122e63f3a1988794bfc8b636ff650ff18d7ee5ce577c96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:8e9a39712b70467ffd55b496e427350ec7bec0c92fd2be1a8ad6c8f18413a1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.7 MB (225671305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3da3d3a5c8c4f45e91ab03f977f8bf182c968de3d6f6318a7420ea1095fe9ac`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Wed, 08 Jan 2025 03:54:41 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6cd0ba0e30bab290202bddc8a12159db089559fba101e3d9868c78765edbe9`  
		Last Modified: Wed, 16 Oct 2024 19:00:00 GMT  
		Size: 198.2 MB (198160245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e0e7854615e1ca41695d17087669f1674d39952ad9ec75845fa4890ff00d20a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51725d07308bce46188274d984c70258cbc1e36671d28a6ed781256132b28644`

```dockerfile
```

-	Layers:
	-	`sha256:df3717bafbb1b3bac9d761e0adfd28cff731871eb059a76dd78d82f2aa900526`  
		Last Modified: Wed, 16 Oct 2024 18:59:58 GMT  
		Size: 2.1 MB (2132052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6d9a4fed8bfd384a669b1994925cb85e7db42cc4a4aae2bd35c086da98b775d`  
		Last Modified: Wed, 16 Oct 2024 18:59:58 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f2dd717ef75e33698ca1fe97b138f106518af74549ca215582fa58d61dad9001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.8 MB (222831534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c32920e636f1bcc9dcb7f9510c6c333ff8a2b796fcfa7c438e200000d7959c6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f223bb8dd7bf392302e5a07de3246a50b741a9b600404b875a63e4db02f7fc23`  
		Last Modified: Wed, 16 Oct 2024 19:38:55 GMT  
		Size: 196.9 MB (196857706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:83f749af854c90021a472c8698789de514458f3cf69083fcddad19c30d29dcaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451265db627dab3d9a66c54eb6042db4502069842fe2d1c2614219fa3b4ed4ff`

```dockerfile
```

-	Layers:
	-	`sha256:ce5734a45f394a43fe8dce1f3565a86650dd8b46fadf778e5394b120c5736053`  
		Last Modified: Wed, 08 Jan 2025 03:57:20 GMT  
		Size: 2.1 MB (2131679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57995566f06fccba8acef6f5502b2803ba9f1813a6e0a057878d875961123015`  
		Last Modified: Wed, 16 Oct 2024 19:38:50 GMT  
		Size: 8.8 KB (8815 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b265177c28b844ee2e158546fe6e03378a944c62972f1d2d3431da4c4b2b48aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230776338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12600bf557dfff44a72a751073c3f28e11d0709a47f4233e4c0cca2cb9ba6001`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a219082a14a80be31ea92329f83b99c6c7c3d8c77cda8b4c9115140a6dc485`  
		Last Modified: Wed, 16 Oct 2024 20:07:44 GMT  
		Size: 198.7 MB (198699832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:86d8ff7e9bc11693f8eb1b53b90eb80de3f9d2787342619a52a6e7e7609cbc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2142560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395fafe55a22059cf251cc190c251956994043beb44bb028477e12c605fb952a`

```dockerfile
```

-	Layers:
	-	`sha256:235e6c2b7d1ef5da79f7f704d788959850739a99f1c566a909e6fbe9bcd582b3`  
		Last Modified: Wed, 16 Oct 2024 20:07:36 GMT  
		Size: 2.1 MB (2133805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff00ec57afcbaaa4e4a8846501ebb3936b6ee0cbe75abfd9a37fd532a9b182bf`  
		Last Modified: Wed, 16 Oct 2024 20:07:35 GMT  
		Size: 8.8 KB (8755 bytes)  
		MIME: application/vnd.in-toto+json
