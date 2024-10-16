## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:e4e5dbd72a194cd1cab9f0fb94a1ee64b3046eae3ad5e6145524cc2620b6edcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:1472940bebe5ae0f3f08b14d27be753737752c5998efec263ffe659adbb8c6cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.3 MB (252284282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2921f6ed87587d40c00d6e5e5aeda37702f5357414057e848336de76ad4e40`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337d89d178e9798a7399a0e2265c51ed3fb09e3339863584dfc52a6c3a3abb03`  
		Last Modified: Wed, 16 Oct 2024 18:59:04 GMT  
		Size: 222.5 MB (222533919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:latest` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7be4111d4a572d393c2b71796e026ac2a2a4726c50e51d66fe7ceb03d8fa4e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2473794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fa1fc0569340c01aab5edb4f64f25c56ead84beed252235a5c2f46d42b7897`

```dockerfile
```

-	Layers:
	-	`sha256:d604f3a69f3137dfe8a7ff77a51b2f387a9b934d897c3e8c4f37adb5339c635f`  
		Last Modified: Wed, 16 Oct 2024 18:58:57 GMT  
		Size: 2.5 MB (2460725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5de5b182382b29e7f84ad17bb432b929f07ef291143c76ef9a056213718e3db7`  
		Last Modified: Wed, 16 Oct 2024 18:58:56 GMT  
		Size: 13.1 KB (13069 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:latest` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:254562debe8c5dd62a9803cc1e33b4a0fa6bf1c26ea80dde7e39254cd54d3af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249403272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6055b29f70840ce323cc08dfe09ad3cacb1dcbda09f157fca551c7ed780939d2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eeef27d15eb0de1a2843de2a60ca495828be93f7a46641dc5990d8f3ce051ea`  
		Last Modified: Wed, 16 Oct 2024 18:58:43 GMT  
		Size: 220.5 MB (220517427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:latest` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eed2d64c4fdf90f9312679890717fe166ec2aeb36cd6d012338837ff24c1719f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4769faa4a8695baa7ac78fbd98b836f14560075baddf761c4a4118a1ee0dad`

```dockerfile
```

-	Layers:
	-	`sha256:76eccfd49873dbb577d51811889e87dab85d564933b68d8b1f390885c39746a8`  
		Last Modified: Wed, 16 Oct 2024 18:58:38 GMT  
		Size: 2.5 MB (2460729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d99afc952c23e95e155bc4bafe86b32d14816597592096a4d4046b1c0d677c7`  
		Last Modified: Wed, 16 Oct 2024 18:58:38 GMT  
		Size: 13.3 KB (13334 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:latest` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ae8d3f5783e2c24fd8f0e6bec8a21d93abb86015d132690de2d18fd1559c85a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258071078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b45f39d31f0336f29fed73baf33072742707419483b3c7d25ada144653f372a`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750abcfad739c02a09e3c6f61e6cdea4270ced245042f8eb08f90c778ff8282e`  
		Last Modified: Wed, 16 Oct 2024 18:59:14 GMT  
		Size: 223.7 MB (223682109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:latest` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6873578cd2b5e2163bfe6590b64b1d199fb3a4423ab8db43d42492ca5b8f1908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a018d41e925c390799b85ea4ead8040fcfdf0a875e78ccc0958d6c5e67955fd`

```dockerfile
```

-	Layers:
	-	`sha256:da34cc5f18b68ae5809ad1efd6ce0038ad4913095cb5ee674d2c7cef8ac6ea7d`  
		Last Modified: Wed, 16 Oct 2024 18:59:08 GMT  
		Size: 2.5 MB (2462178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52754fd9b96317e15adac4185255024440aa3dc629e17076a756250a5bd6765`  
		Last Modified: Wed, 16 Oct 2024 18:59:08 GMT  
		Size: 13.2 KB (13189 bytes)  
		MIME: application/vnd.in-toto+json
