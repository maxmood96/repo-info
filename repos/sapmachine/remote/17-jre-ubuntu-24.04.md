## `sapmachine:17-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:30581d5d4877033df5a7943b93573404e56da0c138fa23d06202c81c6fb479e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:eed1f53791249129998f0742bd111d8039410205e8915ac4494ab7e1fd2e142d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83846238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642008c33b69a2cae01748903d5cd4ba7b93ded2771955d5d3e860efb3b102c8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae046600c1e05ba314c526b3b7c0ff21ee97145a602d4c61a53b6df3056ce2a`  
		Last Modified: Wed, 16 Oct 2024 16:17:41 GMT  
		Size: 54.1 MB (54095875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f5dcda8762ef99e59b822428cf0c9f24040d94186523d9b0e349a40ba121da90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2372666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a268457292890512ebaa5ada859eaaf898020ae9f6faff4fb6256711d5af2a`

```dockerfile
```

-	Layers:
	-	`sha256:e5500e76786dd8e16cb07390a2ab908d958321fd946092348132fa5e3e18152e`  
		Last Modified: Wed, 16 Oct 2024 16:17:40 GMT  
		Size: 2.4 MB (2363411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26106ddd67bbddf5052adceb4be1495287147d576198d746e44d5f7e3d52a756`  
		Last Modified: Wed, 16 Oct 2024 16:17:40 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f869a05efab02b7187b142b2ad17eb13fd4abff2bdffeca94e974ea8c8335590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.4 MB (82371055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a645dfaecbf26e80ef5170810c14cb9c3eb68582da30982f9e98e6b97029936`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3530c2ced5e92e79ace69ee77d87ab2d704fee0e500f19080f1a959a50158b4`  
		Last Modified: Wed, 16 Oct 2024 04:40:35 GMT  
		Size: 53.5 MB (53485210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e1ec784797e3be50f4331bcbd8ef7f53bbf67f47b94d929a5afc415eeb5b8982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a4da03bec13dd1ceef4e9cba7be2a3b3fed9ceb5f4e69f59b1d1f6dab0b5a4`

```dockerfile
```

-	Layers:
	-	`sha256:9d10ed656c7f9cc04c9248442ed399cd65f997d2e265361c025f8b49dd2633a9`  
		Last Modified: Wed, 16 Oct 2024 04:40:34 GMT  
		Size: 2.4 MB (2363902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89feb9484fe24f6d61bdc83a0a46ae4f5253216383361a4667955f882756b9f7`  
		Last Modified: Wed, 16 Oct 2024 04:40:33 GMT  
		Size: 9.4 KB (9377 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3e70b79ad20fa948bcab4360367176d19b50efc6a2ff6a7fe4f2c11328589b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90097187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a71b065eb3ea0debff18a925e57a67ab7f9dfbc59d8a95f59384a6db356e9b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e162af10dbf0e0fe992a6f68dd0f8e36b65cb64d7b155fa9517a721ac3284bf0`  
		Last Modified: Wed, 16 Oct 2024 03:00:13 GMT  
		Size: 55.7 MB (55708218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f294732b7e1d82e54a93e8b4ef670395265eccfbc438b520bdc41eb808c926ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2376665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa0456549140fa3ece047d69d417f33c56e0a8cafe90aa3559e2df21bddd2e2`

```dockerfile
```

-	Layers:
	-	`sha256:6c677893ebb8df5c42180e06a9d31e64ba6c03f8172b7fa3f76ad269f4e2a78d`  
		Last Modified: Wed, 16 Oct 2024 03:00:12 GMT  
		Size: 2.4 MB (2367360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8f84301c5ed8e5a1195d83743e671a6bbefd02bc463afd9f43b00eebc550f37`  
		Last Modified: Wed, 16 Oct 2024 03:00:11 GMT  
		Size: 9.3 KB (9305 bytes)  
		MIME: application/vnd.in-toto+json
