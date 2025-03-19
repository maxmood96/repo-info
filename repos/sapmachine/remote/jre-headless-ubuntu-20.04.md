## `sapmachine:jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:6d2383324be6555dcc4caa8757c693fc9aebd0134c9fd3fc77bf53a98286edea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e166fa1f56080de5f167305b25bead15a2993c712ab3063a0e9a028c0c95a3ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93524404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7e1b060b4f23076ec749e92bb596bf68a56be310d7a88b52e22984f5868617`
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
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad426968a1f350f152b47138ac2f5ce6607da38ab03f7b851e892879b1f273e3`  
		Last Modified: Wed, 19 Mar 2025 20:33:20 GMT  
		Size: 66.0 MB (66013344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2655466f74aea2d35f82f3a8eec60295383d96f7569026f035f454f1503e344a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2078505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4036d7530fac9c010cfc038c3ccddc7df3ec32fa1e4b976c4ca8c67eb9799db4`

```dockerfile
```

-	Layers:
	-	`sha256:2de9f917db7e2996d942f3cb6f6aead8022bfac1524b15c9ac4483dc64e0dec0`  
		Last Modified: Wed, 19 Mar 2025 20:33:19 GMT  
		Size: 2.1 MB (2069618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6966ef03e0a53c2bcb48144d899aa93768d9101828dd7f95ae897d35e1ed40c0`  
		Last Modified: Wed, 19 Mar 2025 20:33:19 GMT  
		Size: 8.9 KB (8887 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cb65528c83b8b667a09a3ddcbd6dccfa4d67d1c758f14da677ff3cca9886e2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91014526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392298cf2f84e5d12db54e4a01cbff041a2593fcc752d5730546f0635a50b3b3`
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
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3bebc157b11aac3fdffbaff16d4cee87e151550133238b1487424847f1fbe`  
		Last Modified: Wed, 19 Mar 2025 20:43:15 GMT  
		Size: 65.0 MB (65040698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:464764f6fce7b51efc2e987df751afa7f724e4f0eade94552f7d75ab4c98e42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2078234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4d28f6dae0f2b1f9a62177ac0d844f6e4f17933f24583d43950441f33df2f3`

```dockerfile
```

-	Layers:
	-	`sha256:45cf9cf826b934498545334069bf5c621851cef40656de7a17a403cd357f99f8`  
		Last Modified: Wed, 19 Mar 2025 20:43:12 GMT  
		Size: 2.1 MB (2069244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d2b0b7a01cfe25fd66edbbe07c23adfeb43770a6c796d18513b5496ccc2b1ef`  
		Last Modified: Wed, 19 Mar 2025 20:43:12 GMT  
		Size: 9.0 KB (8990 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:12738c3ad8a11952b4e4f42a190e74642f7ca6b3c366ebd4d0ac665a246fd9a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98815516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282648b2179e2fce1faef76efa6114c74373580897f13609f718c3f9f36b42cc`
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
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8d919e6cf7e192678ea5d3aaba0206c94f9e92801d575f992b92c125365bef`  
		Last Modified: Wed, 19 Mar 2025 20:48:40 GMT  
		Size: 66.7 MB (66739010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:161962d08e1a1aada2a536f85f7f2f2758d357461174d8d3a14adb31b9e685d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2081623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fed607a64ffcc456c1188841c5d78c19a2ade44e8d87d04da570f4af0261565`

```dockerfile
```

-	Layers:
	-	`sha256:f55c39512b19acd6a6727d0bd72db0fb42ef97ae539b9b03632f3f1442187a2a`  
		Last Modified: Wed, 19 Mar 2025 20:48:38 GMT  
		Size: 2.1 MB (2072692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa8a819c516730324d514d44bbd26acec218c1a1b238ce849f87e80efa10ff3a`  
		Last Modified: Wed, 19 Mar 2025 20:48:37 GMT  
		Size: 8.9 KB (8931 bytes)  
		MIME: application/vnd.in-toto+json
