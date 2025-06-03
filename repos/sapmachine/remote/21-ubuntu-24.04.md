## `sapmachine:21-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:b8c9b0da51525f3a936fb1b89d27821bdcb61495723c8d53ed40aa43bdac056f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d5f207e361d87c282c1f72ce4fb5a1a9443d0dd03839c674fd8f0f62019c3334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244836056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50126a0861c4ce9891079856c6d1c697c2e87d270f0cf9f98e4d92f0019369f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561be86f29e7fcaf4b4181d6462c52fff294fe5a23fbe7accdbd859857134f64`  
		Last Modified: Tue, 03 Jun 2025 04:17:47 GMT  
		Size: 215.1 MB (215120719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1788fe014e95f51c0fc828a8fc6334713a5affa6da21ecb7e10df51c4ea14937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2511738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c67c5a0d5ef0461c000ad5858782289109c11f40ccf1cade69e9f9234b0f5f`

```dockerfile
```

-	Layers:
	-	`sha256:74ce0b56a9ecdd9c566310ac9d3bae6bfe747ba3184295b2186b93552029770e`  
		Last Modified: Tue, 03 Jun 2025 04:17:43 GMT  
		Size: 2.5 MB (2498419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:122db0ce9bc629bf01e51c2d96ac5795cd4d3f0de20c4c30a0e67fc2af2eecf0`  
		Last Modified: Tue, 03 Jun 2025 04:17:43 GMT  
		Size: 13.3 KB (13319 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c3c41b1a9abd3c6ca830d06c01a1fffa02bcb4586dbce4155be540d301ca4690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242233534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2467947a9692a98f80948bb1593628d60d34d24ce8d4168f58ebb19e36e05e23`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52c2e358d2b41df079fc922c2377505411d22bb1106722324a21da4bf4a25aa`  
		Last Modified: Mon, 05 May 2025 18:31:07 GMT  
		Size: 213.4 MB (213386658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:00d831fa74a28f2265f6d40320f859ecd1b28936d7c9dbd7c64c928e590927d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3764fd889d3a14bfb2d91f2b65622c9aa029981c26cbf6d8907e25aed0badb0`

```dockerfile
```

-	Layers:
	-	`sha256:a583dfbbcaa800c75a1cbbc49c239df74a11060c605a62d2a21f4999b0989530`  
		Last Modified: Mon, 05 May 2025 18:31:00 GMT  
		Size: 2.5 MB (2474847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5c3a1e61f64b96ee28fb42420e4588d3b2a0639494c68f02ecb48829e057942`  
		Last Modified: Mon, 05 May 2025 18:30:59 GMT  
		Size: 13.6 KB (13591 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:42123a596f6136230ffdf48dee04f0924d645eb8baaddc52dbab8ffb4b642976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250871537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88994d655d82321adf17100906f48cc2ae8519dcea5e4ed09b7ba19cd57e81ae`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3772178e2ced5c18004c67a9f500c7ad2e8b10841d86432905ba108d473bfa2a`  
		Last Modified: Mon, 05 May 2025 18:22:53 GMT  
		Size: 216.5 MB (216530699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f348f99ec73e30b69c6b15187ad5cfec437fb13d39d5f73f4bb3738c44de27f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2489734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab671f78ea7e657162d4e4e0fa43b21dfd7e45e71797b492a3cbd26637bbe83`

```dockerfile
```

-	Layers:
	-	`sha256:14eb423612f1cba9e2c33d95d8b0c533e8a09451fbc34051d7e31feece7fca7f`  
		Last Modified: Mon, 05 May 2025 18:22:48 GMT  
		Size: 2.5 MB (2476288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73e5b9f09b8d9d38128847e429196e01be74f3672943344d462593669c82c790`  
		Last Modified: Mon, 05 May 2025 18:22:47 GMT  
		Size: 13.4 KB (13446 bytes)  
		MIME: application/vnd.in-toto+json
