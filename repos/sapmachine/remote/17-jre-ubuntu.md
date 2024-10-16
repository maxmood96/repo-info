## `sapmachine:17-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:140ce1846212c7514785a6cb5c562ba2a5648a616cc59315133db43acb9298f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:42a7b30b4201c2ecfedaebd1d10f1a29858fad5fe5e971a78220d4d9b187dd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83846439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d0c2987129edae600ff3f6600075947e41e46516ed3c423f0ec7b6e6a78e97`
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
ADD file:f77876c7db6df55380fb32e200969af6e12f1e932f742c4a63bd9da235d83413 in / 
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
	-	`sha256:d1fbec07a2e50e73803e0c9ea0fc8f9fb48ad1215583bb1bbb8852660f52abeb`  
		Last Modified: Thu, 10 Oct 2024 08:59:45 GMT  
		Size: 29.8 MB (29750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ba201b899a9ffc1ff2a966013468221a041ccd59229724cd5d48c782058957`  
		Last Modified: Sat, 12 Oct 2024 00:01:04 GMT  
		Size: 54.1 MB (54095982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5d51ea332d630df3d79f3f3fd8e7ebf6228757ef2badbd6eb96401a027764e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2372666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9136584e82301942642fd5ba01baa10e9ea49709c917f9566ddca421a8acceef`

```dockerfile
```

-	Layers:
	-	`sha256:730b47738197f684b336af9a4742b9e05fa83917a7f9b63f49fc218df59038da`  
		Last Modified: Sat, 12 Oct 2024 00:01:03 GMT  
		Size: 2.4 MB (2363411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:071ea4369cb6303894f23f936019166225acd99f7240cdc3139d3dbf0a6fdbba`  
		Last Modified: Sat, 12 Oct 2024 00:01:03 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; arm64 variant v8

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

### `sapmachine:17-jre-ubuntu` - unknown; unknown

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

### `sapmachine:17-jre-ubuntu` - linux; ppc64le

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

### `sapmachine:17-jre-ubuntu` - unknown; unknown

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
