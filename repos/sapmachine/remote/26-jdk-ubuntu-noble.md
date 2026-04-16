## `sapmachine:26-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:dcb8a459a1ef9a437123b7f46a7126e3e3ca8938bd13499f6010d5b62286c97e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:ea0c6c9122290bb1bdae0b48d5a03442e73416ef942cca5d27f19ba65e20a604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256091353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64694f4cfd3ea0506715954d7e48461300cc04308d5ccb702d759d55f855587b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:56:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:56:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 20:56:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d26625260ee574b572eae3ebd5a287cc9d461ddfec5b3eb5e0d1c772174a37`  
		Last Modified: Wed, 15 Apr 2026 20:57:02 GMT  
		Size: 226.4 MB (226358375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4376c83593acbca942025a62a75c18075173410263995dfc805b3bc4b2409df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2607038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3f7589439b7cb31d322c1b5c16118407459473e4cdc4d26e1cb494d96962a0`

```dockerfile
```

-	Layers:
	-	`sha256:56d366086a4aea8a99d9f87fc67e16dde9a3851435ad7ab76ea286ddc2f8bc40`  
		Last Modified: Wed, 15 Apr 2026 20:56:57 GMT  
		Size: 2.6 MB (2594558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f2c466f07fabdba4de71b700132be120ea73805381f439418bdc954c0bb7bb`  
		Last Modified: Wed, 15 Apr 2026 20:56:57 GMT  
		Size: 12.5 KB (12480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:35e57a0f12598d20151026c7717bbf1b13f22f5be4f2793bb01ba9c27aefa16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253111081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22157d7b9a86b491ca9831d341def8aff64857a770b798ab2f76351b04c2e89e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:06:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:06:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 21:06:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98811f1f7f1b906ec42bbfac81da12f49a09c9edd0bbea284b80e9cd8a244ab`  
		Last Modified: Wed, 15 Apr 2026 21:06:36 GMT  
		Size: 224.2 MB (224235296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:61ac266d170f7d6b3cf03852f5a3089756c21b6a3175eb6e0d01a3d076374a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2607895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7c64fbca8d83eb7e130bfba05840e9a55a57c8164b9606336aba380f9c9e2a`

```dockerfile
```

-	Layers:
	-	`sha256:646f0606ac051f1b2a333392f8e61634f6abed53cb343ddc66e6b6ac12a5a757`  
		Last Modified: Wed, 15 Apr 2026 21:06:26 GMT  
		Size: 2.6 MB (2595167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bca6e44f0ac65007ab29b34de0566fa21cc16cb4b63d85e97f56b771470b7f7c`  
		Last Modified: Wed, 15 Apr 2026 21:06:26 GMT  
		Size: 12.7 KB (12728 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:43a127a7bd4e76eb400fde3f7060f2cac2354973cca18b895d4377cbc6239d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.9 MB (261931111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbeecf752dd13cae4ad9b950ce0a7841c078121c69f6a43fdfe6508b843eb0e4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:19:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:19:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 23:19:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9664bba08b3d0249eb3c4136e07f8afc48d5b42bcd12525be99e0deb1b7729d5`  
		Last Modified: Wed, 15 Apr 2026 23:20:08 GMT  
		Size: 227.6 MB (227616933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8cbaa4da85b97ff6f47f95a884abe3022d7d599eb8e6b49254d106619c75c758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2604136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2f5fa5cd9dff27a0871b2ef43710594cb1e103c9a00e37812389b03cd4930f`

```dockerfile
```

-	Layers:
	-	`sha256:8a9ea64bcd21246fb7534d1bf7be70c5e89cdc40e815a91d15001c5122b5c2e6`  
		Last Modified: Wed, 15 Apr 2026 23:20:04 GMT  
		Size: 2.6 MB (2591540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40c66fb6cf87db6e0511c4855bfdbd66fd8bd57b63cc4342aed1bcad4c1c03ef`  
		Last Modified: Wed, 15 Apr 2026 23:20:03 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json
