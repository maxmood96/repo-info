## `sapmachine:jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:a4f7ce4e30afa75b9c04c7944751b1378bbb1fc6c5d857d442ebdd487a389527
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:fbaf75f82250318f5eb41b2d1266455641d52ae8243237eaa432f945c9a9a78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86835887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a50686f2042906d0af9f34aa8b4fc08bfb3ad8b308b02c4371419800b87b84`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3fc03e5dab1a916072a8062b8e975dd9bb3ba03c7a4c72270482245a7c73ad`  
		Last Modified: Tue, 28 Jan 2025 01:30:00 GMT  
		Size: 59.3 MB (59324827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eb7419e50b43a47eb3fcd6173d3d790459a1fd23c977106582960a3dcf36aaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffed98687f1f13684ead89797517c04b6eb8fb95febbf6b37e2dbfe5695a435`

```dockerfile
```

-	Layers:
	-	`sha256:9dfb494bee40d0fb53730833f6fb7548b401d59ed4f8ac789c380c9f3dc1a048`  
		Last Modified: Tue, 28 Jan 2025 01:29:58 GMT  
		Size: 2.3 MB (2302383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57f647a65dd00dc29c2de0531eb88d0279d75201c5818b4eaaeaecde5b341ff2`  
		Last Modified: Tue, 28 Jan 2025 01:29:57 GMT  
		Size: 9.5 KB (9464 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9844935d2088f1a8cbe42c91d444786f0638c61ed4b119c712386a452aa4956d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84352020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5c1c5f3a737e3a873b9abc6e9f99839d192bb8c21006c1da885f79e1030fae`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a082204db924226bec2cddb5e77051c0c5fa36081fc8fd73a527246e0a53bbcc`  
		Last Modified: Tue, 28 Jan 2025 02:33:23 GMT  
		Size: 58.4 MB (58378192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c52c441c120a52961e65aeaa9fbe2207baa2f80f0a38a438377931e7986f19ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9098f7c3c007b8c7c5b2be505b6d22be4d794fe8919b723912c85638bba8a7e`

```dockerfile
```

-	Layers:
	-	`sha256:efe41e57add238e5db14bec91c681a8528c8b174acb93e2747b1448712271003`  
		Last Modified: Tue, 28 Jan 2025 02:33:22 GMT  
		Size: 2.3 MB (2301415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9a6eedc630f0c8e6c9fff032ffe8485231df0bbbbd39f63d40dc7f1f075dddb`  
		Last Modified: Tue, 28 Jan 2025 02:33:21 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:668d7a7ebe76656a2c837d9201b01d567e1acbaaf668732dd50f141e1b8d0898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92459227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cac3520eb90bf5ddf238a7df2cfe8f14cbe54a36bff66a99e1f941eaf82a59`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19756a53e5b420918a09c5e886bb63b7c10997ea15b2ecb2a5d371797346729c`  
		Last Modified: Tue, 28 Jan 2025 05:38:40 GMT  
		Size: 60.4 MB (60382721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:25ac74a8be77f20324081eae44beafd3a5504c81e7cb6dc920dfb50a6e77ab48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2315052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdea32c745b1aad739a2039a0f968b34413877a5d8482cca7f4665f54ef4c4e`

```dockerfile
```

-	Layers:
	-	`sha256:f475bb063f872c8750c06a0a63a65a60622f43cda407e3854eb055a37ae7874e`  
		Last Modified: Tue, 28 Jan 2025 05:38:37 GMT  
		Size: 2.3 MB (2305532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b68ed9f4a4f18a4142e640186014585f09bfdf5a44ea823b49de000bd0705e8`  
		Last Modified: Tue, 28 Jan 2025 05:38:37 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
