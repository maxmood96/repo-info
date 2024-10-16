## `sapmachine:17-jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:8d687e0a00ccd64fa308ebdd8f8823f014c7e57352765a7e5146696f61dbb71d
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
$ docker pull sapmachine@sha256:6d218a8ccf1cb438004d397bbf215dc8a49f74672d07a744858508a13c025a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225899854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf5b0e29c2f545a5e0e40aba13fe3eb441514717e79c8c5034724a18180464b`
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
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f9bdefc46cff4639fc5e996e3f273b26c88b3ddc9224c2e063c8955f65660e`  
		Last Modified: Wed, 16 Oct 2024 16:18:16 GMT  
		Size: 198.4 MB (198388794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cb70823b3e07481df1b43f0a79bfa79a39ac0cd300fdc70a575b9f66980e0e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fcefdd6c526cff1acba0a7a4e3acdaed013ac6ed05c7696c5285e16a26cb5aa`

```dockerfile
```

-	Layers:
	-	`sha256:30de9513976a5b96c52aad88b5ffa8abb2ceede1dd3481519dd34e387eb02be4`  
		Last Modified: Wed, 16 Oct 2024 16:18:13 GMT  
		Size: 2.1 MB (2125406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:925105b036df0c06dec30c7fb4bf646e8445b08379411df9dbd20c9d4464fa6c`  
		Last Modified: Wed, 16 Oct 2024 16:18:13 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:673487f8dec52492356f4efaff9e9f74a0590bd1bf2e36d37507dfe7be902a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222996372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad443eba1ef0382d165c92e9920bd2a7e2f35c4b7b95a9b4252f53d703617004`
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
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
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
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33722728a7096ec996247bed3e0760e04383b78042ec6c2425d3126c86ca98f4`  
		Last Modified: Wed, 16 Oct 2024 04:44:05 GMT  
		Size: 197.0 MB (197022544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:14f95f7409a5c3400c71e94f67ada72d4ae83cbcce47b4897267274abe03dd92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a99f248cd79a66a1d652f67c4e54899fa39c460e590928db2988cc4c1cc1e7b`

```dockerfile
```

-	Layers:
	-	`sha256:23dabceb0457602da0e6f43fa6320ce09ef2934d3504b11aef103467efc0e229`  
		Last Modified: Wed, 16 Oct 2024 04:44:01 GMT  
		Size: 2.1 MB (2125033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3b668750d4b7f61cede35913f0ffc446aca58f6590cb99a86b5d94498847bca`  
		Last Modified: Wed, 16 Oct 2024 04:44:01 GMT  
		Size: 8.8 KB (8815 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:520f28ae338c74f4cdaac8c1ed2fab9b2403f6f068296b4e57d0cb9923d365ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231006339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7c3156dd51494236db3d53be0be471b003a0f4eb609713db9e5a0913507781`
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
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
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
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4ed9132c251d26426c0c3d2cc32b79572d740bb3e98e87fd87d382ced22639`  
		Last Modified: Wed, 16 Oct 2024 03:05:23 GMT  
		Size: 198.9 MB (198929833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:955fc55b71f23188dc01fa9baae83052d27ffa5cc6f30074159c145cc38cb1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f63ab302bcdbe7995bbd7fa987b3b58cf29c368e21b36140e461c7400a1d20e`

```dockerfile
```

-	Layers:
	-	`sha256:4407bb28ecedfc86fa39b09f4ad11422973ecbd15c42023a8d890e0ebf4fffb7`  
		Last Modified: Wed, 16 Oct 2024 03:05:18 GMT  
		Size: 2.1 MB (2127159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a0e2534c46cee97b805f417cb19e310b588c9f96f69ea2917a492622d2c3309`  
		Last Modified: Wed, 16 Oct 2024 03:05:18 GMT  
		Size: 8.8 KB (8755 bytes)  
		MIME: application/vnd.in-toto+json
