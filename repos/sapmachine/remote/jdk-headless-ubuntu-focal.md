## `sapmachine:jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:ee6198eba1fa0e5949949e2ea0d1db7a04ea5a1301c9db7c7c69ec29410e99e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:147537739adce2a297c82cad58b6c92e7a5c56463872e8f738d5735c5796b5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247654942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c124e462392b67906ddf555403b90c73b45c78fa9b2f34c9b2a81d2dd0d70e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55b1f37bbbfeaa5e09c91d4d48dee50adc1ad2109f24ba1c3b21d59244b6b25`  
		Last Modified: Fri, 20 Sep 2024 16:58:02 GMT  
		Size: 220.1 MB (220143173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6f9421e5c2c18423b4101226142f85c78b0c405d4a468e377d5574894772c859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 KB (11065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c076736d244b8d85904ef06873edd3ebbab6f5b5c78d32692f443e48a49bb498`

```dockerfile
```

-	Layers:
	-	`sha256:638341240e196e3ddbaf11945200957fcf367a8263a50bda94b98846367e85fe`  
		Last Modified: Fri, 20 Sep 2024 16:57:59 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd2dea98c4df554e7ddf6c7e1d37a1103dbbc4c52a4bea3812f9bdfd13e1962`  
		Last Modified: Fri, 20 Sep 2024 16:57:59 GMT  
		Size: 8.6 KB (8634 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8a393bf993f80b1665e8d0632e4eff1a709673139b0f0858b87c2f0ed21512d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244091180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16467f4d8dcbe4ea7eefebf4630e0ff44408a7fc368272ad4e7b837b3f33ba37`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a346293ef0a30c3768a8f85e9deb7b870f2529cca14e91f690fffc1a849f7b`  
		Last Modified: Fri, 20 Sep 2024 17:12:35 GMT  
		Size: 218.1 MB (218116963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4329ed989c878ec9c845314e710fe3893a4353fff9392fd03d149a7269a2caa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6e7da21ba5ec9fe8d532f397a6070a591c14648b47c8098a175cbb81e05b73`

```dockerfile
```

-	Layers:
	-	`sha256:e90032c2516a7db08dff06d8541ae4921745bf289a586cd307859936d82b42db`  
		Last Modified: Fri, 20 Sep 2024 17:12:30 GMT  
		Size: 2.1 MB (2128795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c073c8b1a6a0217f9a8ebfc8cf228a3e21e0f4d6f676b0ada24d590a9efdebfa`  
		Last Modified: Fri, 20 Sep 2024 17:12:30 GMT  
		Size: 8.9 KB (8935 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d9824fb7cc07f1d3f1607031242f54e7b99b60bcc9c37fffa4a0591b6f596932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252659137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:174134163465d91a3c594fde4f1baee581285459d93b233f8f33e57c84fe479e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dc326ec944b7858d5d87a7b0cb86c8d0aacc5f789574834b5e1a503f685abba1`  
		Last Modified: Tue, 13 Aug 2024 10:24:07 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c402d8e2262b26cc0ac2595aecdf00d9076c68bfae983abb66710659c70a725`  
		Last Modified: Fri, 20 Sep 2024 17:17:30 GMT  
		Size: 220.6 MB (220581997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6a78e6f9e96cb700636f7d406579506f4baa48bf0faca96f78c9e457e39c1ce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2d33b1be96126498f8ef211dee150f664a088b9ab63d37caa55b6e470d760a`

```dockerfile
```

-	Layers:
	-	`sha256:95ead99021c273b8332245fcb4b295e8e35af71a9f3cd9cb4f910f66283184b8`  
		Last Modified: Fri, 20 Sep 2024 17:17:25 GMT  
		Size: 2.1 MB (2130933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460d4d97ed384d0a31a3bedd533b382af268013715bc365d2c3dc5dad7fe202b`  
		Last Modified: Fri, 20 Sep 2024 17:17:24 GMT  
		Size: 8.7 KB (8672 bytes)  
		MIME: application/vnd.in-toto+json
