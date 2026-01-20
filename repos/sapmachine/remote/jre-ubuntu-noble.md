## `sapmachine:jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:6e7a2042561e8cabcf02044eedbec54b691acfe37ac6be866e1651d2fa016612
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:bbf3c75a51dbc60a645533483e2bbd063aa4d13771eb0dfe04a3d8296baca3e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87003002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab74874c507d276705a966fc3776879c265338fbf31970b1f4d4bb0b55b95ea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:41:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:41:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 22:41:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65a2c8ccf599e7ae4ac4a1d44693dab2d70b4eb05e69f24feb1bfdadb09d733`  
		Last Modified: Thu, 15 Jan 2026 22:41:23 GMT  
		Size: 57.3 MB (57276991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:001470ed1eadef5a2ba283b8f3d3802df249cf8ec0a9b351641c6d196d98392e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfd25633826e6e5279532c21c71b4404bbb263d4825fd29c921da5069a71482`

```dockerfile
```

-	Layers:
	-	`sha256:96d39f4acdff2f6f559175cf72641c7670a56242a3950accaa84b8b6c65319ed`  
		Last Modified: Fri, 16 Jan 2026 01:15:33 GMT  
		Size: 2.5 MB (2526036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f3a508fa3e968f8f3523e33ef7289012e67d11e7bb04d1c2fce447699764307`  
		Last Modified: Fri, 16 Jan 2026 01:15:35 GMT  
		Size: 12.3 KB (12293 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a1a70092ce3364c9c0179564d44f56f92c8ac9aa6f65087c442417722576275a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85083335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6394e9c6c7305ee2afba5cc1da4f2e1d71e43992135b5ded745e706b3362b14`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:40:13 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:40:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:40:13 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:40:17 GMT
ADD file:6089c6bede9eca8ec4f424e5798a0ae0712a6fe38c9b97f9afb9d24d9675024e in / 
# Tue, 13 Jan 2026 05:40:17 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:44:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 22:44:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:36bf709aa36d66b784b0ba1aa3276848f28501175eeb4d7a310b1a98578f8558`  
		Last Modified: Tue, 13 Jan 2026 07:03:33 GMT  
		Size: 28.9 MB (28863824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e41f3222066aff1d57cb1d853f55212b97b118d6b0dbef78ec37a7ae75dc71`  
		Last Modified: Thu, 15 Jan 2026 22:44:52 GMT  
		Size: 56.2 MB (56219511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:520dc89e66c25c3aa233f6f1c390034de24e204668985472437df4500901aaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a201b81d4629655f64c45ae14f98c68c24c0c0a3a2ff204894816f3d7371a8`

```dockerfile
```

-	Layers:
	-	`sha256:1ccb108878ef048aca63b7f989d94f6858c58277a699f1b02d77167cdcefc779`  
		Last Modified: Fri, 16 Jan 2026 01:15:39 GMT  
		Size: 2.5 MB (2526633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13cce58fb1fd671513eac9e715888eaedabf641e25da690e1f30a7311e3a5f52`  
		Last Modified: Thu, 15 Jan 2026 22:44:42 GMT  
		Size: 12.5 KB (12528 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b8bcac3e71ea599e21414f9e689c2a1a9a636cd35b7f19b7a434c2739732398d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92487418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed156a626e28c69b57db4c225b2f1d8ccd105422ef466a83e4d3417f1d3060bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:39:44 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:39:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:39:44 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:39:47 GMT
ADD file:2f07f2a41a0f9535d0bb4dbf76ba28288335a19d601419d55d8004fa2b0faf12 in / 
# Tue, 13 Jan 2026 05:39:48 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:26:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:26:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 23:26:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dea13cf1fe062734821309e5f773a18c9ad629d9e93e3eba340bea036bccd8a`  
		Last Modified: Tue, 13 Jan 2026 06:35:59 GMT  
		Size: 34.3 MB (34306159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738212d90d8a7b9e29c6cd0d548d0fee33570cab51ffc6a85c83d8dbad0cf505`  
		Last Modified: Thu, 15 Jan 2026 23:26:49 GMT  
		Size: 58.2 MB (58181259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f7800f9efe667edd3c316cf036171f0d296f82cd9769f09df2bfe05adaab4e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4a8b67748489c27e008e9bd1ff97987a35da35866c9a0b7d475ab32fd9b124`

```dockerfile
```

-	Layers:
	-	`sha256:eb3a4890fdfa6410e2bd688c28bafd7d20de2f999dc29b9a6659a393331fc8ed`  
		Last Modified: Fri, 16 Jan 2026 01:15:44 GMT  
		Size: 2.5 MB (2523529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229c1f276b4e6e29d789b99ea042f7f2f1e930840eb9158d1fb65f1d6679c67a`  
		Last Modified: Fri, 16 Jan 2026 01:15:45 GMT  
		Size: 12.4 KB (12403 bytes)  
		MIME: application/vnd.in-toto+json
