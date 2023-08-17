## `sapmachine:jre-ubuntu-11.0.20`

```console
$ docker pull sapmachine@sha256:f5ed065014d374e2fdd766744b45827417beadfef70d7ab00bb28c04b401afa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:jre-ubuntu-11.0.20` - linux; amd64

```console
$ docker pull sapmachine@sha256:18494e615ccc3658607444ab0aeaf2652bcfd32f8d0ec477ac151c9225f70936
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80142983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4071e1591c63b535004a5263732c00e9d682221c91a5eacbcbd50a83d4c68be1`
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
# Thu, 17 Aug 2023 08:00:01 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.20     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Thu, 17 Aug 2023 08:00:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 17 Aug 2023 08:00:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19174274be4365b5dcd7b77e9ca87517e13dc52207451b5e527ae101402f9286`  
		Last Modified: Thu, 17 Aug 2023 08:06:33 GMT  
		Size: 49.7 MB (49705023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jre-ubuntu-11.0.20` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:57bbb8c21332c1a916d57b176ac88edef3a1bf1dd5b04754dd8fb83e470ddc30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77334799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47596cf46c59da5d791002162a4323d557bd1de5128801a1b88aff41913c3d61`
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
# Wed, 16 Aug 2023 14:52:00 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.20     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:52:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Aug 2023 14:52:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf75c9b366bcd5a1dca59596144248dc2c11bcd67fb5a40a1d0d93c2e090a69`  
		Last Modified: Wed, 16 Aug 2023 14:58:17 GMT  
		Size: 48.9 MB (48942896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jre-ubuntu-11.0.20` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:67ca8eddc893e3a27372100ac865cf2f1c1414c220fe6867af238208f7d0f4bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84003809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40afbe595e98e68f8d2c4e35f2f2c8a0fd8b24f6bd22940bd735be2bb36997fa`
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
# Thu, 17 Aug 2023 07:32:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.20     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:32:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 17 Aug 2023 07:32:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:09f4821f68917c7929419fff8bc583c406640180ea7d58eea03a95e463b8fb21`  
		Last Modified: Wed, 16 Aug 2023 02:15:01 GMT  
		Size: 35.7 MB (35712693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e751b9b5c54983a2ce50dda52b3532290a4a5ea9385d953856b20e3b2c9a9b14`  
		Last Modified: Thu, 17 Aug 2023 07:45:09 GMT  
		Size: 48.3 MB (48291116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
