## `sapmachine:11-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:7e366e5ae18f83b5208a07a2dc505e64cd239e3458f0d46f74c651956071c881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:11-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:1635fa319ad5ae88643d59082b734038afaced40fac36a84d976ef6c27845fd9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230462982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b72314b874e27f6ef75f4c1ed63fbe161379ab5e327e4de73e0609c2a070b3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:23:50 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:23:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 17 Jun 2024 23:23:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51ce3282305532bea89368e5f714e6302802bdcabee381469a5e1af24b0e615`  
		Last Modified: Mon, 17 Jun 2024 23:35:22 GMT  
		Size: 199.9 MB (199896356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c408d142e203c54e2d903ca082f6b8392357b04c8eb15722a0d137768d7c10e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228308174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b638f06a0f20f771c6b4bd58700c40a59a2c0fa9fe7c3b77b2efa5317dbbac4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:31:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:31:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 17 Jun 2024 23:31:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e36771aa55358fb82405695b9f13c50bb5d6d8647c3ba3d8451201dcb037f0`  
		Last Modified: Mon, 17 Jun 2024 23:42:26 GMT  
		Size: 198.4 MB (198400194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:11-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:295413912f93011206483693be8fba66b88aeaa464ae6cfe9937ec4407f155f7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222108804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde329c8bfe57c7c031c70b46cead90969c3fd038fa9ea5ec6387835b5754f68`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:04:22 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:04:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 17 Jun 2024 23:04:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d379a2c77e61a4478a0dc07a23dd3b6ca006c7f436a2b5678b3279cc7715097`  
		Last Modified: Mon, 17 Jun 2024 23:16:30 GMT  
		Size: 186.5 MB (186481846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
