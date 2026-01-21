## `sapmachine:17-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:ea806a87e9237c66b893a875e4fa4d71a6c07ab55259004b8d92e42dd28f7389
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d0b206f5492742382199322b12c5ecf229f89b4e261fbbe3161cb616484e294e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230395126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6959107dfc832497d4e8df7cfe2b4971b610aafd639c5dba66df792eecbb8c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:44:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 22:44:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633b3755719dc492d38e33c895e452e0a1c804f6e8f0ee64680fac0cc65a0fe6`  
		Last Modified: Thu, 15 Jan 2026 22:45:06 GMT  
		Size: 200.7 MB (200669115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e2b4c849272ba979cbde59f1c5ac91fc694bdba4aeeafbcc8f8f5fd930307d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7671b9dfdff6e2c356c302250a84d02869b22586101808fa30ce2c738566cdb3`

```dockerfile
```

-	Layers:
	-	`sha256:4e1b795cee9e0ed228443e5852acc0aa6133493ae858dc143c6179718278a228`  
		Last Modified: Thu, 15 Jan 2026 22:45:03 GMT  
		Size: 2.6 MB (2602862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb5ed5a8d75210bbc067779923c973b082f27951645222087e39d0fcc2bd562e`  
		Last Modified: Thu, 15 Jan 2026 22:45:02 GMT  
		Size: 12.6 KB (12606 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:91706d9f47d04fb393fabc310c551aee85e59cb836967d39b8c52f9fe6804e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228255814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55b13564466b39e6a452078eb173abd3f878ecdf068ff98eb96d4d9d7e40316`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:47:18 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:47:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 22:47:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f088f3557c22df49bc8905b29b2234527a7bc4c5decb14d2ef33c4b56489282e`  
		Last Modified: Thu, 15 Jan 2026 22:47:40 GMT  
		Size: 199.4 MB (199391990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1d406ac87f396118e919c42a9d12b25ae2700c7b3e547dd99e768d0b6f856e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee64314179bc6b4b1d2d29f1d86f00f72fce251e1464424ea3d6ae3d32ccb05`

```dockerfile
```

-	Layers:
	-	`sha256:571d00ea638315e7f95d8c27b088260423992867f91b376843a421ba3c8935ca`  
		Last Modified: Fri, 16 Jan 2026 01:07:48 GMT  
		Size: 2.6 MB (2603474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b74e25e89817058e52678aa069856a5158e771a823a6e193a00a4a9392cc3c`  
		Last Modified: Thu, 15 Jan 2026 22:47:36 GMT  
		Size: 12.9 KB (12855 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a174454a211653be0775ae34a1788be3d9ef859fb605472ebe5b4e04f656251b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235760136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc4f87796adeb140d2dc48aba918ab5f0319d1af54e855b85ee6defdf4c8f76`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:41:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:41:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 15 Jan 2026 23:41:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501be381e843027f54034e915a7db9dab98cc0f55273d6fe7ceb5be3274b5b52`  
		Last Modified: Thu, 15 Jan 2026 23:42:29 GMT  
		Size: 201.5 MB (201453977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:520bfbdfce42d7353fde9938310c8b2ee022478121e08436f5c8a79d85a05beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2611768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64592172111aaadac4f54d3f928e6acf54f38ec846ffad1c7700d379228ea60e`

```dockerfile
```

-	Layers:
	-	`sha256:8cdfd449735ab7dca43ce8706302e74854cdabcbb47f50fbd62f7278f5c74de3`  
		Last Modified: Thu, 15 Jan 2026 23:42:24 GMT  
		Size: 2.6 MB (2599045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8a6d25bfc23e506fb6a76391389e54e25c50a5f9fcf1a44b79060db91ce7f67`  
		Last Modified: Thu, 15 Jan 2026 23:42:23 GMT  
		Size: 12.7 KB (12723 bytes)  
		MIME: application/vnd.in-toto+json
