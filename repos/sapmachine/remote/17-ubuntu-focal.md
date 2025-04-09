## `sapmachine:17-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:6e0fa86a206afa3c35a8b529642275d46e8058b0400320da267e3a6c31b8d09c
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
$ docker pull sapmachine@sha256:ed7be9e1a8536992456144a60c2aed43e382e17eabd2cacb6ca348bcb808589e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (226979573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61b805fffbe3de42d0d371bf791d918cf6854906bf371cada32f290dbe8946c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33c8d0189019711c0214632f86b1b7d5366263579343d1f04cc2953de1f35cb`  
		Last Modified: Wed, 09 Apr 2025 01:22:10 GMT  
		Size: 199.5 MB (199469179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fb0fac90df7b35ed9cdf537b999cef6fbf5cde28d0686bfd9fdae19949966b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2393665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00665dfbaa98656fd26f5971feded775f13bb640f95faf9f86d6d0386ebdd3e9`

```dockerfile
```

-	Layers:
	-	`sha256:b212f270df613b3a56a4927b4646ec2d0380a5218f262cbf7dc164938619ccf8`  
		Last Modified: Wed, 09 Apr 2025 01:22:06 GMT  
		Size: 2.4 MB (2383527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0df6eedf499e38257efeb7e85d71fdd5a042d50a5b035123581a3c0ad1f4502`  
		Last Modified: Wed, 09 Apr 2025 01:22:06 GMT  
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
