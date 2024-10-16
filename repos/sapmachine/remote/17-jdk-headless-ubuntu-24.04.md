## `sapmachine:17-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:4c3ecb05b3e39ab426b132ef91f30534785c909be2a1f933cf07e6818b23acae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8ec3a0e3dc1465e3ab73dd6326065a3caa12acb382652730f8c1243fc18ea8b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228998995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a9af936b23d379f16b0e4a6d96b74eee866b72a1c131ff774a448d3a9b4f47`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:0477d251523a557fca5e57785e8fcec205055582e55e9a3366d8b4ac4b1c4c66`  
		Last Modified: Wed, 16 Oct 2024 16:18:12 GMT  
		Size: 199.2 MB (199248632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:389f8c4e75d22d1823c62f6961ecc5e59d8778b85aa6b210d800ecb99b8f4b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2219758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67272a6641b20f8dcd7a0992e6ccbfe28eab78a8de420753183b724660665bb0`

```dockerfile
```

-	Layers:
	-	`sha256:4f1743b353a894b7a5deef150e80383df618768f3de72c30813fedc877a02c0a`  
		Last Modified: Wed, 16 Oct 2024 16:18:08 GMT  
		Size: 2.2 MB (2210355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6078b9ce42261dc6ffb98d4c214ea735ebc3efff65e08cde200949f8a1ddf54f`  
		Last Modified: Wed, 16 Oct 2024 16:18:08 GMT  
		Size: 9.4 KB (9403 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cac57d4d589701876ec60edc284291d350eea0ed9b30d2427b54e72d0c99f005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226768220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a526a612ded8ebd149ceb0abb17de18729679d57381ead8413bc83c4a31d72`
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
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
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
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce2164d48e4f10fdd474d15fcc7f6728b61ef83f227d91890b40ede55f2153d`  
		Last Modified: Wed, 16 Oct 2024 04:39:36 GMT  
		Size: 197.9 MB (197882375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:434cb1bd2b84c0bbaea13062b29ea3e290347c4f0bb3b1056b31799e5936159c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2220362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ce1fcce46a1ad3908c14517ad1fc44682f3311f17b2b2eb7618b80aa5fe336`

```dockerfile
```

-	Layers:
	-	`sha256:0153f044ec07fb2de5097d0af1494c6c8938a22a0004035c92850058cf55c606`  
		Last Modified: Wed, 16 Oct 2024 04:39:31 GMT  
		Size: 2.2 MB (2210837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:320f59d021bb49da2fe1e39f578ae78926cce7c51ca0745fc9b51935b3a2ccc0`  
		Last Modified: Wed, 16 Oct 2024 04:39:30 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:16d1da5047719cb64dd78198064d925a59043f3382b68b4ce7e365316e7c2d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234643532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94ff04da22ad67b770c2d61c7589ed27923423b744d9389831a33d1081b44f6`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:687dd5b125b098392921efcfa77b2986b157df432c5870c98fecfa9fac06d3d7`  
		Last Modified: Wed, 16 Oct 2024 02:59:04 GMT  
		Size: 200.3 MB (200254563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7f20dfcf84a0be0fadd56b9d8e11457bf1dbd75b40cecbf222ae12ec710242f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc081656ede31ddf1b405d46bd6fa66c00e4f5d595d3a00eb915047bd3a43e38`

```dockerfile
```

-	Layers:
	-	`sha256:8c1c8cde6dd673e6c3665cda9b87df855b8a3adeeb062bbf361f9564bdc1dc02`  
		Last Modified: Wed, 16 Oct 2024 02:58:59 GMT  
		Size: 2.2 MB (2212292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eed63baeafbc8dec199bddf8f05086fb4a7ad05c8905a9a9c889f8df2cae1686`  
		Last Modified: Wed, 16 Oct 2024 02:58:59 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.in-toto+json
