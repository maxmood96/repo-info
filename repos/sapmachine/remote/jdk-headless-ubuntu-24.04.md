## `sapmachine:jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:cd46ad8c461bb85696d70e2e721c639ca23a67a7b837c980c702bec7b54c3c1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8686ebc7e049cd85f5ec03dd15717c76264e783351a855d02e512d51698e71d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251108024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b1356cee89e0d671d1a415481657c7976dfccd3762f2a69a8243011fe23706`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:19 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:19 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439227b613b5399a4fef1855336c36a46c34b67904f34af21f215a68a1dbff9e`  
		Last Modified: Tue, 03 Dec 2024 02:35:23 GMT  
		Size: 221.4 MB (221356056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6b90e8046c263bfa35c92ccc1ca89279784d7958487ebe955be9b0cc24ca9596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2246249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf8cbd567d4c9c3d764e6ca1d1fef2edbbd2b06d252fb386db98e46dca43836`

```dockerfile
```

-	Layers:
	-	`sha256:6d5dc9fa2362e56f17ca73d5257ea63746fd0933601d3ff5d7f3b1dd003e8166`  
		Last Modified: Tue, 03 Dec 2024 02:35:20 GMT  
		Size: 2.2 MB (2235621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:377ce60329ba66d2ed39f0c0e3603df985a604ee9c9616e658145423cd2bc454`  
		Last Modified: Tue, 03 Dec 2024 02:35:20 GMT  
		Size: 10.6 KB (10628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d9180cd84ca9ebbd8b2024eae56acf1f1008f10973ceca1c4b7523b165cc72be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.2 MB (248215242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15d9c098244e8cffac568b4bcae6ab7c72558dc2d55cb05fd4e9218e280468b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a54d764af4a0b3b85e0f58e28aec0edba90437c531d14351d2a3ed447159618`  
		Last Modified: Sat, 16 Nov 2024 03:44:38 GMT  
		Size: 219.3 MB (219322817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4897d2cf958b61904f9ada19e1cdc4412371ad57354d6308b637cd032a7f98ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2246280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135988b94b779a49d596068ea42ffb29c6952b5ee9ddf5797bb80b315fe96666`

```dockerfile
```

-	Layers:
	-	`sha256:885120ec3463bf7a35b76573b8b4729177278d6b8e47e6e3f430828c9560d605`  
		Last Modified: Sat, 16 Nov 2024 03:44:30 GMT  
		Size: 2.2 MB (2235488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ad9d37f4b54f63b32fcebec75925a02d067911907db88285df724cc34b1e425`  
		Last Modified: Sat, 16 Nov 2024 03:44:29 GMT  
		Size: 10.8 KB (10792 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fc174ae0fd850645ad7e034d2faabb587b0cdef0954cafe2c05b2e882890990c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256695347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b11ec029c1aba471c17c4dcddcd358a1a7a6b4c188d0da9568f568a1c59b2f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:19 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:19 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa3efb5d593b75d1c8b2f982d578e5f23052621a6a6b416384250fc3a92160`  
		Last Modified: Tue, 03 Dec 2024 08:27:42 GMT  
		Size: 222.3 MB (222306527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:25c119f1390880d167ede5a217f025bd1e2d89162061f0b78185b8f269bacba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7dc7b237aff550d013b9aa268bb89d520514827b0d42807f357a7ebad5e3aa`

```dockerfile
```

-	Layers:
	-	`sha256:2293bdea303269cbde03327d97921147ac876db843b0a08fe884a798acc26339`  
		Last Modified: Tue, 03 Dec 2024 08:27:36 GMT  
		Size: 2.2 MB (2236957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93661cd1285ae4586881e1fd7fba7119bb7b69ba907d84ba736eb02a1099dbca`  
		Last Modified: Tue, 03 Dec 2024 08:27:36 GMT  
		Size: 10.7 KB (10702 bytes)  
		MIME: application/vnd.in-toto+json
