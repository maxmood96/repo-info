## `sapmachine:11-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:70f68cece540f8b64654bd383027b2887d177632f27a4639004072ad294db595
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:7db417494bba678692d7a869ef7d73f06c19aaafd982a9deab45da34eb98d254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79490972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938af1bcd560af10c7ce39453a2eedd266ab60234b2eec6ee8413d4d7247d1b0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862f89c42d81f3e94179c7f89fd58d6f726fefdd953a4eeca1063f434ef3e12b`  
		Last Modified: Fri, 19 Jul 2024 18:00:33 GMT  
		Size: 50.0 MB (49956917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1561afcff2227771786435d3e969ddc31fbaae7fcc92e4f2e0f1e7737b178536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2407494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3f9db95fc2b92317cc7aef4beb1db6823c46e0bd82b3925c93008c9fde6b00`

```dockerfile
```

-	Layers:
	-	`sha256:22cb1b414f0ab5f4bf256184a189eea569db18d8137b4117c48ee4e271daac27`  
		Last Modified: Fri, 19 Jul 2024 18:00:31 GMT  
		Size: 2.4 MB (2398928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48881a4d30429497c8428a6373f777ebaa0eb903d2589f6d52cfd91bf8012002`  
		Last Modified: Fri, 19 Jul 2024 18:00:31 GMT  
		Size: 8.6 KB (8566 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:76348c31e93dcfc9130ce3bc35b7eb0289d7e7b384ae72ef1dd205544a2be205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76575541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ee02481d8f79350e477043d32100c27aeefd84dc8c5f7bdc7e614d364ac005`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2bc664c06313b50ae5d3c2df995fd3dc824362efdf42c4531b5aeba09233e2`  
		Last Modified: Wed, 03 Jul 2024 00:08:04 GMT  
		Size: 49.2 MB (49215516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5341db938adfd1e3f3b4026863ef4520f7c90eeeabb8c20ebbc26a26158c722c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d70cd7c4e4f00333f2476a2c575709d8476721d7a422540c7abf74068c45b34`

```dockerfile
```

-	Layers:
	-	`sha256:b4bdb88f77c21e1b633d080040a1b9f7e5c598015f491e09cc61dae615de7483`  
		Last Modified: Wed, 03 Jul 2024 00:08:02 GMT  
		Size: 2.4 MB (2371056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6abe380839eb7e342c442f5b9e991ae0be049e2dca73becc0014b8063899d0a6`  
		Last Modified: Wed, 03 Jul 2024 00:08:01 GMT  
		Size: 8.9 KB (8886 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f6c31eb3f10e1181258295f927b3d88a28ef5363c6ffdbf7f8236dc49e45d9a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83025500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf87bb33449ce5523628cfec10580791322a12ea450aa714fa85901279bd630`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20722ab1b9610b0cf5951c817f767ae1ec98e508fffb05c8532c7d08a053ee1`  
		Last Modified: Tue, 02 Jul 2024 21:40:22 GMT  
		Size: 48.6 MB (48564419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1e501a435fc371e5849705443bddbad4483b9c2004328c7000ba08726c0f4f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d43de420f4577c1bdf412e822ca87727c2e7686c4915f2424d1580e956593c9`

```dockerfile
```

-	Layers:
	-	`sha256:077e42979f3f421b5cd54a2fd1cabb14c348bd1cff4a3de24aef3b12b32593a5`  
		Last Modified: Tue, 02 Jul 2024 21:40:21 GMT  
		Size: 2.4 MB (2374733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af8bd5090202e16694d48de339f3b75e0bc369accdc259eb271abaa8e8aebbf6`  
		Last Modified: Tue, 02 Jul 2024 21:40:20 GMT  
		Size: 8.6 KB (8623 bytes)  
		MIME: application/vnd.in-toto+json
