## `sapmachine:11-jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:f2abff912b3ec240d52026f7777129fa1b4fbf56c804da8ffc79a54f9c469823
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:98a5391956428767f900fa53436d10f78411b7de90409c8040d430a580ae54b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226696192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e227a243290f555c36c85981525b9ce59d35b6c8ba7cb6366a9808e753364f`
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
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0977344bdfd557d4ee640d0ad41e78a01d41bd64f8c708619f76dff0f92bc39c`  
		Last Modified: Tue, 28 Jan 2025 01:30:57 GMT  
		Size: 199.2 MB (199185132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f063be314531c0249776718d2c450ff6decb163d80d60f5662d89c1f47d7ec36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bf5b0796f1e746a0f536cafe8e9fe69fe4c8dc655bc0d1e49294927b007956`

```dockerfile
```

-	Layers:
	-	`sha256:6acd91976d45bdc340f5a223d156bca5a0f8961034bc37c5d1beaf04dbf2a44c`  
		Last Modified: Tue, 28 Jan 2025 01:30:54 GMT  
		Size: 2.2 MB (2156783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72a535a32de38a1af03acc49c0f1fb14b5b772d7b028ef905e01bd884d5e8bee`  
		Last Modified: Tue, 28 Jan 2025 01:30:54 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fe9c084a30bb5980802a05f57310cd3ec317fa767b99e9e2d9ec27c13e6a03d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 MB (223667080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64542ce59956156aa8378aa03d8cff54a095e4ac5c9b8011aa69748c66e85a7`
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
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0a8bac4dc6627fb05e5e39e5bc8adc27fc2742d27c9ad422b844265a5b5436`  
		Last Modified: Wed, 16 Oct 2024 19:52:39 GMT  
		Size: 197.7 MB (197693252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:74b6afe2035c5aa1e01f2fb7629fe31f2b01e9432cb54a25ce179caba71b0dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2153679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9092cc91af64f6d36b573a51c3ed81c136996166f52a7a1a3480779fdc87fcf`

```dockerfile
```

-	Layers:
	-	`sha256:2a83b6febc796d3362dac8a22cd62e871f213a25b09d40c83de57ff473d91f47`  
		Last Modified: Wed, 16 Oct 2024 19:52:34 GMT  
		Size: 2.1 MB (2144864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7538bad38ea374dfe555b59b4dfec6324dc5f1006508f61b50d9a96ad856c26b`  
		Last Modified: Wed, 16 Oct 2024 19:52:34 GMT  
		Size: 8.8 KB (8815 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a8f8486feed0cc9ac864a4f6ace6c376863ccee4f9f58b3e94b47c42a1d889fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.4 MB (217393768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586a4cc4cdc8148b3a9654a9b47462378ba461f4b63a0e8db991ffe6cc5acca0`
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
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e67cd1d2afff61b42a7a4203f1785b9138b791e0b7bccd144f9c5d0c26570d`  
		Last Modified: Wed, 16 Oct 2024 20:30:52 GMT  
		Size: 185.3 MB (185317262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8c35a22c55ed3db6118bce5003946000b34e28bfac7dc44c7e42be0ae4cbd76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2154492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2025954051c26df2eece1cff9f57cdca6c694047940f64762436800432e7fd3`

```dockerfile
```

-	Layers:
	-	`sha256:5c7a172140d7c37ac45c4778e44729c25d177c3c1eb73662010ecc93c8b3d455`  
		Last Modified: Wed, 16 Oct 2024 20:30:47 GMT  
		Size: 2.1 MB (2145737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e14f969bb31a33862e6a5a11354253523f86d95366d652895d315afb28eef921`  
		Last Modified: Wed, 16 Oct 2024 20:30:47 GMT  
		Size: 8.8 KB (8755 bytes)  
		MIME: application/vnd.in-toto+json
