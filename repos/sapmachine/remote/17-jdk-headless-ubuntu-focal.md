## `sapmachine:17-jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:680a6759c59dac449eca5f2ee85409da1b91163bcabde6286ecf7cc4a9757095
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
$ docker pull sapmachine@sha256:0f5abe7f04c2b8fba9e34690cd854b90dec8da006fe5d38bf48fa6026e13bc07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225900018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21235c435527a021aa582f6673fbefe9e2c090fb2dced533d4ce747fd4bf0193`
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
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ea158b6dbb39c255910d7c410ecd8fdf8ca6c1534ca50bd6adfad0c69cab89`  
		Last Modified: Fri, 19 Jul 2024 18:00:33 GMT  
		Size: 198.4 MB (198388249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d0ef345fa5e3729666a1a739bb3eb2358587c42a2a261cd317d1e937c46784a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe02e32269258822db058b6d7a6bb57aa51cab3854bfe2c72dc307d5a9a1aafd`

```dockerfile
```

-	Layers:
	-	`sha256:7f5f630477c07a8fac626565e6259ceba60aa8e63fb25ea38b6f82f26253772e`  
		Last Modified: Fri, 19 Jul 2024 18:00:30 GMT  
		Size: 2.1 MB (2125393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c5f9310fb8de30a288678dd4b3b9029a4298dad72bdcf51a5c9aae803d3403`  
		Last Modified: Fri, 19 Jul 2024 18:00:29 GMT  
		Size: 8.7 KB (8679 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c3e1fcdbc52c8c94034f8567fc038ce64d87376e44413ada55c614cf6aab1e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222996226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f996109119156a95a10b874e1953cc003dc9c6252477f29bd7b2877c11a6fb`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa3417ac5906ae7ebecf41f7183dec034f0943f73ce7279b6ab1a41c6f49525`  
		Last Modified: Sat, 17 Aug 2024 04:39:13 GMT  
		Size: 197.0 MB (197022009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:00ea49c6ee72c39aba7664ccda0c4fce600fcc739ef8777e707cbbe253357931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae31d050c8c61b24efdc881d42c4f3b805a3fd4aa4017f6120e34fd8f43997be`

```dockerfile
```

-	Layers:
	-	`sha256:9e5fc02f3c5b6347da2c3cd1ba90a96058d8bda6808e1fe5578e2cb7f306730a`  
		Last Modified: Sat, 17 Aug 2024 04:39:09 GMT  
		Size: 2.1 MB (2125020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29da81760d0db9efedee3b468f9a97360a1949945154a9300d67fcd098daa3dd`  
		Last Modified: Sat, 17 Aug 2024 04:39:08 GMT  
		Size: 9.0 KB (8980 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7911e7daf5dcb32626b628820b150832b2dca34651c87dfcf9ee1498851d74f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231007241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f32b92d90c0db8ac61bd0ad96046571a3b3c9a384ca6b5beea2e429dfe3e32`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e85da2f5c55526b4c5ac03f93a58dd9a67ea1f3b61d9c6fed39ad28ef18f99`  
		Last Modified: Sat, 17 Aug 2024 03:23:19 GMT  
		Size: 198.9 MB (198930101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0ac79e1a03cd28c048489a089c346b000731362823c3130f9248098904a737c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb9194041421c4ddad0cd18da1f56461820bb2aaf29326fb5ca720393fff6ad`

```dockerfile
```

-	Layers:
	-	`sha256:2823ef9a73dba42434382ae17a9cac82f4487cfd371f407846e1ab9e4862bb28`  
		Last Modified: Sat, 17 Aug 2024 03:23:14 GMT  
		Size: 2.1 MB (2127146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e891097bfa86c0117174c5a27e11a116560461f03bc40e31c1b6443a044950`  
		Last Modified: Sat, 17 Aug 2024 03:23:14 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json
