## `sapmachine:17-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:b2603376102b1bb7f04bd575f351ad98f9b6bd280d36de7a94a91df0c6fbe570
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e5b51d4b65fd68fd3d444908ee0035dd05a76bc6cadbde9975b8adcd54a43a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82656688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cd0d60255b456658ef318caf30b4781cdc6d504f8cd36a8da85a781a1d0aa0`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:fb91467e5fbb9548c5fa9c70b547bcb6b453af9179bf06d411a46fb364f6b9eb`  
		Last Modified: Wed, 16 Oct 2024 16:17:55 GMT  
		Size: 52.9 MB (52906325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8fb84975c8e520f221ea7b5a7ebf3b0fdbb23dbcbc6c8a08451cf77ca13d9919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2136717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af798a2558f1e4fcf12879243fae3abc421e9cc2cbbdf3f6ee88b1b5bb0fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:28f0ad3be10154060002188a979c8837a405db013f7c388d2084fe1cfa81aebe`  
		Last Modified: Wed, 16 Oct 2024 16:17:54 GMT  
		Size: 2.1 MB (2127316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686a17c85cbd377d108255239113fe88819a8c41c03acac0161cb3198f520fed`  
		Last Modified: Wed, 16 Oct 2024 16:17:54 GMT  
		Size: 9.4 KB (9401 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4eeca9429d1bf63c90fa7fd68cbe54aaca25dd890d34eb063cb30bd6e8a03bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81174904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2338a925bfe9abbe29f9b291c3b9409c86eb56ef92f2638e53a30c6b1f9b3f`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:11e7b63ec57d6d416dc44914a7599bb6b520a3fe7e05bd2f8a5310836c58c45d`  
		Last Modified: Wed, 16 Oct 2024 04:41:22 GMT  
		Size: 52.3 MB (52289059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2881e9a658673691bdbfbe7db7ba71d4d05bcb73ac3e59e207bfc247aa79dd6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66bb9bca80be8917a4b2dfda22f13cf53e879bc533bd7038d6d2c3ff7aa604fc`

```dockerfile
```

-	Layers:
	-	`sha256:0ae038715de1555f056e11f1eb14e6aa2589b25948b79bd8c0328d2b73c52514`  
		Last Modified: Wed, 16 Oct 2024 04:41:20 GMT  
		Size: 2.1 MB (2127798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b95d5683bd9f3e64665b277adc5e79032437544c99487313a27767d9ad7f77dc`  
		Last Modified: Wed, 16 Oct 2024 04:41:20 GMT  
		Size: 9.5 KB (9524 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d9e535cc5cfdda58087756376f01a11378556ede97fd9444055b728da1f3c99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88715754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a721cf8c972fb81d074b377d2199f49b89993086a455910a6ea66c790a6a24e1`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:342ae7ccf7127672004426cbbfe6aebe9a768491bd2d610eed7cb3f1a752aec9`  
		Last Modified: Wed, 16 Oct 2024 03:01:17 GMT  
		Size: 54.3 MB (54326785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f886f9da64872683bbae64241336966fa7c4418babe3125b2189b456bc5392fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2140654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6897e211f4ea19d147220aa08eb65940b24335a631720ad753285ad3b209a7`

```dockerfile
```

-	Layers:
	-	`sha256:e2f9a22a0b368a11956ce29b3c4e182d801c9a7e6a2a27d818297cf35a765aac`  
		Last Modified: Wed, 16 Oct 2024 03:01:15 GMT  
		Size: 2.1 MB (2131202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f8e9635da33d37d6a2d5a57e1131310e660f9b007bdf71807cb4b5908778ff0`  
		Last Modified: Wed, 16 Oct 2024 03:01:15 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
