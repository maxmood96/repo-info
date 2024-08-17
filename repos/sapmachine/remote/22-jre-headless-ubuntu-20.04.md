## `sapmachine:22-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:e6206364e2a716dacc583853e37808226e121f2858c3ad782681e7e567037288
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:1f5216e61ab4fb65fee004386eed91f2375d5546c34bb367327faace57ea63cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (84988660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b9d565fbb1cd5eed855c8d600d7178f27977950398280c7cc5417fd9e745d1`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f052767a95b07d7479429dd0d2ed15833a3fcee1497eab963011f36583e7066`  
		Last Modified: Fri, 19 Jul 2024 17:59:16 GMT  
		Size: 57.5 MB (57476891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aef87b3054837809d8c5f7ecbe803a91cf782069e4a11f036b417fdc20bb95bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25cd9c10d69beb4ef2015b659c31627cb992e767bc1e9c3ad57f6003b6a4991`

```dockerfile
```

-	Layers:
	-	`sha256:889981fb3ad554be47169c7adce34ca492b93fc7e29acf4cfab012ec2b88dad4`  
		Last Modified: Fri, 19 Jul 2024 17:59:15 GMT  
		Size: 2.0 MB (2045568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aec8986a0d1ca64b756dc791116f62087a92e5a88c0f9d2ea4715506ebbf5ce`  
		Last Modified: Fri, 19 Jul 2024 17:59:14 GMT  
		Size: 9.4 KB (9357 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3a7ad11d0717b9a1efb53addffd636665c2e0047227c520902cc872959a0ceb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82490174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94f6d804128ab7d22c47215b05232d44e3ef60db60e488f6bc7b92a1532a0b1a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0e45e764a3b00cd2370b9602947e567f3ecd0d3f541e07309a613758fc26af`  
		Last Modified: Sat, 17 Aug 2024 04:15:01 GMT  
		Size: 56.5 MB (56515957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8975a5853c8bbe339f6f9c83c113c666011df40eeb20fc7a89ecf6e0ab2b712e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0ac3e7aeafd47caa154e55d2e22dd0b3c167d458c21c1467706205dca913e0`

```dockerfile
```

-	Layers:
	-	`sha256:3f10754e28f9e79f7199debf68bf4c4bb3298bff8eeea74c45300ae598a3635c`  
		Last Modified: Sat, 17 Aug 2024 04:14:59 GMT  
		Size: 2.0 MB (2044588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b752b8c076ea991d3bb9986da78f1e12e18ec47e0a9d92770f3e5c844f8dbdfd`  
		Last Modified: Sat, 17 Aug 2024 04:14:59 GMT  
		Size: 9.7 KB (9682 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4a6893f154a1114528974dc716475953508c80b81ce1144085f4ee5fe4703c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90446885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4077e0681c11db71e14fa474987bf1480d2a67e4abef74f985aca35723846d53`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df16f6497ee56e35e46cadaf015a6b2828683ac80b1491d0f8d6e0d8fc07ec8`  
		Last Modified: Sat, 17 Aug 2024 02:44:44 GMT  
		Size: 58.4 MB (58369745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d994bb378b1aefec843b3e8964beaffe0a870125734f28a8dc89292806d7b018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2058058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2711fd0ab82494a539462f8d0fd0e4e011e56b83dd346c7ef400e139000947`

```dockerfile
```

-	Layers:
	-	`sha256:2a60a52cd204e4b98dc8db167f100aa039b75689a03b0426ad95a6f39fbe4e2c`  
		Last Modified: Sat, 17 Aug 2024 02:44:42 GMT  
		Size: 2.0 MB (2048651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f727833f0d6bccf7a75abb7d20ac916f527acc3eec9f5698ad142085268f8454`  
		Last Modified: Sat, 17 Aug 2024 02:44:42 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json
