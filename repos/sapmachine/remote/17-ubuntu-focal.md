## `sapmachine:17-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:5b6805c87c49d05bbe02a780d2e53dbc2b5108eb3f998212b1b2b55aab093b2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:1c497008e6c8ed071dbf9bca0b8513b0b18becbdd614ba994f6112d6538007c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (226980259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67efc963a4936780ac88fb440b4ed6ab93429c44e56f40e0b7165d8303b6870`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9df4bd3815db16f8fe3ac120c6c6213341e4f2474a6ae275a63742f1a7c4ac`  
		Last Modified: Tue, 28 Jan 2025 01:31:10 GMT  
		Size: 199.5 MB (199469199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:13bbf90520eafed23e2c3751e6f43164dd1031bcc170c26c056980ac5241b087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9ada06342f96be95922d04424d9426659198338fff75496bf0d541cbe0c38a7`

```dockerfile
```

-	Layers:
	-	`sha256:3f2af202b1d24279a1f48f0d8b2ef4209c939a9b35468118320df1dcd2391420`  
		Last Modified: Tue, 28 Jan 2025 01:31:06 GMT  
		Size: 2.4 MB (2383427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a24a42ddb8e804fd9dc8fe303042dc0c23f899f10a6fa1ba504452688390406`  
		Last Modified: Tue, 28 Jan 2025 01:31:06 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f6cb5090a39db79032165e01e845326b120bd0106b277152a361ebfa20fe102e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224177611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4927d99b6dc11456d16c4e63bc6942bca27894ffd597ac5563ced359d32d3eee`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddddb717301be009f48a72dd51bcdf8facff96a4a7ef36e1262263813d66d76b`  
		Last Modified: Tue, 28 Jan 2025 02:56:36 GMT  
		Size: 198.2 MB (198203783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ec85d112f5ba8c769168194405ea8c5dc0f2f5d7240b8fc659eb07e79d9b558c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3be4395a4d1a9eb831a9dd46bdd10edd4f692dfb676782edc2e16b464a71772`

```dockerfile
```

-	Layers:
	-	`sha256:1f508439370c271e3ee6c65a73dcaf945c55df69862a90389688e2985eca8e41`  
		Last Modified: Tue, 28 Jan 2025 02:56:30 GMT  
		Size: 2.4 MB (2383113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b92a30c11da541f9bafa5dd2fab24a0b26667a221dc580670a882658a1bb53a6`  
		Last Modified: Tue, 28 Jan 2025 02:56:30 GMT  
		Size: 10.3 KB (10290 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0ca093224b2dfd84f467be7b2bb71fde395f9c18b52cc3401844cfdb1d6f2911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232240408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a632ca0125cb8b6546c659c0397eec9403747924c4f021ce0d6b0a624cb9884e`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb6f207a3bf4c60dc3d7a094fe2b9657206c6c0b612142c28a7c27fef9b18f6`  
		Last Modified: Tue, 28 Jan 2025 06:25:56 GMT  
		Size: 200.2 MB (200163902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:53bdb21a4b5f76b523bc0bc8a09caabedb5472509276e6f61432cfa6a08a8325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece77d8118208272950b6f73642e3b8e2dd74730bf4684808603623f35340d97`

```dockerfile
```

-	Layers:
	-	`sha256:9ff40a092ce5de7b6ba4bcc4aafd19f20f78c72411e9e05b7a8964c00266ffeb`  
		Last Modified: Tue, 28 Jan 2025 06:25:50 GMT  
		Size: 2.4 MB (2385272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aeaa743888f80371643b2962c33fcf1f56a25a70693e234a049ed3c4827f979d`  
		Last Modified: Tue, 28 Jan 2025 06:25:49 GMT  
		Size: 10.2 KB (10206 bytes)  
		MIME: application/vnd.in-toto+json
