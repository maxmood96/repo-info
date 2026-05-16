## `sapmachine:21-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:c0f8cbf7e2204a3bfdd7e42f1f12239dbb0f7da477c2b97c4c385b2674ea9f12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:2a4287e9be667bef3b939b6f74ebcec375e61dbb6ac599ced636040d14bfd30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244840199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ffb763e51d47c39349b40a678828556892d4376be3550a8791563e4a7a2990`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:21:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 15 May 2026 21:21:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7934fc32305514aaf89eef1b90d477e81a4b439e051beedeeb58dc066673cde6`  
		Last Modified: Fri, 15 May 2026 21:22:12 GMT  
		Size: 215.1 MB (215103515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:40dc216a9bbd649c86096214d3c2b68151c5604c0e351b7a05589d1cd79214c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2389554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17d4e67267f086d15bfdb2bf571d88ebf1b375e21351cfe0ec98569feef8031`

```dockerfile
```

-	Layers:
	-	`sha256:523856a4bf13528e5ec9db7c76a0daec712435f5d24b24fd2553500b17d5581f`  
		Last Modified: Fri, 15 May 2026 21:22:07 GMT  
		Size: 2.4 MB (2380664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d74f5f7d5915b85a33be0a34bc8580b1b43c512b95cb54e95babe832fe5e62b8`  
		Last Modified: Fri, 15 May 2026 21:22:06 GMT  
		Size: 8.9 KB (8890 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9135a90d89eddd0f180ea44c85d982b17c37c17aec01002aa69b51fc54fc5827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240934030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d008f1a062bd539c82de79ce15a62106abaef0449a43581f66950c38b91e59`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:22:10 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:22:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 15 May 2026 21:22:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039407082770d6fe97ecded07e1bafa76ee0f9dd587b3d65988d24603c06e4f3`  
		Last Modified: Fri, 15 May 2026 21:22:34 GMT  
		Size: 213.3 MB (213327407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ed6628c43e657061b1116e3aca3298b476d650ecb118460b34e3302cfcdeb8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2389329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82013bce4c063bea5b2c16c706c778f1cc02419de6c926f2cb1333b3c11e052f`

```dockerfile
```

-	Layers:
	-	`sha256:161107f2ff05c7c44b1ac700fdc14c51f6797d5cf58d77d5e82ec329ac734884`  
		Last Modified: Fri, 15 May 2026 21:22:29 GMT  
		Size: 2.4 MB (2380336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae65104064031a5b5bd00023132e9b4cb0184b7acacc1bb2ee113bdca8dd42d`  
		Last Modified: Fri, 15 May 2026 21:22:28 GMT  
		Size: 9.0 KB (8993 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b5600112359c67ea6b234972ed7648fdaa19d63ef17287d6e0c951a5d17f5385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250542889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc971830157d6f7d6ab9ea10c1fc5cf60651ebb0febf98e6f78426a391b9149`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:39:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:39:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 15 May 2026 21:39:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6a01b44c3e99d2052c275d98fee294d4e86246056f1703c1b1226f485c69dd`  
		Last Modified: Fri, 15 May 2026 21:40:34 GMT  
		Size: 215.9 MB (215896169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e4472d79501f5b872eab8dea74d85cf317d42df1c0845b7505500ae1752d0262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bdc8283ca3e25bc68888b743a8a445b654b716bf0e07f5f3d6f81915141748`

```dockerfile
```

-	Layers:
	-	`sha256:9adde70d93b27a2914504c43a4ed268c02a7e873c7e404fad9234ad5cf2f4bdd`  
		Last Modified: Fri, 15 May 2026 21:40:29 GMT  
		Size: 2.4 MB (2378160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4323d091bdd1ee08c1fb34f05ac2935a3c8d767f2a415d0c28172da3ecf2d85f`  
		Last Modified: Fri, 15 May 2026 21:40:29 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json
