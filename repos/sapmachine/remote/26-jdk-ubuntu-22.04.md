## `sapmachine:26-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:1c27e187c18cd503b012816d8682e065fa451033c6a4ab4d30f1b1edfb86d1cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:1d3d38cb9e6105db77076e3ccb05679dd5bbdc33e686219b27c3803a6529deb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255718021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d0f9441920fc40608bdf8876dd8187ebcbc463548550bf24cdb26a4573b94d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:02:45 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:02:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:02:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fc17ce8ec545eeea52d4a03803012d8cdc57e62699924287c449427a240adf`  
		Last Modified: Tue, 21 Apr 2026 23:03:13 GMT  
		Size: 226.0 MB (225981523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3b3a76f21d05d8e00585d96142785ff36ef58b4106292cbf53c154716d057a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2632323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd9d9857e8bf197ea4b25089a4f091f73aa077a2d581f08ce34a2379df923e0`

```dockerfile
```

-	Layers:
	-	`sha256:5f2a9f5dfa065e09028832a692b7f5429f72ee3f78404b784dc110d7e780c64d`  
		Last Modified: Tue, 21 Apr 2026 23:03:02 GMT  
		Size: 2.6 MB (2620953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1352bf590ac2c680e342e3c5565eeb1ba202ab58871ca6ab249957f8483716a0`  
		Last Modified: Tue, 21 Apr 2026 23:03:02 GMT  
		Size: 11.4 KB (11370 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9c4b3aa18f8b53d5e55a78ebd44be9b0debcf376b3dcd588e6f5a174d5d9a588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251418880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7848960ec6e17fe822afb30251fffc99110a634113adede1423493d5a6b3366`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:04:57 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:04:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed36f6316d00f8af4c4d39c4275965906218e231557c5abb70e193d92419d61`  
		Last Modified: Tue, 21 Apr 2026 23:05:25 GMT  
		Size: 223.8 MB (223812337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f800c74efb1800ea90bafe8ada581df25437b364b3670444fd1c4c25746a3138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2632298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757feffc65a818554ec1657d3e3d701e57bb26fecc5a7a39aee322d68baa376f`

```dockerfile
```

-	Layers:
	-	`sha256:c25e391c13c00a68edfb71c35de17e5ff93000216791540ac6b356b775409f2f`  
		Last Modified: Tue, 21 Apr 2026 23:05:20 GMT  
		Size: 2.6 MB (2620728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa4176e8d875f12b16da2b1c28f6982b8aeb840fb6fcb77d41bfccac7c5b10a1`  
		Last Modified: Tue, 21 Apr 2026 23:05:20 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:67898e2496437480b1a977ca5f21dfe7c5b5e8d7e706c4cb624800af4c5d1d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261778503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af80956d2c6f961fe8bbd4a702dbf19103df15be74757b44f70099994ebe6d3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:22:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:22:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 23:22:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b363f15650e30bb65bcae1712a41375986b5aceede08b5f50fd19b7b8909df`  
		Last Modified: Wed, 15 Apr 2026 23:23:39 GMT  
		Size: 227.1 MB (227130105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5bb86cb7b7e9c1cd97b34c854afd15a3c21ef964a09168e3c90b9d458acb7e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2626671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f778731999e82a833e70a439108dc968241769d62d5d6d832adb013068ca151b`

```dockerfile
```

-	Layers:
	-	`sha256:fb6ba47a5219dd88c5a116f27a2ee1a0c0a1729e097b39740b02b18a64b91128`  
		Last Modified: Wed, 15 Apr 2026 23:23:34 GMT  
		Size: 2.6 MB (2616585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82c9d6cd11b79e854e6a0c6ef800c574abacb3bd9fd84933c6c9a7e1f2048cee`  
		Last Modified: Wed, 15 Apr 2026 23:23:34 GMT  
		Size: 10.1 KB (10086 bytes)  
		MIME: application/vnd.in-toto+json
