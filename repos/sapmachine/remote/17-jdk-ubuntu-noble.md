## `sapmachine:17-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:b331f9817cba77ece3469fddc8d704afdb66377fb9afcac820bc0183b10dc745
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:6598e4f2dd5d2a7e7c7f6855484c439cc1ffdc91be072de684364768a5a64ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230182172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb8ab87a1f093a4cb5cf99d005e4d51c8387f54fa6121c50dab191c4f7ebead`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189055ea527b73d3211166e2181598fe1089c006fb45d3a70730cd13bee0f07b`  
		Last Modified: Wed, 16 Oct 2024 16:18:00 GMT  
		Size: 200.4 MB (200431809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a2741923e8741732634fc237fff971f58b764073bae7080e10d2284c978122b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31dd8b906a2c4b63557b56e345810665f1aa8465d1c061453f1c6d91840b028b`

```dockerfile
```

-	Layers:
	-	`sha256:e8792242a6d78bcee6e87794a87ac6d0a23c90b7cc7addc46e45d936ae31cbc5`  
		Last Modified: Wed, 16 Oct 2024 16:17:56 GMT  
		Size: 2.4 MB (2448372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acb7235efdfb304eb2d01e8bf71154bcd13bfee4e91b0d7949b199f470b85c2b`  
		Last Modified: Wed, 16 Oct 2024 16:17:56 GMT  
		Size: 11.2 KB (11178 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2bd18f2ad6885f981c8888c0602597dfc2c242e21fdb5aedb108c7a7c0c5716a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227813114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb67578b87dde4fbbf59bb9564d4771e7fbe50b0bc3dface2c07590fdd82e14`
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
# Wed, 16 Oct 2024 12:49:12 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Oct 2024 12:49:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca9ec1316cc93b061ea69c954add2b1e69972aa3ad608b4fc504c0cfbbfe140`  
		Last Modified: Wed, 16 Oct 2024 19:28:09 GMT  
		Size: 198.9 MB (198927269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e812f4cc794d7207e7f852ec4dc215f247743fbbee32f6d74612531865292953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c64be2b1d20068435377a445cf559121531e62bc1638e0d0d4ad06786be7b8d`

```dockerfile
```

-	Layers:
	-	`sha256:20727c01400d534696ca717462ad54c37a0568fd29408137c938f3c561a53e3f`  
		Last Modified: Wed, 16 Oct 2024 19:28:01 GMT  
		Size: 2.5 MB (2455581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b5412da999d99469fe6e09c331374f41e94a01fdaa6a86831512cfce930597`  
		Last Modified: Wed, 16 Oct 2024 19:28:01 GMT  
		Size: 11.4 KB (11370 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e9a666eebfb862935c4fb586d563701982bc4db1b32919b2abbcdd57b75150e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236027044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c54a88305a59b75339b328998d1833b79fe72d9a0a4cb905f8f908c83b0d250`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1202a68e3f29fbcab8d22c69fab7cf9a2fd88acd612d3842fdb1361bde026c23`  
		Last Modified: Wed, 16 Oct 2024 02:57:24 GMT  
		Size: 201.6 MB (201638075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:01b176ffa3a26057f6975c89e2d2fedb3e31448e8f5c720ee756d590976abc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a699f57b06af78bed4e3f62325256bdfa4568ef8a4ebb321539179ff810153de`

```dockerfile
```

-	Layers:
	-	`sha256:1c57dd2350790252e25fbb87ab2b1c8c579ef91f9ece0af1117f5017f3f1b4d3`  
		Last Modified: Wed, 16 Oct 2024 02:57:18 GMT  
		Size: 2.5 MB (2450408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd4886c5c77c83d96793c535f9fb6837543698b3f695394d9e1f004244e1aba`  
		Last Modified: Wed, 16 Oct 2024 02:57:17 GMT  
		Size: 11.3 KB (11264 bytes)  
		MIME: application/vnd.in-toto+json
