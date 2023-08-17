## `sapmachine:jdk-headless-ubuntu-11.0.20`

```console
$ docker pull sapmachine@sha256:1e174835e47d44f2f33efa64b669acd4b6c03289bb6a0274d39d03072fc15bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:jdk-headless-ubuntu-11.0.20` - linux; amd64

```console
$ docker pull sapmachine@sha256:dba272aa4e0e05bfac6d092229dcedfdd549e379193baba074aef0519994fb55
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229471476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f9eab6f71350eddb08e783932e43c0e4bca0bfc722cdf4b957ea4d4f9227e7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Thu, 17 Aug 2023 08:00:39 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.20     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Thu, 17 Aug 2023 08:00:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 17 Aug 2023 08:00:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16498cc6fdf11e0acfb8cb17bbefc8ead50afb5fd63b67feafed3f3cf9f0d33a`  
		Last Modified: Thu, 17 Aug 2023 08:06:56 GMT  
		Size: 199.0 MB (199033516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jdk-headless-ubuntu-11.0.20` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a806d44f3f72e3c36d8d471f6771d81e5ec84be1470e368df0babb5606fafa93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.8 MB (225815580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89259eaac783bdfc4549800d44b34c4a53b603f2aac26e90e5b718faf149708a`
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
# Wed, 16 Aug 2023 14:52:34 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.20     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:52:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Aug 2023 14:52:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135eb47a2ab0bb73ee17f95459e8c54a5818bee5900dbbb486e3bf306c06ba59`  
		Last Modified: Wed, 16 Aug 2023 14:58:38 GMT  
		Size: 197.4 MB (197423677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jdk-headless-ubuntu-11.0.20` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:eea58796a85c88f0a3b70918c8f94513c7023f06ba70f32e5c2e7f6112cd42bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221137002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84f273770c467efcfebce3c4469346b7b759f05127c3a9e3ede47fd0f48de2e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Aug 2023 04:56:16 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:56:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:56:17 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:56:20 GMT
ADD file:0e9b840e6824ee009acbddc2d337fd5083ebe606393cf7532cdca4f108813ca3 in / 
# Fri, 04 Aug 2023 04:56:20 GMT
CMD ["/bin/bash"]
# Thu, 17 Aug 2023 07:33:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.20     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:33:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 17 Aug 2023 07:34:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:09f4821f68917c7929419fff8bc583c406640180ea7d58eea03a95e463b8fb21`  
		Last Modified: Wed, 16 Aug 2023 02:15:01 GMT  
		Size: 35.7 MB (35712693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d680e8abc1762251667fe0fe4d75f9a34e725015555cc6a13292ad5f5dbcd32`  
		Last Modified: Thu, 17 Aug 2023 07:45:43 GMT  
		Size: 185.4 MB (185424309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
