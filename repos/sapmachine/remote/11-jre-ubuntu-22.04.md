## `sapmachine:11-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:ce141a84aa5d5c047a543deb4cc688c702f63830e01b8301b717b97fbc724eb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:6e8f231f0a94977f6bb298ade9ac88040f352d4d56d35cb1a2048c05f3a9f34f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79472447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4be5403ce8706e12c8dfbf79de55cbaf3f87e437c91725a84f4a18849947672`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780924d290b34498ffb97bd726a45b75996fec5f9794a3f88dcaf57f2828e762`  
		Last Modified: Tue, 02 Jul 2024 03:32:09 GMT  
		Size: 49.9 MB (49938392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8ca50e701967b65449e6a3cb97138ab5adc6f0ad4b983034d8b6ccdb2203b93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58791fc6c47e9de57b6c29f8d732ed2645096aa2c6dbebd6ae698c5ba0b17256`

```dockerfile
```

-	Layers:
	-	`sha256:1c2fa3054860f4e312671af5ce21d2d0ac3ad951265c27f1e187f15ab7a06502`  
		Last Modified: Tue, 02 Jul 2024 03:32:09 GMT  
		Size: 2.4 MB (2370748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b0ae96738dfcb7883616bfbf938208641e274434cd1ee6fb08f977c28dd8a9`  
		Last Modified: Tue, 02 Jul 2024 03:32:09 GMT  
		Size: 8.6 KB (8585 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-22.04` - linux; arm64 variant v8

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

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:11-jre-ubuntu-22.04` - linux; ppc64le

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

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

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
