## `sapmachine:17-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:38255de14fc81004ac8230e7abf31259cc127a71a32364ab801a8ebe42c8d285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:a81037175b46eb2722ffed6fc572400d65b13937e060dd8b3d5b8d6fdbe47d84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228868463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33e54549a8f71338cd043ae81e649a4f5ec3f7856b07618ffc7e3a489167aaa`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:19:06 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.10     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:19:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 16 Feb 2024 03:19:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9d7fe89a0cfadcc894158ebe42f81c548bde256e000b8dccf65c2319f7f9fd`  
		Last Modified: Fri, 16 Feb 2024 03:26:34 GMT  
		Size: 198.4 MB (198418386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9cd577218035e27d03b70d6480c2e34f203b8ab4ec37e8c8070af6df1c94953e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225416321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedcbb243c367d734f6a3fdd72ec0b585ec81e05b9918806a974672a21f6c496`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 04:28:47 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.10     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Fri, 16 Feb 2024 04:28:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 16 Feb 2024 04:28:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cfada40b1157a4d9d554ed151e3aa6778b6513c6a0b6056a38cf05613b54cb`  
		Last Modified: Fri, 16 Feb 2024 04:35:12 GMT  
		Size: 197.0 MB (197016000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:658c0772d845d0560f39993fa2f4d525f50160b4f0cbf9c8d66e24a55f07fb42
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234929497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf20cda74d8bc08494c5259c2dba30f534fe21531caf49ea6af9a4111a2916b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:12 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:12 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:17 GMT
ADD file:c082e39391784606dcfb3aa7298125fa9e8fe08e83ff006496eac650ad180c35 in / 
# Tue, 13 Feb 2024 10:06:17 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 03:35:59 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.10     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Fri, 16 Feb 2024 03:36:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 16 Feb 2024 03:36:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb95b1654dd508e6f2d1e7103bcd3af75a00fa6826603132794816af5418de7c`  
		Last Modified: Fri, 16 Feb 2024 03:06:52 GMT  
		Size: 35.6 MB (35628838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ec7064168310bb1009fa81029033db7a45d453c3160ad6228dfd9889fd8a8c`  
		Last Modified: Fri, 16 Feb 2024 03:48:08 GMT  
		Size: 199.3 MB (199300659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
