## `sapmachine:21-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:8568a657e36e2ad36e8922bc7281bf8982829b986326c9c83a17ec18b0841658
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:0319fd8c298a7c60879be23745f90ff601786ee6c4cafb1e63a3f0e62daa51a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244748264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf60756fae3d946265f75c5f6e081f34dabe332e91a88ce814d4e8e43d80b58`
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
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4da0bfe524222540c1c3948571d2d26896d1dd7ee1df7838464dd2032e9b3ee`  
		Last Modified: Fri, 19 Jul 2024 18:00:33 GMT  
		Size: 215.2 MB (215214209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7d559c55796314ee0af16108779e4959feceb7f9ab049be4f0512d28e2c6fd32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d82f7e9470f1630d148efab8a912d0c4911fb15567a586b702e0f544580192b`

```dockerfile
```

-	Layers:
	-	`sha256:3206f5df28b03a694f2337a29b5c53298b6031cb606d17dbf2b740800f3b2977`  
		Last Modified: Fri, 19 Jul 2024 18:00:30 GMT  
		Size: 2.5 MB (2475042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff026d67fbf337a3ffaa1a91e86b45eea3238f8b8fd9a374a8efdc5ef8a3e06`  
		Last Modified: Fri, 19 Jul 2024 18:00:30 GMT  
		Size: 11.2 KB (11191 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f0942c58a167f78f227878fb005027d7ecbcd7426bbdda3adf55d4c0404e08e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240622524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84bf8a8065cb1a8b807907107b38a1d590b70602b136b4f4f34335fce7f7391`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bde8ac9850bb94039de00a3532b84f8ca3d4499cc0be8f465c3d5ddfc80d55`  
		Last Modified: Sat, 20 Jul 2024 00:12:53 GMT  
		Size: 213.3 MB (213262499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0c9d42e5d446adb28be15a485cca1f3e72658daa476de65f4e1954a271edbc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4f115c1751d54591dafaf32c38d580730b68654eb782cf850b7cc0d19ac5f3`

```dockerfile
```

-	Layers:
	-	`sha256:3f3b623fc100a2d3ad1dce08a91f117552718a56ae01fbd3b52b99bba46baf34`  
		Last Modified: Sat, 20 Jul 2024 00:12:48 GMT  
		Size: 2.5 MB (2474818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eac847dd8894fd67a4f1de7f72ac04d2eb4cb742b021c73ab804f02fa3c2c82`  
		Last Modified: Sat, 20 Jul 2024 00:12:47 GMT  
		Size: 11.6 KB (11588 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f95fdd31991e8b2cb7439a2de9899863fe9bc63fce4a449dabb8fe6c3ff70b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (251003446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d092682d057e56818a178e10596a5e2fd57b3f4d988f085fe96f14e7d040b06f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c0432fa392e916a71d0fe080bf7a4fafb99f8ac470102a5cc7ac285e56781`  
		Last Modified: Fri, 19 Jul 2024 23:17:55 GMT  
		Size: 216.5 MB (216542365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2bc4f43a4585d01145b7a715cb002bfc270a34e0bbdebdf812bf22072b2eee06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc64f28367b814f161c5b5611a18fba15c58b266c833dde71e73f2acd8270660`

```dockerfile
```

-	Layers:
	-	`sha256:eb039f39327c0a4075da8792a98c3d0d7858588c2cc410d50ef32298a6b41fdd`  
		Last Modified: Fri, 19 Jul 2024 23:17:50 GMT  
		Size: 2.5 MB (2477120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa3922c5469ff9a484930d2c4cfcf3f5b3ae3cc54c0b642ba4f34e01fd096afc`  
		Last Modified: Fri, 19 Jul 2024 23:17:49 GMT  
		Size: 11.3 KB (11277 bytes)  
		MIME: application/vnd.in-toto+json
