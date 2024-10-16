## `sapmachine:21-jdk-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:ad895972609330059e44601883b55236f7c8228d26fa1d5296f31d5d891b12cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:01b2af99a8a4bf274cb9a2baa57564b2b5819237a3d3473906448b03512d7670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244693663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60d7629fd965c4879db48a256d2c2b840f804073bc40c8eb9ab71bb9dd97ab2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:48:01 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:48:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:48:01 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:48:03 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Fri, 11 Oct 2024 03:48:04 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aaa23153623b401fb3bca350d1d240a71d763ebbcb6eb111d396eb6384ff18a`  
		Last Modified: Wed, 16 Oct 2024 18:58:44 GMT  
		Size: 214.9 MB (214943300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:26745c2be3c1ca8b7682a932efb03719012aaeca92fee81792751c5a4ef65080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404dbeb461b301076a022c036625ef54ada5bac73eb613d0109e10adc89037d3`

```dockerfile
```

-	Layers:
	-	`sha256:e84b5ed7a124c35fbf64819d71c28d31312a97a763ffdcd24ec695218d6a0872`  
		Last Modified: Wed, 16 Oct 2024 18:58:40 GMT  
		Size: 2.5 MB (2458818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b24513a9f12b3babcf790971e80ea30ea4ac08ecd3a7b659be0cf7bbf936bf8`  
		Last Modified: Wed, 16 Oct 2024 18:58:40 GMT  
		Size: 13.1 KB (13103 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:93fc0939dc45950bf0f4bfe34535df6f12c058a7bc8129e207e0239d511d9195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.0 MB (242031088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef86534f722f2de0c37bd79fcc6cd85913e8093629cf451e44e5a0f41444cf1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:52:53 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:52:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:52:53 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:52:55 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Fri, 11 Oct 2024 03:52:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc45ff638ee9e59ceb59f19373f43e1f98273ad52605d304c664bfdd06cd8e`  
		Last Modified: Wed, 16 Oct 2024 19:13:35 GMT  
		Size: 213.1 MB (213145243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4740cb16ddcf416fb8475d2660d24437371e8c82117c6f13076cdf575ad9799d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba97ba797f6c6d1bc1fb0abed66634a2aa88d15f9afa351b2ccfb9836cb4302`

```dockerfile
```

-	Layers:
	-	`sha256:26803d7bdd3c7108ce4ab05fa39d096d34e5c63e2a166a04ad9c735793473ae0`  
		Last Modified: Wed, 16 Oct 2024 19:13:29 GMT  
		Size: 2.5 MB (2459453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cf6aa5779bffd5222fd9e6ff3baa631b5c2be79db7ec18feb9dd6b4eb5cc3c3`  
		Last Modified: Wed, 16 Oct 2024 19:13:29 GMT  
		Size: 13.4 KB (13369 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2584aa41203d589cf4e71ff038b3dd0c5d7e462677f77f02950c79e57722e649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250783022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221e1d71720a98c45c0750e3faead1759d8090263b838ca39f6715a820f7158f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:51:17 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:51:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:51:17 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 11 Oct 2024 03:51:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Fri, 11 Oct 2024 03:51:21 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295c52d723d16e285482342faefab879201e31cb7e7c767df345c8887f75ee2e`  
		Last Modified: Wed, 16 Oct 2024 19:25:02 GMT  
		Size: 216.4 MB (216394053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d3407b93de9ac12652923c7b8708219e059bec81bdbf57810430a83fd8c84b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2474115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f935f30baf7a83bb25b352043a23b3626a98c54348fcfc207d8265ebdc78e4`

```dockerfile
```

-	Layers:
	-	`sha256:217f496648d2a7b2e52760141094ce155593c097b3319441f957adcd9c73c340`  
		Last Modified: Wed, 16 Oct 2024 19:24:57 GMT  
		Size: 2.5 MB (2460890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae88c5d9b073095c25b5e0d7dd28500cdef5eb70ff545fc6676f68c1a4fa3be8`  
		Last Modified: Wed, 16 Oct 2024 19:24:56 GMT  
		Size: 13.2 KB (13225 bytes)  
		MIME: application/vnd.in-toto+json
