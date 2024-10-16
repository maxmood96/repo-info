## `sapmachine:17-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:893192194f377ecc251a8355285576c3865fdb5d796666d36ecd0697b8250ffe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu` - linux; amd64

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

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

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

### `sapmachine:17-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e71f86eb07ac551ef5368ef7e4f843f03674d3fe83c352fa9c5c0aebe4bfc9cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226616952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4136132d25e89bd4cfcc2ec712b6791f72a389fa6ca33506a32380f1b4ac265e`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.13     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:9593d96f368896d95d7111ee1051e1c409938e8aedb495ea15b6996e6826b836`  
		Last Modified: Wed, 16 Oct 2024 19:29:29 GMT  
		Size: 197.7 MB (197731107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9268215f8d75385d84957111d41c8186fff04e28d50e2165a6922959637f3ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2227008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a87b8f92c7c08bbe6fc3c212d96336cb3739cd35ebf3a82eb25b76ffea3a31`

```dockerfile
```

-	Layers:
	-	`sha256:79416ceab0ae61654b41cfab04a019e24faa0f02cda3753cb9ba9f6e598a9b3c`  
		Last Modified: Wed, 16 Oct 2024 19:29:25 GMT  
		Size: 2.2 MB (2217483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdfbe2dad3107e084f268995d6c4db0f2349e8b6ee5f1b52806d069577ebcfae`  
		Last Modified: Wed, 16 Oct 2024 19:29:25 GMT  
		Size: 9.5 KB (9525 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu` - linux; ppc64le

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

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

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
