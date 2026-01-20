## `sapmachine:21-jdk-headless`

```console
$ docker pull sapmachine@sha256:49c0732644238fee06a6cd740be81636d2611cba9426726e141c6d6c38593a55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:a0325dc3e61228e57f7162e009d852db90bf4cea05f84815024b5e276e017088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243903513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92cf29e731dc12eb17fdf58c6f4db0bd3fe19d453a694bfe73162b805b9a1e1c`
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
# Thu, 15 Jan 2026 22:43:57 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:43:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 22:43:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 06:35:38 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b5ed5d34c419c436dd7d8e873f57f9b03cbcbf1ecdad48d9e05485c9fa216a`  
		Last Modified: Thu, 15 Jan 2026 22:44:35 GMT  
		Size: 214.2 MB (214177502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4a8046a58f7252d5c50d8407a6018f26f23371858ad6a2e8d0ed10b8e81e3264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5647ac772135b9ba291e28e2e3b7df27daa43a42a5f6469dfea2fa645a6cc906`

```dockerfile
```

-	Layers:
	-	`sha256:3d1ba7f52b0002456e15b186f1d8b075ed6086d964c1823931dd3f886f0fa3fd`  
		Last Modified: Thu, 15 Jan 2026 22:44:17 GMT  
		Size: 2.4 MB (2356343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d1cb5f048eb6ab6a0631f950971e1d973221408a6b330b86e688b53c506df97`  
		Last Modified: Fri, 16 Jan 2026 01:11:15 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8017b504f91b2c4e66ef7c53a402cc834dd835d0b210a4ed90b09a7b2f0ca4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241280292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3385e3bae2eea4133bf6a8d6ad9ba3e33ddfe9077543182c5144d48b944b3087`
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
# Thu, 15 Jan 2026 22:45:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:45:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 22:45:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4091f31513c168dc4a5463ffbaae7daf196d2c3f88f463156d9c63f209c4ed6`  
		Last Modified: Thu, 15 Jan 2026 22:47:43 GMT  
		Size: 212.4 MB (212416468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:879930425201bd941384e04863b03829e7e08f962b4ac35461ef3fe50cdefd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2367223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb02a2c8023077f6639df15e8bad1d8e33ec7d9948d8194406c339613f226db`

```dockerfile
```

-	Layers:
	-	`sha256:7f0333c43347e85fd703d91b4654247523d9c20e6a375a137b5a7a8fef9a9e50`  
		Last Modified: Fri, 16 Jan 2026 01:11:19 GMT  
		Size: 2.4 MB (2356850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814751114997ead97fa001dc16d721c31258bead5fb7fa75fc6a301c6b623165`  
		Last Modified: Fri, 16 Jan 2026 01:11:19 GMT  
		Size: 10.4 KB (10373 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:373301a7cae1c06394fa2ec8d2aaf5ceec748d21a54f0796f5a8d20553a95989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249225973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32d84ae5ff8ba3933b8a36ded142257088409fcd816c3dfd8ae0ef1c56bd7176`
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
# Thu, 15 Jan 2026 23:34:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:34:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 23:34:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 07:12:18 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aac89d16b154a5ae69b81c9f6bbbd0e7e0c6feed220b39302c425b0444bd506`  
		Last Modified: Thu, 15 Jan 2026 23:35:56 GMT  
		Size: 214.9 MB (214919814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:14f75d3fc065c335be8573c001f17fdfe88981316f97c73fbd9727873b7a53e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2362686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4014f481fd641438dca4feb6250fb1a17074fb2694a895a1221ecd4c7d7da47f`

```dockerfile
```

-	Layers:
	-	`sha256:f0759718b0d896e3224a3fd41f633e1c3beced1e76ced9a9d356e0c0d7f0186f`  
		Last Modified: Thu, 15 Jan 2026 23:35:08 GMT  
		Size: 2.4 MB (2352397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42aff358f0b097e73b92866348890310df8a668f99c326eb234c8a5885bd052d`  
		Last Modified: Fri, 16 Jan 2026 01:11:24 GMT  
		Size: 10.3 KB (10289 bytes)  
		MIME: application/vnd.in-toto+json
