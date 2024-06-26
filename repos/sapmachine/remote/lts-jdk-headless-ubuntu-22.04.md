## `sapmachine:lts-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:4dd7acc809c01ae154f17e98627a931b9167763f341d3b1d94f355d2c612110d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:1728dc292414adc87a0ed599a71e76d9d6f1956e2ceb434b6b61579b2c4c5aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243394314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d74303314e72de5f86dc37bf2d64b1b4c515e13abecd8aa19e0fd79dd0bad58`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68398e083057ab99d220003215fe63a1d3148f7d69efb3be2e7ecff80e4fef04`  
		Last Modified: Tue, 25 Jun 2024 22:59:00 GMT  
		Size: 213.9 MB (213860560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0a1b0a44e7e4911c863cee540c2df4039ee2c620bf7a96942ed184ca3139e8b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e041ae50e26045502f81d83e7b891c1add7656a6a15dd48c66c3620316d28a2f`

```dockerfile
```

-	Layers:
	-	`sha256:de478dde3812c34de4348e235155e6b346d23ff750ae624ef7d6399eb19af413`  
		Last Modified: Tue, 25 Jun 2024 22:58:57 GMT  
		Size: 2.2 MB (2204375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c39c9c276445346efe071e7fe5466a62d215de6e62ea100bd1d0e42a708b7044`  
		Last Modified: Tue, 25 Jun 2024 22:58:57 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:834427b31c285cefe8cfb232c8779eb9ac9fbc477133a1e781a9fd0dad9a5f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239268181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa37410d575ce7da1542bba013a4152051f16724719b2ce6d5beb194b01eb9a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22c20abd463383fcd096f33708e463f18c5ba7bd7dbc1f865eb278878cfa6f5`  
		Last Modified: Wed, 26 Jun 2024 00:08:06 GMT  
		Size: 211.9 MB (211906399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:99509b487e51d8cbf77599f03ad0e4b0eba75ed7a4778b3ce674f0b19ea50fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e919f01a87fd35e9124458f5d15a4f85d1b864d50c210e0fb14bb9784c25af`

```dockerfile
```

-	Layers:
	-	`sha256:df528925196af3a1a9efb977074aba0d00749cdd64f994046b84d3d0b8900b74`  
		Last Modified: Wed, 26 Jun 2024 00:08:01 GMT  
		Size: 2.2 MB (2204069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24af71df72c9daf786a65038f146226e6bd76ed047f171bfd3df60fb8056d840`  
		Last Modified: Wed, 26 Jun 2024 00:08:01 GMT  
		Size: 9.7 KB (9717 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7898754b8f2d15773bb228e6aa6914531e4d08dbae6464cedd5d7946532c8a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249462696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731173d43dcdc83671c1bea2a5cdd680cfd5ee2181bf85a60675853bca085954`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a738af18a2008e0390cec80ad3b8a5171bb8c9e1d58c1a41ecb9425ed81844`  
		Last Modified: Wed, 26 Jun 2024 00:35:37 GMT  
		Size: 215.0 MB (215002003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4de502d1f607ccfa96bd2310fb7e6d989444e0923c390ffde74cf373f9c656e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2215789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68d004a027357d988b1a325016b4ba5912df0bf9b4f187d1ed7c98369c4ab97`

```dockerfile
```

-	Layers:
	-	`sha256:ecbcefa1639569e5f5021c6cd9ea7c8968edfdfda009c1e650952f41c777b824`  
		Last Modified: Wed, 26 Jun 2024 00:35:32 GMT  
		Size: 2.2 MB (2206347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a86e7df04e15b05822c94743bc6d3024bb21638065281b37dafe53cd9a0dc6`  
		Last Modified: Wed, 26 Jun 2024 00:35:31 GMT  
		Size: 9.4 KB (9442 bytes)  
		MIME: application/vnd.in-toto+json
