## `sapmachine:21-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:529cdff7b2f160703c87123d7c184a092b92ed8da384f585fe261e9fa2c39b0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:5c3a3d0727e8505ed6b8fa5dc4ce3610c1e2bbeade53db19441ca40e8588747e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89927148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91daf0fe7aaa1d66687ca1515812e36a5adac768c9d57eb019d663dd3b3a3ae3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d9c41ea457691f1b67044c70ebd2832bc3f95482cf492cd9a044add3e1c3e8`  
		Last Modified: Thu, 09 Oct 2025 21:28:07 GMT  
		Size: 60.2 MB (60204001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3082af5d7f1b9b78796cd78f17945fe51a8909e33690dbdd5b16e83c631ccae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e66a17839942e7d570c043a904a2bf892635a9b151a775ebf7e015b548d688`

```dockerfile
```

-	Layers:
	-	`sha256:2bdbf081888b9eacd78eb7e2aa6762c5b3b45b7e905df9d0f87f8b5f2180ed5d`  
		Last Modified: Fri, 10 Oct 2025 00:09:28 GMT  
		Size: 2.5 MB (2518632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a870c0eca7aa3e7cd9defeaced4f98b617e132959c514bdd825164b62292af`  
		Last Modified: Fri, 10 Oct 2025 00:09:30 GMT  
		Size: 10.1 KB (10080 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e18d546af8a7c928b9b325536a3bb1293f66b02a9ed69f12410c66dd83f49219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88247218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3efbb98f37b9cafc5e2d5527bb6cda2382aa901dfb4816d4ac7cd5a3b561d3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7a92f4a8b12ca6d42fa27266a9a67f3428474d78a9c76798d132ca91c8c266`  
		Last Modified: Thu, 09 Oct 2025 21:28:11 GMT  
		Size: 59.4 MB (59385506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:817d7680cc50ffd08a1b9c0662a0ba8659573bc6279953d2fbc96104b8082f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f41caa81a24df8da28a9b061e05eda661a86daf068dc9ed8893c01776ef809a`

```dockerfile
```

-	Layers:
	-	`sha256:059bcd6cda581d34e8c14044ff98088b7d54c59c68695a9f90cb92a495b411a9`  
		Last Modified: Fri, 10 Oct 2025 00:09:52 GMT  
		Size: 2.5 MB (2519148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb46365bc0882fd80cff8c044c1560205def087dff80261d023a27a67410ad0`  
		Last Modified: Fri, 10 Oct 2025 00:09:53 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1d30cfe5c372bab5f51c0062c10f78f5fff9ee5e030e2c5cd3876a75c8e0f63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98366543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73080c227757113ad30808c0a1df818469dabbef9e550255502a4cfe18f9e7f3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b663f62421fe3d2c3be3788263f8d374989a69723a0ce541006580d91d2d7032`  
		Last Modified: Thu, 02 Oct 2025 04:31:34 GMT  
		Size: 64.1 MB (64062996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ea9494013bf91f4fdbb9465ce3eee4d110bea84c86aa4cce828ced1000df8c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2526860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853ac2d50afcfe4550c6cadf8ac65ae4e0925363eafd9e1ee44aff9369c927ef`

```dockerfile
```

-	Layers:
	-	`sha256:930e8f8a88d07eb228ed61e96989c5ad9824244251f19f45e8e78bd1e4e0f3f6`  
		Last Modified: Thu, 02 Oct 2025 06:08:15 GMT  
		Size: 2.5 MB (2516713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a1ff61885a33210bae106d14b8ff13b7572440c263f99d187a73799f9705ba1`  
		Last Modified: Thu, 02 Oct 2025 06:08:16 GMT  
		Size: 10.1 KB (10147 bytes)  
		MIME: application/vnd.in-toto+json
