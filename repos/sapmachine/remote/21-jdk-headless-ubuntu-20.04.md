## `sapmachine:21-jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:027552f8c7691c98fed328954267617e805bf802d76be5fd4f2fccb555a78c54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8d55fdd0b4ae5689bfec72a3e8a74fc36b94b6718dee05f0158ffb3cdac3bf4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240417326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72a6fda0ce01c99d17b41a6ead1cae9ed3d8ed1357f6b062aa4cac452fdb562`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c978636deebc0d489e739ca987e70d8c65214b6c2fa7c49cfa17c2ff803a047`  
		Last Modified: Wed, 16 Oct 2024 18:58:56 GMT  
		Size: 212.9 MB (212906266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f2440815ad9260cfb8df6849878d9d252f5ee9d87ea64b70a232b2044d3e7f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2144034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022c6d01c7f8587aa1d2edcb3d3af020fae2ebd074a18d5d782693c517d04818`

```dockerfile
```

-	Layers:
	-	`sha256:48326bb9792f5d834aed10ece037129838d9ef7e42f4a6e78b0323dcfdcf6c00`  
		Last Modified: Wed, 16 Oct 2024 18:58:53 GMT  
		Size: 2.1 MB (2134622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70e33fa2b7f32d6a5697d5c8a05954fc3d0f21679f22ac3dc102a4522792de6c`  
		Last Modified: Wed, 16 Oct 2024 18:58:53 GMT  
		Size: 9.4 KB (9412 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9c430d90dd903bc49a25254b8e77046f252bf6c142f3a688f1b2cc2e590654ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 MB (237062260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70860bcefa7e2764736a7d1ff9b25b2260a1837055fb4ca41273bd6fb050c4ec`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a685e8ffc8a585ba418b32e2452aefd894b5f7e39e1d8062ffcea929271f9a69`  
		Last Modified: Wed, 16 Oct 2024 19:23:53 GMT  
		Size: 211.1 MB (211088432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1820f8138b46a936bfbb3067118c7495c9ae9fe806385340ec0a1c35f7ea72e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2143807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f13727b9e0ed787e49370eb656f06ac838fc0b11833b4c4193409e12d337b4`

```dockerfile
```

-	Layers:
	-	`sha256:406f74ded63c189dda09623401d4dd2eac86d41f3679e45d4f58729c6b623a9e`  
		Last Modified: Wed, 16 Oct 2024 19:23:48 GMT  
		Size: 2.1 MB (2134273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aa2df19fa43fdd3b23d50610c33e4c60cf30a66cd0d0374e7bd12d80b42109b`  
		Last Modified: Wed, 16 Oct 2024 19:23:48 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ba62c7692c56a51dcf04423e269d2ad96af9e1f68a9eb151383f3685dfcf4425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245765068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce21efe9be515a16f571725dfab96a3a200c205e4de6cc8d29c18758dade7e96`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c654b50a2955cd2aea01ed54b88dd3c093437a959906093f5273ee0541d16def`  
		Last Modified: Wed, 16 Oct 2024 19:43:38 GMT  
		Size: 213.7 MB (213688562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38a8d1f90289bc5e9b7f8054b7cc33d04e9ee965ca04ecdbf0194e98af7f9bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2145848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a8495354ec49980cf11067ce3928151b9e7de03f76213c9c43874610f4c5d3`

```dockerfile
```

-	Layers:
	-	`sha256:6b50b1c47c6d591b7fbc805135141e0f8d7f0dced5660f75bd5b483e499b3873`  
		Last Modified: Wed, 16 Oct 2024 19:43:32 GMT  
		Size: 2.1 MB (2136387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:047fefcd41a7c4f882cdaa898c4108c6a7b0fbb27b3d4b97d4cc152f601bb2dd`  
		Last Modified: Wed, 16 Oct 2024 19:43:32 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.in-toto+json
