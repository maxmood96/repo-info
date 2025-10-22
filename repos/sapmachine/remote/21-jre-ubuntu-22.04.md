## `sapmachine:21-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:de6994a12d154466dc5ba2ff678723cadd2a73c979b56dc1664de0ca55274364
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d3b659697a03fa7f77a621f8776b68d9e508cbfe5338dde45cdab90c38548be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89361096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b91d81d4e2c910bdaa308888a11bdaa6511f02a4a50faa79011c8528ed5b4d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e125b5b5effed42bc8d21b4d3bd328a2d2e3f88f3862b0914cc4bf1cfac4b12b`  
		Last Modified: Thu, 02 Oct 2025 05:20:06 GMT  
		Size: 59.8 MB (59824278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d3786e4108799cba9f53d1e76519cffad74dbe3cb08f788494c7a4e0a835dc65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56545ce3dd9468d958395199768e537c4a119a39fd18e51d5b24317f294cb101`

```dockerfile
```

-	Layers:
	-	`sha256:7a1908ae16be115be1ee2d1d8c4a29f80ca15cabb2c1b8ecc36e391c93f43383`  
		Last Modified: Thu, 02 Oct 2025 09:10:12 GMT  
		Size: 2.5 MB (2544889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9f12d3ceb695ffe6b72688345288db0d9d00ec0d7b4a8b3bc023f381b463634`  
		Last Modified: Thu, 02 Oct 2025 09:10:12 GMT  
		Size: 8.8 KB (8812 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9077c2a7a8c31a2bddd168972a9be0602b1e766a5bdefd0cd2976b0ee383c2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86368198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b1096d7cb4009ae2c6851d4e724c53f9482508a5250b640208f92ce3358a086`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e2af85226c385ec50ee39bcf88133233fd3ac87ad6cbc27ea678763e1b83b6`  
		Last Modified: Wed, 22 Oct 2025 00:06:20 GMT  
		Size: 59.0 MB (58985091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b5950d5110e4579bde1ccf8428ca7c64939d561d0c9eaf57e61a6de505264b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab003ecc787f7dc3be2b5ff2bebe55863a32ba57c3622eb987d532cb6059830f`

```dockerfile
```

-	Layers:
	-	`sha256:e8f51a1a57560f4ee7182c71ac7cd77a8fbaa72c1d0f7589eef10896151a85de`  
		Last Modified: Wed, 22 Oct 2025 03:08:18 GMT  
		Size: 2.5 MB (2544571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6224927efd46f7e5c36a3260b21ee8d717f6e010fe081f39af683f859e15a88`  
		Last Modified: Wed, 22 Oct 2025 03:08:19 GMT  
		Size: 8.9 KB (8916 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:910562b5c07f4d7c1f9d5c35663f1b83dd12f7cbf9e7d87372459baf5811f78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95388248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79520256d490416c1148bd9f335fd41a1b1298d627bb7c8329c5c9adb6a4a7ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e62ca6f5127fa6b4672fc4e5329866c0fb6462962f2417bde6be4c66cd2a6b`  
		Last Modified: Thu, 02 Oct 2025 04:39:23 GMT  
		Size: 60.9 MB (60941459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eb8e414440c7ba7e0014a2ecec24d2b98b7e3247eab8a13aa084b0c04d96a26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2551860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ca8340267cc0457f3b8f03770ddc3d4a0dbdde9c3ac68483612f82b6f74ef5`

```dockerfile
```

-	Layers:
	-	`sha256:6f4ba773803e145c07fe1b7fc3586c0f02699ac790d88371569bf0fc3eec28f0`  
		Last Modified: Thu, 02 Oct 2025 06:08:42 GMT  
		Size: 2.5 MB (2543004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7e7ca47c1208beeca9bb1b6ce5323ba712a3997ccadbd3beeae345e74e90f1c`  
		Last Modified: Thu, 02 Oct 2025 06:08:43 GMT  
		Size: 8.9 KB (8856 bytes)  
		MIME: application/vnd.in-toto+json
