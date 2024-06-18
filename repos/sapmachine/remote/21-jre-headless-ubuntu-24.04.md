## `sapmachine:21-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:9709c1f9726b2d17f7482cd7fa8ba5af85907d7f6740ec0a5353d9897ff3bab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:70848b155b5869aeea8cddb044c4fb22598fd986ab97ed978e7a88da09240208
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89650043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c07d6af8e6f105ee30fd2a6c0384cf26a02d14cdf597db8bc7d7ee85486401`
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
# Mon, 17 Jun 2024 23:19:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:19:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 17 Jun 2024 23:19:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189673d7a4c327648d4e70b361c2fac212985cf222cca9c1c06720a224a465e5`  
		Last Modified: Mon, 17 Jun 2024 23:31:55 GMT  
		Size: 59.1 MB (59083417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c2a196d0a7f8b85bb29cea0355786cdb15f655244358a61cadcd9e1dadf516e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88080477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33aa8c8b39e4236a4d9407e405b02f35784a4a2ff7f10b97d8b9d0bb24edd27d`
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
# Mon, 17 Jun 2024 23:28:57 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 17 Jun 2024 23:28:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 17 Jun 2024 23:28:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9679e39aab57f45b1725b97542b68cd615b326dc07bd27185e91eedb1ab633dd`  
		Last Modified: Mon, 17 Jun 2024 23:39:12 GMT  
		Size: 58.2 MB (58172497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e3ff6456261065b6d785e52d7b670532c2a66ddc053f28343a613b0776287969
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96197075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7374294b9ad318c18faa8b99d953c4a3072e38796111653cc57589acf333ad2f`
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
# Mon, 17 Jun 2024 22:58:11 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 17 Jun 2024 22:58:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 17 Jun 2024 22:58:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a6b87acc0a568209f5593370b5b6bcffdf1ec82a13216fce26023e6eac0aaea8`  
		Last Modified: Sun, 09 Jun 2024 02:03:40 GMT  
		Size: 35.6 MB (35626958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5be83fa7bc4845b6433f975e0e812a162dba97d7145cda5283b94b4bd673af`  
		Last Modified: Mon, 17 Jun 2024 23:12:54 GMT  
		Size: 60.6 MB (60570117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
