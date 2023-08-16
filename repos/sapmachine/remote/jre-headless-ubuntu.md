## `sapmachine:jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:562b3549eec64e8932bc3b829a13ce0476dbfe6ea6ccd76a4bff5802b169e6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:194520f37c61f5e22853e63b00c37860ec08b56b90b574c9d6cbfee505eb197f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85885269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e3384320d7ebc1e6de0fcd3cb83b7c985f933ab2302fac8acb3e2947cc3119`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Wed, 19 Jul 2023 23:26:33 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jre-headless=20.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 19 Jul 2023 23:26:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Wed, 19 Jul 2023 23:26:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81a152ef46bd68c863ec908ebcffb8dd708558f1504a4e772f97d07dab7aa1`  
		Last Modified: Wed, 19 Jul 2023 23:31:48 GMT  
		Size: 55.5 MB (55454040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e0be55df9e80e7d07f0d742526892526c41901d5610838d7371db418b746a1f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (82994816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a4b7265b70879b34029a09eda9a940c534255c587252216c37e4b724b7deae`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 14:55:47 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jre-headless=20.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:55:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Wed, 16 Aug 2023 14:55:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1032e9253134fb642ff6d9ba8a1d05c07c4c09636d5278020b859a10e70141fb`  
		Last Modified: Wed, 16 Aug 2023 15:00:45 GMT  
		Size: 54.6 MB (54602913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0ae0f4ce55150a787c8a09f055e6834c202219c67ce041a4bcd68fd1d868524c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92551189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8a39a497eab22444ea5eb595fdc3b1d73ba1a0b89c92253d3cc456f4fb9d59`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 19 Jul 2023 22:52:18 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-20-jre-headless=20.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 19 Jul 2023 22:52:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-20
# Wed, 19 Jul 2023 22:52:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ee69a821447e2597fca31923d6996ab4303a8c14e0a55d7b3ebda7536d25ef`  
		Last Modified: Wed, 19 Jul 2023 23:03:05 GMT  
		Size: 56.8 MB (56839720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
