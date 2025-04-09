## `sapmachine:jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:a42807afc44f2ee269a9ad3ef22530a167813888048121fd9848fd7851bdc71c
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
$ docker pull sapmachine@sha256:3bb069819c0033592fcb37b65bd5a26e837fae6b91b40e0025dafe16897ccef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93523740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f132926e54232f85aa955886fcab3d26d74804498319b62a01466f0d68ff9007`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c51ad1db47418ab4e7b04471b002ec7dad9c021f972536af2900cc91a32c6b4`  
		Last Modified: Wed, 09 Apr 2025 01:20:36 GMT  
		Size: 66.0 MB (66013346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:09094a96da20181b6d1ba2b502610c2282c62940750f30322855b35c510e8ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2078571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fdcd5e484abb9f3b6a8c358d15b114caa8b969970ca9d3fd905e3f3dff6f53`

```dockerfile
```

-	Layers:
	-	`sha256:a2a3cbcb6aeecf1c50c8e9f02e682e7449de161e0872716265f7645b08541c7e`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 2.1 MB (2069684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d1ab85127b2ca43c11e9329ab2849e1b91abb8b7bf45c113a92bfa9cf246214`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
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
