## `sapmachine:jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:d8635fedbdaa273211689bd6d885a5b99bdf7342416dbe3f88b3e85872e234a2
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
$ docker pull sapmachine@sha256:1fdb6f2b439cd3f1f481e1644547c2207bff035f6e8962697f3dfff774ca5dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85228410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdc171d420023acd72af91e90fe2bb117d31081be8895e4725a5004e9979249`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384285201c6d736c0c51a829e986289fd062d4ea79a0acf05abf9a459e6b410d`  
		Last Modified: Wed, 16 Oct 2024 16:17:43 GMT  
		Size: 57.7 MB (57717350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5e1cbcf1c22e005d151dd9f9aef1e0bc4a00fd2b7bf7d3dd2358e334576f2858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1c31ae4a39ea39fb43d0e2207b09c8e4075c92893484957db241105c7db478`

```dockerfile
```

-	Layers:
	-	`sha256:90fa8c7cafa27d7d108abe363fd9e39e2640a93a98ccbb2ba6547e5f82f21ed3`  
		Last Modified: Wed, 16 Oct 2024 16:17:43 GMT  
		Size: 2.0 MB (2045498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3cb365a5fb2f23389e0db5a10f527b909c4a38b91a82684ebf73d80efa65e5c`  
		Last Modified: Wed, 16 Oct 2024 16:17:43 GMT  
		Size: 8.7 KB (8671 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:45c553d6158567fffe5bf74eab26b0f82d286b0a26b2b38e49418f4b8d05c2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82730897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7a274f65060e8b060d1dba6f4ea60015277192b8fbca09710f1caafd8673ca`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b5b2f527964b9b1f4cf8632387984ea7781657bb5d82385453569f8667aa18`  
		Last Modified: Wed, 16 Oct 2024 04:27:34 GMT  
		Size: 56.8 MB (56757069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:78ad385451ef694fa8f090be5932cfc5c1cac9f2868d01447a7748b862d026c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2053262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994df846bed56acfe76229117371006372549fa51676f05a9ed5e8e8cd2bfede`

```dockerfile
```

-	Layers:
	-	`sha256:d938a201f3649c30c44e30b246d7cd876d2a2bb435e4282029643c7e60b6ce0a`  
		Last Modified: Wed, 16 Oct 2024 04:27:32 GMT  
		Size: 2.0 MB (2044494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818ffe0bcd0cb2dd571f544d71fe7aa8317dacb25f82533e1b62df0443a62875`  
		Last Modified: Wed, 16 Oct 2024 04:27:32 GMT  
		Size: 8.8 KB (8768 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e6c996030f9544b2eceb9858b8826127617a0cf08e812c5aa3d2b5480280c945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90635869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08df597ef314f0d852e58477763d29198ba23d68ed4c59d74b286d9208e3d8b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 Sep 2024 13:42:45 GMT
ARG RELEASE
# Thu, 19 Sep 2024 13:42:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 19 Sep 2024 13:42:45 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 19 Sep 2024 13:42:45 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de06c6368c9dc446d47b08ec5ddad16ab5fa4d4413804b173674a8068d700d4`  
		Last Modified: Wed, 16 Oct 2024 02:43:40 GMT  
		Size: 58.6 MB (58559363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:47ca3b1697667ed6cade728790b87f55d370b3919cb3a282d8ebe8be7168ca61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2057278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ef4d5bda1e0b593603ab1a021502c7739b416e5fb1f4df3da2f023b9a127e3`

```dockerfile
```

-	Layers:
	-	`sha256:67270db969de8271d80eb04fa9dd7832afa6fe2192be2bf53494f1671c1c2689`  
		Last Modified: Wed, 16 Oct 2024 02:43:39 GMT  
		Size: 2.0 MB (2048569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0dff173adb9b4c186c6d819c071101cf607d32892b4c02838f915182d15b545`  
		Last Modified: Wed, 16 Oct 2024 02:43:38 GMT  
		Size: 8.7 KB (8709 bytes)  
		MIME: application/vnd.in-toto+json
