## `sapmachine:jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:5787e23b23aa3bb9ffd661e36a243b57696200d6cfd92ec9572689d9689ca490
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d4ce2857c47a401c819a47cff4b3dd37c6c9acdfe80c920eb8cf6ac3a4840a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88331740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b215cd0ced821dd9eeed77591be4ace9e055801feb0815ea7f7fc0c548a8c9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:30 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:32 GMT
ADD file:6f881131af38dde06e3705e8376701ae22ce479e4824821a9580d4e0e0bcf0ac in / 
# Mon, 16 Sep 2024 06:23:33 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eda6120e237e0bdd328bc3e0f610854590400d4f96d9678dfcf781edb2f541d0`  
		Last Modified: Mon, 16 Sep 2024 07:36:26 GMT  
		Size: 29.7 MB (29749860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53b6c475e79b2f0fa22662abffb8d946564fd79d329cd79708b0a49e19729f4`  
		Last Modified: Wed, 02 Oct 2024 01:59:50 GMT  
		Size: 58.6 MB (58581880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dc7039809231b7924b4428168cf75e3fecef7c7e8aca321c91527cf2144faab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f2375997ad0f7f756bd519e0459f4677f9edf3908fd7140a82d53008f0b468`

```dockerfile
```

-	Layers:
	-	`sha256:78d317c0c1b2cd58252dc2ba2775ecf2c128cd0c1c710bb166a162c8a7d3092c`  
		Last Modified: Wed, 02 Oct 2024 01:59:49 GMT  
		Size: 2.1 MB (2129792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7efcb41d88743ea2f7d03ec13b3dc1f85257260f84a901b05a27fcd0aaae88a1`  
		Last Modified: Wed, 02 Oct 2024 01:59:49 GMT  
		Size: 9.3 KB (9308 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3b8fa85759e3905d1aaa91e694128c94c4c0c4718641777bce446d5dddf0f696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86497664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a734b684f08cbea4aebed801c45945fd6fd53363f62875810fe15d3839c654`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Sep 2024 06:23:55 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:23:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:23:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:23:58 GMT
ADD file:9d8a15341d364d2508ffca0657b4cb175a35d2edbdb0cf2476f7c4fff4f6c66a in / 
# Mon, 16 Sep 2024 06:23:59 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:25a614108e8d9c23a53cb3193f34ba623efe45c81ccaaa2281092b512ef7e07e`  
		Last Modified: Mon, 16 Sep 2024 07:36:32 GMT  
		Size: 28.9 MB (28885430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b87dcd1f68e888611129acbc7220f6fc0c43898a56ee41108484865fd1b58e`  
		Last Modified: Wed, 02 Oct 2024 03:44:34 GMT  
		Size: 57.6 MB (57612234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4e66c2630076dc9acc9e46b60f84c84397805dfe084515051d3dbc49e4acfe98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141c1b3ac79a9a3d7dacba1307eb4aa462f1f77bc7a374d5baf7370fca4970a1`

```dockerfile
```

-	Layers:
	-	`sha256:e447facfec23191be1bbdb4383d513ddba433fc109686b0bc1c4fa97b655796d`  
		Last Modified: Wed, 02 Oct 2024 03:44:32 GMT  
		Size: 2.1 MB (2129643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cac0ecd1675da195a73a8e9280499635b40c42ed5dc5d393d3df25df4a2d7fe`  
		Last Modified: Wed, 02 Oct 2024 03:44:32 GMT  
		Size: 9.4 KB (9430 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:92574abdb2196f2cbd13e7b5c6e70a260ad09677ec4c90685855fa9468eb5ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94283188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907fecb368e9ed4361949acfd4c05540c280f671f39d09177b3cdd71df41ab4c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Sep 2024 06:25:02 GMT
ARG RELEASE
# Mon, 16 Sep 2024 06:25:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 16 Sep 2024 06:25:02 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 16 Sep 2024 06:25:05 GMT
ADD file:5fe4accfd69653c9efcd106650478901cff305ef72427da563b841cc55cd5df4 in / 
# Mon, 16 Sep 2024 06:25:05 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:02d903566b998a9262d33a607ddfd51e0fd03d28f420fe11f8a2d4fed1eefb53`  
		Last Modified: Mon, 16 Sep 2024 07:36:44 GMT  
		Size: 34.4 MB (34392021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc4ddd6d9a29a83c4b81f4c1bb566a956bb957cc07cbcd57fed9de2ff153794`  
		Last Modified: Wed, 02 Oct 2024 02:49:34 GMT  
		Size: 59.9 MB (59891167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7edc927c849efdc7ed9383b4c77a8787ee6b4cdae017cc7d767211498b81b5f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2142405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31516efbc1b7bb5bb269cc23f585f275385d45da4ca2d24c73f4861b32941c6b`

```dockerfile
```

-	Layers:
	-	`sha256:215116d04c946ae8d5ebeb13a85f4181438aa8b8227e756f366631e44b989ffa`  
		Last Modified: Wed, 02 Oct 2024 02:49:32 GMT  
		Size: 2.1 MB (2133047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72c35fe833fb713704d18a3b2403fbd64edb75fb25ec2a76f54d04b7ba429e32`  
		Last Modified: Wed, 02 Oct 2024 02:49:32 GMT  
		Size: 9.4 KB (9358 bytes)  
		MIME: application/vnd.in-toto+json
