## `sapmachine:21-jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:60d3a4fdede58b423cc17c2504eabf1e8bf7ce8a6d03144781c80eab766b9071
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:ba0d8bdf4630860da748e74b79d546ec5ad5762ffb3442b08c1c42f3e50b149a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241067571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b10e64223afa36ce063573c64d7dedc112d6642471fc0ab55e5066407d10567`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0dfc0b30c96fdce32abd1fcb78d6278d7decfcaf45cc7cde7a057f2da83d42`  
		Last Modified: Wed, 02 Oct 2024 02:00:13 GMT  
		Size: 213.6 MB (213556519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:427794d14cf9ac35e32afb3a5f34ab1bf684f80b01682b9f236572b4ea62a27f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0abd9cc7ca2b3f74f65fde29bb2116e263142c21010a253d23d6620875c804`

```dockerfile
```

-	Layers:
	-	`sha256:2090c504a041ebaf7a5d16d1b7a00a56e82bc93c798d13d79a284c3331723ae9`  
		Last Modified: Wed, 02 Oct 2024 02:00:12 GMT  
		Size: 2.1 MB (2128619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fc0cd6418b165e32311a6f0b70512578c52691e903f399d351027a2abacc51e`  
		Last Modified: Wed, 02 Oct 2024 02:00:12 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4eaf77791e8d550aa9b88994fdb9c2fa0a0249c582072206456c9e6423c155cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237624322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9523c2f8f6c336696aecfb90dc257a8110b71bd5cc6387e5f1b735711e6d857`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219b4504e88b8ff3eb13a8e120381439b84317e932f2a3f75be5d44f8ff5ce62`  
		Last Modified: Wed, 16 Oct 2024 04:35:25 GMT  
		Size: 211.7 MB (211650494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:25c53fde279c96f964c6afd797098e0b5049261a9120083db050f899ec46f781
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc319cd62dc2780e815f39a81f08a3071ab7994c635d3bbf50f2ef1ec74d8c8`

```dockerfile
```

-	Layers:
	-	`sha256:b22612db8488280f61c06fac0d8a80776e39f980174a365e635b4f9e99b004c3`  
		Last Modified: Wed, 16 Oct 2024 04:35:20 GMT  
		Size: 2.1 MB (2128270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f0b5fdcc1aa8f56aa23b10c11adc52f2656d691ee261beb587f7b4d6a215d5`  
		Last Modified: Wed, 16 Oct 2024 04:35:20 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d82532659f22f0ffec6e4e985f8e64efa52c2ee44d8093d5a1069c2e3daaa7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246416511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da92b555bc4e00b7904f0039e9a78d0660d5f8dc83dff6ed65a255a912f6c68`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8213d2a47dd9b1a7b7b592c734b6b4d77a41bbf87ec3f1f38805d21f7abf3c`  
		Last Modified: Wed, 16 Oct 2024 02:53:02 GMT  
		Size: 214.3 MB (214340005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a4ec799121383d82d23bdf2cf41e3d358369c1657f1a8fa670afd3b4eb824fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d395b921f56bb2fddcbc2213977761e0b4c327680652f0c4a455f1e184fdcc5`

```dockerfile
```

-	Layers:
	-	`sha256:00dd6bd9b2f17e8ea87c605a29d96df4324d9ae9f5f5d671110d5eb4d9769f0a`  
		Last Modified: Wed, 16 Oct 2024 02:52:57 GMT  
		Size: 2.1 MB (2130384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27dfd6f8dcff0f22ce0d67d5cead5dc398548d7284f7a88d61f4eab723153047`  
		Last Modified: Wed, 16 Oct 2024 02:52:57 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json
